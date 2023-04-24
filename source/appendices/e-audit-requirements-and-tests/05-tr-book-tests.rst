.. The COUNTER Code of Practice Release 5 © 2017-2021 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

E.5 Title Report Audit Tests for Books and Reference_Works
----------------------------------------------------------

This section of the appendix outlines tests that MUST be run during audits for a Host_Type that is required to offer the Title Report and which includes Book and/or Reference_Work content requiring delivery of the book-related Standard Views of the Title Report (TR_B1, TR_B2, TR_B3). Title Report audit tests for Book and/or Reference_Work apply to Host_Types Aggregated_Full_Content, eBook, and eBook_Collection.

The Title Report will be COUNTER-compliant for Book and/or Reference_Work content if the following audit tests are passed. The book-related Standard Views of the Title Report (TR_B1, TR_B2, TR_B3) will be COUNTER-compliant if the metrics match those in the Title Report, with the appropriate aggregation.

Audit test requirements vary depending on the set up of the platform, as indicated by the Options within the tests below.

Note that Data_Types Book and Reference_Work are included in the audit tests, as Reference_Works are included in the book-related Standard Views of the Title Report.


E.5.1 Book Access Types and Unique Title Metrics
""""""""""""""""""""""""""""""""""""""""""""""""

Within the Title Report, breakdowns by Access_Type are essential. There are therefore a series of audit tests designed to determine report providers’ compliance with requirements for reporting Access_Type.


E.5.1.1 Available as Book_Segments and/or Reference_Items
'''''''''''''''''''''''''''''''''''''''''''''''''''''''''

These tests apply where users can only access Books and/or Reference_Works segment-by-segment.

**Option 1**: Report provider offers Book_Segments and/or Reference_Items under only one Access_Type.

The auditor MUST request 70 Book_Segments and/or Reference_Items, 10 each from 7 different Books and/or Reference_Works.

This MUST result in 70 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 7 each of Unique_Title_Investigations and Unique_Title_Requests with the appropriate Access_Type.

**Option 2**: Report provider offers Book_Segments and/or Reference_Items under two different Access_Types.

The auditor MUST request 50 Book_Segments and/or Reference_Items, 10 each from 5 different Books and/or Reference_Works, from each Access_Type represented on the platform.

This MUST result in 50 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 5 each of Unique_Title_Investigations and Unique_Title_Requests with each Access_Type.

The Access_Type combinations might be: Controlled plus Open, Controlled plus Free_To_Read, or Open plus Free_To_Read.

**Option 3**: Report provider offers Book_Segments and/or Reference_Items under all three Access_Types (Controlled, Open and Free_To_Read).

The auditor MUST request

* 40 Book_Segments and/or Reference_Items, 10 each from 4 different Books and/or Reference_Works with Access_Type Controlled.
* 40 Book_Segments and/or Reference_Items, 10 each from 4 different Books and/or Reference_Works with Access_Type Open.
* 20 Book_Segments and/or Reference_Items, 10 each from 2 different Books and/or Reference_Works with Access_Type Free_To_Read.

This MUST result in 40 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 4 each of Unique_Title_Investigations and Unique_Title_Requests with Access_Type Controlled; the same again for Access_Type Open; and 20 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 2 each of Unique_Title_Investigations and Unique_Title_Requests with Access_Type Free_To_Read.


E.5.1.2 Available as Both Book_Segments and/or Reference_Items and Whole Books and/or Reference_Works
'''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''

These tests apply where Books and/or Reference_Works are available as both whole Books and/or Reference_Works and as Book_Segments and/or Reference_Items. These tests also apply where Books and/or Reference_Works are available only as whole Books and/or Reference_Works, but Book_Segments and/or Reference_Items can be identified for reporting purposes.

**Option 1**: Report provider offers Book_Segments and/or Reference_Items and Whole Books and/or Reference_Works under only one Access_Type.

The auditor MUST request 

* 50 Book_Segments and/or Reference_Items, 10 each from 5 different Books and/or Reference_Works
* 20 Books and/or Reference_Works, noting the count of Book_Segments and/or Reference_Items from each Title.

This MUST result in 50, plus the count of Book_Segments and/or Reference_Items from the Title downloads, of each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 25 each of Unique_Title_Investigations and Unique_Title_Requests with the appropriate Access_Type.

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


E.5.1.3 Available as Whole Books and/or Reference_Works
'''''''''''''''''''''''''''''''''''''''''''''''''''''''

These tests apply where Books and/or Reference_Works are only available as single downloads (i.e. no Book_Segments and/or Reference_Items can be identified).

**Option 1**: Report provider offers Books and/or Reference_Works, without Book_Segments and/or Reference_Items, under only one Access_Type.

The auditor MUST request 25 Books and/or Reference_Works with the appropriate Access_Type.

This MUST result in 25 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations, Unique_Item_Requests, Unique_Title_Investigations and Unique_Title_Requests with the appropriate Access_Type.

**Option 2**: Report provider offers Books and/or Reference_Works, without Book_Segments and/or Reference_Items, under two different Access_Types.

The auditor MUST request 25 Books and/or Reference_Works with each Access_Type.

This MUST result in 25 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations, Unique_Item_Requests, Unique_Title_Investigations and Unique_Title_Requests with each Access_Type.

The Access_Type combinations might be: Controlled plus Open, Controlled plus Free_To_Read, or Open plus Free_To_Read.

**Option 3**: Report provider offers Books and/or Reference_Works, without Book_Segments and/or Reference_Items, under all three Access_Types (Controlled, Open and Free_To_Read).

The auditor MUST request

* 20 Books and/or Reference_Works with Access_Type Controlled.
* 20 Books and/or Reference_Works with Access_Type Open.
* 10 Books and/or Reference_Works with Access_Type Free_To_Read.

This MUST result in 20 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations, Unique_Item_Requests, Unique_Title_Investigations and Unique_Title_Requests with Access_Type Controlled; the same again for Access_Type Open; and 10 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations, Unique_Item_Requests, Unique_Title_Investigations and Unique_Title_Requests with Access_Type Free_To_Read.