.. The COUNTER Code of Practice Release 5 © 2017-2023 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

.. _platform-reports:

Platform Reports
----------------

Platform Reports provide a summary of activity on a given platform to support the evaluation of platforms and to provide high-level statistical data to support surveys and reporting to funders.

Table 4 (below): Platform Report and Standard Views of the Platform Report

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.13}|>{\raggedright\arraybackslash}\Y{0.17}|>{\parskip=\tparskip}\Y{0.37}|>{\raggedright\arraybackslash}\Y{0.33}|

.. list-table::
   :class: longtable
   :widths: 10 18 48 24
   :header-rows: 1

   * - Report_ID
     - Report_Name
     - Details
     - Host_Types

   * - PR
     - Platform Report
     - A customizable report summarizing activity across a content provider’s platforms that allows the user to apply filters and select other configuration options.
     - All Host_Types

   * - PR_P1
     - Platform Usage
     - Platform-level usage summarized by Metric_Type.
     - All Host_Types

\*Data repositories may choose to conform to the Code of Practice Release 5 or, alternatively, may wish to work with the Code of Practice for Research Data.


Report Header
"""""""""""""

The table below shows the header details for the Platform Report and its Standard Views. For the tabular reports, elements MUST appear in the exact order shown, and spelling, casing, and punctuation of labels (Column A) and fixed data elements such as report names (Column B) MUST match exactly. The JSON version of the report MUST comply with the Report_Header definition in the COUNTER_SUSHI API Specification (see :numref:`sushi` below). Entries in the table appearing in italics describe the values to include.

Table 4.a (below): Header for Platform Report and Standard Views of the Platform Report

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.1}|>{\raggedright\arraybackslash}\Y{0.2}|>{\raggedright\arraybackslash}\Y{0.35}|>{\raggedright\arraybackslash}\Y{0.35}|

.. flat-table::
   :class: longtable
   :widths: 8 15 39 38
   :header-rows: 2

   * - :rspan:`1` Row in Tabular Report
     - :rspan:`1` Label for Tabular Report (Column A)
     - :cspan:`1` Value for Tabular Report (Column B)

   * - PR
     - PR_P1

   * - 1
     - Report_Name
     - Platform Report
     - Platform Usage

   * - 2
     - Report_ID
     - PR
     - PR_P1

   * - 3
     - Release
     - 5
     - 5

   * - 4
     - Institution_Name
     - :cspan:`1` *Name of the institution the usage is attributed to.*

   * - 5
     - Institution_ID
     - :cspan:`1` *Identifier(s) for the institution in the format of {namespace}:{value}. Leave blank if identifier is not known. Multiple identifiers may be included by separating with semicolon-space (“; ”).*

   * - 6
     - Metric_Types
     - *Semicolon-space delimited list of Metric_Types included in the report.*
     - Searches_Platform; Total_Item_Requests; Unique_Item_Requests; Unique_Title_Requests

   * - 7
     - Report_Filters
     - *Semicolon-space delimited list of filters applied to the data to generate the report.*
     - Access_Method=Regular*

   * - 8
     - Report_Attributes
     - *Semicolon-space delimited list of report attributes applied to the data to generate the report.*
     - *(blank)*

   * - 9
     - Exceptions
     - :cspan:`1` *Any exceptions that occurred in generating the report, in the format “{Exception Code}: {Exception Message} ({Data})” with multiple exceptions separated by semicolon-space (“; ”).*

   * - 10
     - Reporting_Period
     - :cspan:`1` *Date range requested for the report in the form of “Begin_Date=yyyy-mm-dd; End_Date=yyyy-mm-dd”. The “dd” of the Begin_Date is 01. The “dd” of the End_Date is the last day of the month.*

   * - 11
     - Created
     - :cspan:`1` *Date and time the report was run in RFC3339 date-time format (yyyy-mm-ddThh:mm:ssZ).*

   * - 12
     - Created_By
     - :cspan:`1` *Name of organization or system that generated the report.*

   * - 13
     - *(blank)*
     - *(blank)*
     - *(blank)*

\*If a Platform filter is used (see :numref:`filters-attributes` for details), it MUST be included in Report_Filters.


.. _platform-elements:

Column Headings/Elements
""""""""""""""""""""""""

The following elements MUST appear in the tabular report in the order they appear in the table below. For guidance on how these elements appear in the JSON format, refer to the COUNTER_SUSHI API Specification (see :numref:`sushi` below). Mandatory (M) elements MUST be included in the report. The other elements MUST only be included in the COUNTER Report if called for (C), and if included they MUST be listed in Attributes_To_Show in the Report_Attributes header.

Table 4.b (Below): Column Headings/Elements for Platform Report and Standard Views of the Platform Report

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.28}|>{\raggedright\arraybackslash}\Y{0.1}|>{\raggedright\arraybackslash}\Y{0.1}|

.. list-table::
   :class: longtable
   :widths: 28 10 10
   :header-rows: 1

   * - Element Name (Tabular)
     - PR
     - PR_P1

   * - Platform
     - M
     - M

   * - Data_Type
     - C
     -

   * - Access_Method
     - C
     -

   * - Metric_Type
     - M
     - M

   * - Reporting_Period_Total
     - M
     - M

   * - *Mmm-yyyy*
     - M*
     - M

\*unless Exclude_Monthly_Details=True is used


.. _platform-filters:

Filters and Attributes
""""""""""""""""""""""

The following table presents the values that can be chosen for the Platform Report and that are pre-set for the Standard Views of the Platform Report. If a filter is not included in the request, the default applies. For the Standard Views an empty cell indicates that the filter is not applied.

Table 4.c (below) Filters/Attributes for Platform Report and Standard Views of the Platform Report

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.28}|>{\raggedright\arraybackslash}\Y{0.38}|>{\raggedright\arraybackslash}\Y{0.34}|

.. flat-table::
   :class: longtable
   :widths: 21 50 22
   :header-rows: 2

   * - :rspan:`1` Filter/Attribute
     - :cspan:`1` Filters available (options for Platform Report and required for Standard Views of the Platform Report)

   * - PR
     - PR_P1

   * - Data_Type
     - One or more or all (default) of the Data_Types applicable to the platform.
     -

   * - Access_Method
     - One or all (default) of:\ |br|\ |lb|
       - Regular\ |br|\ |lb|
       - TDM
     - Regular

   * - Metric_Type
     - One or more or all (default) of:\ |br|\ |lb|
       - Searches_Platform\ |br|\ |lb|
       - Total_Item_Investigations\ |br|\ |lb|
       - Total_Item_Requests\ |br|\ |lb|
       - Unique_Item_Investigations\ |br|\ |lb|
       - Unique_Item_Requests\ |br|\ |lb|
       - Unique_Title_Investigations\ |br|\ |lb|
       - Unique_Title_Requests
     - Searches_Platform\ |br|\ |lb|
       Total_Item_Requests\ |br|\ |lb|
       Unique_Item_Requests\ |br|\ |lb|
       Unique_Title_Requests

   * - Exclude_Monthly_Details
     - False (default) or True
     -

If a filter is applied to a column that doesn’t show on the report, usage for all selected attribute values is summed and the totals are presented in the report.
