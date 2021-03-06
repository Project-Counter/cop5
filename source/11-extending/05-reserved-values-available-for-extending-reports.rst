.. The COUNTER Code of Practice Release 5 © 2017-2021 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

.. _reserved-elements:

Reserved Elements and Values Available for Extending Reports
------------------------------------------------------------

COUNTER recognizes that there are some common extensions that content providers might want to include in Master Reports or when creating custom reports; therefore the following element names and values have been reserved for this common use:

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.19}|>{\parskip=\tparskip}\Y{0.57}|>{\raggedright\arraybackslash}\Y{0.11}|>{\raggedright\arraybackslash}\Y{0.13}|

.. list-table::
   :class: longtable
   :widths: 14 64 12 10
   :header-rows: 1

   * - Element Name
     - Description
     - Reports
     - Examples

   * - Customer_ID
     - When a Master Report contains usage for multiple organizations, this element can be used to break the usage down by institution. The Customer_ID MUST match the Customer_ID in the report header in a JSON report for that institution and the Customer_ID for the institution returned by the /members COUNTER_SUSHI API path. If Customer_ID is included in a tabular report, it MUST be the second column if Institution_Name is also included, or the first column if Institution_Name is not included.
     - PR, DR, TR, IR
     - C12345

   * - Institution_Name
     - When a Master Report contains usage for multiple organizations, this element can be used to break the usage down by institution. The Institution_Name MUST match the Institution_Name in the report header in a report for that institution and the Name for the institution returned by the /members COUNTER_SUSHI API path. If Institution_Name is included in a tabular report, it MUST be the first column.
     - PR, DR, TR, IR
     - Mt. Laurel University

   * - Format
     - By tracking the Format, content providers can generate R4 usage reports from R5 usage during the transition period. Reserved values for Format are:

       * HTML
       * PDF
       * Other

       The Format element MUST only be used in the Title Master Report (or custom reports) and for Metric_Type Total_Item_Requests. If Format is included in a tabular report, it MUST be the last column before Metric_Type, and for other Metric_Types than Total_Item_Requests the cells in the Format column MUST be empty.
     - TR
     - PDF

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
     - Whether the content provider was able to attribute the usage to an institution or not. Valid values are Yes and No. With this extension usage of open content that could not be attributed to an institution can be reported. The extension usually would be used in a report for “The World” (see :numref:`report-header`) which could be broken down by geolocation with the Country and Subdivision extensions.
     - PR, DR, TR, IR
     - No

Note that by supporting the Institution_Name and Customer_ID extensions content providers can offer COUNTER Master Reports to consortia with usage broken down by their members. If a consortium requests a report with Institution_Name and/or Customer_ID, the usage would be broken down by institution if the extension is supported by the content provider, otherwise the usage would be summarised over all consortium members as usual.
