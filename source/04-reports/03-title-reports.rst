.. The COUNTER Code of Practice Release 5 © 2017-2023 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

.. _title-reports:

Title Reports
-------------

Title Reports provide a summary of activity related to content at the title level and provide a means of evaluating the impact a title has for an institution’s patrons.

To better facilitate open access reporting, report providers are encouraged to provide a Global Title Report including all global usage, whether attributed to institutions or not. The Global Title Report could be filtered and broken down as usual, including by using Attributed and other extensions (see :numref:`reserved-elements`).

Table 4.h (below): Title Report and Standard Views of the Title Report

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.13}|>{\raggedright\arraybackslash}\Y{0.16}|>{\parskip=\tparskip}\Y{0.45}|>{\raggedright\arraybackslash}\Y{0.26}|

.. list-table::
   :class: longtable
   :widths: 10 18 53 19
   :header-rows: 1

   * - Report_ID
     - Report_Name
     - Details
     - Host_Types

   * - TR
     - Title Report
     - A customizable report detailing activity at the title level (journal, book, etc.) that allows the user to apply filters and select other configuration options.
     - Aggregated_Full_Content\ |br|\ |lb|
       eBook\ |br|\ |lb|
       eBook_Collection\ |br|\ |lb|
       eJournal

   * - TR_B1
     - Book Requests (Controlled)
     - Reports on full-text activity for books (Data_Types Book and Reference_Work), excluding Open and Free_To_Read content, as Total_Item_Requests and Unique_Title_Requests. The Unique_Title_Requests provides comparable usage across book platforms. The Total_Item_Requests shows overall activity; however, numbers between sites will vary significantly based on how the content is delivered (e.g. delivered as a complete book or by chapter).
     - Aggregated_Full_Content\ |br|\ |lb|
       eBook\ |br|\ |lb|
       eBook_Collection

   * - TR_B2
     - Book Access Denied
     - Reports on Access Denied activity for books (Data_Types Book and Reference_Work) where users were denied access because simultaneous-use licenses were exceeded or their institution did not have a license for the book.
     - Aggregated_Full_Content\ |br|\ |lb|
       eBook\ |br|\ |lb|
       eBook_Collection

   * - TR_B3
     - Book Usage by Access Type
     - Reports on book usage (Data_Types Book and Reference_Work) showing all applicable Metric_Types broken down by Access_Type.
     - Aggregated_Full_Content\ |br|\ |lb|
       eBook\ |br|\ |lb|
       eBook_Collection

   * - TR_J1
     - Journal Requests (Controlled)
     - Reports on usage of journal content, excluding Open and Free_To_Read content, as Total_Item_Requests and Unique_Item_Requests. The Unique_Item_Requests provides comparable usage across journal platforms by reducing the inflationary effect that occurs when an HTML full text automatically displays and the user then accesses the PDF version. The Total_Item_Requests shows overall activity.
     - Aggregated_Full_Content\ |br|\ |lb|
       eJournal

   * - TR_J2
     - Journal Access Denied
     - Reports on Access Denied activity for journal content where users were denied access because simultaneous-use licenses were exceeded or their institution did not have a license for the title.
     - Aggregated_Full_Content\ |br|\ |lb|
       eJournal

   * - TR_J3
     - Journal Usage by Access Type
     - Reports on usage of journal content for all Metric_Types broken down by Access_Type.
     - Aggregated_Full_Content\ |br|\ |lb|
       eJournal

   * - TR_J4
     - Journal Requests by YOP (Controlled)
     - Breaks down the usage of journal content, excluding Open and Free_To_Read content, by year of publication (YOP), providing counts for the Metric_Types Total_Item_Requests and Unique_Item_Requests. Provides the details necessary to analyze usage of content in backfiles or covered by perpetual access agreement. Note that COUNTER reports do not provide access model or perpetual access rights details.
     - Aggregated_Full_Content\ |br|\ |lb|
       eJournal


Report Header
"""""""""""""

