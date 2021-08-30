.. The COUNTER Code of Practice Release 5 © 2017-2021 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

E.3 Audit Compliance
--------------------

E.3.1 Data Integrity
""""""""""""""""""""

During the audit testing, the auditor’s activities must be isolated from other activities on the content provider’s site. Depending on the site being tested, the auditor must conduct the audit test from a computer with a unique IP address and/or using a unique account number.

The auditor must accept user/machine and session cookies when prompted.

To ensure reporting is counting correctly as per the COUNTER R5 Code of Practice, it is important the browser cache settings of the machines used for testing are disabled. It is also important the auditee confirms before the audit period whether they operate a cache server.


E.3.2 Report Delivery
"""""""""""""""""""""

The auditor will check the following:

* The delivery of reports in tabular format.
* The reports are downloadable using the SUSHI protocol

This testing of report delivery and formats may be undertaken using the COUNTER Report Validation Tool (see :numref:`validation-tool` of the COUNTER R5 Code of Practice).

The JSON-formatted reports produced by SUSHI must match the total usage counted on the equivalent tabular report. A report should produce the same results irrespective of the delivery format.


E.3.3 Report Format
"""""""""""""""""""

**The auditor will confirm each of the audit reports complies with the COUNTER R5 Code of Practice.**

The following items will be checked:

* The layout of the report (headers, number of fields, field sequence, totals field, and format of reported numbers)
* The conformity of identifiers to the required standard (e.g. ISSNs must be provided as nine digits, with a hyphen as the middle digit)
* The presence of all required file formats (a Microsoft Excel or tab-separated value (TSV) file or both, additional file formats that can be easily imported into spreadsheet programs without loss or corruption may be offered at the vendor’s discretion)
* Email alerts set to report usage reports are updated in a timely manner
* Flexibility in the reporting period so customers can specify the start and end months of data reported in the COUNTER reports
* That COUNTER reports are available in JSON format in accordance with the COUNTER_SUSHI API Specification (the specification is maintained by COUNTER on SwaggerHub, see :numref:`sushi` of the COUNTER R5 Code of Practice for details)
* That all required COUNTER reports are available via the COUNTER_SUSHI API
* That the JSON formatted reports produced via SUSHI matches the total of the relevant usage counted on the equivalent TSV/Excel report offered by the content provider, i.e. a report should produce the same results irrespective of the format in which it is delivered
