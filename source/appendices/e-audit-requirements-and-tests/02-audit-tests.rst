.. The COUNTER Code of Practice Release 5 © 2017-2021 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

E.2 Audit Tests
---------------


E.2.1 Validation Tool
"""""""""""""""""""""

Once reports are available for testing (i.e. up to 28 days after the end of the seeding month), auditors MUST run the COUNTER Reports and Standard Views of COUNTER Reports that are within the scope of the audit through the Validation Tool.

Where report providers have elected to follow the pre-flight preparation step outlined in Section 9 of the Code of Practice, this audit test should not result in any errors.


E.2.2 Platform Report Audit Tests
"""""""""""""""""""""""""""""""""

The Platform Report will be COUNTER-compliant if the following audit tests are passed. The Platform Usage (PR_P1) Standard View of the Platform Report will be COUNTER-compliant if the metrics match those in the Platform Report, with the appropriate aggregation.


E.2.2.1 Searches_Platform
'''''''''''''''''''''''''

**Option 1**: Platform has multiple databases and the user can search the whole platform, multiple selected databases, or a single database.

The auditor MUST run 100 searches on the platform
* 50 searches against only 1 selected database.
* 25 searches against 2 selected databases.
* 25 searches against all databases on the platform.

The auditor activity MUST result in 100 Searches_Platform (1 per search).

**Option 2**: Platform has multiple databases and the user can search the whole platform or a single database.

The auditor MUST run 100 searches on the platform
* 50 searches against only 1 selected database.
* 50 searches against all databases on the platform.

The auditor activity MUST result in 100 Searches_Platform (1 per search).

**Option 3**: Platform has multiple databases but the user can only search the whole platform OR the platform has just one database.

The auditor MUST run 100 searches on the platform. 

The auditor activity MUST result in 100 Searches_Platform (1 per search).

**Option 4**: Platform has multiple databases but the user can only search a single database at a time.

The auditor MUST run 100 searches across at least 10% of the available databases, restricted to one database at a time. 

The auditor activity MUST result in 100 Searches_Platform (1 per search).


E.2.2.2 Platform Investigations and Requests
''''''''''''''''''''''''''''''''''''''''''''

Where possible, 50% of items requested SHOULD be via browsing the platform and 50% via searching the platform. If either browsing or searching is not possible, all items can be requested via the only available option.

**Option 1**: Platforms with mixtures of Data_Types including Data_Type=Book.

The auditor MUST make a total of 100 requests
* 50 requests against different items with Data_Type other than Book.
* 10 requests against different items within each of 5 books, for 50 total requests.

If a platform only delivers book content as a whole-book download (i.e. without Book_Segments), then each request SHOULD be for a separate book.

The auditor activity MUST result in 100 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 5 Unique_Title_Requests (1 per book).

**Option 2**: Platforms that only include Data_Type=Book.

The auditor MUST make a total of 100 requests
* 10 requests against different items within each of 10 books, for 100 total requests.

If a platform only delivers book content as a whole-book download (i.e. without Book_Segments), then each request SHOULD be for a separate book. 

The auditor activity MUST result in 100 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 10 Unique_Title_Requests (1 per book).

**Option 3**: Platforms that do not include content with Data_Type=Book.

The auditor MUST make a total of 100 requests against different items, resulting in 100 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests. There should be 0 Unique_Title_Investigations and 0 Unique_Title_Requests.


