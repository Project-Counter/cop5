.. The COUNTER Code of Practice Release 5 © 2017-2021 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

E.6 Title Report Audit Tests for Journals
-----------------------------------------

This section of the appendix outlines tests that MUST be run during audits for a Host_Type that is required to offer the Title Report and which includes Journal content requiring delivery of the journal-related Standard Views of the Title Report (TR_J1, TR_J2, TR_J3, TR_J4). Title Report audit tests for journals apply to Host_Types Aggregated_Full_Content and eJournal.

The Title Report will be COUNTER-compliant for journal content if the following audit tests are passed. The journal-related Standard Views of the Title Report (TR_J1, TR_J2, TR_J3, TR_J4) will be COUNTER-compliant if the metrics match those in the Title Report, with the appropriate aggregation.

Audit test requirements vary depending on the set up of the platform, as indicated by the Options within the tests below.

For ease of reading the term ‘journal articles’ has been used to indicate content items within Data_Type=Journal.


E.6.1 Journal Access Types
""""""""""""""""""""""""""

Within the Title Report, breakdowns by Access_Type are essential. There are therefore a series of audit tests designed to determine report providers’ compliance with requirements for reporting Access_Type.

**Option 1**: Report provider offers journal articles under just one Access_Type.

The auditor MUST request 100 journal articles.

This MUST result in 100 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests with the appropriate Access_Type.

**Option 2**: Report provider offers journal articles under two Access_Types.

The auditor MUST request 50 journal articles with each Access_Type.

This MUST result in 50 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests with each Access_Type.

The Access_Type combinations might be: Controlled plus Open, Controlled plus Free_To_Read, or Open plus Free_To_Read.

**Option 3**: Report provider offers Controlled, Open and Free_To_Read journal articles.

The auditor MUST request

* 40 journal articles with Access_Type Controlled.
* 40 journal articles with Access_Type Open.
* 20 journal articles with Access_Type Free_To_Read.

This MUST result in 40 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests with Access_Type Controlled; the same again for Access_Type Open; and 20 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests with Access_Type Free_To_Read.


E.6.2 Total_Item_Requests and Unique_Item_Requests
""""""""""""""""""""""""""""""""""""""""""""""""""

Where possible, 50% of items requested SHOULD be via browsing the platform and 50% via searching the platform. If either browsing or searching is not possible, all items can be requested via the only available option.

The auditor MUST make a total of 80 requests against 40 different journal articles, resulting in 80 each of Total_Item_Investigations and Total_Item_Requests, and 40 each of Unique_Item_Investigations and Unique_Item_Requests.


E.6.3 Total_Item_Investigations and Unique_Item_Investigations
""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""

This test is required when investigations can be reported independently of a request. If all investigations have a matching request, please apply to the COUNTER Project Director for an audit exception prior to the audit commencing.

Where possible, 50% of items investigated SHOULD be via browsing the platform and 50% via searching the platform. If either browsing or searching is not possible, all items may be investigated via the only available option.

The auditor MUST make a total of 80 investigations against 40 different journal articles, resulting in 80 Total_Item_Investigations and 40 Unique_Item_Investigations.


E.6.4 Journal Year of Publication
"""""""""""""""""""""""""""""""""

For journal content, year of publication (YOP) is useful in evaluating usage of archive content.

The auditor MUST confirm the Year of Publication (YOP) of articles covered in other audit tests described in this appendix (headings E.2.5.1, E.2.5.2 and E.2.5.3) with appropriate and proportionate spot checks covering a minimum of 10% of all journal articles tested.

If the YOP appearing in the reports is different from that of the journal article for more than 10% of the checked items, the auditor must expand their spot checks to cover at least 25% of tested journal articles. If 10% or more of the journal articles have a different YOP from that in the reports, the report provider has failed the Journal YOP audit test.
