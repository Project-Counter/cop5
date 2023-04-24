.. The COUNTER Code of Practice Release 5 © 2017-2023 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

E.5 Audit Tests for Investigations and Requests by Access Type, Books and Reference_Works
-----------------------------------------------------------------------------------------

This section of the appendix outlines tests that MUST be run during audits for any platform delivering Book and/or Reference_Work content. For report providers operating multiple platforms including one or more with Book and/or Reference_Work content, the audit scope as defined in :numref:`audit` MUST include one of these platforms and be subject to the audit tests outlined here. Note that these tests refer to Data_Types Book and Book_Segment for ease of reading. In all cases, Book includes Data_Types Book and Reference_Work, while Book_Segment includes Data_Types Book_Segment and Reference_Item.

These tests apply to the Platform Report, Database Report, Title Report and Item Report. The PR_P1, DR_D1, TR_B1 and TR_B3 Standard Views of the COUNTER Reports will be deemed COUNTER-compliant if the metrics and Data_Types match those in the relevant COUNTER Report, with the appropriate aggregation. 

Unique_Title_Investigations and Unique_Title_Requests are referenced in these audit tests. These MUST NOT appear in the Item Report.

These audit tests specify minimum numbers of Books and Book_Segments to be tested. Where a platform has fewer than the required number of Books, the auditor MUST make at least one request for each Book on the platform, and where necessary undertake duplicate actions to reach the required threshold.

Audit test requirements vary depending on the set up of the platform, as indicated by the Options within the tests below.


E.5.1 Books Available as Book_Segments
""""""""""""""""""""""""""""""""""""""

These tests apply where users can only access books segment-by-segment (i.e. it is not possible to download an entire book as a single file).

**Option 1**: Report provider offers Book_Segments under only one Access_Type.

The auditor MUST request 70 Book_Segments across 7 different Books.

This MUST result in 70 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 7 each of Unique_Title_Investigations and Unique_Title_Requests with the appropriate Access_Type.

**Option 2**: Report provider offers Book_Segments under two different Access_Types.

The auditor MUST request 50 Book_Segments across 5 different Books, from each Access_Type represented on the platform.

This MUST result in 50 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 5 each of Unique_Title_Investigations and Unique_Title_Requests with each Access_Type.

The Access_Type combinations might be: Controlled plus Open, Controlled plus Free_To_Read, or Open plus Free_To_Read.

**Option 3**: Report provider offers Book_Segments under all three Access_Types (Controlled, Open and Free_To_Read).

The auditor MUST request

* 40 Book_Segments across 4 different Books with Access_Type Controlled.
* 40 Book_Segments across 4 different Books with Access_Type Open.
* 20 Book_Segments across 2 different Books with Access_Type Free_To_Read.

This MUST result in 40 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 4 each of Unique_Title_Investigations and Unique_Title_Requests with Access_Type Controlled; the same again for Access_Type Open; and 20 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 2 each of Unique_Title_Investigations and Unique_Title_Requests with Access_Type Free_To_Read.


E.5.2 Books Available as Both Book_Segments and Whole Books
"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""

These tests apply where users can access books segment-by-segment and it is also possible to download an entire book as a single file. These tests also apply where books are available only as whole-books downloads, but Book_Segments can be identified for reporting purposes.

**Option 1**: Report provider offers Book_Segments and Whole Books under only one Access_Type.

The auditor MUST request 

* 50 Book_Segments across 5 different Books
* 20 whole Books, noting the count of Book_Segments from each Title.

This MUST result in 50, plus the count of Book_Segments from the Title downloads, of each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 25 each of Unique_Title_Investigations and Unique_Title_Requests with the appropriate Access_Type.

**Option 2**: Report provider offers Book_Segments and Whole Books under two different Access_Types.

The auditor MUST request 

* 30 Book_Segments across 3 different Books, for each Access_Type
* 10 whole Books, noting the count of Book_Segments, for each Access_Type.

This MUST result in 30, plus the count of Book_Segments from the Title downloads, of each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 13 each of Unique_Title_Investigations and Unique_Title_Requests, for each of the two Access_Types.

The Access_Type combinations might be: Controlled plus Open, Controlled plus Free_To_Read, or Open plus Free_To_Read.

**Option 3**: Report provider offers Book_Segments and Whole Books under all three Access_Types (Controlled, Open and Free_To_Read).

The auditor MUST request 

* 20 Book_Segments across 2 different Books, for each Access_Type
* 5 Books, noting the count of Book_Segments from each Title, for each Access_Type

This MUST result in 20, plus the count of Book_Segments from the Title downloads, of each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 7 each of Unique_Title_Investigations and Unique_Title_Requests, for each of the Access_Types.


E.5.3 Books Available as Whole Books Only
"""""""""""""""""""""""""""""""""""""""""

These tests apply where Books are only available as single downloads and it is not possible to identify Book_Segments.

**Option 1**: Report provider offers Books without Book_Segments under only one Access_Type.

The auditor MUST request 25 Books with the appropriate Access_Type.

This MUST result in 25 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations, Unique_Item_Requests, Unique_Title_Investigations and Unique_Title_Requests with the appropriate Access_Type.

**Option 2**: Report provider offers Books without Book_Segments under two different Access_Types.

The auditor MUST request 25 Books and/or Reference_Works with each Access_Type.

This MUST result in 25 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations, Unique_Item_Requests, Unique_Title_Investigations and Unique_Title_Requests with each Access_Type.

The Access_Type combinations might be: Controlled plus Open, Controlled plus Free_To_Read, or Open plus Free_To_Read.

**Option 3**: Report provider offers Books without Book_Segments under all three Access_Types (Controlled, Open and Free_To_Read).

The auditor MUST request

* 20 Books with Access_Type Controlled.
* 20 Books with Access_Type Open.
* 10 Books with Access_Type Free_To_Read.

This MUST result in 20 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations, Unique_Item_Requests, Unique_Title_Investigations and Unique_Title_Requests with Access_Type Controlled; the same again for Access_Type Open; and 10 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations, Unique_Item_Requests, Unique_Title_Investigations and Unique_Title_Requests with Access_Type Free_To_Read.