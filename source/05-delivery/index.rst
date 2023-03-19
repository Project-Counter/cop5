.. The COUNTER Code of Practice Release 5 © 2017-2023 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

.. _delivery:

Delivery of COUNTER Reports
===========================

Report providers MUST make COUNTER Reports and Standard Views of the COUNTER Reports available in JSON format via the COUNTER_SUSHI API. Report providers MUST also make tabular versions of their reports available from an administrative/reporting site accessible by members of the institution requesting the report.

* Reports MUST be provided monthly.
* Data MUST be updated within 4 weeks of the end of the reporting period.
* Usage MUST be processed for the entire month before any usage for that month can be included in reports. If usage for a given month is not available yet, the report provider MUST NOT return usage for that month and MUST include exception 3031 in the report/response to indicate that usage is not ready for requested dates.
* A minimum of the current year plus the prior 24 months of usage data MUST be available, unless the report provider is newly COUNTER compliant.
* When report providers become compliant with a new release of the Code of Practice, they begin compiling usage compliant with the new release from the time they become compliant; and they MUST continue to provide the older usage that complies with the previous release(s) of the Code of Practice to fulfil the requirement.
* The reports MUST allow the report consumer the flexibility to specify a date range, in terms of months, within the most recent 24-month period.
* Report providers should provide reports on a per-customer basis where it is possible to do so accurately. That is, if a business school has a separate customer ID from its parent university and it is possible to separately identify usage from each customer ID (e.g. there are different IP ranges for the university and the business school), the school and the university should be sent separate COUNTER reports.


Delivering JSON Reports
"""""""""""""""""""""""

* JSON reports MUST be formatted in accordance with the COUNTER_SUSHI API Specification (see :numref:`sushi` below).
* The reports MUST be encoded using UTF-8. JSON reports and other SUSHI server responses MUST NOT include a byte order mark (according to `RFC 8259, Section 8.1 <https://datatracker.ietf.org/doc/html/rfc8259#section-8.1>`_).
* Reports MUST be available for harvesting via the COUNTER_SUSHI API within 4 weeks of the end of the reporting period.


Delivering Tabular Reports
""""""""""""""""""""""""""

* Tabular reports MUST be encoded using UTF-8. Tabular reports in text formats SHOULD include a byte order mark, so that spreadsheet programs can automatically detect the encoding in tabular form as either an Excel or a tab-separated-value (TSV) file, or both. Additional file formats that can be easily imported into spreadsheet programs without loss or corruption may be offered at the vendor's discretion.
* Each report MUST be delivered as a separate file to facilitate automated processing of usage reports into ERM and usage consolidation systems. For clarity, multiple reports MUST NOT be included in the same Excel file as separate worksheets.
* Tabular reports MUST be made available through a website.

  * The website may be password-controlled.
  * Email alerts may be sent when data is updated.
  * The report interface MUST provide filter and configuration options for the COUNTER Reports that apply to the report provider.
  * The report interface MUST offer all Standard Views of the COUNTER Reports the report provider is required to provide, and Standard Views options MUST automatically apply the REQUIRED filter and configuration options and not allow the report consumer to alter the filters or configuration options except for the usage begin and end dates.
  * The date range fields on the user interface MUST default to the latest month with complete usage. For example, if the current date is 15 May 2024 and April usage has been processed, the begin date would default to 01 April 2024 and the end date would default to 30 April 2024. If the April usage has not yet been processed, the start and end dates would default to 01 March 2024 and 31 March 2024.
  * COUNTER Reports must include the option to Exclude_Monthly_Details.
  * Item Reports must include the option to Include_Parent_Details. If reporting on Components is supported, Item Reports MUST include the option to Include_Component_Details (see :numref:`filters-attributes` for details).

.. toctree::
   :maxdepth: 1

   01-access-to-usage-for-consortia
