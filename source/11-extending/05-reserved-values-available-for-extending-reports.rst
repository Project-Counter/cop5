.. The COUNTER Code of Practice © 2017-2024 by COUNTER Metrics
   is licensed under CC BY 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by/4.0/

.. _reserved-elements:

Reserved Elements and Values Available for Extending Reports
------------------------------------------------------------

COUNTER recognizes that there are some common extensions that report providers might want to include in COUNTER Reports or when creating custom reports; therefore the following element names and values have been reserved for this common use:

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.22}|>{\parskip=\tparskip}\Y{0.54}|>{\raggedright\arraybackslash}\Y{0.11}|>{\raggedright\arraybackslash}\Y{0.13}|

.. list-table::
   :class: longtable
   :widths: 16 62 12 10
   :header-rows: 1

   * - Element Name
     - Description
     - Reports
     - Examples

   * - Customer_ID
     - When a COUNTER Report contains usage for multiple organizations, this element can be used to break the usage down by institution. The Customer_ID MUST be included in the Institution_ID report header in a report for that institution (usually as a proprietary identifier with the platform ID as namespace), and it MUST match the Customer_ID for the institution returned by the /r51/members COUNTER_SUSHI API path. Customer_ID 0000000000000000 is reserved for delivery of global reports to "The World". If Customer_ID is included in a tabular report, it MUST be the second column if Institution_Name is also included, or the first column if Institution_Name is not included.
     - PR, DR, TR, IR
     - C12345

   * - Institution_Name
     - When a COUNTER Report contains usage for multiple organizations, this element can be used to break the usage down by institution. The Institution_Name MUST match the Institution_Name in the report header in a report for that institution and the Name for the institution returned by the /r51/members COUNTER_SUSHI API path. If Institution_Name is included in a tabular report, it MUST be the first column.
     - PR, DR, TR, IR
     - Mt. Laurel University

   * - Book_Segment_Count
     - The number of Book_Segments within a Book. Note that this extension MUST only be used where the number of Book_Segments is known, and MUST NOT be used where the number of Book_Segments is only being estimated.
     - TR
     - 52

   * - Country_Name
     - Name of the country according to ISO 3166-1. Note that the standard allows country names in different languages. The name is included for easier reading, for processing the reports the Country_Code should be used.
     - PR, DR, TR, IR
     - Canada

   * - Country_Code
     - ISO 3166-1 alpha-2 code of the country.
     - PR, DR, TR, IR
     - CA

   * - Subdivision_Name
     - Name of the country subdivision according to ISO 3166-2. Note that the standard allows country subdivision names in different languages. The name is included for easier reading, for processing the reports the Subdivision_Code should be used.
     - PR, DR, TR, IR
     - Quebec\ |br|\ |lb|
       Québec

   * - Subdivision_Code
     - ISO 3166-2 code of the country subdivision.
     - PR, DR, TR, IR
     - CA-QC

   * - Attributed
     - Whether the report provider was able to attribute the usage to an institution or not. Valid values are Yes and No. With this extension usage of open content that could not be attributed to an institution can be reported. The extension usually would be used in a Global Platform Report, Global Database Report, Global Title Report or Global Item Report for “The World” (see :numref:`report-header`) which could be broken down by geolocation with the Country and Subdivision extensions.
     - PR, DR, TR, IR
     - No

Note that by supporting the Institution_Name and Customer_ID extensions report providers can offer COUNTER Reports to consortia with usage broken down by their members. If a consortium requests a report with Institution_Name and/or Customer_ID, the usage would be broken down by institution if the extension is supported by the report provider, otherwise the usage would be summarised over all consortium members as usual.
