.. The COUNTER Code of Practice © 2017-2024 by COUNTER Metrics
   is licensed under CC BY 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by/4.0/

Creating Custom Elements/Columns Headings
-----------------------------------------

Custom elements/column headings can be added to the COUNTER Reports (PR, DR, TR, IR) and custom reports. The element name MUST take the form of *{namespace}*:*{element name}*. An example of a custom elements/column heading could be:

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.27}|

.. list-table::
   :class: longtable
   :widths: 27
   :header-rows: 1

   * - Element Name

   * - EBSCOhost:Total_Linkouts

Custom elements/column headings MUST only be included in COUNTER Reports if called for, and if included they MUST be listed in Attributes_To_Show in the Report_Attributes header.
