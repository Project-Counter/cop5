.. The COUNTER Code of Practice Release 5 © 2017-2023 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

.. _item-reports:

Item Reports
------------

Item Reports provide a summary of activity related to content at the item level and provide a means of evaluating the impact an item has for an institution’s patrons. 

To better facilitate open access reporting, Release 5.1 encourages all Host_Types to provide a Global Item Report, which provides a granular per-item view of all usage, whether attributed to institutions or not. This is particularly relevant for report providers with open access content. The Global Item Report is an Item Report to "The World" including all global usage, whether attributed to an institution or not, which could be broken down by geolocation with the Country and Subdivision extensions, as well as by using Attributed and other extensions (see :numref:`reserved-elements`).

Table 4.n (below): Item Report and Standard Views of the Item Report

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.13}|>{\raggedright\arraybackslash}\Y{0.17}|>{\parskip=\tparskip}\Y{0.37}|>{\raggedright\arraybackslash}\Y{0.33}|

.. list-table::
   :class: longtable
   :widths: 10 20 46 24
   :header-rows: 1

   * - Report_ID
     - Report_Name
     - Details
     - Host_Types

   * - IR
     - Item Report
     - A granular, customizable report showing activity at the level of the item (article, chapter, media object, etc.) that allows the user to apply filters and select other configuration options.
     - Data_Repository*\ |br|\ |lb|
       Multimedia\ |br|\ |lb|
       Repository\ |br|\ |lb|
       Scholarly_Collaboration_Network

   * - IR_A1
     - Journal Article Requests
     - Reports on journal article requests at the article level. This report is limited to content with a Data_Type of Article and Metric_Types of Total_Item_Requests and Unique_Item_Requests.
     - Repository\ |br|\ |lb|
       Scholarly_Collaboration_Network

   * - IR_M1
     - Multimedia Item Requests
     - Reports on multimedia requests at the item level.
     - Multimedia

\*Data repositories may choose to conform to the Code of Practice Release 5 or, alternatively, may wish to work with the Code of Practice for Research Data.


Report Header
"""""""""""""

The table below shows the header details for the Item Report and its Standard Views. For the tabular reports, elements MUST appear in the exact order shown, and spelling, casing and punctuation of labels (Column A) and fixed data elements such as report names (Column B) MUST match exactly. The JSON version of the report MUST comply with the Report_Header definition in the COUNTER_SUSHI API Specification (see :numref:`sushi` below). Entries in the table appearing in italics describe the values to include.

Note that for the Global Item Report, if provided, the Institution_Name should be “The World”.

Table 4.o (below): Header for Item Report and Standard Views of the Item Report

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.1}|>{\raggedright\arraybackslash}\Y{0.19}|>{\raggedright\arraybackslash}\Y{0.17}|>{\raggedright\arraybackslash}\Y{0.28}|>{\raggedright\arraybackslash}\Y{0.26}|

.. flat-table::
   :class: longtable
   :widths: 8 15 31 23 23
   :header-rows: 2

   * - :rspan:`1` Row in Tabular Report
     - :rspan:`1` Label for Tabular Report (Column A)
     - :cspan:`2` Value for Tabular Report (Column B)

   * - IR
     - IR_A1
     - IR_M1

   * - 1
     - Report_Name
     - Item Report
     - Journal Article Requests
     - Multimedia Item Requests

   * - 2
     - Report_ID
     - IR
     - IR_A1
     - IR_M1

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
     - Total_Item_Requests; Unique_Items_Requests
     - Total_Item_Requests; Unique_Items_Requests

   * - 7
     - Report_Filters
     - *Semicolon-space delimited list of filters applied to the data to generate the report.*
     - Data_Type=Article; Access_Method=Regular*
     - Data_Type=Audiovisual|Image|Interactive_Resource|Multimedia|Sound; Access_Method=Regular*

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
     - Registry
     - :cspan:`1` *Link to the platform's COUNTER Registry record.*

   * - 14
     - *(blank)*
     - *(blank)*
     - *(blank)*
     - *(blank)*

\*If a Platform filter is used (see :numref:`filters-attributes` for details), it MUST be included in Report_Filters.


.. _item-elements:

Column Headings/Elements
""""""""""""""""""""""""

The following elements MUST appear in the tabular report in the order they appear in the table below. For guidance on how these elements appear in the JSON format, refer to the COUNTER_SUSHI API Specification (see :numref:`sushi` below). Mandatory (M) elements MUST be included in the report. The Parent elements MUST only be included in the COUNTER Report if called for (C) via Include_Parent_Details. For report providers who elect to offer component usage information, the Component elements MUST only be included in the COUNTER Report if called for (C) via Include_Component_Details. If they are included, then the corresponding Include_Parent_Details=True or Include_Component_Details=True MUST be included in the Report_Attributes header. The other elements also MUST only be included if called for (C), and if included they MUST be listed in Attributes_To_Show in the Report_Attributes header.

