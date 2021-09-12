.. The COUNTER Code of Practice Release 5 © 2017-2021 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

E.4 Audit Conclusion
--------------------

If the auditor identifies one or more issues, the content provider MUST resolve them and pass the audit within 3 months to maintain COUNTER-compliant status. Please see :numref:`audit-result` in the COUNTER R5 Code of Practice.

The auditor will provide to the COUNTER Project Director a summary report including, as a minimum, the following information:

* The name of the content provider
* The audit period and date
* The usage report(s) tested
* For each usage report tested, the test results, indicated as a % of the reported figures over the expected
* A summary of any material issues noted with the format/structure, data integrity, and/or delivery of the content provider’s reports. If there are no issues, a PASS should be noted.
* A clear indication of the outcome of the audit: PASS, QUALIFIED PASS, or FAIL.
* Any other comments that relate to the audit and are worthy of consideration by the COUNTER Executive Committee.


Sample Audit Report:

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.11}|>{\raggedright\arraybackslash}\Y{0.1}|>{\raggedright\arraybackslash}\Y{0.1}|>{\raggedright\arraybackslash}\Y{0.11}|>{\raggedright\arraybackslash}\Y{0.115}|>{\raggedright\arraybackslash}\Y{0.11}|>{\raggedright\arraybackslash}\Y{0.09}|>{\raggedright\arraybackslash}\Y{0.105}|>{\raggedright\arraybackslash}\Y{0.17}|

.. flat-table::
   :class: longtable
   :widths: 9 8 8 19 9 9 8 9 21

   * - Content Provider
     - :cspan:`4` <name>
     - :cspan:`2` :rspan:`1`

   * - Audit Period
     - :cspan:`1` <mmm/yyyy>
     - Date
     - :cspan:`1` <mmm/yyyy>

   * - :rspan:`1` Report
     - :rspan:`1` Usage Activity Result
     - :cspan:`1` Report Format
     - :rspan:`1` Data Integrity
     - :cspan:`1` Delivery
     - :rspan:`1` Opinion
     - :rspan:`1` Comments

   * - Tabular
     - SUSHI/JSON
     - Reports Interface
     - SUSHI Server

   * - TR_J1
     - 100%
     - PASS
     - PASS
     - PASS
     - PASS
     - PASS
     - PASS
     -

   * - TR_B1
     - 112%
     - PASS
     - REPORT TOTALS included
     - PASS
     - PASS
     - PASS
     - FAIL
     - SUSHI versions of reports must not have totals.

A content provider may need to submit multiple audit reports, some of which may PASS and some of which may FAIL. The results of each report’s tests should be submitted on a separate line. For a content provider to maintain COUNTER-compliant status, each audited report must PASS.
