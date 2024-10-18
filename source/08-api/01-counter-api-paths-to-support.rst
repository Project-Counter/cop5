.. The COUNTER Code of Practice © 2017-2024 by COUNTER Metrics
   is licensed under CC BY 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by/4.0/

.. _api-paths:

COUNTER API Paths to Support
----------------------------

Starting with Release 5.1, the COUNTER API paths include the Release in the format */r{Release without .}*, so that the COUNTER API is properly versioned.

Report providers SHOULD use the same COUNTER API base URL for all releases. For example, if the URL for requesting the list of reports is ``https://example.org/counter/reports`` in R5, it should be ``https://example.org/counter/r51/reports`` in R5.1, so that the base URL for both releases is ``https://example.org/counter``.

The following paths (methods) MUST be supported:

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.11}|>{\raggedright\arraybackslash}\Y{0.24}|>{\parskip=\tparskip}\Y{0.65}|

.. list-table::
   :class: longtable
   :widths: 8 17 75
   :header-rows: 1

   * - HTTP Method
     - Path
     - Description

   * - GET
     - /r51/status
     - Returns the current status of the COUNTER API service. This path returns a message that includes the operating status of the API, the URL to the service’s entry in the COUNTER Registry, and an array of service alerts (if any).

       This path MUST be public, i.e. not protected by the methods described in :numref:`api-security`, to allow report consumers to easily check whether a COUNTER API server is live.

   * - GET
     - /r51/reports
     - Returns a list of reports supported by the COUNTER API service. The response includes an array of reports, including the report identifier, the release number, the report name, a description, the path to use when requesting the report (optional but recommended for custom reports), and the first and last months for which usage data has been processed and is available. This information SHOULD be specific for each customer ID.

   * - GET
     - /r51/reports/*{Report_ID in lower case}*
     - Each supported report has its own path, e.g. GET /r51/reports/tr_b1 for “Book Requests (Controlled)”, GET /r51/reports/tr_j1 for “Journal Requests (Controlled)”.

       The paths for the COUNTER Reports offer parameters that allow report consumers to customize the reports by applying report filters and report attributes (see :numref:`filters-attributes`), including filters for some common extensions (see :numref:`reserved-elements`). Support for common extensions is optional. Report providers that support one of the extensions also SHOULD support the corresponding parameter. If filtering by an extension is not supported, report providers MUST handle this as described for Exception 3060 in :ref:`Appendix D <appendix-d>`.

   * - GET
     - /r51/members
     - Returns the institutions associated with the customer ID in the request and their customer IDs and requestor IDs. The associated institutions can be consortium members, or sites for multi-site customers. If the customer in the request is neither a consortium nor multi-site, the response only includes the details for the customer itself. The response is an array of customer account information, including for each the customer ID (for requesting COUNTER reports and making other API calls), the requestor ID (if required for API calls and differing from the requestor ID in the request), the institution name, and additional identifiers for the institution (if any).
