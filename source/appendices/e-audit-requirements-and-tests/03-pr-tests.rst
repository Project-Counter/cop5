.. The COUNTER Code of Practice Release 5 © 2017-2021 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

E.3 Platform Report Audit Tests
-------------------------------

This section of the appendix outlines tests that MUST be run during all audits, and which are specific to the Platform Report.

The Platform Report will be COUNTER-compliant if the following audit tests are passed. The Platform Usage (PR_P1) Standard View of the Platform Report will be COUNTER-compliant if the metrics match those in the Platform Report, with the appropriate aggregation.

Audit test requirements vary depending on the set up of the platform, as indicated by the Options within the tests below.

Platform Report tests apply to all Host_Types.


E.3.1 Searches_Platform
"""""""""""""""""""""""

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

**Option 5**: Platform does not include any databases.

The auditor MUST run 100 searches on the platform.

The auditor activity MUST result in 100 Searches_Platform (1 per search).

E.3.2 Platform Investigations and Requests
""""""""""""""""""""""""""""""""""""""""""

Where possible, 50% of items requested SHOULD be via browsing the platform and 50% via searching the platform. If either browsing or searching is not possible, all items can be requested via the only available option.

**Option 1**: Platforms with mixtures of Data_Types including Data_Type=Book and/or Reference_Work.

The auditor MUST make a total of 100 requests

* 50 requests against different items with Data_Type other than Book and/or Reference_Work.
* 10 requests against different items within each of 5 Books and/or Reference_Works, for 50 total requests.

The auditor activity MUST result in 100 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 5 each of Unique_Title_Investigations and Unique_Title_Requests (1 per Book and/or Reference_Work).

If a platform only delivers Book and/or Reference_Work content as a single download, and it is not possible to identify Book_Segments and/or Reference_Items, then each request MUST be for a separate Book and/or Reference_Work. In this case the auditor activity MUST result in 100 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 50 each of Unique_Title_Investigations and Unique_Title_Requests (1 per Book and/or Reference_Work).

In the specific case of platforms offering Books and/or Reference_Works as whole-title downloads where Book_Segments and/or Reference_Items can be identified, the metric counts will deviate from those specified. The auditor MUST note the number of Book_Segments and/or Reference_Items in the titles subject to double-click tests, and the number of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests must reflect the number of Book_Segments and/or Reference_Items in addition to any other items tested.

**Option 2**: Platforms that only include Data_Type=Book and/or Reference_Work.

The auditor MUST make 10 requests against different items within each of 10 Books and/or Reference_Works, for 100 total requests.

The auditor activity MUST result in 100 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 10 each of Unique_Title_Investigations and Unique_Title_Requests (1 per Book and/or Reference_Work).

If a platform only delivers Book and/or Reference_Work content as a single download, and it is not possible to identify Book_Segments and/or Reference_Items, then each request MUST be for a separate Book and/or Reference_Work. In this case the auditor activity MUST result in 100 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 100 each of Unique_Title_Investigations and Unique_Title_Requests (1 per Book and/or Reference_Work).

In the specific case of platforms offering Books and/or Reference_Works as whole-title downloads where Book_Segments and/or Reference_Items can be identified, the metric counts will deviate from those specified. The auditor MUST note the number of Book_Segments and/or Reference_Items in the titles subject to double-click tests, and the number of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests must reflect the number of Book_Segments and/or Reference_Items in addition to any other items tested.

**Option 3**: Platforms that do not include content with Data_Type=Book and/or Reference_Work.

The auditor MUST make a total of 100 requests against different items, resulting in 100 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests. There should be no Unique_Title_Investigations or Unique_Title_Requests. Zero usage MUST NOT appear in COUNTER Reports.
