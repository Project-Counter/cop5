.. The COUNTER Code of Practice Release 5 © 2017-2023 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

.. _validation-tool:

COUNTER Validation Tool
-----------------------

The `COUNTER Validation Tool <https://www.projectcounter.org/validation-tool/>`_ allows report providers and auditors to quickly perform compliance checks related to format and consistency of both JSON and tabular reports. Report providers SHOULD use this free tool to check their reports and COUNTER_SUSHI API implementation and fix issues detected by the tool before they begin the audit. It is recommended to use the tool not just when preparing for the audit, but to integrate the testing in the regular QA processes or at least test regularly to make sure the reports stay compliant. We recommend testing reports using the Validation Tool once every four months at a minimum, and monthly where possible. 

The COUNTER Release 5 Validation Tool uses the following error levels to report issues with different severity:

* **Fatal error** - Validation was aborted because an unrecoverable error was encountered, for example a missing or invalid Reporting_Period. The fatal error MUST be fixed before the report can be fully validated.
* **Critical error** - Validation has detected a serious error that MUST be fixed, for example inconsistent data like a title with more Unique_Item_Requests than Total_Item_Requests or missing data. A critical error indicates that there could be a serious issue that would cause the audit to fail.
* **Error** - Validation has detected an error that MUST be fixed to pass the audit.
* **Warning** - Validation has detected an issue that needs to be checked by the auditor and might affect the result of the audit.
* **Notice** - Additional information, for example about deprecations or amendments that must be addressed at some point in the future but currently will not affect the result of an audit.
