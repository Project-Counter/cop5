.. The COUNTER Code of Practice Release 5 © 2017-2023 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

Transitioning from COUNTER R5 to R5.1
-------------------------------------

The transition from R5 to R5.1 meets the general requirements outlined in :numref:`transitioning-new-cop`.

* Report providers MUST be compliant by Feburary 2025 for delivery of reports starting with January 2025 usage.
* Report providers may choose to become compliant with R5.1 before February 2025.
* Report providers MUST offer R5-compliant reports until April 2025 for delivery of reports up to and including March 2025 usage.
* Report providers may choose to offer access to R5 reports beyond April 2025 at their discretion.


Comparing R5 and R5.1 COUNTER Reports
"""""""""""""""""""""""""""""""""""""

R5 and R5.1 reports are broadly comparable, provided some care is applied.

* In R5.1, the rule that items are the unit of reporting is applied consistently for all Data_Types. This means item-level requests and investigations for books may be larger in R5.1 reports. To compare R5 to R5.1, report consumers should use the Unique_Title_Investigations and Unique_Title_Requests.
* For the same reason, R5.1 does not use the Section_Type attribute.
* The list of Data_Types has been expanded. This means that conference proceedings, for example, can be more accurately classified. Report consumers are advised to use the Title Report to gain a full understanding of usage, rather than using Standard Views of the Title Report which are restricted to reporting on books and journals.
* The definition and application of Access_Types has been clarified. The primary impact here is on the TR_B1, TR_J1 and TR_J4 Standard Views of the Title Report, which will show only Controlled content without Free_To_Read materials. Report consumers are advised to use the Title Report to gain a full understanding of usage.
* Components, an aspect of the Item Report, are optional in R5.1. Report consumers should sum up item usage from R5 Item Reports offering Components to compare like-for-like with item usage in R5.1 Item Reports not offering Components.


A note on JSON
""""""""""""""

The R5.1 JSON schema is more compact, resulting in smaller files that are easier to produce, validate, and consume. It can be converted back to the R5 structure, but other changes in R5.1, specifically those detailed above, mean care should be taken when comparing usage reported in R5 and R5.1 formats.
