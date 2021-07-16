.. The COUNTER Code of Practice Release 5 © 2017-2021 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

.. _delivery:

Delivery of COUNTER Reports
===========================

Content providers MUST make tabular versions of COUNTER reports available from an administrative/reporting site accessible by members of the institution requesting the report. All COUNTER reports provided by the content provider MUST also be available via the COUNTER_SUSHI API. Delivery requirements are:

* Reports MUST be provided in the following formats:

  * In tabular form as either an Excel or a tab-separated-value (TSV) file, or both. Additional file formats that can be easily imported into spreadsheet programs without loss or corruption may be offered at the vendor's discretion.
  * JSON formatted in accordance with the COUNTER_SUSHI API Specification (see :numref:`sushi` below).

* The reports in JSON, TSV and other text formats MUST be encoded using UTF-8.
* Each report MUST be delivered as a separate file to facilitate automated processing of usage reports into ERM and usage consolidation systems. For clarity, multiple reports MUST NOT be included in the same Excel file as separate worksheets.
* Tabular reports MUST be made available through a website.

  * The website may be password-controlled.
  * Email alerts may be sent when data is updated.
  * The report interface MUST provide filter and configuration options for the Master Reports that apply to the content provider.
  * The report interface MUST offer all Standard Views the content provider is required to provide, and Standard Views options MUST automatically apply the REQUIRED filter and configuration options and not allow the user to alter the filters or configuration options except for the usage begin and end dates.
  * The date range fields on the user interface MUST default to the latest month with complete usage. For example, if the current date is 15 May 2019 and April usage has been processed, the begin date would default to 01 April 2019 and the end date would default to 30 April 2019. If the April usage has not yet been processed, the start and end dates would default to 01 March 2019 and 31 March 2019.
  * Master Reports must include the option to Exclude_Monthly_Details. Item Master Reports must include the options to Include_Parent_Details and Include_Component_Details (see :numref:`filters-attributes` for details).

* Reports MUST be provided monthly.
* Data MUST be updated within 4 weeks of the end of the reporting period.
* Usage MUST be processed for the entire month before any usage for that month can be included in reports. If usage for a given month is not available yet, no usage for that month MUST be returned and an exception 3031 included in the report/response to indicate that usage is not ready for requested dates.
* A minimum of the current year plus the prior 24 months of usage data MUST be available, unless the content provider is newly COUNTER compliant.
* When content providers become compliant with a new release of the Code of Practice, they begin compiling usage compliant with the new release from the time they become compliant; and they MUST continue to provide the older usage that complies with the previous release(s) of the Code of Practice to fulfil the requirement.
* The reports MUST allow the customer the flexibility to specify a date range, in terms of months, within the most recent 24-month period.
* Reports MUST be available for harvesting via the COUNTER_SUSHI API within 4 weeks of the end of the reporting period.

.. toctree::
   :maxdepth: 1

   01-access-to-usage-for-consortia
