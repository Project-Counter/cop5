.. The COUNTER Code of Practice Release 5 © 2017-2021 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

E.8 Audit Tests for Double-Click Filtering
------------------------------------------

This audit test applies to investigations and requests metrics across all COUNTER Reports and should represent the scope of the platform. That is, where a platform is made up of a mixture of content with Data_Types Article, Multimedia and Patent, the auditor should represent each of those Data_Types proportionately in the audit test.

The test consists of making requests to an item twice in succession (double-clicks). If the two clicks occur within a 30-second time-span, only the second request MUST be recorded, resulting in 1 Total_Item_Investigation and 1 Total_Item_Request. If the two clicks occur with more than 30 seconds between them, then 2 Total_Item_Investigations and 2 Total_Item_Requests must be counted. In both cases only 1 Unique_Item_Investigation and 1 Unique_Item_Request will be reported.

The auditor MUST carry out a total of 30 tests:

* 15 “Inside” tests, whereby 2 identical requests are made and the second request is within 30 seconds of the first.
* 15 “Outside” tests, whereby 2 identical requests are made and the second request is more than 30 seconds after the first.

The “Inside” tests MUST result in 15 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and the “Outside” tests MUST result in 30 Total_Item_Investigations, 30 Total_Item_Requests, 15 Unique_Item_Investigations and 15 Unique_Item_Requests, for a total of 45 Total_Item_Investigations, 45 Total_Item_Requests, 30 Unique_Item_Investigations and 30 Unique_Item_Requests.