E.2.3 Database Report Audit Tests
"""""""""""""""""""""""""""""""""

The Database Report will be COUNTER-compliant if the following audit tests are passed. The Database Search and Item Usage (DR_D1) and Database Access Denied (DR_D2) Standard Views of the Database Report will be COUNTER-compliant if the metrics match those in the Database Report, with the appropriate aggregation.


E.2.3.1 Searches_Regular and Searches_Automated
'''''''''''''''''''''''''''''''''''''''''''''''

**Option 1**: Platform has multiple databases and the user can search the whole platform, multiple selected databases, or a single database.

The auditor MUST run 100 searches on the platform
* 50 searches against only 1 selected database, resulting in 50 Searches_Regular against that database.
* 25 searches against 2 selected databases, resulting in 25 Searches_Regular against both databases.
* 25 searches against all databases on the platform, resulting in 25 Searches_Regular against every database.

**Option 2**: Platform has multiple databases and the user can search the whole platform or a single database.

The auditor MUST run 100 searches on the platform
* 50 searches against only 1 selected database, resulting in 50 Searches_Regular against that database.
* 50 searches against all databases on the platform, resulting in 50 Searches_Regular against every database.

**Option 3**: Platform has multiple databases but the user can only search the whole platform.

The auditor MUST run 100 searches, resulting in 100 Searches_Automated (1 per search).

**Option 4**: Platform has multiple databases but the user can only search a single database at a time.

The auditor MUST run 100 searches across at least 10% of the available databases, restricted to one database at a time, resulting in 100 Searches_Regular (1 per search).

**Option 5**: Platform has only one database.

The auditor MUST run 50 searches, resulting in 50 Searches_Regular (1 per search).


E.2.3.2 Total_Item_Requests
'''''''''''''''''''''''''''

Where possible, 50% of items requested SHOULD be via browsing the platform and 50% via searching the platform. If either browsing or searching is not possible, all items can be requested via the only available option.

The auditor MUST make a total of 80 requests against different items, resulting in 80 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests.

Where a platform has fewer than 80 items, the auditor MUST make at least one request per item and testing should result in 80 each of Total_Item_Investigations and Total_Item_Requests, and the item-count of Unique_Item_Investigations and Unique_Item_Requests.


E.2.3.3 Total_Item_Investigations
'''''''''''''''''''''''''''''''''

This test is required when investigations can be reported independently of a request. If all investigations have a matching request, please apply to the COUNTER Project Director for an audit exception prior to the audit commencing.

Where possible, 50% of items investigated SHOULD be via browsing the platform and 50% via searching the platform. If either browsing or searching is not possible, all items may be investigated via the only available option.

The auditor MUST make a total of 80 investigations against different items, resulting in 80 each of Total_Item_Investigations and Unique_Item_Investigations.

Where a platform has fewer than 80 items, the auditor MUST make at least one investigation per item and testing should result in 80 Total_Item_Investigations and the item-count of Unique_Item_Investigations.


E.2.4 Title Report Audit Tests: Books
"""""""""""""""""""""""""""""""""""""

The Title Report will be COUNTER-compliant if the following audit tests are passed. The book-related Standard Views of the Title Report (TR_B1, TR_B2, TR_B3) will be COUNTER-compliant if the metrics match those in the Title Report, with the appropriate aggregation.

Audit test requirements vary depending on the set up of the platform and any related database(s), as indicated by the Options within the tests below.


E.2.4.1 Book Unique_Title_Requests
''''''''''''''''''''''''''''''''''

**Option 1**: Book_Segments are available, users can elect to access books segment-by-segment.

The auditor MUST request 100 Book_Segment items, 10 each from 10 different Books. This MUST result in 100 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 10 each of Unique_Title_Investigations and Unique_Title_Requests.

**Option 2**: Only whole Books are available, with no Book_Segments.

The auditor MUST request 20 Book items, twice each. This MUST result in 40 each of Total_Item_Investigations and Total_Item_Requests, and 20 each of Unique_Item_Investigations, Unique_Item_Requests, Unique_Title_Investigations and Unique_Title_Requests.


E.2.4.2 Book Access Types: Book_Segments
''''''''''''''''''''''''''''''''''''''''

Within the Title Report, breakdowns by Access_Type are essential. There are therefore a series of audit tests designed to determine report providers’ compliance with requirements for reporting Access_Type. These tests only apply where Books with more than one Access_Type are available on a platform, and they are available as Book_Segments.

**Option 1**: Report provider offers Controlled and Open Book_Segments.

The auditor MUST request 
* 50 Book_Segment items, 10 each from 5 different Books with Access_Type Controlled.
* 50 Book_Segment items, 10 each from 5 different Books with Access_Type Open.

This MUST result in 50 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 5 each of Unique_Title_Investigations and Unique_Title_Requests with Access_Type Controlled, and the same again for Access_Type Open.

**Option 2**: Report provider offers Controlled, Open and Free_To_Read Book_Segments.

The auditor MUST request
* 40 Book_Segment items, 10 each from 4 different Books with Access_Type Controlled.
* 40 Book_Segment items, 10 each from 4 different Books with Access_Type Open.
* 20 Book_Segment items, 10 each from 2 different Books with Access_Type Free_To_Read.

This MUST result in 40 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 4 each of Unique_Title_Investigations and Unique_Title_Requests with Access_Type Controlled; the same again for Access_Type Open; and 20 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 2 each of Unique_Title_Investigations and Unique_Title_Requests with Access_Type Free_To_Read.

**Option 3**: Report provider offers Controlled and Free_To_Read Book_Segments.

The auditor MUST request
* 50 Book_Segment items, 10 each from 5 different Books with Access_Type Controlled.
* 50 Book_Segment items, 10 each from 5 different Books with Access_Type Free_To_Read.

This MUST result in 50 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 5 each of Unique_Title_Investigations and Unique_Title_Requests with Access_Type Controlled, and the same again for Access_Type Free_To_Read.

**Option 4**: Report provider offers Open and Free_To_Read Book_Segments.

The auditor MUST request
* 50 Book_Segment items, 10 each from 5 different Books with Access_Type Open.
* 50 Book_Segment items, 10 each from 5 different Books with Access_Type Free_To_Read.

This MUST result in 50 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 5 each of Unique_Title_Investigations and Unique_Title_Requests with Access_Type Open, and the same again for Access_Type Free_To_Read.


E.2.4.3 Book Access Types: Whole Books
''''''''''''''''''''''''''''''''''''''

Within the Title Report, breakdowns by Access_Type are essential. There are therefore a series of audit tests designed to determine report providers’ compliance with requirements for reporting Access_Type. These tests only apply where Books with more than one Access_Type are available on a platform, and they are only available without Book_Segments.

**Option 1**: Report provider offers Controlled and Open Books, without Book_Segments.

The auditor MUST request
* 25 Books with Access_Type Controlled.
* 25 Books with Access_Type Open.

This MUST result in 25 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations, Unique_Item_Requests, Unique_Title_Investigations and Unique_Title_Requests with Access_Type Controlled, and the same again for Access_Type Open.

Where there are fewer than the required number of books that are Controlled or Open, the auditor MUST test every book with that Access_Type.

**Option 2**: Report provider offers Controlled, Open and Free_To_Read Books, without Book_Segments.

The auditor MUST request
* 20 Books with Access_Type Controlled.
* 20 Books with Access_Type Open.
* 10 Books with Access_Type Free_To_Read.

This MUST result in 20 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations, Unique_Item_Requests, Unique_Title_Investigations and Unique_Title_Requests with Access_Type Controlled; the same again for Access_Type Open; and 10 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations, Unique_Item_Requests, Unique_Title_Investigations and Unique_Title_Requests with Access_Type Free_To_Read.

Where there are fewer than the required number of books that are Controlled, Open or Free_To_Read, the auditor MUST test every book with that Access_Type.

**Option 3**: Report provider offers Controlled and Free_To_Read Books, without Book_Segments.

The auditor MUST request 
* 25 Books with Access_Type Controlled.
* 25 Books with Access_Type Free_To_Read.

This MUST result in 25 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations, Unique_Item_Requests, Unique_Title_Investigations and Unique_Title_Requests with Access_Type Controlled, and the same again for Access_Type Free_To_Read.

Where there are fewer than the required number of books that are Controlled or Free_To_Read, the auditor MUST test every book with that Access_Type.

**Option 4**: Report provider offers Open and Free_To_Read Books, without Book_Segments.

The auditor MUST request
* 25 Books with Access_Type Open.
* 25 Books with Access_Type Free_To_Read.

This MUST result in 25 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations, Unique_Item_Requests, Unique_Title_Investigations and Unique_Title_Requests with Access_Type Open, and the same again for Access_Type Free_To_Read.

Where there are fewer than the required number of books that are Open or Free_To_Read, the auditor MUST test every book with that Access_Type.


E.2.5 Title Report Audit Tests: Journals
""""""""""""""""""""""""""""""""""""""""

