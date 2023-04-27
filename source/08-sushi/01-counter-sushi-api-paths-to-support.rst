.. The COUNTER Code of Practice Release 5 © 2017-2023 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

.. _sushi-paths:

COUNTER_SUSHI API Paths to Support
----------------------------------

Starting with Release 5.1, the COUNTER_SUSHI API paths include the Release in the format */r{Release without .}*, so that the COUNTER_SUSHI API is properly versioned.

Report providers SHOULD use the same COUNTER_SUSHI API base URL for all releases. For example, if the URL for requesting the list of reports is ``https://example.org/sushi/reports`` in R5, it should be ``https://example.org/sushi/r51/reports`` in R5.1, so that the base URL for both releases is ``https://example.org/sushi``.

The following paths (methods) MUST be supported:

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.11}|>{\raggedright\arraybackslash}\Y{0.24}|>{\parskip=\tparskip}\Y{0.65}|

.. list-table::
   :class: longtable
   :widths: 8 17 75
   :header-rows: 1

   * - HTTP Method
     - Path
     - Description

   * - GET
     - /r51/status
     - Returns the current status of the COUNTER_SUSHI API service. This path returns a message that includes the operating status of the API, the URL to the service’s entry in the Register of COUNTER Compliant Report Providers, and an array of service alerts (if any).

       This path MUST be public, i.e. not protected by the methods described in :numref:`sushi-security`, to allow report consumers to easily check whether a SUSHI server is live.

   * - GET
     - /r51/reports
     - Returns a list of reports supported by the COUNTER_SUSHI API service. The response includes an array of reports, including the report identifier, the release number, the report name, a description, the path to use when requesting the report (optional but recommended for custom reports), and the first and last months for which usage data has been processed and is available. This information SHOULD be specific for each customer ID.

   * - GET
     - /r51/reports/*{Report_ID in lower case}*
     - Each supported report has its own path, e.g. GET /r51/reports/tr_b1 for “Book Requests (Controlled)”, GET /r51/reports/tr_j1 for “Journal Requests (Controlled)”.

   * - GET
     - /r51/members
     - Returns the list of consortium members or sites for multi-site customers. The response includes an array of customer account information, including for each the customer ID (to use when requesting COUNTER reports), the requestor ID (to use when requesting COUNTER reports), the customer account name, and additional identifiers for the organization (if any). Note that if the customer ID specified in the parameter for the /r51/members path is not a multi-site organization, then the response will simply return the details for that customer.
