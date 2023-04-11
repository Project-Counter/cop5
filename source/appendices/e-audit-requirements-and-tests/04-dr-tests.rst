.. The COUNTER Code of Practice Release 5 © 2017-2021 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

E.4 Database Report Audit Tests
-------------------------------

This section of the appendix outlines tests that MUST be run during audits for a Host_Type that is required to offer the Database Report.

The Database Report will be COUNTER-compliant if the following audit tests are passed. The Database Search and Item Usage (DR_D1) and Database Access Denied (DR_D2) Standard Views of the Database Report will be COUNTER-compliant if the metrics match those in the Database Report, with the appropriate aggregation.

Audit test requirements vary depending on the set up of the platform and database(s), as indicated by the Options within the tests below.

Database Report tests apply to Host_Types A&I_Database, Aggregated_Full_Content, Discovery_Service, eBook_Collection, Full_Content_Database, and Multimedia_Collection.

E.4.1 Searches_Regular and Searches_Automated
"""""""""""""""""""""""""""""""""""""""""""""

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


E.4.2 Total_Item_Requests and Unique_Item_Requests
""""""""""""""""""""""""""""""""""""""""""""""""""

Where possible, 50% of items requested SHOULD be via browsing the platform and 50% via searching the platform. If either browsing or searching is not possible, all items can be requested via the only available option.

The auditor MUST make a total of 80 requests against different items, resulting in 80 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests.

Where a platform has fewer than 80 items, the auditor MUST make at least one request per item and testing should result in 80 each of Total_Item_Investigations and Total_Item_Requests, and the item-count of Unique_Item_Investigations and Unique_Item_Requests.


E.4.3 Total_Item_Investigations and Unique_Item_Investigations
""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""

This test is required when investigations can be reported independently of a request. If all investigations have a matching request, please apply to the COUNTER Project Director for an audit exception prior to the audit commencing.

Where possible, 50% of items investigated SHOULD be via browsing the platform and 50% via searching the platform. If either browsing or searching is not possible, all items may be investigated via the only available option.

The auditor MUST make a total of 80 investigations against different items, resulting in 80 each of Total_Item_Investigations and Unique_Item_Investigations.

Where a platform has fewer than 80 items, the auditor MUST make at least one investigation per item and testing should result in 80 Total_Item_Investigations and the item-count of Unique_Item_Investigations.