The Title Report will be COUNTER-compliant if the following audit tests are passed. The journal-related Standard Views of the Title Report (TR_J1, TR_J2, TR_J3, TR_J4) will be COUNTER-compliant if the metrics match those in the Title Report, with the appropriate aggregation.

Audit test requirements vary depending on the set up of the platform and any related database(s), as indicated by the Options within the tests below.

For ease of reading the term ‘journal articles’ has been used to indicate content items within Data_Type=Journal.


E.2.5.1 Journal Access Types
''''''''''''''''''''''''''''

Within the Title Report, breakdowns by Access_Type are essential. There are therefore a series of audit tests designed to determine report providers’ compliance with requirements for reporting Access_Type. These tests only apply where Journals with more than one Access_Type are available on a platform.

**Option 1**: Report provider offers Controlled and Open journal items.

The auditor MUST request
* 50 journal articles with Access_Type Controlled.
* 50 journal articles with Access_Type Open.

This MUST result in 50 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests with Access_Type Controlled, and the same again for Access_Type Open.

**Option 2**: Report provider offers Controlled, Open and Free_To_Read journal items.

The auditor MUST request
* 40 journal articles with Access_Type Controlled.
* 40 journal articles with Access_Type Open.
* 20 journal articles with Access_Type Free_To_Read.

This MUST result in 40 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests with Access_Type Controlled; the same again for Access_Type Open; and 20 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests with Access_Type Free_To_Read.

*Option 3**: Report provider offers Controlled and Free_To_Read journal items.

The auditor MUST request
* 50 journal articles with Access_Type Controlled.
* 50 journal articles with Access_Type Free_To_Read.

This MUST result in 50 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests with Access_Type Controlled, and the same again for Access_Type Free_To_Read.

**Option 4**: Report provider offers Open and Free_To_Read journal items.

The auditor MUST request
* 50 journal articles with Access_Type Open.
* 50 journal articles with Access_Type Free_To_Read.

This MUST result in 50 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests with Access_Type Open, and the same again for Access_Type Free_To_Read.


E.2.5.2 Journal Year of Publication
'''''''''''''''''''''''''''''''''''