The table below shows the header details for the Title Report and its Standard Views. For the tabular reports, elements MUST appear in the exact order shown, and spelling, casing, and punctuation of labels (Column A) and fixed data elements such as report names (Column B) MUST match exactly. The JSON version of the report MUST comply with the Report_Header definition in the COUNTER_SUSHI API Specification (see :numref:`sushi` below). Entries in the table appearing in italics describe the values to include.

Note that for the Global Title Report, if provided, the Institution_Name should be “The World”.

|blscape|

Table 4.i (below) Header for Title Report and Standard Views of the Title Report - Part 1 (for Books)

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.07}|>{\raggedright\arraybackslash}\Y{0.13}|>{\raggedright\arraybackslash}\Y{0.27}|>{\raggedright\arraybackslash}\Y{0.17}|>{\raggedright\arraybackslash}\Y{0.17}|>{\raggedright\arraybackslash}\Y{0.19}|

.. flat-table::
   :class: longtable
   :widths: 4 14 22 20 19 21
   :header-rows: 2

   * - :rspan:`1` Row in Tabular Report
     - :rspan:`1` Label for Tabular Report (Column A)
     - :cspan:`3` Value for Tabular Report (Column B)

   * - TR
     - TR_B1
     - TR_B2
     - TR_B3

   * - 1
     - Report_Name
     - Title Report
     - Book Requests (Controlled)
     - Book Access Denied
     - Book Usage by Access Type

   * - 2
     - Report_ID
     - TR
     - TR_B1
     - TR_B2
     - TR_B3

   * - 3
     - Release
     - 5
     - 5
     - 5
     - 5

   * - 4
     - Institution_Name
     - :cspan:`3` *Name of the institution the usage is attributed to.*

   * - 5
     - Institution_ID
     - :cspan:`3` *Identifier(s) for the institution in the format of {namespace}:{value}. Leave blank if identifier is not known. Multiple identifiers may be included by separating with semicolon-space (“; ”).*

   * - 6
     - Metric_Types
     - *Semicolon-space delimited list of Metric_Types included in the report.*
     - Total_Item_Requests;\ |br|\ |lb|
       Unique_Title_Requests
     - Limit_Exceeded;\ |br|\ |lb|
       No_License
     - Total_Item_Investigations;\ |br|\ |lb|
       Total_Item_Requests;\ |br|\ |lb|
       Unique_Item_Investigations;\ |br|\ |lb|
       Unique_Item_Requests;\ |br|\ |lb|
       Unique_Title_Investigations;\ |br|\ |lb|
       Unique_Title_Requests

   * - 7
     - Report_Filters
     - *Semicolon-space delimited list of filters applied to the data to generate the report.*
     - Data_Type=Book; Reference_Work;\ |br|\ |lb|
       Access_Type=Controlled;\ |br|\ |lb|
       Access_Method=Regular*
     - Data_Type=Book; Reference_Work;\ |br|\ |lb|
       Access_Method=Regular*
     - Data_Type=Book; Reference_Work;\ |br|\ |lb|
       Access_Method=Regular*

   * - 8
     - Report_Attributes
     - *Semicolon-space delimited list of report attributes applied to the data to generate the report.*
     - *(blank)*
     - *(blank)*
     - *(blank)*

   * - 9
     - Exceptions
     - :cspan:`3` *Any exceptions that occurred in generating the report, in the format “{Exception Code}: {Exception Message} ({Data})” with multiple exceptions separated by semicolon-space (“; ”).*

   * - 10
     - Reporting_Period
     - :cspan:`3` *Date range requested for the report in the form of “Begin_Date=yyyy-mm-dd; End_Date=yyyy-mm-dd”. The “dd” of the Begin_Date is 01. The “dd” of the End_Date is the last day of the month.*

   * - 11
     - Created
     - :cspan:`3` *Date and time the report was run in RFC3339 date-time format (yyyy-mm-ddThh:mm:ssZ).*

   * - 12
     - Created_By
     - :cspan:`3` *Name of organization or system that generated the report.*

   * - 13
     - *(blank)*
     - *(blank)*
     - *(blank)*
     - *(blank)*
     - *(blank)*

