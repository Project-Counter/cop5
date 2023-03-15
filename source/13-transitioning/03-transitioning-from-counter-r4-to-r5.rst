.. The COUNTER Code of Practice Release 5 © 2017-2023 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

Transitioning from COUNTER R4 to R5
-----------------------------------

The transition from R4 to R5 meets the general requirements outlined in :numref:`transitioning-new-cop`.

* Report providers MUST be compliant by February 2019 for delivery of R5 reports starting with January 2019 usage.
* Report providers may choose to release their R5 compliant reporting service before February 2019.
* A report provider’s customers MUST be able to obtain R4-compliant reports for that report provider from the time the report provider’s R5 reporting service was released through to April 2019 (providing access to March 2019 usage). A report provider may provide access to R4 reports beyond April 2019 at their discretion.
* Report providers may choose to meet the requirement to provide R4 reports based on R5 metrics. The following R4 reports must be supported (when applicable to the platform): BR1, BR2, BR3, DB1, DB2, JR1, JR2, JR5, and PR1. The following table presents the equivalent R4 metric types and R5 Metric_Types and filters by report.

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.12}|>{\raggedright\arraybackslash}\Y{0.35}|>{\raggedright\arraybackslash}\Y{0.53}|

.. flat-table::
   :class: longtable
   :widths: 10 34 56
   :header-rows: 1

   * - R4 Report
     - R4 metric
     - R5 equivalent

   * - BR1
     - Full-text requests (at the book level)
     - Unique_Title_Requests AND Data_Type=Book AND Section_Type=Book

   * - BR2
     - Full-text requests (at the chapter/section level)
     - Total_Item_Requests AND Data_Type=Book AND Section_Type=Chapter|Section

   * - :rspan:`1` BR3
     - Access denied - concurrent/simultaneous user limit exceeded
     - Limit_Exceeded AND Data_Type=Book

   * - Access denied - content item not licensed
     - No_License AND Data_Type=Book

   * - :rspan:`3` DB1
     - Regular searches
     - Searches_Regular

   * - Searches - federated and automated
     - SUM (Searches_Automated, Searches_Federated)

   * - Result clicks
     - Total_Item_Investigations attributed to the database

   * - Record views
     - Total_Item_Investigations attributed to the database. (Note that resulting result click and record view counts will be the same. Report consumers should use one or the other and not add them up.)

   * - :rspan:`1` DB2
     - Access denied - concurrent/simultaneous user limit exceeded
     - Limit_Exceeded AND Data_Type=Database

   * - Access denied - content item not license
     - No_License AND Data_Type=Database

   * - :rspan:`2` JR1
     - Full-text requests
     - Total_Item_Requests AND Data_Type=Journal

   * - HTML requests
     - Leave blank unless format of HTML and PDF are also logged in which case: Total_Item_Requests AND Data_Type=Journal AND Format=HTML

   * - PDF requests
     - Leave blank unless format of HTML and PDF are also logged in which case: Total_Item_Requests AND Data_Type=Journal AND Format=PDF

   * - :rspan:`1` JR2
     - Access denied - concurrent/simultaneous user limit exceeded
     - Limit_Exceeded AND Data_Type=Journal

   * - Access denied - content item not licensed
     - No_License AND Data_Type=Journal

   * - JR5
     - Full-text requests (by year of publications)
     - Total_Item_Requests AND Data_Type=Journal, pivot on YOP

   * - :rspan:`3` PR1
     - Regular searches
     - Searches_Platform

   * - Searches - federated and automated
     - Leave blank (Searches performed on the platform via federated and automated searching are included in Searches_Platform).

   * - Result clicks
     - SUM (Total_Item_Investigations attributed to the databases)

   * - Record views
     - SUM (Total_Item_Investigations attributed to the databases). (Note that resulting result click and record view counts will be the same. Report consumers should use one or the other and not add them up.)