For journal content, year of publication (YOP) is useful in evaluating usage of archive content.

The auditor MUST confirm the Year of Publication (YOP) of articles covered in other Title Report audit tests with appropriate and proportionate spot checks covering a minimum of 10% of all Title Report Audit Tests: Journals.

If the YOP appearing in the reports is different from that of the journal article for more than 10% of the checked items, the auditor must expand their spot checks to cover at least 25% of tested journal articles. If 10% or more of the journal articles have a different YOP from that in the reports, the report provider has failed the Journal YOP audit test.


E.2.6 Item Report Audit Tests
"""""""""""""""""""""""""""""

The Item Report will be COUNTER-compliant if the following audit tests are passed. The Standard Views of the Item Report (IR_A1 and IR_M1) will be COUNTER-compliant if the metrics match those in the Item Report.

In order for the Item Report to be accurately audited, the report provider MUST supply the auditor with a list of Data_Types represented on the platform.


E.2.6.1 Total_Item_Requests and Unique_Item_Requests
''''''''''''''''''''''''''''''''''''''''''''''''''''

The auditor MUST make a total of 100 requests on 50 unique items representing the scope of the platform. That is, where a platform is made up of a mixture of content with Data_Types Article, Multimedia and Patent, the auditor should represent each of those Data_Types proportionately in the audit test.

This MUST result in 100 Total_Item_Requests and 50 Unique_Item_Requests. The auditor MUST record the Data_Types for each item (e.g. Multimedia) and the resulting Item Report MUST reflect those records.


E.2.7 Audit Tests for Double-Click Filtering
""""""""""""""""""""""""""""""""""""""""""""

This audit test applies to investigations and requests metrics across all COUNTER Reports and should represent the scope of the platform. That is, where a platform is made up of a mixture of content with Data_Types Article, Multimedia and Patent, the auditor should represent each of those Data_Types proportionately in the audit test.

The test consists of making requests to an item twice in succession (double-clicks). If the two clicks occur within a 30-second time-span, only the second request MUST be recorded, resulting in 1 Total_Item_Investigation and 1 Total_Item_Request. If the two clicks occur with more than 30 seconds between them, then 2 Total_Item_Investigations and Total_Item_Requests must be counted. In both cases only 1 Unique_Item_Investigation and 1 Unique_Item_Request will be reported.

The auditor MUST carry out a total of 30 tests:
* 15 “Inside” tests, whereby 2 identical requests are made and the second request is within 30 seconds of the first.
* 15 “Outside” tests, whereby 2 identical requests are made and the second request is more than 30 seconds after the first.

The “Inside” tests MUST result in 15 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and the “Outside” tests MUST result in 30 Total_Item_Investigations, 30 Total_Item_Requests, 15 Unique_Item_Investigations and 15 Unique_Item_Requests, for a total of 45 Total_Item_Investigations, 45 Total_Item_Requests, 30 Unique_Item_Investigations and 30 Unique_Item_Requests.


E.2.8 Audit Tests for Denials
"""""""""""""""""""""""""""""

