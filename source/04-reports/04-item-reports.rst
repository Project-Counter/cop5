.. The COUNTER Code of Practice Release 5 © 2017-2021 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

.. _item-reports:

Item Reports
------------

Item Reports provide a summary of activity related to content at the item level and provide a means of evaluating the impact an item has for an institution’s patrons.

Table 4.n (below): Item Master Report and Standard Views

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
     - Item Master Report
     - A granular, customizable report showing activity at the level of the item (article, chapter, media object, etc.) that allows the user to apply filters and select other configuration options.
     - Data_Repository*\ |br|\ |lb|
       Multimedia\ |br|\ |lb|
       Repository\ |br|\ |lb|
       Scholarly_Collaboration_Network

   * - IR_A1
     - Journal Article Requests
     - Reports on journal article requests at the article level. This report is limited to content with a Data_Type of Article, Parent_Data_Type of Journal, and Metric_Types of Total_Item_Requests and Unique_Item_Requests.

       This Standard View must be provided only if (a) it is clear for all articles in IR whether they are journal articles or not and (b) the parent item is known for all journal articles.
     - Repository\ |br|\ |lb|
       Scholarly_Collaboration_Network

   * - IR_M1
     - Multimedia Item Requests
     - Reports on multimedia requests at the item level.
     - Multimedia

\*Data repositories may choose to conform to the Code of Practice Release 5 or, alternatively, may wish to work with the Code of Practice for Research Data.


Report Header
"""""""""""""

The table below shows the header details for the Item Master Report and its Standard Views. For the tabular reports, elements MUST appear in the exact order shown, and spelling, casing and punctuation of labels (Column A) and fixed data elements such as report names (Column B) MUST match exactly. The JSON version of the report MUST comply with the Report_Header definition in the COUNTER_SUSHI API Specification (see :numref:`sushi` below). Entries in the table appearing in italics describe the values to include.

Table 4.o (below): Header for Item Master Report and Standard Views

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
     - Item Master Report
     - Journal Article Requests
     - Multimedia Item Requests

   * - 2
     - Report_ID
     - IR
     - IR_A1
     - IR_M1

   * - 3
     - Release
     - 5
     - 5
     - 5

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
     - Total_Item_Requests

   * - 7
     - Report_Filters
     - *Semicolon-space delimited list of filters applied to the data to generate the report.*
     - Data_Type=Article; Parent_Data_Type=Journal; Access_Method=Regular*
     - Data_Type=Multimedia; Access_Method=Regular*

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
     - *(blank)*
     - *(blank)*
     - *(blank)*
     - *(blank)*

\*If a Platform filter is used (see :numref:`filters-attributes` for details), it MUST be included in Report_Filters.


.. _item-elements:

Column Headings/Elements
""""""""""""""""""""""""

The following elements MUST appear in the tabular report in the order they appear in the table below. For guidance on how these elements appear in the JSON format, refer to the COUNTER_SUSHI API Specification (see :numref:`sushi` below). Mandatory (M) elements MUST be included in the report. The Parent and Component elements MUST only be included in the Master Report if requested (R) via Include_Parent_Details and Include_Component_Details, respectively (they are not supposed to be selected individually). If they are included, then the corresponding Include_Parent_Details=True or Include_Component_Details=True MUST be included in the Report_Attributes header. The other elements also MUST only be included if requested (R), and if included they MUST be listed in Attributes_To_Show in the Report_Attributes header.

Table 4.p (below): Column Headings/Elements for Item Master Report and Standard Views

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
     - R
     - M
     -

   * - Publication_Date
     - R
     - M
     -

   * - Article_Version
     - R
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
     - R
     - M
     -

   * - Parent_Authors
     - R
     - M
     -

   * - Parent_Publication_Date
     - R
     -
     -

   * - Parent_Article_Version
     - R
     - M
     -

   * - Parent_Data_Type
     - R
     -
     -

   * - Parent_DOI
     - R
     - M
     -

   * - Parent_Proprietary_ID
     - R
     - M
     -

   * - Parent_ISBN
     - R
     -
     -

   * - Parent_Print_ISSN
     - R
     - M
     -

   * - Parent_Online_ISSN
     - R
     - M
     -

   * - Parent_URI
     - R
     - M
     -

   * - Component_Title
     - R
     -
     -

   * - Component_Authors
     - R
     -
     -

   * - Component_Publication_Date
     - R
     -
     -

   * - Component_Data_Type
     - R
     -
     -

   * - Component_DOI
     - R
     -
     -

   * - Component_Proprietary_ID
     - R
     -
     -

   * - Component_ISBN
     - R
     -
     -

   * - Component_Print_ISSN
     - R
     -
     -

   * - Component_Online_ISSN
     - R
     -
     -

   * - Component_URI
     - R
     -
     -

   * - Data_Type
     - R
     -
     -

   * - YOP
     - R
     -
     -

   * - Access_Type
     - R
     - M
     -

   * - Access_Method
     - R
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

The following table presents the values that can be chosen for the Item Master Report and that are pre-set for the Standard Views. If a filter is not included in the request, the default applies. For the Standard Views an empty cell indicates that the filter is not applied.

Table 4.q (below): Filters/Attributes for Item Master Report and Standard Views

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.28}|>{\raggedright\arraybackslash}\Y{0.285}|>{\raggedright\arraybackslash}\Y{0.225}|>{\raggedright\arraybackslash}\Y{0.21}|

.. flat-table::
   :class: longtable
   :widths: 20 47 17 16
   :header-rows: 2

   * - :rspan:`1` Filter/Attribute
     - :cspan:`2` Filters available (options for Master Report and required for Standard Views)

   * - IR
     - IR_A1
     - IR_M1

   * - Data_Type
     - One or more or all (default) of the Data_Types applicable to the platform.
     - Article
     - Multimedia

   * - YOP
     - All years (default), a specific year in the format yyyy, or a range of years in the format yyyy-yyyy. Use 0001 for unknown or 9999 for articles in press.

       Note that the COUNTER_SUSHI API allows the specification of multiple years and ranges separated by the vertical pipe (“|”) character.
     -
     -

   * - Access_Type
     - One or more or all (default) of:\ |br|\ |lb|
       - Controlled\ |br|\ |lb|
       - OA_Gold\ |br|\ |lb|
       - Other_Free_To_Read
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
     - Total_Item_Requests

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