\*If a Platform filter is used (see :numref:`filters-attributes` for details), it MUST be included in Report_Filters.

|elscape|
|blscape|

Table 4.j (below): Header for Standard Views of the Title Report - Part 2 (for Journals)

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.07}|>{\raggedright\arraybackslash}\Y{0.13}|>{\raggedright\arraybackslash}\Y{0.25}|>{\raggedright\arraybackslash}\Y{0.18}|>{\raggedright\arraybackslash}\Y{0.19}|>{\raggedright\arraybackslash}\Y{0.18}|

.. flat-table::
   :class: longtable
   :widths: 4 14 20 20 21 21
   :header-rows: 2

   * - :rspan:`1` Row in Tabular Report
     - :rspan:`1` Label for Tabular Report (Column A)
     - :cspan:`3` Value for Tabular Report (Column B)

   * - TR_J1
     - TR_J2
     - TR_J3
     - TR_J4

   * - 1
     - Report_Name
     - Journal Requests (Controlled)
     - Journal Access Denied
     - Journal Usage by Access Type
     - Journal Requests by YOP (Controlled)

   * - 2
     - Report_ID
     - TR_J1
     - TR_J2
     - TR_J3
     - TR_J4

   * - 3
     - Release
     - 5
     - 5
     - 5
     - 5

   * - 4
     - Institution_Name
     - :cspan:`3` *Name of the institution the usage is attributed to.*

   * - 5
     - Institution_ID
     - :cspan:`3` *Identifier(s) for the institution in the format of {namespace}:{value}. Leave blank if identifier is not known. Multiple identifiers may be included by separating with semicolon-space (“; ”).*

   * - 6
     - Metric_Types
     - Total_Item_Requests;\ |br|\ |lb|
       Unique_Item_Requests
     - Limit_Exceeded;\ |br|\ |lb|
       No_License
     - Total_Item_Investigations;\ |br|\ |lb|
       Total_Item_Requests;\ |br|\ |lb|
       Unique_Item_Investigations;\ |br|\ |lb|
       Unique_Item_Requests
     - Total_Item_Requests;\ |br|\ |lb|
       Unique_Item_Requests

   * - 7
     - Report_Filters
     - Data_Type=Journal;\ |br|\ |lb|
       Access_Type=Controlled;\ |br|\ |lb|
       Access_Method=Regular*
     - Data_Type=Journal;\ |br|\ |lb|
       Access_Method=Regular*
     - Data_Type=Journal;\ |br|\ |lb|
       Access_Method=Regular*
     - Data_Type=Journal;\ |br|\ |lb|
       Access_Type=Controlled;\ |br|\ |lb|
       Access_Method=Regular*

   * - 8
     - Report_Attributes
     - *(blank)*
     - *(blank)*
     - *(blank)*
     - *(blank)*

   * - 9
     - Exceptions
     - :cspan:`3` *Any exceptions that occurred in generating the report, in the format “{Exception Code}: {Exception Message} ({Data})” with multiple exceptions separated by semicolon-space (“; ”).*

   * - 10
     - Reporting_Period
     - :cspan:`3` *Date range requested for the report in the form of “Begin_Date=yyyy-mm-dd; End_Date=yyyy-mm-dd”. The “dd” of the Begin_Date is 01. The “dd” of the End_Date is the last day of the month.*

   * - 11
     - Created
     - :cspan:`3` *Date and time the report was run in RFC3339 date-time format (yyyy-mm-ddThh:mm:ssZ).*

   * - 12
     - Created_By
     - :cspan:`3` *Name of organization or system that generated the report.*

   * - 13
     - Registry
     - :cspan:`1` *Link to the platform's COUNTER Registry record.*

   * - 14
     - *(blank)*
     - *(blank)*
     - *(blank)*
     - *(blank)*
     - *(blank)*

