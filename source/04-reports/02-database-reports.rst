.. The COUNTER Code of Practice © 2017-2024 by COUNTER Metrics
   is licensed under CC BY 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by/4.0/

.. _database-reports:

Database Reports
----------------

Database Reports provide a summary of activity related to a given database or fixed collection of content that is packaged like a database. These reports provide a means of evaluating the impact a database has for an institution’s users.

To better facilitate open access reporting, report providers are encouraged to provide a Global Database Report including all global usage, whether attributed to institutions or not. The Global Database Report could be filtered and broken down as usual, including by using Attributed and other extensions (see :numref:`reserved-elements`).

To achieve compliance, a report provider MUST offer the COUNTER Reports and Standard Views of the COUNTER Reports that are applicable to their Host_Types, with the exception of Standard Views that always would be empty (e.g. an Access Denied Standard View if denials cannot occur).

Table 4.d (below): Database Report and Standard Views of the Database Report

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.13}|>{\raggedright\arraybackslash}\Y{0.17}|>{\parskip=\tparskip}\Y{0.44}|>{\raggedright\arraybackslash}\Y{0.26}|

.. list-table::
   :class: longtable
   :widths: 10 18 53 19
   :header-rows: 1

   * - Report_ID
     - Report_Name
     - Details
     - Host_Types

   * - DR
     - Database Report
     - A customizable report detailing activity by database that allows the user to apply filters and select other configuration options.
     - A&I_Database\ |br|\ |lb|
       Aggregated_Full_Content\ |br|\ |lb|
       Discovery_Service\ |br|\ |lb|
       eBook_Collection\ |br|\ |lb|
       Full_Content_Database\ |br|\ |lb|
       Multimedia_Collection

   * - DR_D1
     - Database Search and Item Usage
     - Reports on key Searches, Investigations and Requests metrics needed to evaluate a database.
     - A&I_Database\ |br|\ |lb|
       Aggregated_Full_Content\ |br|\ |lb|
       Discovery_Service\ |br|\ |lb|
       eBook_Collection\ |br|\ |lb|
       Full_Content_Database\ |br|\ |lb|
       Multimedia_Collection

   * - DR_D2
     - Database Access Denied
     - Reports on Access Denied activity for databases where users were denied access because simultaneous-use licenses were exceeded or their institution did not have a license for the database.
     - A&I_Database\ |br|\ |lb|
       Aggregated_Full_Content\ |br|\ |lb|
       Discovery_Service\ |br|\ |lb|
       eBook_Collection\ |br|\ |lb|
       Full_Content_Database\ |br|\ |lb|
       Multimedia_Collection


Report Header
"""""""""""""

The table below shows the header details for the Database Report and its Standard Views. For the tabular reports, elements MUST appear in the exact order shown, and spelling, casing, and punctuation of labels (Column A) and fixed data elements such as report names (Column B) MUST match exactly. The JSON version of the report MUST comply with the Report_Header definition in the COUNTER_SUSHI API Specification (see :numref:`sushi` below). Entries in the table appearing in italics describe the values to include.

Note that for the Global Database Report, if provided, the Institution_Name should be “The World”.

Table 4.e (below): Header for Database Report and Standard Views of the Database Report

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.1}|>{\raggedright\arraybackslash}\Y{0.19}|>{\raggedright\arraybackslash}\Y{0.19}|>{\raggedright\arraybackslash}\Y{0.26}|>{\raggedright\arraybackslash}\Y{0.26}|

.. flat-table::
   :class: longtable
   :widths: 8 15 27 25 25
   :header-rows: 2

   * - :rspan:`1` Row in Tabular Report
     - :rspan:`1` Label for Tabular Report (Column A)
     - :cspan:`2` Value for Tabular Report (Column B)

   * - DR
     - DR_D1
     - DR_D2

   * - 1
     - Report_Name
     - Database Report
     - Database Search and Item Usage
     - Database Access Denied

   * - 2
     - Report_ID
     - DR
     - DR_D1
     - DR_D2

   * - 3
     - Release
     - 5.1
     - 5.1
     - 5.1

   * - 4
     - Institution_Name
     - :cspan:`2` *Name of the institution the usage is attributed to.*

   * - 5
     - Institution_ID
     - :cspan:`2` *Identifier(s) for the institution in the format of {namespace}:{value}. Leave blank if identifier is not known. Multiple identifiers may be included by separating with semicolon-space (“; ”).*

   * - 6
     - Metric_Types
     - *Semicolon-space delimited list of Metric_Types included in the report.*
     - Searches_Automated; Searches_Federated; Searches_Regular; Total_Item_Investigations; Total_Item_Requests; Unique_Item_Investigations; Unique_Item_Requests
     - Limit_Exceeded; No_License

   * - 7
     - Report_Filters
     - *Semicolon-space delimited list of filters applied to the data to generate the report.*
     - Access_Method=Regular*
     - Access_Method=Regular*

   * - 8
     - Report_Attributes
     - *Semicolon-space delimited list of report attributes applied to the data to generate the report.*
     - *(blank)*
     - *(blank)*

   * - 9
     - Exceptions
     - :cspan:`2` *Any exceptions that occurred in generating the report, in the format “{Exception Code}: {Exception Message} ({Data})” with multiple exceptions separated by semicolon-space (“; ”).*

   * - 10
     - Reporting_Period
     - :cspan:`2` *Date range requested for the report in the form of “Begin_Date=yyyy-mm-dd; End_Date=yyyy-mm-dd”. The “dd” of the Begin_Date is 01. The “dd” of the End_Date is the last day of the month.*

   * - 11
     - Created
     - :cspan:`2` *Date and time the report was run in RFC3339 date-time format (yyyy-mm-ddThh:mm:ssZ).*

   * - 12
     - Created_By
     - :cspan:`2` *Name of organization or system that generated the report.*

   * - 13
     - Registry_Record
     - :cspan:`2` *Link to the platform's COUNTER Registry record.*

   * - 14
     - *(blank)*
     - *(blank)*
     - *(blank)*
     - *(blank)*

