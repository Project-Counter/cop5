.. The COUNTER Code of Practice © 2017-2026 by COUNTER Metrics
   is licensed under CC BY 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by/4.0/

.. _api-extensions:

Extensions for the COUNTER API
-------------------------------

In addition to the extensions that can be included in COUNTER Reports (see :numref:`reserved-elements`), COUNTER recognizes that report providers may want to extend the COUNTER API to provide additional information to report consumers. This section describes OPTIONAL API extensions that can be included in COUNTER API responses.


Requesting API Extensions
"""""""""""""""""""""""""

API extensions can either be additional API paths or extensions to existing paths. In the latter case they are requested using an ``include_{element name in lower case}`` parameter with permissible values ``False`` (default) and ``True``. This follows the same pattern as the ``include_parent_details`` and ``include_component_details`` report attributes (see :numref:`filters-attributes`).

Support for API extensions is OPTIONAL. If a report provider does not support an extension to an existing path, the response SHOULD be the same as when the parameter is omitted or set to ``False``. Report providers that do not support an extension are not expected to implement any special way of signaling that the extension is not supported.

When an extension is supported, the information SHOULD be customer specific where possible. For example, the date on which data for a month last changed may depend on the customer ID and other credentials used in the request.

When information for an extension is not available, the corresponding element MUST be omitted rather than included with an empty or placeholder value.


Month_Details Extension
"""""""""""""""""""""""

The Month_Details extension allows report providers to signal to report consumers when data for a report has changed and may need reharvesting. Because the date of change may be report specific and may depend on the credentials used in the request, this information is provided in the response for the ``/r51/reports`` COUNTER API path (see :numref:`api-paths`), which MUST be protected by the methods described in :numref:`api-security`.

The extension is requested using the ``include_month_details`` parameter with permissible values ``False`` (default) and ``True``.

When ``include_month_details=True``, each report in the response MAY include a ``Month_Details`` element. The ``Month_Details`` element is an object whose keys are months in ``yyyy-mm`` format. Each month key maps to an object that contains information about that month. The elements defined for each month are ``Last_Change_Date`` and, optionally, ``Last_Change_Note``. The structure is extensible so that additional per-month elements can be defined in the future. Report consumers MUST ignore elements in ``Month_Details`` that they do not recognize.

The required ``Last_Change_Date`` element gives the date and time when the data for that month last changed, in RFC3339 date-time format (*yyyy-mm-ddThh:mm:ssZ*). Report providers MUST include a month in ``Month_Details`` only when ``Last_Change_Date`` information is available for that month. Months for which the information is not available MUST be omitted. If no months have ``Last_Change_Date`` information for a report, the ``Month_Details`` element MUST be omitted for that report.

The optional ``Last_Change_Note`` element allows the report provider to include information about why the data for that month has changed.

An example of a report entry in the response for ``/r51/reports`` with the Month_Details extension is:

.. code-block:: JSON

   {
     "Report_Name": "Platform Report",
     "Report_ID": "PR",
     "Release": "5.1",
     "Report_Description": "A customizable report summarizing activity across a report provider’s platforms that allows the user to apply filters and select other configuration options.",
     "First_Month_Available": "2024-01",
     "Last_Month_Available": "2026-03",
     "Month_Details": {
       "2026-03": {
         "Last_Change_Date": "2026-04-18T20:30:40Z",
         "Last_Change_Note": "Data restated after correction of duplicate request counts."
       },
       "2026-02": {
         "Last_Change_Date": "2026-03-29T01:02:03Z"
       }
     }
   }


The ``Month_Details`` element MAY be included for some reports in the response and omitted for others. Report consumers can compare the ``Last_Change_Date`` value for a month with the date and time when they last harvested usage data for that report and month to determine whether reharvesting is needed.

No particular order is required for the month keys in ``Month_Details`` but descending chronological order is RECOMMENDED. Each month key MUST be within the range from ``First_Month_Available`` to ``Last_Month_Available`` inclusive for that report.


Platforms Extension
"""""""""""""""""""

The Platforms extension allows report providers to return the list of platforms supported by the COUNTER API server for the credentials included in the request. Support for the Platforms extension is OPTIONAL, i.e. report providers can decide whether to support the extension or not. If the Platforms extension is not supported, the COUNTER API server MUST respond with HTTP status code 404 (as required by :ref:`Appendix D <appendix-d>` for unsupported paths).

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.11}|>{\raggedright\arraybackslash}\Y{0.18}|>{\parskip=\tparskip}\Y{0.71}|

.. list-table::
   :class: longtable
   :widths: 8 14 78
   :header-rows: 1

   * - HTTP Method
     - Path
     - Description

   * - GET
     - /r51/platforms
     - Returns the list of platforms supported by the COUNTER API server for the credentials included in the request. The response SHOULD be customer specific if possible. For each platform the response includes a ``Platform_Parameter`` value to be used for the ``platform`` parameter on other API paths,  a ``Platform_Name`` for identifying the platform, and an optional ``Platform_Description`` for providing additional information about the platform.

       If the COUNTER API server requires the ``platform`` parameter for the standard API paths, the response includes the platforms that can be requested with the given credentials. If the COUNTER API server uses the ``platform`` parameter as a usual report filter, the response includes the values available for the Platform filter.

       This path MUST be protected by the methods described in :numref:`api-security`.

The Platforms extension could not only be useful for report providers who want to make this information available, and for report consumers who want to harvest reports for specific platforms on which usage occured, but also for usage consolidation platforms that harvest COUNTER reports from multiple report provider platforms and offer a COUNTER API for access to the harvested reports. Here is an example of what a ``/r51/platforms`` response could look like for such a platform:

.. code-block:: JSON

   [
     {
       "Platform_Parameter": "12",
       "Platform_Name": "EBSCOhost"
     },
     {
       "Platform_Parameter": "23",
       "Platform_Name": "ProQuest",
       "Platform_Description": "Reports for the www.proquest.com platform"
     },
     {
       "Platform_Parameter": "41",
       "Platform_Name": "ScienceDirect"
     }
   ]

For example ``platform=12`` would be used for requesting EBSCOhost reports from the platform.
