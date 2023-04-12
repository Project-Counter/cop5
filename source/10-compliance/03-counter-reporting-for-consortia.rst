.. The COUNTER Code of Practice Release 5 © 2017-2023 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

.. _compliance-consortia:

COUNTER Reporting for Consortia
-------------------------------

Consortia license content for their members, and consortia managers and administrators need access to COUNTER statistics that show how each member within a given consortium has used the licensed resources.


Types of Consortia-Level Report
"""""""""""""""""""""""""""""""

There are three types of consortia-level reporting:

* Report providers MUST offer summary reports that show total usage for all members of the consortium rolled up to the consortia level, and which cannot be broken down by institution. Summary reports MUST be offered for all relevant COUNTER Reports and Standard Views of the COUNTER Reports. The totals on the summary report may differ from the sum of the totals on individual member reports for the same items if an authentication method used identifies to multiple member sites and usage it attributed to each such site (e.g. overlapping IP ranges).
* Report providers may elect to offer detailed reports that show total usage for all members of the consortium, and which can be broken down by institution. As with the summary report, the totals on the detailed report may differ from the sum of the totals on individual member reports for the same items.
* Institutional reports are the individual institutional-level reports. Consortia managers and administrators MUST be able to retrieve institutional reports.


Creating Detailed Consortia-Level Reports
"""""""""""""""""""""""""""""""""""""""""

COUNTER recognizes that consolidated reports can be helpful to consortia, and that some report providers may want to meet the needs of their consortium customers by providing detailed reports. This can be done using existing extensions to the Code of Practice (see :numref:`reserved-elements`):

* The Customer_ID used in a detailed report MUST match that used in a report to the individual institution, and the ID for the institution returned by the /members COUNTER_SUSHI API path.
* If provided, the Institution_Name used in a detailed report MUST match that used in a report to the individual institution, and the name for the institution returned by the /members COUNTER_SUSHI API path.
* If provided, Institution_Name MUST be the first column in the tabular report, with Customer_ID the second column. Otherwise Customer_ID should be the first column. 

As they are optional, detailed reports are not subject to COUNTER audits.


Accessing Consortia-Level Reports
"""""""""""""""""""""""""""""""""

Consortia managers and administrators MUST be able to access usage reports through the same user interface or SUSHI service as any other report consumer. 

To facilitate gathering institutional reports, report providers MUST support the /members COUNTER_SUSHI API path to provide the consortium with the list of their members on the platform and the SUSHI credentials for each member. This will enable tools to be created to efficiently retrieve member usage and create separate or consolidated reporting, such as those described on the `COUNTER website <https://www.projectcounter.org/counter-harvester-tools/>`_.

The report provider MUST NOT place limits on the SUSHI service (such as requests per day or amount of data transferred) that would prevent a consortium from retrieving reports for all its members.


Privacy and Confidentiality
"""""""""""""""""""""""""""

COUNTER acknowledges that some organizations treat their usage data as sensitive and private information. Report providers may include the option for consortium members to opt-out of consortium reporting. COUNTER recommends the default setting for an organization is to opt-in to consortium reporting.


Content to Report Usage On
""""""""""""""""""""""""""

When a COUNTER report is harvested by a consortium administrator, a report provider may choose to limit member usage to include only content acquired through the consortium. Note that when such a limitation is in place the resulting report may differ from the member-sites own version of the report. Since not all report providers can provide such limits, the consortium will be responsible for ensuring usage is filtered to the content they license for members.

When the report provider chooses to limit member usage to only content acquired through the consortium, they MUST include a message to this effect in the Notes element in their implementation of the /members path in the COUNTER_SUSHI API (see :numref:`sushi` above).
