.. The COUNTER Code of Practice Release 5 © 2017-2021 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

.. _custom-reports:

Creating Custom COUNTER Reports
-------------------------------

Custom COUNTER reports can be created as long as the general layout for COUNTER reports is followed. Custom reports MUST be given an identifier and a name in the format of *{namespace}*:*{report ID}* and *{namespace}*:*{report name}*. An example of a custom report could be:

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.18}|>{\raggedright\arraybackslash}\Y{0.30}|

.. list-table::
   :class: longtable
   :widths: 18 30
   :header-rows: 1

   * - Report_ID
     - Report_Name

   * - EBSCOhost:LR1
     - EBSCOhost:Link-out Report 1

It is recommended to make custom reports available both from the administrative/reporting site and via the COUNTER_SUSHI API and to include them in the response for the /reports path in the COUNTER_SUSHI API (see :numref:`sushi`).
