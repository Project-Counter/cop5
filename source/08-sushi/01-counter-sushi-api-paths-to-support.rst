.. The COUNTER Code of Practice Release 5 © 2017-2023 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

COUNTER_SUSHI API Paths to Support
----------------------------------

The following paths (methods) MUST be supported:

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.11}|>{\raggedright\arraybackslash}\Y{0.21}|>{\parskip=\tparskip}\Y{0.68}|

.. list-table::
   :class: longtable
   :widths: 8 17 75
   :header-rows: 1

   * - HTTP Method
     - Path
     - Description

   * - GET
     - /status
     - Returns the current status of the COUNTER_SUSHI API service. This path returns a message that includes the operating status of the API, the URL to the service’s entry in the Register of COUNTER Compliant Content Providers, and an array of service alerts (if any).

   * - GET
     - /reports
     - Returns a list of reports supported by the COUNTER_SUSHI API service. The response includes an array of reports, including the report identifier, the release number, the report name, a description, and (optional but recommended for custom reports) the path to use when requesting the report.

   * - GET
     - /reports/*{Report_ID in lower case}*
     - Each supported report has its own path, e.g. GET /reports/tr_b1 for “Book Requests (Excluding OA_Gold)”, GET /reports/tr_j1 for “Journal Requests (Excluding OA_Gold)”.

   * - GET
     - /members
     - Returns the list of consortium members or sites for multi-site customers. The response includes an array of customer account information, including for each the customer ID (to use when requesting COUNTER reports), the requestor ID (to use when requesting COUNTER reports), the customer account name, and additional identifiers for the organization (if any). Note that if the customer ID specified in the parameter for the /members path is not a multi-site organization, then the response will simply return the details for that customer.
