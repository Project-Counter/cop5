.. The COUNTER Code of Practice Release 5 © 2017-2023 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

B.1 Changes from COUNTER Release 4 (R4)
---------------------------------------

Changes in the nature of online content and how it is accessed have resulted in the COUNTER Code of Practice evolving in an attempt to accommodate those changes. This evolution resulted in some ambiguities and, in some cases, conflicts and confusions within the Code of Practice. Release 5 (R5) of the COUNTER Code of Practice is focused on improving the consistency, credibility, and comparability of usage reporting.


.. _appendix-b-1-1:

B.1.1 List of Reports
"""""""""""""""""""""

R5 reduces the overall number of reports by replacing many of the special-purpose reports that are seldom used with four COUNTER Reports and a number of Standard Views of the COUNTER Reports that are more flexible. All COUNTER R4 reports have either been renamed or eliminated in favour of R5 COUNTER Reports or Standard Views of the COUNTER Reports.

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.29}|>{\raggedright\arraybackslash}\Y{0.2}|>{\parskip=\tparskip}\Y{0.51}|

.. list-table::
   :class: longtable
   :widths: 29 15 56
   :header-rows: 1

   * - R4 report
     - R5 Report/Status
     - Comments

   * - Book Report 1: Number of Successful Title Requests by Month and Title
     - Book Requests (Excluding OA_Gold)
     - The Unique_Title_Requests metric is equivalent to the full-text requests in Book Report 1.

   * - Book Report 2: Number of Successful Section Requests by Month and Title
     - Book Requests (Excluding OA_Gold)
     - The Total_Item_Requests metric is equivalent to full text requests in Book Report 2.

   * - Book Report 3: Access Denied to Content Items by Month, Title and Category
     - Book Access Denied
     - Limit_Exceeded and No_License metrics are equivalent to those found in Book Report 3.

   * - Book Report 4: Access Denied to Content items by Month, Platform and Category
     - Eliminated (no equivalent)
     - “Book Access Denied” can be used to provide summary statistics by platform. For book collections the denials would be reported in “Database Access Denied”.

   * - Book Report 5: Total Searches by Month and Title
     - Eliminated (no equivalent)
     - For most platforms, attempting to track searches by titles is not reasonable since all titles are included in most searches.

   * - Book Report 7: Number of Successful Unique Title Requests by Month and Title in a Session
     - Book Requests (Excluding OA_Gold)
     - The Unique_Title_Requests metric is equivalent to the full-text requests in Book Report 7.

   * - Consortium Report 1: Number of Successful Full-Text Journal Article or Book Chapter Requests by Month and Title
     - Eliminated
     - Consortium administrators will request “Journal Requests (Excluding OA_Gold)” for each member. This can be automated via the COUNTER_SUSHI API using the /members path. Tools will be provided to create consolidated reports that are functionally equivalent to Consortium Report 1.

   * - Consortium Report 2: Total Searches by Month and Database
     - Eliminated
     - Consortium administrators will request “Database Search and Item Usage” for each member. This can be automated via the COUNTER_SUSHI API using the /members path. Tools will be provided to create consolidated reports that are functionally equivalent to Consortium Report 2.

   * - Consortium Report 3: Number of Successful Multimedia Full Content Unit Requests by Month and Collection
     - Eliminated
     - For multimedia collections that are equivalent to databases, consortium administrators will request “Database Search and Item Usage” for each member. This can be automated via the COUNTER_SUSHI API using the /members path. Tools will be provided to create consolidated reports that are functionally equivalent to Consortium Report 3.

   * - Database Report 1: Total Searches, Result Clicks and Record Views by Month and Database
     - Database Search and Item Usage
     - Result Clicks and Record Views have been replaced by Total_Item_Investigations. Metrics for regular searches remains unchanged, and federated and automated searches are now reported separately. The report also includes Requests metrics.

   * - Database Report 2: Access Denied by Month, Database and Category
     - Database Access Denied
     - Report renamed and updated Metric_Types used.

   * - Journal Report 1: Number of Successful Full-Text Article Requests by Month and Journal
     - Journal Requests (Excluding OA_Gold)
     - Total_Item_Requests is the equivalent to full text total. HTML and PDF totals have been eliminated, but Unique_Item_Requests can be used to evaluate the effect of the user interface on statistics and offers a comparable statistics for cost-per-unique-use analysis.

   * - Journal Report 1 GOA: Number of Successful Gold Open Access Full-Text Article Requests by Month and Journal
     - Title Report
     - The Title Report can be filtered by “Access\_\ |lb|\ Type=OA_Gold; Metric_Type=Total_Item_Requests” to obtain equivalent results.

   * - Journal Report 1a: Number of Successful Full-Text Article Requests from an Archive by Month and Journal
     - Journal Requests by YOP (Excluding OA_Gold)
     - The R5 report breaks out usage by year of publication (YOP) to enable evaluation of usage of content for which perpetual access rights are available.

   * - Journal Report 2: Access Denied to Full-Text Articles by Month, Journal and Category
     - Journal Access Denied
     - The Limit_Exceeded and No_License metrics are equivalent to corresponding metrics in R4 report.

   * - Journal Report 3: Number of Successful Item Requests by Month, Journal and Page-type
     - Title Report\ |br|\ |lb|
       Item Report
     - The Title Report can be configured to show Section_Types, which provides details similar to JR3. Other details like the audio and video usage can be reported in the Item Report (using the Component elements where appropriate).

   * - Journal Report 3 Mobile: Number of Successful Item Requests by Month, Journal and Page-type for usage on a mobile device
     - Eliminated (no equivalent)
     - Capturing usage by mobile devices is less relevant with the responsive design of most sites. The variety of mobile devices also makes it difficult, as does the fact that today’s smartphones have screen resolutions that exceed those of some desktops.

   * - Journal Report 4: Total Searches Run By Month and Collection
     - Eliminated (no equivalent)
     - To the extent that a journal collection is organized for searching as a discrete collection (rare), usage would be reported in “Database Search and Item Usage”.

   * - Journal Report 5: Number of Successful Full-Text Article Requests by Year-of-Publication (YOP) and Journal
     - Journal Requests by YOP (Excluding OA_Gold)
     - This R5 report offers a breakdown of journal usage by year of publication (YOP) and the resulting report can be analysed using filters or pivot tables.

   * - Multimedia Report 1: Number of Successful Full Multimedia Content Unit Requests by Month and Collection
     - Database Search and Item Usage
     - Multimedia usage, where multimedia is packaged and accessed as separate collections, would be reported using “Database Search and Item Usage”.

   * - Multimedia Report 2: Number of Successful Full Multimedia Content Unit Requests by Month, Collection and Item Type
     - Multimedia Item Requests
     - The R5 report provides a more detailed breakdown by item and includes attributes such as Data_Type. This report can be used to provide summary statistics by type.

   * - Platform Report 1: Total Searches, Result Clicks and Record Views by Month and Platform
     - Platform Usage
     - The R5 report provides equivalent metrics as well as additional metrics related to item full-text requests.

   * - Title Report 1: Number of Successful Requests for Journal Full-Text Articles and Book Sections by Month and Title
     - Title Report
     - The Title Report offers a single report for books and journals and can show the usage broken down by Section_Type.

   * - Title Report 1 Mobile: Number of Successful Requests for Journal Full-Text Articles and Book Sections by Month and Title (formatted for normal browsers/delivered to mobile devices AND formatted for mobile devices/delivered to mobile devices
     - Eliminated (no equivalent)
     - Capturing usage by mobile devices is less relevant with the responsive design of most sites. The variety of mobile devices also makes it difficult, as does the fact that today’s smartphones have screen resolutions exceeding those of some desktops.

   * - Title Report 2: Access Denied to Full-Text Items by Month, Title and Category
     - Title Report
     - The Title Report offers a single report for books and journals and includes the options to show Access Denied metrics.

   * - Title Report 3: Number of Successful Item Requests by Month, Title and Page Type
     - Title Report
     - The Title Report offers a single report for books and journals and can show Requests metrics.

   * - Title Report 3 Mobile: Number of Successful Item Requests by Month, Title and Page Type (formatted for normal browsers/delivered to mobile devices AND formatted for mobile devices/delivered to mobile devices
     - Eliminated (no equivalent)
     - Capturing usage by mobile devices is less relevant with the responsive design of most sites. The variety of mobile devices also makes it difficult, as does the fact that today’s smartphones have screen resolutions exceeding those of some desktops.


.. _appendix-b-1-2:

B.1.2 Report Format
"""""""""""""""""""

With R5, all COUNTER reports are structured the same way to ensure consistency, not only between reports, but also between the JSON and tabular versions of the reports. Now all reports share the same format for the header, the report body is derived from the same set of element names, total rows have been eliminated, and data values are consistent between the JSON and tabular version. (See :numref:`formats`). R5 also addresses the problem of terminology and report layouts varying from report to report, as well as JSON and tabular versions of the same report producing different results while still being compliant.


.. _appendix-b-1-3:

B.1.3 Metric Types
""""""""""""""""""

Release 5 of the COUNTER Code of Practice strives for simplicity and clarity by reducing the number of metric types and standardizing them across all reports, as applicable. With R4, Book Reports had different metric types from those in Journal Reports or in additional attributes such as mobile usage, usage by format, etc. Most COUNTER R4 metric types have either been renamed or eliminated in favour of new R5 Metric_Types. The table below show the R4 metric types as documented for SUSHI and their R5 state.

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.17}|>{\raggedright\arraybackslash}\Y{0.28}|>{\parskip=\tparskip}\Y{0.55}|

.. list-table::
   :class: longtable
   :widths: 14 21 65
   :header-rows: 1

   * - R4 Metric Types
     - R5 Equivalence or Status
     - Comments

   * - abstract
     - Total_Item_Investigations\ |br|\ |lb|
       Unique_Item_Investigations\ |br|\ |lb|
       Unique_Title_Investigations
     - Actions against an item are tracked using the more generic Total_Item_Investigations metric. Due to the variety of types of item attributes that can be investigated, COUNTER no longer attempts to track them with separate Metric_Types.

   * - audio
     - Eliminated
     - This metric was only used in JR3/TR3 reports which saw little implementation or use. The intent was to represent activity of objects embedded in articles.

   * - data_set
     - Eliminated
     - When a content item was a data_set, the Total_Item_Requests metrics would be used in combination with a Data_Type of Dataset.

   * - ft_epub
     - Total_Item_Requests\ |br|\ |lb|
       Unique_Item_Requests\ |br|\ |lb|
       Unique_Title_Requests
     - More generic Total_Item_Requests are now used in place of format-specific metrics.

   * - ft_html
     - Total_Item_Requests\ |br|\ |lb|
       Unique_Item_Requests\ |br|\ |lb|
       Unique_Title_Requests
     - More generic Total_Item_Requests are now used in place of format-specific metrics.

   * - ft_html_mobile
     - Eliminated
     - Tracking of activity by mobile devices is no longer required for COUNTER compliance.

   * - ft_pdf
     - Total_Item_Requests\ |br|\ |lb|
       Unique_Item_Requests\ |br|\ |lb|
       Unique_Title_Requests
     - More generic Total_Item_Requests are now used in place of format-specific metrics.

   * - ft_pdf_mobile
     - Eliminated
     - Tracking of activity by mobile devices is no longer required for COUNTER compliance.

   * - ft_ps
     - Total_Item_Requests\ |br|\ |lb|
       Unique_Item_Requests\ |br|\ |lb|
       Unique_Title_Requests
     - More generic Total_Item_Requests are now used in place of format-specific metrics.

   * - ft_ps_mobile
     - Eliminated
     - Tracking of activity by mobile devices is no longer required for COUNTER compliance.

   * - ft_total
     - Total_Item_Requests
     - Total_Item_Requests is a comparable metric.

   * - image
     - Eliminated
     - This metric was only used in JR3/TR3 reports which saw little implementation or use. The intent was to represent activity of objects embedded in articles.

   * - multimedia
     - Total_Item_Requests\ |br|\ |lb|
       Unique_Item_Requests\ |br|\ |lb|
       Unique_Title_Requests
     - More generic Total_Item_Requests are now used in place of format-specific metrics.

   * - no_license
     - No_License
     - No change.

   * - other
     - Eliminated
     - Other usage provides no value.

   * - podcast
     - Eliminated
     - This metric was only used in JR3/TR3 reports which saw little implementation or use. The intent was to represent activity of objects embedded in articles.

   * - record_view
     - Total_Item_Investigations\ |br|\ |lb|
       Unique_Item_Investigations\ |br|\ |lb|
       Unique_Title_Investigations
     - Actions against an item are tracked using the more generic Total_Item_Investigations metrics. Due to the variety of types of item attributes that can be investigated, COUNTER no longer attempts to track them with separate Metric_Types.

   * - reference
     - Total_Item_Investigations\ |br|\ |lb|
       Unique_Item_Investigations\ |br|\ |lb|
       Unique_Title_Investigations
     - Actions against an item are tracked using the more generic Total_Item_Investigations metrics. Due to the variety of types of item attributes that can be investigated, COUNTER no longer attempts to track them with separate Metric_Types.

   * - result_click
     - Total_Item_Investigations\ |br|\ |lb|
       Unique_Item_Investigations\ |br|\ |lb|
       Unique_Title_Investigations
     - Actions against an item are tracked using the more generic Total_Item_Investigations metrics. Due to the variety of types of item attributes that can be investigated, COUNTER no longer attempts to track them with separate Metric_Types.

   * - search_fed
     - Searches_Federated\ |br|\ |lb|
       Searches_Automated
     - The R4 automated and federated search metrics have been separated into two separate metrics since the nature of the activity is very different.

   * - search_reg
     - Searches_Regular\ |br|\ |lb|
       Searches_Platform
     - For database reports, use Searches_Regular. When reporting at the platform level use Searches_Platform.

   * - sectioned_html
     - Total_Item_Requests\ |br|\ |lb|
       Unique_Item_Requests\ |br|\ |lb|
       Unique_Title_Requests
     - More generic Total_Item_Requests are now used in place of format-specific metrics.

   * - toc
     - Total_Item_Investigations\ |br|\ |lb|
       Unique_Item_Investigations\ |br|\ |lb|
       Unique_Title_Investigations
     - Actions against an item are tracked using the more generic Total_Item_Investigations metrics. Due to the variety of types of item attributes that can be investigated, COUNTER no longer attempts to track them with separate Metric_Types. Note that for journals TOCs aren’t item-level objects, therefore TOC usage MUST NOT be reported for journals.

   * - turnaway
     - Limit_Exceeded
     - Renamed to provide more clarity into the nature of the access-denied event.

   * - video
     - Eliminated
     - This metric was only used in JR3/TR3 reports which saw little implementation or use. The intent was to represent activity of objects embedded in articles.


.. _appendix-b-1-4:

B.1.4 New elements and attributes introduced
""""""""""""""""""""""""""""""""""""""""""""

With R4 the nature of the usage sometimes had to be inferred based on the name of the report. In an effort to provide more consistent and comparable reporting, R5 introduces some additional attributes that content providers can track with the usage and use to create breakdowns and summaries of usage.

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.17}|>{\parskip=\tparskip}\Y{0.57}|>{\raggedright\arraybackslash}\Y{0.26}|

.. list-table::
   :class: longtable
   :widths: 10 70 20
   :header-rows: 1

   * - Attribute
     - Description
     - Values

   * - Access_Type
     - Used in conjunction with Investigations and Requests, this attribute indicates if, at the time of the investigation or request, access to the item was controlled (e.g. subscription or payment required) or was available as Open Access or other free-to-read option.
     - Controlled\ |br|\ |lb|
       OA_Delayed (reserved for future)\ |br|\ |lb|
       OA_Gold\ |br|\ |lb|
       Other_Free_to_Read

   * - Access_Method
     - This attribute is used to distinguish between regular usage (users accessing scholarly information for research purposes) and usage for the purpose of Text and Data Mining (TDM).
     - Regular\ |br|\ |lb|
       TDM

   * - Data_Type
     - Used to generally classify the nature of the item the usage is being presented for.
     - Article\ |br|\ |lb|
       Book\ |br|\ |lb|
       Book_Segment\ |br|\ |lb|
       Database\ |br|\ |lb|
       Dataset\ |br|\ |lb|
       Journal\ |br|\ |lb|
       Multimedia\ |br|\ |lb|
       Newspaper_or_Newsletter\ |br|\ |lb|
       Other\ |br|\ |lb|
       Platform\ |br|\ |lb|
       Report\ |br|\ |lb|
       Repository_Item\ |br|\ |lb|
       Thesis_or_Dissertation

   * - Publisher_ID
     - A unique identifier for the publisher, preferably a standard identifier such as ISNI. For the JSON version of the report, the type (namespace) and value are separate. For tabular, the format is *{namespace}*:*{value}*.
     - ISNI:1233344455678889

   * - Section_Type
     - Used in conjunction with Data_Type, this attribute tracks requests to the level of the section requested. Used mostly with books where content may be delivered by chapter or section, this element defines the nature of the section retrieved.
     - Article\ |br|\ |lb|
       Book\ |br|\ |lb|
       Chapter\ |br|\ |lb|
       Other\ |br|\ |lb|
       Section

   * - YOP
     - This attribute records the year of publication of the item. The YOP attribute replaces the year-of-publication ranges in R4’s JR5 report and is tracked for all metrics in Title and Item Reports.
     - A 4-digit year, e.g. 2023\ |br|\ |lb|
       0001 for unknown\ |br|\ |lb|
       9999 for articles in press