Report providers operating platforms where turnaways or denials are in operation MUST be subject to audit tests for denials. For report providers operating multiple platforms, the audit scope as defined in :numref:`audit` MUST include platforms where turnaways or denials are in operation. Where either Limit_Exceeded or No_License denials do not apply to a report provider, auditors MUST note this in the audit report. This does not require an exemption from the COUNTER Project Director.

These audit tests apply to denial metrics across all COUNTER Reports and should represent the scope of the platform under audit. That is, where a platform is made up of a mixture of content with Data_Types Article, Multimedia and Patent, the auditor SHOULD represent each of those Data_Types proportionately in the audit test.


E.2.8.1 Limit_Exceeded
''''''''''''''''''''''

Note that the account used for this testing MUST have concurrent / simultaneous-user limit (concurrency limits) set at a single user. A second user attempting to access the database would be denied.

**Option 1**: The report provider denies the user access when the concurrency limit is exceeded upon login.

The auditor MUST force 50 Limit_Exceeded access denials by logging into the site causing the user limit to reach the maximum allowance. The auditor will then attempt to log into the site using a different computer, or a different browser, which should be refused access. Each time access is refused, the auditor will record this as 1 Limit_Exceeded.

The test MUST result in 50 Limit_Exceeded.

**Option 2**: The report provider denies the user access when the concurrency limit is exceeded upon searching or accessing a database.

The auditor MUST force 50 Limit_Exceeded turnaways by logging into the site, then either selecting and searching a database or browsing to a database causing the user limit to reach the maximum allowance. The auditor will then log into the same site using a different computer, or a different browser, and repeat the action, which should be refused access. Each time access is refused, the auditor will record this as 1 Limit_Exceeded.

The test MUST result in 50 Limit_Exceeded.

**Option 3**: The report provider denies the user access when the concurrency limit is exceeded upon accessing an item within a database.

The auditor MUST force 50 Limit_Exceeded turnaways by logging into the site and requesting an item, causing the user limit to reach the maximum allowance.The auditor will then log into the site again using a different computer, or a different browser, and repeat the action, which should be refused access. Each time access is refused, the auditor will record this as 1 Limit_Exceeded.

The test MUST result in 50 Limit_Exceeded.


E.2.8.2 No_Licence
''''''''''''''''''

The content for which the auditor has no license MUST be declared by the report provider prior to audit testing.

The auditor MUST force 50 No_License turnaways by logging into the site and requesting an item. Each time access is refused, the auditor will record this as 1 No_License.

The test MUST result in 50 No_License.