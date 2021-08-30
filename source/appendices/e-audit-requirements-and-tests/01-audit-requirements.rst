.. The COUNTER Code of Practice Release 5 © 2017-2021 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

E.1 Audit Requirements
----------------------

The COUNTER audit seeks to mirror the activity of an institution (a customer) carrying out usage on the content provider’s platform. The COUNTER audit procedures and tests are to ensure the usage reports provided by content providers comply with the COUNTER R5 Code of Practice. 

Third-party hosts and vendors must be taken into account for usage reporting. Both hosts and vendors have additional audit requirements. The details are below:

* **Third-party hosts**: Some publishers have their online content hosted by a third party that provides standard usage statistics reporting as part of a broader hosting service. In these cases, it is the third-party host that is audited. For the audit the third-party host must provide the auditor with a list of all publishers hosted by them and the related COUNTER Reports and Standard Views. The auditor will then select a minimum of two publishers at random from the list and audit accordingly.
* **Third-party vendors**: Some publishers use third-party companies that provide bespoke usage-statistics reporting services, where the solutions used may differ significantly for each client publisher. In this case the third-party vendor must provide the auditor with a list of all their client publishers and the COUNTER Reports and Standard Views offered by each. The auditor will then select 10% of the publishers (up to a maximum of 5, with a minimum of 2) from this list and carry out the audit tests specified below.

Prior to an audit any third-party host/vendor must discuss with COUNTER how they provide usage statistics reporting. COUNTER can advise which category applies.

**The auditor will request written confirmation from COUNTER prior to proceeding.**


E.1.1 Audit Tests and Process
"""""""""""""""""""""""""""""

COUNTER defines specific audit tests for each of the COUNTER required usage reports. As content providers may work with different auditors, the audit test scripts help to ensure each auditor follows a common auditing procedure. This is covered in greater depth in Section E.2 Audit Tests.

There are three audit compliance stages:

* **Stage 1: Format.** The usage reports are reviewed by the auditor to confirm they adhere to the COUNTER R5 Code of Practice. This review includes format and presentation of all relevant COUNTER reports.
* **Stage 2: Data Integrity.** The usage statistics reported by the content provider are verified by the auditor to accurately record the activity carried out during the audit. The auditor will check that the content provider supplies consistent usage statistics when reports are accessed using different browsers, including Google Chrome, Internet Explorer, and Mozilla Firefox as a minimum. Note: COUNTER will review the selected browsers annually. 

  To ensure reports are counting correctly as per the COUNTER R5 Code of Practice, it is important browser cache settings of the test machines are disabled. It is also important the content provider confirms before the audit period whether or not they operate a cache server. If they do, tests may not report as the COUNTER R5 Code of Practice expects. It is likely there will be some under-reporting.
* **Stage 3: Report Delivery.** The auditor tests the content provider has implemented the COUNTER_SUSHI API correctly and reports can be accessed using SUSHI according to the instructions supplied by the content provider (which must comply with the COUNTER_SUSHI API specification). Note: Implementation of the COUNTER_SUSHI API is a requirement for compliance and is covered by the Declaration of COUNTER Compliance signed by all compliant content providers. Delivery of reports via Excel or tab separated value (TSV) file will still be required as specified in the COUNTER R5 Code of Practice.

The COUNTER auditor cannot express an opinion regarding usage reported in any other accounts/institutions, or regarding aspects of the COUNTER R5 Code of Practice, not specifically tested.


E.1.2 Frequency of the Audit
""""""""""""""""""""""""""""

Once a content provider is listed in the Register of COUNTER Compliant Content Providers an independent audit is required within 6 months to maintain COUNTER-compliant status. Independent audits must be completed annually thereafter. Content providers that are members of COUNTER in the Smaller Publisher category, may be audited biennially with permission from COUNTER. Failure to meet these audit requirements will result in a content provider losing its COUNTER-compliant status.

If COUNTER does not receive a satisfactory auditor’s report within the specified timeframe, the following control procedures apply:

**New content providers having signed the Declaration of Compliance:**

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.25}|>{\parskip=\tparskip}\Y{0.75}|

.. list-table::
   :class: longtable
   :widths: 18 82

   * - 6 months after signing
     - A reminder from COUNTER that the first auditor’s report is required

   * - 8 months after signing
     - A final reminder from COUNTER that the first auditor’s report is required

   * - 9 months after signing
     - The content provider is removed from the registry and is notified by COUNTER that they are non-compliant and must not make reference to COUNTER or use the COUNTER logo.

**Content providers previously audited:**

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.25}|>{\parskip=\tparskip}\Y{0.75}|

.. list-table::
   :class: longtable
   :widths: 27 73

   * - 3 months following the due audit date
     - A reminder from COUNTER that an auditor’s report is required

   * - 2 months following the due audit date
     - A further reminder from COUNTER that an auditor’s report is required

   * - 5 months following the due audit date
     - A **final** reminder from the Chair of the COUNTER Executive Committee that an auditor’s report is required

   * - 6 months following the due audit date
     - The content provider is removed from the registry and is notified by COUNTER that they are non-compliant and must not make reference to COUNTER or use the COUNTER logo.


E.1.3 Host Types and COUNTER Reports
""""""""""""""""""""""""""""""""""""

Independent audits are required for COUNTER reports according to Host_Types. See Table 1 (below).