\*If a Platform filter is used (see :numref:`filters-attributes` for details), it MUST be included in Report_Filters.

|elscape|


.. _title-elements:

Column Headings/Elements
""""""""""""""""""""""""

The following elements MUST appear in the tabular report in the order they appear in the table below. For guidance on how these elements appear in the JSON format, refer to the COUNTER_SUSHI API Specification (see :numref:`sushi` below). Mandatory (M) elements MUST be included in the report. The other elements MUST only be included in the COUNTER Report if called for (C), and if included they MUST be listed in Attributes_To_Show in the Report_Attributes header.

Table 4.k (below): Column Headings/Elements for Title Report and Standard Views of the Title Report

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.28}|>{\raggedright\arraybackslash}\Y{0.09}|>{\raggedright\arraybackslash}\Y{0.09}|>{\raggedright\arraybackslash}\Y{0.09}|>{\raggedright\arraybackslash}\Y{0.09}|>{\raggedright\arraybackslash}\Y{0.09}|>{\raggedright\arraybackslash}\Y{0.09}|>{\raggedright\arraybackslash}\Y{0.09}|>{\raggedright\arraybackslash}\Y{0.09}|

.. list-table::
   :class: longtable
   :widths: 28 9 9 9 9 9 9 9 9
   :header-rows: 1

   * - Element Name (Tabular)
     - TR
     - TR_B1
     - TR_B2
     - TR_B3
     - TR_J1
     - TR_J2
     - TR_J3
     - TR_J4

   * - Title
     - M
     - M
     - M
     - M
     - M
     - M
     - M
     - M

   * - Publisher
     - M
     - M
     - M
     - M
     - M
     - M
     - M
     - M

   * - Publisher_ID
     - M
     - M
     - M
     - M
     - M
     - M
     - M
     - M

   * - Platform
     - M
     - M
     - M
     - M
     - M
     - M
     - M
     - M

   * - DOI
     - M
     - M
     - M
     - M
     - M
     - M
     - M
     - M

   * - Proprietary_ID
     - M
     - M
     - M
     - M
     - M
     - M
     - M
     - M

   * - ISBN
     - M
     - M
     - M
     - M
     -
     -
     -
     -

   * - Print_ISSN
     - M
     - M
     - M
     - M
     - M
     - M
     - M
     - M

   * - Online_ISSN
     - M
     - M
     - M
     - M
     - M
     - M
     - M
     - M

   * - URI
     - M
     - M
     - M
     - M
     - M
     - M
     - M
     - M

   * - Data_Type
     - M
     - M
     - M
     - M
     -
     -
     -
     -

   * - YOP
     - C
     - M
     - M
     - M
     -
     -
     -
     - M

   * - Access_Type
     - C
     -
     -
     - M
     -
     -
     - M
     -

   * - Access_Method
     - R
     -
     -
     -
     -
     -
     -
     -

   * - Metric_Type
     - M
     - M
     - M
     - M
     - M
     - M
     - M
     - M

   * - Reporting_Period_Total
     - M
     - M
     - M
     - M
     - M
     - M
     - M
     - M

   * - *Mmm-yyyy*
     - M*
     - M
     - M
     - M
     - M
     - M
     - M
     - M

\*unless Exclude_Monthly_Details=True is used


.. _title-filters:

