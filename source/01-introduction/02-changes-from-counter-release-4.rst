.. The COUNTER Code of Practice Release 5 © 2017-2023 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

Changes from COUNTER Release 4
------------------------------

Changes in the nature of online content and how it is accessed have resulted in the COUNTER Code of Practice evolving in an attempt to accommodate those changes. This evolution resulted in some ambiguities and, in some cases, conflicts and confusions within the Code of Practice. R5 of the COUNTER Code of Practice is focused on improving the clarity, consistency, and comparability of usage reporting.


List of Reports
"""""""""""""""

R5 of the COUNTER Code of Practice reduces the overall number of reports by replacing many of the special-purpose reports that are seldom used with a small number of flexible generic reports. All COUNTER R4 reports have either been renamed or eliminated in favour of other COUNTER R5 report options.

See :ref:`Appendix B, Section B.1.1 <appendix-b-1-1>` for more details.


Report Format
"""""""""""""

The Standardized Usage Statistics Harvesting Initiative (SUSHI) protocol used in R4 was designed to simplify the gathering of usage statistics by librarians. In R5 the SOAP/XML based SUSHI protocol is replaced with the RESTful COUNTER_SUSHI API that uses JavaScript Object Notation (JSON) for a more lightweight data-interchange. The JSON format not only is easy for humans to read and write, but it is easy for machines to parse and generate. Support of the COUNTER_SUSHI API is mandatory for compliance with R5 (see :numref:`sushi` below).

With R5, all COUNTER reports are structured the same way to ensure consistency, not only between reports, but also between the JSON and tabular versions of the reports. Now, all reports share the same format for the header, the report body is derived from the same set of element names, total rows have been eliminated, and data values are consistent between the JSON and tabular version. R5 also addresses the problems of terminology and report layouts varying from report to report, as well as JSON and tabular versions of the same report producing different results while still being compliant.


Metric Types
""""""""""""

R5 strives for simplicity and clarity by reducing the number of Metric_Types and applying these Metric_Types across all reports, as applicable. With R4, Book Reports had metric types that could be considered different from metric types in Journal Reports and metric types attempting to reflect additional attributes such as mobile usage, usage by format, etc. Most R4 metric types have either been renamed or eliminated in favour of new R5 Metric_Types.

See :ref:`Appendix B, Section B.1.3 <appendix-b-1-3>` for a table showing the R4 metric types and their R5 equivalence or status.


New Elements and Attributes Introduced
""""""""""""""""""""""""""""""""""""""

With R4 the nature of the usage sometimes had to be inferred based on the name of the report. To provide more consistent and comparable reporting, R5 introduces some additional attributes that content providers can use to create breakdowns and summaries of usage.

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.17}|>{\parskip=\tparskip}\Y{0.83}|

.. list-table::
   :class: longtable
   :widths: 14 86

   * - Access_Type
     - Used to track usage of content that is either Open (open access), Free_To_Read, or Controlled (requires a license).

   * - Access_Method
     - Used to track if the purpose of the access was for regular use or for text and data mining (TDM). This attribute allows TDM usage to be excluded from Standard Views and reported on separately.

   * - Data_Type
     - Identifies the type of content usage being reported on. Expanded to include additional Data_Types, including Article, Book, Book_Segment, Database, Dataset, Journal, Multimedia, Newspaper_or_Newsletter, Other, Platform, Report, Repository_Item, and Thesis_or_Dissertation.

   * - Publisher_ID
     - Introduced to improve matching and reporting by publisher.

   * - Section_Type
     - Identifies the type of section that was accessed by the user, including Article, Book, Chapter, Other and Section. Used primarily for reporting on book usage where content is delivered by section.

   * - YOP
     - Year of publication as a single element, simplifies reporting by content age.

The above items are covered in more detail in :numref:`specifications` below as well as in :ref:`Appendix B, Section B.1.4 <appendix-b-1-4>`.
