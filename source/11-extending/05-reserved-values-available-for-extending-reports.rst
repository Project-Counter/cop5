.. The COUNTER Code of Practice Release 5 © 2017-2021 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

Reserved Values Available for Extending Reports
-----------------------------------------------

This Code of Practice recognizes that there are some common extensions that content providers might want to include in Master Reports or when creating custom reports; therefore, the following element names and element values have been reserved for this common use:

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.19}|>{\parskip=\tparskip}\Y{0.41}|>{\parskip=\tparskip}\Y{0.4}|

.. list-table::
   :class: longtable
   :widths: 14 35 51
   :header-rows: 1

   * - Reserved Name
     - Description
     - Use-case

   * - Customer_ID
     - An element/column heading for the body of the report.
     - When a report contains usage for multiple organizations.

   * - Institution_Name
     - An element/column heading for the body of the report.
     - When a report contains usage for multiple organizations.

   * - Format
     - An element name used to identify the format of the content. Reserved Values include:

       * HTML
       * PDF
       * Other

     - By tracking the format, the content provider can use R5 usage logs to generate R4 usage reports during the transition period.
