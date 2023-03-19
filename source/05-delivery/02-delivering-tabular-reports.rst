.. The COUNTER Code of Practice Release 5 © 2017-2023 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

Delivering Tabular Reports
--------------------------

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
