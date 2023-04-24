.. The COUNTER Code of Practice Release 5 © 2017-2021 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

E.8 Item Report Audit Tests
---------------------------

This section of the appendix outlines tests that MUST be run during audits for a Host_Type that is required to offer the Item Report. Item Report audit tests apply to Host_Types Data_Repository, Multimedia, Repository, and Scholarly_Collaboration_Network. Auditors SHOULD also run Item Report audit tests on other Host_Types that have opted to provide Item Reports.

The Item Report will be COUNTER-compliant if the following audit tests are passed. The Standard Views of the Item Report (IR_A1 and IR_M1) will be COUNTER-compliant if the metrics match those in the Item Report.

In order for the Item Report to be accurately audited, the report provider MUST supply the auditor with a list of Data_Types represented on the platform.

Note that because Components are optional for Release 5.1, they SHOULD be omitted from Item Report audit tests.


E.8.1 Total_Item_Requests and Unique_Item_Requests
""""""""""""""""""""""""""""""""""""""""""""""""""

The auditor MUST make a total of 100 requests on 50 unique items representing the scope of the platform. That is, where a platform is made up of a mixture of content with Data_Types Audio, Patent and Report, the auditor should represent each of those Data_Types proportionately in the audit test.

This MUST result in 100 Total_Item_Requests and 50 Unique_Item_Requests. The auditor MUST record the Data_Types for each item (e.g. Audio) and the resulting Item Report MUST reflect those records.


E.8.2 Total_Item_Investigations and Unique_Item_Investigations
""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""

This test is required when investigations can be reported independently of a request. If all investigations have a matching request, please apply to the COUNTER Project Director for an audit exception prior to the audit commencing.

The auditor MUST make a total of 100 investigations on 50 unique items representing the scope of the platform. That is, where a platform is made up of a mixture of content with Data_Types Audio, Patent and Report, the auditor should represent each of those Data_Types proportionately in the audit test.

This MUST result in 100 Total_Item_Investigations and 50 Unique_Item_Investigations. The auditor MUST record the Data_Types for each item (e.g. Audio) and the resulting Item Report MUST reflect those records.


E.8 Access Types
""""""""""""""""

**Option 1**: Report provider offers items under just one Access_Type.

The auditor MUST request 100 items.

This MUST result in 100 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests with the appropriate Access_Type.

**Option 2**: Report provider offers items under two Access_Types.

The auditor MUST request 50 items with each Access_Type.

This MUST result in 50 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests with each Access_Type.

The Access_Type combinations might be: Controlled plus Open, Controlled plus Free_To_Read, or Open plus Free_To_Read.

**Option 3**: Report provider offers Controlled, Open and Free_To_Read items.

The auditor MUST request

* 40 items with Access_Type Controlled.
* 40 items with Access_Type Open.
* 20 items with Access_Type Free_To_Read.

This MUST result in 40 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests with Access_Type Controlled; the same again for Access_Type Open; and 20 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests with Access_Type Free_To_Read.