.. The COUNTER Code of Practice Release 5 © 2017-2021 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

.. _compliance-consortia:

COUNTER Reporting for Consortia
-------------------------------

Consortia license content for their members and consortium administrators need access to COUNTER statistics that show how each member has used the licensed resources.


Access to SUSHI Credentials for Member Sites
""""""""""""""""""""""""""""""""""""""""""""

Content providers MUST support the /members COUNTER_SUSHI API path to provide the consortium with the list of their members on the platform and the SUSHI credentials for each member. This will enable tools to be created to efficiently retrieve member usage and create separate or consolidated reporting.


Privacy and Confidentiality
"""""""""""""""""""""""""""

COUNTER acknowledges that some organizations treat their usage data as sensitive and private information. Content providers may include the option for consortium members to opt-out of consortium reporting. COUNTER recommends the default setting for an organization is to opt-in to consortium reporting.


Content to Report Usage On
""""""""""""""""""""""""""

When a COUNTER report is harvested by a consortium administrator, a content provider may choose to limit member usage to include only content acquired through the consortium. Note that when such a limitation is in place the resulting report may differ from the member-sites own version of the report. Since not all content providers can provide such limits, the consortium will be responsible for ensuring usage is filtered to the content they license for members.

When the content provider chooses to limit member usage to only content acquired through the consortium, they MUST include a message to this effect in the Notes element in their implementation of the /members path in the COUNTER_SUSHI API (see :numref:`sushi` above).


Detailed versus Summary Reports
"""""""""""""""""""""""""""""""

A content provider MUST offer the option to provide consortium-level summary of usage for the consortium. For a consortium summary report (usage for all members of the consortium rolled up at the consortia level), COUNTER acknowledges that the totals on the summary report may differ from the sum of the totals on individual member reports for the same items if an authentication method used identifies to multiple member sites and usage it attributed to each such site (e.g. overlapping IP ranges).

Note that it is possible to create Master Reports for a consortium with usage broken down by member sites with extensions (see :numref:`reserved-elements`), but this isn’t required for compliance.


SUSHI Service Limits
""""""""""""""""""""

The content provider MUST NOT place limits on the SUSHI service (such as requests per day or amount of data transferred) that would prevent a consortium from retrieving reports for all its members.
