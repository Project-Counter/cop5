.. The COUNTER Code of Practice Release 5 © 2017-2021 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

E.5 Title Report Audit Tests for Books and Reference_Works
----------------------------------------------------------

This section of the appendix outlines tests that MUST be run during audits for a Host_Type that is required to offer the Title Report and which includes Book and/or Reference_Work content requiring delivery of the book-related Standard Views of the Title Report (TR_B1, TR_B2, TR_B3).

The Title Report will be COUNTER-compliant for book and/or reference work content if the following audit tests are passed. The book-related Standard Views of the Title Report (TR_B1, TR_B2, TR_B3) will be COUNTER-compliant if the metrics match those in the Title Report, with the appropriate aggregation.

Audit test requirements vary depending on the set up of the platform, as indicated by the Options within the tests below.

Title Report audit tests for books and reference works apply to Host_Types Aggregated_Full_Content, eBook, and eBook_Collection.

Note that Data_Types Book and Reference_Work are included in the audit tests, as Reference_Works are included in the book-related Standard Views of the Title Report.


E.5.1 Unique_Title_Investigations and Unique_Title_Requests
"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""

**Option 1**: Book_Segments and/or Reference_Items are available, users can only access Books and/or Reference_Works segment-by-segment.

* The auditor MUST request 80 Book_Segments and/or Reference_Items, 10 each from 8 different Books and/or Reference_Works.
* The auditor MUST request 10 Book_Segments and/or Reference_Items, all from the same Book and/or Reference_Work. 

This MUST result in 90 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 9 each of Unique_Title_Investigations and Unique_Title_Requests.

**Option 2**: Only whole Books and/or Reference_Works are available, with no identifiable Book_Segments and/or Reference_Works.

The auditor MUST request 20 Books and/or Reference_Works, twice each. This MUST result in 40 each of Total_Item_Investigations and Total_Item_Requests, and 20 each of Unique_Item_Investigations, Unique_Item_Requests, Unique_Title_Investigations and Unique_Title_Requests.

**Option 3**: Books and/or Reference_Works are available as whole titles, within which Book_Segments and/or Reference_Items can be identified. Alternatively, Books and/or Reference_Works are available as both whole titles and as Book_Segments and/or Reference_Items.

* The auditor MUST request 80 Book_Segments and/or Reference_Items, 10 each from 8 different Books and/or Reference_Works.
* The auditor MUST request 10 Books and/or Reference_Works, twice each, recording the number of Book_Segments and/or Reference_Items pertaining to each title.

This MUST result in 80 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests from the first set of requests, plus a count of Total_Item_Investigations and Total_Item_Requests that is equal to the sum of the Book_Segments and/or Reference_Items from the second set of requests and half that number of Unique_Item_Investigations and Unique_Item_Requests. It MUST also result in 18 each of Unique_Title_Investigations and Unique_Title_Requests.


