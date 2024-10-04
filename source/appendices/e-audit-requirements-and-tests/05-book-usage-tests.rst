.. The COUNTER Code of Practice Release 5 © 2017-2023 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

E.5 Audit Tests for Investigations and Requests for Books and Reference_Works
-----------------------------------------------------------------------------

This section of the appendix outlines tests that MUST be run during audits for any platform delivering Book and/or Reference_Work content. For report providers operating multiple platforms including one or more with Book and/or Reference_Work content, the audit scope as defined in :numref:`audit` MUST include one of these platforms and be subject to the audit tests outlined here. Note that these tests refer to Data_Types Book and Book_Segment for ease of reading. In all cases, Book includes Data_Types Book and Reference_Work, while Book_Segment includes Data_Types Book_Segment and Reference_Item.

These tests apply to the Platform Report, Database Report, Title Report and Item Report. The counts specified in the tests are those required for the Title Report and Item Report, which must be aggregated appropriately for the Platform Report and Database Report where multiple Access_Types are present on the platform under test. The PR_P1, DR_D1, TR_B1 and TR_B3 Standard Views of the COUNTER Reports will be deemed COUNTER-compliant if the metrics and Data_Types match those in the relevant COUNTER Report, with the appropriate aggregation. 

Unique_Title_Investigations and Unique_Title_Requests are referenced in these audit tests. These MUST NOT appear in the Item Report.

These audit tests specify minimum numbers of Books and Book_Segments to be tested. Where a platform has fewer than the required number of Books, the auditor MUST make at least one request for each Book on the platform, and where necessary undertake duplicate actions to reach the required threshold.

Audit test requirements vary depending on the set up of the platform, as indicated by the Options within the tests below.


E.5.1 Books Available as Book_Segments
""""""""""""""""""""""""""""""""""""""

These tests apply where users can access books segment-by-segment.

Where possible, 50% of items requested SHOULD be via browsing the platform and 50% via searching the platform. If either browsing or searching is not possible, all items can be requested via the only available option.

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


E.5.2 Books Available as Whole Books Where Book_Segments Can Be Identified
""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""

These tests apply where books are available as whole-books downloads, and Book_Segments can be identified for reporting purposes.

Where possible, 50% of items requested SHOULD be via browsing the platform and 50% via searching the platform. If either browsing or searching is not possible, all items can be requested via the only available option.

**Option 1**: Report provider offers whole Books with identifiable Book_Segments under only one Access_Type.

The auditor MUST request 50 whole Books, noting the count of Book_Segments from each Title.

This MUST result in  the sum of Book_Segments of each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 50 each of Unique_Title_Investigations and Unique_Title_Requests with the appropriate Access_Type.

**Option 2**: Report provider offers whole Books with identifiable Book_Segments under two different Access_Types.

The auditor MUST request 30 whole Books, noting the count of Book_Segments, for each Access_Type.

This MUST result in the sum of Book_Segments of each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 30 each of Unique_Title_Investigations and Unique_Title_Requests, for each of the two Access_Types.

The Access_Type combinations might be: Controlled plus Open, Controlled plus Free_To_Read, or Open plus Free_To_Read.

**Option 3**: Report provider offers whole Books with identifiable Book_Segments under all three Access_Types (Controlled, Open and Free_To_Read).

The auditor MUST request 20 whole Books, noting the count of Book_Segments from each Title, for each Access_Type

This MUST result in the sum of Book_Segments of each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and 20 each of Unique_Title_Investigations and Unique_Title_Requests, for each of the Access_Types.


E.5.3 Books Available as Whole Books Where Book_Segments Cannot Be Identified
"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""

These tests apply where Books are only available as single downloads and it is not possible to identify Book_Segments.

Where possible, 50% of items requested SHOULD be via browsing the platform and 50% via searching the platform. If either browsing or searching is not possible, all items can be requested via the only available option.

**Option 1**: Report provider offers whole Books without identifable Book_Segments under only one Access_Type.

The auditor MUST request 25 Books.

This MUST result in 25 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations, Unique_Item_Requests, Unique_Title_Investigations and Unique_Title_Requests with the appropriate Access_Type.

**Option 2**: Report provider offers whole Books without identifable Book_Segments under two different Access_Types.

The auditor MUST request 25 Books with each Access_Type.

This MUST result in 25 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations, Unique_Item_Requests, Unique_Title_Investigations and Unique_Title_Requests with each Access_Type.

The Access_Type combinations might be: Controlled plus Open, Controlled plus Free_To_Read, or Open plus Free_To_Read.

**Option 3**: Report provider offers whole Books without identifable Book_Segments under all three Access_Types (Controlled, Open and Free_To_Read).

The auditor MUST request 20 Books of each Access_Type.

This MUST result in 20 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations, Unique_Item_Requests, Unique_Title_Investigations and Unique_Title_Requests for each Access_Type.


E.5.4 Investigations Independent of Requests
""""""""""""""""""""""""""""""""""""""""""""

These audit tests applies where Investigations can be reported independently of Requests. If all Investigations have a matching Request, auditors MUST note this in the audit report. This does not require an exemption from the COUNTER Executive Director.

The tests mimic those defined above, but the auditor MUST undertake a separate Investigation activity for each audit test, resulting in a doubling of the Total_Item_Investigation counts.