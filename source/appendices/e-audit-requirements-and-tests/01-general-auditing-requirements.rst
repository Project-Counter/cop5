.. The COUNTER Code of Practice Release 5 © 2017-2021 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

E.1 General Auditing Requirements
---------------------------------

Audit Philosophy
""""""""""""""""

The COUNTER audit procedures and tests set out in this Appendix seek to ensure that the usage reports provided by content providers are in line with the COUNTER Code of Practice and follow uniform agreed procedures. To this end, the COUNTER audit seeks to mirror the activity of an institution (a customer) carrying out usage on the content provider’s platform.


Third Party Hosts and Vendors
"""""""""""""""""""""""""""""

Two broad categories must be taken into account for usage statistics reporting, and each has additional audit requirements. These categories are:

* Third-party hosts: Some publishers have their online content hosted by a third party that provides standard usage statistics reporting as part of a broader hosting service. In these cases, it is the third-party host that is audited. For the audit the third-party host must provide the auditor with a list of all publishers hosted by them and the COUNTER Reports and Standard Views offered by each. The auditor will then select a minimum of two publishers at random from the list and carry out the audit tests as specified below on the selected publishers.
* Third-party vendors: Some publishers use third-party companies that provide bespoke usage-statistics reporting services, where the solutions used may differ significantly for each client publisher. In this case the third-party vendor must provide the auditor with a list of all their client publishers and the COUNTER Reports and Standard Views offered by each. The auditor will then select 10% of the publishers (up to a maximum of 5, with a minimum of 2) from this list and carry out the audit tests specified below.

**No two third-party hosts/vendors are exactly alike.** Prior to the audit each must discuss with COUNTER how they provide usage statistics reporting so that COUNTER can advise which of the two categories above applies to them.


Auditing and Test-Scripts
"""""""""""""""""""""""""

There are three stages in the COUNTER audit:

* Stage 1: Format. Here the auditor reviews usage reports to confirm that they adhere to the COUNTER Code of Practice specification, not only in terms of overall format, but to make sure relevant identifiers, such as ISSNs and ISBNs, are presented correctly. Deviations from the specified COUNTER-compliant format, such as blank rows not required by the code specification or incorrectly formatted ISSNs, can cause problems when the COUNTER usage reports are processed automatically.
* Stage 2: Data Integrity. Here the auditor confirms that the usage statistics reported by the content provider accurately record the activity carried out by the auditor during the audit. This includes checking that the content provider provides consistent usage statistics when its reports are accessed using different browsers, including Google Chrome, Internet Explorer, and Mozilla Firefox as a minimum. Note: COUNTER will review the selected browsers annually. The selection may change in the future, depending on which browsers are most widely used.
* Stage 3: Report Delivery. Here the auditor tests that the content provider has implemented SUSHI correctly and that its reports can be accessed using SUSHI according to the instructions supplied by the content provider (which must comply with the NISO/COUNTER SUSHI standard). Implementation of SUSHI is a requirement for compliance and is covered by the Declaration of COUNTER Compliance signed by all compliant content providers. Delivery of reports via Excel or .tab separated value (TSV) file will still be required as specified in the COUNTER Code of Practice.

COUNTER defines specific audit test-scripts for each of the COUNTER-required usage reports. Because content providers may work with different auditors, the test-scripts help to ensure that each auditor follows a common auditing procedure.

The COUNTER auditor cannot express an opinion as to usage reported in respect of any other accounts or institutions, or as to aspects of the COUNTER Code of Practice, not specifically tested. Release 5-compliant content providers are reminded, however, that their signed Declaration of COUNTER compliance also covers these aspects of the COUNTER Code of Practice.


1. Frequency of the Audit
'''''''''''''''''''''''''

To maintain COUNTER-compliant status an independent audit is required within 6 months of a content provider being listed in the Register of COUNTER Compliant Content Providers and annually thereafter. (Excepted are content providers that are members of COUNTER in the Smaller Publisher category, which may be audited biennially, with permission from COUNTER). Failure to meet these audit requirements will result in a content provider losing its COUNTER-compliant status.

If COUNTER does not receive a satisfactory auditor’s report within the specified time, the following control procedures apply:

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