E.5.2 Book Access Types
"""""""""""""""""""""""

Within the Title Report, breakdowns by Access_Type are essential. There are therefore a series of audit tests designed to determine report providers’ compliance with requirements for reporting Access_Type.


E.5.2.1 Available as Book_Segments and/or Reference_Items
'''''''''''''''''''''''''''''''''''''''''''''''''''''''''

These tests apply where users can only access Books and/or Reference_Works segment-by-segment.

**Option 1**: Report provider offers Book_Segments and/or Reference_Items under only one Access_Type.

The auditor MUST request 70 Book_Segments and/or Reference_Items, 10 each from 7 different Books and/or Reference_Works.

This MUST result in 70 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 7 each of Unique_Title_Investigations and Unique_Title_Requests with the appropriate Access_Type.

**Option 2**: Report provider offers Book_Segments and/or Reference_Items under all three Access_Types (Controlled, Open and Free_To_Read).

The auditor MUST request

* 40 Book_Segments and/or Reference_Items, 10 each from 4 different Books and/or Reference_Works with Access_Type Controlled.
* 40 Book_Segments and/or Reference_Items, 10 each from 4 different Books and/or Reference_Works with Access_Type Open.
* 20 Book_Segments and/or Reference_Items, 10 each from 2 different Books and/or Reference_Works with Access_Type Free_To_Read.

This MUST result in 40 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 4 each of Unique_Title_Investigations and Unique_Title_Requests with Access_Type Controlled; the same again for Access_Type Open; and 20 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 2 each of Unique_Title_Investigations and Unique_Title_Requests with Access_Type Free_To_Read.

**Option 3**: Report provider offers Book_Segments and/or Reference_Items under two different Access_Types.

The auditor MUST request 50 Book_Segments and/or Reference_Items, 10 each from 5 different Books and/or Reference_Works, from each Access_Type represented on the platform.

This MUST result in 50 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 5 each of Unique_Title_Investigations and Unique_Title_Requests with each Access_Type.

The Access_Type combinations might be: Controlled plus Open, Controlled plus Free_To_Read, or Open plus Free_To_Read.


E.5.2.2 Available as Both Book_Segments and/or Reference_Items and Whole Books and/or Reference_Works
'''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''

These tests apply where Books and/or Reference_Works are available as both whole Books and/or Reference_Works and as Book_Segments and/or Reference_Items.

**Option 1**: Report provider offers Book_Segments and/or Reference_Items and Whole Books and/or Reference_Works under only one Access_Type.

The auditor MUST request 

* 50 Book_Segments and/or Reference_Items, 10 each from 5 different Books and/or Reference_Works
* 20 Books and/or Reference_Works, noting the count of Book_Segments and/or Reference_Items from each Title.

This MUST result in 50, plus the count of Book_Segments and/or Reference_Items from the Title downloads, of each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 27 each of Unique_Title_Investigations and Unique_Title_Requests with the appropriate Access_Type.

**Option 2**: Report provider offers Book_Segments and/or Reference_Items under two different Access_Types.

The auditor MUST request 

* 30 Book_Segments and/or Reference_Items, 10 each from 3 different Books and/or Reference_Works, for each Access_Type
* 10 Books and/or Reference_Works, noting the count of Book_Segments and/or Reference_Items from each Title, for each Access_Type.

This MUST result in 30, plus the count of Book_Segments and/or Reference_Items from the Title downloads, of each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 13 each of Unique_Title_Investigations and Unique_Title_Requests, for each of the two Access_Types.

The Access_Type combinations might be: Controlled plus Open, Controlled plus Free_To_Read, or Open plus Free_To_Read.

**Option 3**: Report provider offers Book_Segments and/or Reference_Items under all three Access_Types (Controlled, Open and Free_To_Read).

The auditor MUST request 

* 20 Book_Segments and/or Reference_Items, 10 each from 2 different Books and/or Reference_Works, for each Access_Type
* 5 Books and/or Reference_Works, noting the count of Book_Segments and/or Reference_Items from each Title, for each Access_Type

This MUST result in 20, plus the count of Book_Segments and/or Reference_Items from the Title downloads, of each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 7 each of Unique_Title_Investigations and Unique_Title_Requests, for each of the Access_Types.


E.5.2.3 Available as Whole Books and/or Reference_Works
'''''''''''''''''''''''''''''''''''''''''''''''''''''''

These tests apply where Books and/or Reference_Works are only available as single downloads (i.e. no Book_Segments and/or Reference_Items can be identified).

**Option 1**: Report provider offers Books and/or Reference_Works, without Book_Segments and/or Reference_Items, under only one Access_Type.

The auditor MUST request 25 Books and/or Reference_Works with the appropriate Access_Type.

This MUST result in 25 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations, Unique_Item_Requests, Unique_Title_Investigations and Unique_Title_Requests with the appropriate Access_Type.

Where there are fewer than the required number of Books and/or Reference_Works, the auditor MUST test every item.

**Option 2**: Report provider offers Books and/or Reference_Works, without Book_Segments and/or Reference_Items, under two different Access_Types.

The auditor MUST request 25 Books and/or Reference_Works with each Access_Type.

This MUST result in 25 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations, Unique_Item_Requests, Unique_Title_Investigations and Unique_Title_Requests with each Access_Type.

Where there are fewer than the required number of Books and/or Reference_Works under an Access_Type, the auditor MUST test every item with that Access_Type.

The Access_Type combinations might be: Controlled plus Open, Controlled plus Free_To_Read, or Open plus Free_To_Read.

**Option 3**: Report provider offers Books and/or Reference_Works, without Book_Segments and/or Reference_Items, under all three Access_Types (Controlled, Open and Free_To_Read).

The auditor MUST request

* 20 Books and/or Reference_Works with Access_Type Controlled.
* 20 Books and/or Reference_Works with Access_Type Open.
* 10 Books and/or Reference_Works with Access_Type Free_To_Read.

This MUST result in 20 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations, Unique_Item_Requests, Unique_Title_Investigations and Unique_Title_Requests with Access_Type Controlled; the same again for Access_Type Open; and 10 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations, Unique_Item_Requests, Unique_Title_Investigations and Unique_Title_Requests with Access_Type Free_To_Read.

Where there are fewer than the required number of Books and/or Reference_Works that are Controlled, Open or Free_To_Read, the auditor MUST test every item with that Access_Type.
