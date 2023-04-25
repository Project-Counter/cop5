.. The COUNTER Code of Practice Release 5 © 2017-2023 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

E.6 Audit Tests for Investigations and Requests for Other Data_Types
--------------------------------------------------------------------

This section of the appendix outlines tests that MUST be run during audits for any platform delivering any Data_Type that is not Book or Reference_Work content. For report providers operating multiple platforms including one or more with non-Book or Reference_Work content, the audit scope as defined in :numref:`audit` MUST include one of these platforms and be subject to the audit tests outlined here. Note that these tests refer to 'item' for ease of reading, without specifying Data_Type.

These tests apply to the Platform Report, Database Report, Title Report and Item Report. The PR_P1, DR_D1, TR_J1, TR_J3, TR_J4 and IR_A1 Standard Views of the COUNTER Reports will be deemed COUNTER-compliant if the metrics and Data_Types match those in the relevant COUNTER Report, with the appropriate aggregation.

These audit tests specify minimum numbers of items to be tested. Where a platform has fewer than the required number of items, the auditor MUST make at least one request for each item on the platform, and where necessary undertake duplicate actions to reach the required threshold.

Audit test requirements vary depending on the set up of the platform, as indicated by the Options within the tests below.


E.6.1 Access Types
""""""""""""""""""

Where possible, 50% of items requested SHOULD be via browsing the platform and 50% via searching the platform. If either browsing or searching is not possible, all items can be requested via the only available option.

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


E.6.2 Year of Publication
"""""""""""""""""""""""""

Year of publication (YOP) is useful in evaluating usage of archive content for Data_Types that can be published serially, namely:

* Article
* Conference_Item
* Conference
* Journal
* News_Item
* Newspaper_or_Newsletter

The auditor MUST confirm the YOP of items covered in other audit tests described above, with appropriate and proportionate spot checks covering a minimum of 20% of all items tested from the relevant Data_Types.

If the YOP appearing in the COUNTER Reports is different from that of the item for more than 10% of the checked items, the auditor must expand their spot checks to cover at least 40% of tested items. If 10% or more of the items have a different YOP from that in the COUNTER Reports, the report provider has failed the YOP audit test. To use the example of audit tests under Option 1 above:

* 100 items are subject to audit tests.
* 20 of these are checked to ensure the YOP matches between the item and the COUNTER Report, of which 3 are found to conflict.
* An additional 20 items are checked to ensure the YOP matches between the item and the COUNTER Report.
* If a total of 4 YOPs do not match between the item and the COUNTER Report, the audit test is failed.