Filters and Attributes
""""""""""""""""""""""

The following table presents the values that can be chosen for the Title Report and that are pre-set for the Standard Views of the Title Report. If a filter is not included in the request, the default applies. For the Standard Views an empty cell indicates that the filter is not applied.

|blscape|

Table 4.l (below): Filters/Attributes for Title Report and Standard Views of the Title Report - Part 1 (for Books)

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.18}|>{\raggedright\arraybackslash}\Y{0.33}|>{\raggedright\arraybackslash}\Y{0.17}|>{\raggedright\arraybackslash}\Y{0.13}|>{\raggedright\arraybackslash}\Y{0.19}|

.. flat-table::
   :class: longtable
   :widths: 19 31 17 13 20
   :header-rows: 2

   * - :rspan:`1` Filter/Attribute
     - :cspan:`3` Filters available (options for Title Report and required for Standard Views of the Title Report)

   * - TR
     - TR_B1
     - TR_B2
     - TR_B3

   * - Data_Type
     - One or more or all (default) of the Data_Types applicable to the platform.
     - Book\ |br|\ |lb|
       Reference_Work
     - Book\ |br|\ |lb|
       Reference_Work
     - Book\ |br|\ |lb|
       Reference_Work

   * - YOP
     - All years (default), a specific year in the format yyyy, or a range of years in the format yyyy-yyyy. Use 0001 for unknown or 9999 for articles in press.

       Note that the COUNTER_SUSHI API allows the specification of multiple years and ranges separated by the vertical pipe (“|”) character.
     -
     -
     -

   * - Access_Type
     - One or more or all (default) of:\ |br|\ |lb|
       - Controlled\ |br|\ |lb|
       - Open\ |br|\ |lb|
       - Free_To_Read
     - Controlled
     -
     -

   * - Access_Method
     - One or all (default) of:\ |br|\ |lb|
       - Regular\ |br|\ |lb|
       - TDM
     - Regular
     - Regular
     - Regular

   * - Metric_Type
     - One or more or all (default) of:\ |br|\ |lb|
       - Total_Item_Investigations\ |br|\ |lb|
       - Total_Item_Requests\ |br|\ |lb|
       - Unique_Item_Investigations\ |br|\ |lb|
       - Unique_Item_Requests\ |br|\ |lb|
       - Unique_Title_Investigations\ |br|\ |lb|
       - Unique_Title_Requests\ |br|\ |lb|
       - Limit_Exceeded\ |br|\ |lb|
       - No_License
     - Total_Item_Requests\ |br|\ |lb|
       Unique_Title_Requests
     - Limit_Exceeded\ |br|\ |lb|
       No_License
     - Total_Item_Investigations\ |br|\ |lb|
       Total_Item_Requests\ |br|\ |lb|
       Unique_Item_Investigations\ |br|\ |lb|
       Unique_Item_Requests\ |br|\ |lb|
       Unique_Title_Investigations\ |br|\ |lb|
       Unique_Title_Requests

   * - Exclude_Monthly_Details
     - False (default) or True
     -
     -
     -

|elscape|
|blscape|

Table 4.m (below): Filters/Attributes for Standard Views of the Title Report - Part 2 (for Journals)

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.18}|>{\raggedright\arraybackslash}\Y{0.22}|>{\raggedright\arraybackslash}\Y{0.17}|>{\raggedright\arraybackslash}\Y{0.23}|>{\raggedright\arraybackslash}\Y{0.2}|

.. flat-table::
   :class: longtable
   :widths: 21 20 15 23 21
   :header-rows: 2

   * - :rspan:`1` Filter/Attribute
     - :cspan:`3` Filters available (options for Title Report and required for Standard Views of the Title Report)

   * - TR_J1
     - TR_J2
     - TR_J3
     - TR_J4

   * - Data_Type
     - Journal
     - Journal
     - Journal
     - Journal

   * - YOP
     -
     -
     -
     -

   * - Access_Type
     - Controlled
     -
     -
     - Controlled

   * - Access_Method
     - Regular
     - Regular
     - Regular
     - Regular

   * - Metric_Type
     - Total_Item_Requests\ |br|\ |lb|
       Unique_Item_Requests
     - Limit_Exceeded\ |br|\ |lb|
       No_License
     - Total_Item_Investigations\ |br|\ |lb|
       Total_Item_Requests\ |br|\ |lb|
       Unique_Item_Investigations\ |br|\ |lb|
       Unique_Item_Requests
     - Total_Item_Requests\ |br|\ |lb|
       Unique_Item_Requests

   * - Exclude_Monthly_Details
     -
     -
     -
     -

If a filter is applied to a column that doesn’t show on the report, usage for all selected attribute values is summed and the totals are presented in the report.

|elscape|