Table 4.p (below): Column Headings/Elements for Item Report and Standard Views of the Item Report

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.32}|>{\raggedright\arraybackslash}\Y{0.1}|>{\raggedright\arraybackslash}\Y{0.1}|>{\raggedright\arraybackslash}\Y{0.1}|

.. list-table::
   :class: longtable
   :widths: 34 10 10 10
   :header-rows: 1

   * - Element Name (Tabular)
     - IR
     - IR_A1
     - IR_M1

   * - Item
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

   * - Authors
     - C
     - M
     -

   * - Publication_Date
     - C
     - M
     -

   * - Article_Version
     - C
     - M
     -

   * - DOI
     - M
     - M
     - M

   * - Proprietary_ID
     - M
     - M
     - M

   * - ISBN
     - M
     -
     -

   * - Print_ISSN
     - M
     - M
     -

   * - Online_ISSN
     - M
     - M
     -

   * - URI
     - M
     - M
     - M

   * - Parent_Title
     - C
     - M
     -

   * - Parent_Authors
     - C
     - M
     -

   * - Parent_Publication_Date
     - C
     -
     -

   * - Parent_Article_Version
     - C
     - M
     -

   * - Parent_Data_Type
     - C
     -
     -

   * - Parent_DOI
     - C
     - M
     -

   * - Parent_Proprietary_ID
     - C
     - M
     -

   * - Parent_ISBN
     - C
     -
     -

   * - Parent_Print_ISSN
     - C
     - M
     -

   * - Parent_Online_ISSN
     - C
     - M
     -

   * - Parent_URI
     - C
     - M
     -

   * - Component_Title
     - C
     -
     -

   * - Component_Authors
     - C
     -
     -

   * - Component_Publication_Date
     - C
     -
     -

   * - Component_Data_Type
     - C
     -
     -

   * - Component_DOI
     - C
     -
     -

   * - Component_Proprietary_ID
     - C
     -
     -

   * - Component_ISBN
     - C
     -
     -

   * - Component_Print_ISSN
     - C
     -
     -

   * - Component_Online_ISSN
     - C
     -
     -

   * - Component_URI
     - C
     -
     -

   * - Data_Type
     - M
     -
     - M

   * - YOP
     - C
     -
     -

   * - Access_Type
     - C
     - M
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


.. _item-filters:

Filters and Attributes
""""""""""""""""""""""

The following table presents the values that can be chosen for the Item  Report and that are pre-set for the Standard Views of the Item Report. If a filter is not included in the request, the default applies. For the Standard Views of the Item Report an empty cell indicates that the filter is not applied.

Table 4.q (below): Filters/Attributes for Item Report and Standard Views of the Item Report

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.28}|>{\raggedright\arraybackslash}\Y{0.285}|>{\raggedright\arraybackslash}\Y{0.225}|>{\raggedright\arraybackslash}\Y{0.21}|

.. flat-table::
   :class: longtable
   :widths: 20 47 17 16
   :header-rows: 2

   * - :rspan:`1` Filter/Attribute
     - :cspan:`2` Filters available (options for Item Report and required for Standard Views of the Item Report)

   * - IR
     - IR_A1
     - IR_M1

   * - Data_Type
     - One or more or all (default) of the Data_Types applicable to the platform.
     - Article
     - Audiovisual; Image; Interactive_Resource; Multimedia; Sound

   * - YOP
     - All years (default), a specific year in the format yyyy, or a range of years in the format yyyy-yyyy. Use 0001 for unknown or 9999 for articles in press.

       Note that the COUNTER_SUSHI API allows the specification of multiple years and ranges separated by the vertical pipe (“|”) character.
     -
     -

   * - Access_Type
     - One or more or all (default) of:\ |br|\ |lb|
       - Controlled\ |br|\ |lb|
       - Open\ |br|\ |lb|
       - Free_To_Read
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
       - Total_Item_Investigations\ |br|\ |lb|
       - Total_Item_Requests\ |br|\ |lb|
       - Unique_Item_Investigations\ |br|\ |lb|
       - Unique_Item_Requests\ |br|\ |lb|
       - Limit_Exceeded\ |br|\ |lb|
       - No_License
     - Total_Item_Requests\ |br|\ |lb|
       Unique_Item_Requests
     - Total_Item_Requests\ |br|\ |lb|
       Unique_Item_Requests

   * - Include_Parent_Details
     - False (default) or True
     -
     -

   * - Include_Component_Details
     - False (default) or True
     -
     -

   * - Exclude_Monthly_Details
     - False (default) or True
     -
     -

If a filter is applied to a column that doesn’t show on the report, usage for all selected attribute values is summed and the totals are presented in the report.