Table 1: COUNTER Reports Requiring Audit

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.12}|>{\raggedright\arraybackslash}\Y{0.13}|>{\raggedright\arraybackslash}\Y{0.23}|>{\raggedright\arraybackslash}\Y{0.18}|>{\raggedright\arraybackslash}\Y{0.34}|

.. list-table::
   :class: longtable
   :widths: 10 11 32 14 35
   :header-rows: 1

   * - Category
     - Report_ID
     - R5 Report_Name
     - Master Report / Standard View
     - Host_Type

   * - Platform
     - PR
     - Platform Master Report
     - Master Report
     - All

   * - Platform
     - PR_P1
     - Platform Usage
     - Standard View
     - All

   * - Database
     - DR
     - Database Master Report
     - Master Report
     - - Aggregated_Full_Content\ |br|\ |lb|
       - A&I_Database\ |br|\ |lb|
       - Discovery_Service\ |br|\ |lb|
       - eBook_Collection\ |br|\ |lb|
       - Full_Content_Database\ |br|\ |lb|
       - Multimedia_Collection

   * - Database
     - DR_D1
     - Database Searches and Item Usage
     - Standard View
     - - Aggregated_Full_Content\ |br|\ |lb|
       - A&I_Database\ |br|\ |lb|
       - Discovery_Service\ |br|\ |lb|
       - eBook_Collection\ |br|\ |lb|
       - Full_Content_Database\ |br|\ |lb|
       - Multimedia_Collection

   * - Database
     - DR_D2
     - Database Access Denied
     - Standard View
     - - Aggregated_Full_Content\ |br|\ |lb|
       - A&I_Database\ |br|\ |lb|
       - Discovery_Service\ |br|\ |lb|
       - eBook_Collection\ |br|\ |lb|
       - Full_Content_Database\ |br|\ |lb|
       - Multimedia_Collection

   * - Title
     - TR
     - Title Master Report
     - Master Report
     - - Aggregated_Full_Content\ |br|\ |lb|
       - eBook\ |br|\ |lb|
       - eBook_Collection\ |br|\ |lb|
       - eJournal

   * - Title
     - TR_B1
     - Book Requests (excluding OA_Gold)
     - Standard View
     - - Aggregated_Full_Content\ |br|\ |lb|
       - eBook\ |br|\ |lb|
       - eBook_Collection

   * - Title
     - TR_B2
     - Book Access Denied
     - Standard View
     - - Aggregated_Full_Content\ |br|\ |lb|
       - eBook\ |br|\ |lb|
       - eBook_Collection

   * - Title
     - TR_B3
     - Book Usage by Access Type
     - Standard View
     - - Aggregated_Full_Content\ |br|\ |lb|
       - eBook\ |br|\ |lb|
       - eBook_Collection

   * - Title
     - TR_J1
     - Journal Requests (excluding OA_Gold)
     - Standard View
     - - Aggregated_Full_Content\ |br|\ |lb|
       - eJournal

   * - Title
     - TR_J2
     - Journal Access Denied
     - Standard View
     - - Aggregated_Full_Content\ |br|\ |lb|
       - eJournal

   * - Title
     - TR_J3
     - Journal Usage by Access Type
     - Standard View
     - - Aggregated_Full_Content\ |br|\ |lb|
       - eJournal

   * - Title
     - TR_J4
     - Journal Requests by YOP (excluding OA_Gold)
     - Standard View
     - - Aggregated_Full_Content\ |br|\ |lb|
       - eJournal

   * - Item
     - IR
     - Item Master Report
     - Master Report
     - - Data_Repository\ |br|\ |lb|
       - Multimedia\ |br|\ |lb|
       - Repository\ |br|\ |lb|
       - Scholarly_Collaboration_Network

   * - Item
     - IR_A1
     - Journal Article Requests
     - Standard View
     - - Repository\ |br|\ |lb|
       - Scholarly_Collaboration_Network

   * - Item
     - IR_M1
     - Multimedia Item Requests
     - Standard View
     - - Multimedia


E.1.4 Audit Test Requirements
"""""""""""""""""""""""""""""

COUNTER defines a reporting period as a calendar month. A report run for any given month MUST reflect all activity of a customer for the entire selected audit month. The auditor must also conduct and conclude all audit tests within the audit month.

To prevent any collision of reported data, an auditor must be allowed to set up and maintain separate accounts for each of the audit tests. During the audit month, there should not be any activity on the audit accounts other than activity generated by the auditor. Any non-auditor activity on the test accounts will make the test reports unreliable, may result in further audit tests and may incur additional costs.

Prior to the audit, the content provider must supply to the auditor:

* Account details for at least 4 separate accounts with access to all areas required to be tested (or specific restrictions for turn-away testing).
* Links to download usage reports in all required formats. COUNTER reports must be provided as tabular versions, which can be easily imported into Microsoft Excel.
* SUSHI credentials for the test accounts to enable verification of SUSHI harvesting and formatting of the harvested reports.
* A declaration confirming federated and automated searches have been disaggregated from any searches reported. See the COUNTER R5 Code of Practice for further information on the protocols regarding federated and automated searches.
* If server-side caching is implemented, information on cache settings used should be provided.

  **Note:** Server-side caching can cause a discrepancy between the usage recorded in the audit tests and the usage reported by the content provider. Information on cache settings enables the auditor to take them into account when evaluating the results of the report tests. If the content provider does not provide this information, the auditor is likely to require further audit tests that may incur additional costs.