\*If a Platform filter is used (see :numref:`filters-attributes` for details), it MUST be included in Report_Filters.


.. _database-elements:

Column Headings/Elements
""""""""""""""""""""""""

The following elements MUST appear in the tabular report in the order they appear in the table below. For guidance on how these elements appear in the JSON format, refer to the COUNTER_SUSHI API Specification (see :numref:`sushi` below). Mandatory (M) elements MUST be included in the report. The other elements MUST only be included in the COUNTER Report if called for (C), and if included they MUST be listed in Attributes_To_Show in the Report_Attributes header.

Table 4.f (below): Column Headings/Elements for Database Report and Standard Views of the Database Report

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.28}|>{\raggedright\arraybackslash}\Y{0.1}|>{\raggedright\arraybackslash}\Y{0.1}|>{\raggedright\arraybackslash}\Y{0.1}|

.. list-table::
   :class: longtable
   :widths: 28 10 10 10
   :header-rows: 1

   * - Element Name (Tabular)
     - DR
     - DR_D1
     - DR_D2

   * - Database
     - M
     - M
     - M

   * - Publisher
     - M
     - M
     - M

   * - Publisher_ID
     - M
     - M
     - M

   * - Platform
     - M
     - M
     - M

   * - Proprietary_ID
     - M
     - M
     - M

   * - Data_Type
     - M
     -
     -

   * - Access_Method
     - C
     -
     -

   * - Metric_Type
     - M
     - M
     - M

   * - Reporting_Period_Total
     - M
     - M
     - M

   * - *Mmm-yyyy*
     - M*
     - M
     - M

\*unless Exclude_Monthly_Details=True is used


.. _database-filters:

Filters and Attributes
""""""""""""""""""""""

The following table presents the values that can be chosen for the Database Report and that are pre-set for the Standard Views of the Database Report. If a filter is not included in the request, the default applies. For the Standard Views an empty cell indicates that the filter is not applied.

Table 4.g (below): Filters/Attributes for Database Report and Standard Views of the Database Report

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.26}|>{\raggedright\arraybackslash}\Y{0.31}|>{\raggedright\arraybackslash}\Y{0.26}|>{\raggedright\arraybackslash}\Y{0.17}|

.. flat-table::
   :class: longtable
   :widths: 21 50 21 15
   :header-rows: 2

   * - :rspan:`1` Filter/Attribute
     - :cspan:`2` Filters available (options for Database Report and required for Standard Views of the Database Report)

   * - DR
     - DR_D1
     - DR_D2

   * - Data_Type
     - One or more or all (default) of the Data_Types applicable to the platform.
     -
     -

   * - Access_Method
     - One or all (default) of:\ |br|\ |lb|
       - Regular\ |br|\ |lb|
       - TDM
     - Regular
     - Regular

   * - Metric_Type
     - One or more or all (default) of:\ |br|\ |lb|
       - Searches_Automated\ |br|\ |lb|
       - Searches_Federated\ |br|\ |lb|
       - Searches_Regular\ |br|\ |lb|
       - Total_Item_Investigations\ |br|\ |lb|
       - Total_Item_Requests\ |br|\ |lb|
       - Unique_Item_Investigations\ |br|\ |lb|
       - Unique_Item_Requests\ |br|\ |lb|
       - Unique_Title_Investigations\ |br|\ |lb|
       - Unique_Title_Requests\ |br|\ |lb|
       - Limit_Exceeded\ |br|\ |lb|
       - No_License
     - Searches_Automated\ |br|\ |lb|
       Searches_Federated\ |br|\ |lb|
       Searches_Regular\ |br|\ |lb|
       Total_Item_Investigations\ |br|\ |lb|
       Total_Item_Requests\ |br|\ |lb|
       Unique_Item_Investigations\ |br|\ |lb|
       Unique_Item_Requests
     - Limit_Exceeded\ |br|\ |lb|
       No_License

   * - Exclude_Monthly_Details
     - False (default) or True
     -
     -

If a filter is applied to a column that doesn’t show on the report, usage for all selected attribute values is summed and the totals are presented in the report.