2. COUNTER Usage Reports for which an Independent Audit is Required
'''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''

Independent audits are required for COUNTER reports according to host type(s). See Table 1 (below).

Table 1: COUNTER Reports Requiring Audit

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.12}|>{\raggedright\arraybackslash}\Y{0.13}|>{\raggedright\arraybackslash}\Y{0.23}|>{\raggedright\arraybackslash}\Y{0.18}|>{\raggedright\arraybackslash}\Y{0.34}|

.. list-table::
   :class: longtable
   :widths: 10 11 32 14 35
   :header-rows: 1

   * - Category
     - Report ID (for SUSHI)
     - R5 Report Name
     - Master Report / Standard View
     - Host Type

   * - Platform
     - PR
     - Platform Master Report
     - Master
     - All

   * - Platform
     - PR_P1
     - Platform Usage
     - Standard View
     - All

   * - Database
     - DR
     - Database Master Report
     - Master
     - - Aggregated Full Content\ |br|\ |lb|
       - A&I Database\ |br|\ |lb|
       - Discovery Service\ |br|\ |lb|
       - eBook Collections\ |br|\ |lb|
       - Multimedia Collection

   * - Database
     - DR_D1
     - Database Searches and Item Usage
     - Standard View
     - - Aggregated Full Content\ |br|\ |lb|
       - A&I Database\ |br|\ |lb|
       - Discovery Service\ |br|\ |lb|
       - eBook Collections\ |br|\ |lb|
       - Multimedia Collection

   * - Database
     - DR_D2
     - Database Access Denied
     - Standard View
     - - Aggregated Full Content\ |br|\ |lb|
       - A&I Database\ |br|\ |lb|
       - Discovery Service\ |br|\ |lb|
       - eBook Collections\ |br|\ |lb|
       - Multimedia Collection

   * - Title
     - TR
     - Title Master Report
     - Master
     - - Aggregated Full Content\ |br|\ |lb|
       - eBooks\ |br|\ |lb|
       - eBook Collections\ |br|\ |lb|
       - eJournals

   * - Title
     - TR_B1
     - Book Requests (excluding OA_Gold)
     - Standard View
     - - Aggregated Full Content\ |br|\ |lb|
       - eBooks\ |br|\ |lb|
       - eBook Collections

   * - Title
     - TR_B2
     - Book Access Denied
     - Standard View
     - - eBooks\ |br|\ |lb|
       - eBook Collections

   * - Title
     - TR_B3
     - Book Usage by Access Type
     - Standard View
     - - Aggregated Full Content\ |br|\ |lb|
       - eBooks\ |br|\ |lb|
       - eBook Collections

   * - Title
     - TR_J1
     - Journal Requests (excluding OA_Gold)
     - Standard View
     - - Aggregated Full Content\ |br|\ |lb|
       - eJournals

   * - Title
     - TR_J2
     - Journal Access Denied
     - Standard View
     - - eJournals

   * - Title
     - TR_J3
     - Journal Usage by Access Type
     - Standard View
     - - Aggregated Full Content\ |br|\ |lb|
       - eJournals

   * - Title
     - TR_J4
     - Journal Requests by YOP (excluding OA_Gold)
     - Standard View
     - - Aggregated Full Content\ |br|\ |lb|
       - eJournals

   * - Item
     - IR
     - Item Master Report
     - Master
     - - Data Repository\ |br|\ |lb|
       - Multimedia Collection\ |br|\ |lb|
       - Repository\ |br|\ |lb|
       - Scholarly Collaboration Network

   * - Item
     - IR_A1
     - Journal Article Requests
     - Standard View
     - - Repository

   * - Item
     - IR_M1
     - Multimedia Item Requests
     - Standard View
     - - Multimedia Collection


3. General Conditions for Carrying out an Audit Test
''''''''''''''''''''''''''''''''''''''''''''''''''''

COUNTER defines a reporting period as a calendar month. A report run for any given month MUST reflect all activity of a customer for the entire month in question.

This applies also to auditing activity. An auditor should always finalize the audit tests within one and the same calendar month. During the audit period, all activity on the audit accounts not instigated by the auditor should be prevented, as this will make the test reports unreliable and may result in further audit tests that may incur additional costs.

To prevent any collision of reported data, an auditor should be allowed to set up and maintain separate accounts for each of the audit tests. All accounts should be set up in such a way that only the auditor carrying out a test can access the content provider’s platform.

Prior to the audit, the content provider must supply to the auditor:

#. Account details for at least 4 separate accounts with access to all areas required to be tested (or specific restrictions for turn-away testing).
#. Links to download usage reports in all required formats. COUNTER usage reports must be provided as tabular versions, which can be easily imported into Microsoft Excel pivot tables.
#. SUSHI credentials for the test accounts to enable verification of SUSHI harvesting and formatting of the harvested reports.
#. A declaration that federated and automated searches have been disaggregated from any searches reported. See the COUNTER Code of Practice for further information on the protocols that apply to federated and automated searches.
#. If server-side caching is implemented, information on cache settings used should be provided. Note: Server-side caching can cause a discrepancy between the usage recorded in the audit tests and the usage reported by the content provider. Information on cache settings enables the auditor to take them into account when evaluating the results of the report tests. If the content provider does not provide this information, the auditor is likely to require further audit tests that may incur additional costs.

