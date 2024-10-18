Change Log
==========

Starting with Release 5.0.2 the COUNTER Code of Practice Release 5 is maintained in the GitHub repository `Project-Counter/cop5 <https://github.com/Project-Counter/cop5>`_. The HTML and PDF version are build with `Sphinx <https://www.sphinx-doc.org/>`_ from the `reStructuredText <https://www.sphinx-doc.org/en/master/usage/restructuredtext/index.html>`_ in the `source <source/>`_ directory and can be read online at

  https://cop5.projectcounter.org/

All changes to the COUNTER Code of Practice Release 5 are tracked with GitHub issues and linked pull requests. Starting with the publication of Release 5.0.2 the SwaggerHub feature "GitHub Sync" will be used to also track changes to the COUNTER_SUSHI API Specification, for Release 5.0.2 there are only issues for these changes.

The change log below is ordered by type of change. It shows the GitHub issue titles and numbers and the impact of the change (metric calcuation, report structure, permitted attribute values, sushi, documentation), with links to the issues. From Release 5.1, the structure reflects our Explicit Versioning system (see :ref:`maintenance`).


Release 5.1
-------------

`List of issues on GitHub <https://github.com/Project-Counter/cop5/issues?q=is%3Aissue+milestone%3A%22Release+5.1%22>`_

**Breaking Changes**

* Report headers: links to COUNTER Registry `#134 <https://github.com/Project-Counter/cop5/issues/134>`_ [report structure]
* Components moved from required to optional `#135 <https://github.com/Project-Counter/cop5/issues/135>`_ [report structure]
* Access_Type: updated definitions `#140 <https://github.com/Project-Counter/cop5/issues/140>`_ [permitted attribute values]
* Item as the unit of reporting `#142 <https://github.com/Project-Counter/cop5/issues/142>`_ [metric calculation]
* Removal of Section_Type `#143 <https://github.com/Project-Counter/cop5/issues/143>`_ [metric calcuation]
* Amendment of item counts for whole-book downloads `#149 <https://github.com/Project-Counter/cop5/issues/149>`_ [metric calculation]
* Data_Types: include Data_Type in COUNTER Reports `#150 <https://github.com/Project-Counter/cop5/issues/150>`_ [report structure]
* Data_Types: extend the list of Data_Types `#151 <https://github.com/Project-Counter/cop5/issues/151>`_ [permitted attribute values]
* Data_Types: include Data_Type in PR_P1 `#155 <https://github.com/Project-Counter/cop5/issues/155>`_ [report structure]
* SUSHI: Remove IP address authorization from COUNTER_SUSHI API `#206 <https://github.com/Project-Counter/cop5/issues/206>`_ [sushi]
* SUSHI: Include Release in the COUNTER_SUSHI API path `#207 <https://github.com/Project-Counter/cop5/issues/207>`_ [sushi]
* SUSHI: /r51/status as a public endpoint `#216 <https://github.com/Project-Counter/cop5/issues/216>`_ [sushi]
* SUSHI: include available months of data in path /r51/reports `#218 <https://github.com/Project-Counter/cop5/issues/218>`_ [sushi]
* SUSHI: clarify requirements for /r51/members endpoint `#219 <https://github.com/Project-Counter/cop5/issues/219>`_ [sushi]
* SUSHI: add common extension parameters to COUNTER_SUSHI API paths `#224 <https://github.com/Project-Counter/cop5/issues/224>`_ [report structure]
* SUSHI: remove search parameter from COUNTER_SUSHI API path /r51/reports `#232 <https://github.com/Project-Counter/cop5/issues/232>`_ [documentation]
* SUSHI/JSON: upgrade COUNTER_SUSHI API Specification to OpenAPI3.1/JSON schema `#182 <https://github.com/Project-Counter/cop5/issues/182>`_ [report structure]
* JSON: JSON format changes `#183 <https://github.com/Project-Counter/cop5/issues/183>`_ [report structure]
* JSON: remove Customer_ID from report header `#204 <https://github.com/Project-Counter/cop5/issues/204>`_ [report structure] 

**New Features**

* Global Item Reports: encouraging Item Reports `#136 <https://github.com/Project-Counter/cop5/issues/136>`_ [documentation]
* Global Item Reports: encouraging Global Reports `#137 <https://github.com/Project-Counter/cop5/issues/137>`_ [report structure]
* Global Item Reports: standard Customer_ID `#138 <https://github.com/Project-Counter/cop5/issues/138>`_ [attribute values]
* Common extension for number of Book_Segments `#148 <https://github.com/Project-Counter/cop5/issues/148>`_ [report structure]

**Bug Fixes**

* Versioning: use of explicit versioning `#131 <https://github.com/Project-Counter/cop5/issues/131>`_ [documentation]
* Versioning: submitting proposed changes `#132 <https://github.com/Project-Counter/cop5/issues/132>`_ [documentation]
* Versioning: and timelines for release `#133 <https://github.com/Project-Counter/cop5/issues/133>`_ [documentation]
* Clarifying the application of Access_Types `#139 <https://github.com/Project-Counter/cop5/issues/139>`_ [documentation]
* Transition notes: addition of R5.1 `#141 <https://github.com/Project-Counter/cop5/issues/141>`_ [documentation]
* Transition notes: clarification of rules around transitioning `#144 <https://github.com/Project-Counter/cop5/issues/144>`_ [documentation]
* Audit guidance `#146 <https://github.com/Project-Counter/cop5/issues/146>`_ [documentation]
* Revision of Appendix E, audit scripts `#184 <https://github.com/Project-Counter/cop5/issues/184>`_ [documentation]
* Technical guidance moved from Friendly Guide into Code of Practice `#147 <https://github.com/Project-Counter/cop5/issues/147>`_ [documentation]
* Consortia reporting `#153 <https://github.com/Project-Counter/cop5/issues/153>`_ [documentation]
* Replacement sample reports (tsv) `#154 <https://github.com/Project-Counter/cop5/issues/154>`_ [documentation]
* Replacement sample reports (json) `#173 <https://github.com/Project-Counter/cop5/issues/173>`_ [documentation]
* Replacement sample reports (Excel) `#230 <https://github.com/Project-Counter/cop5/issues/230>`_ [documentation]
* Removal of comparisons to Release 4 `#192 <https://github.com/Project-Counter/cop5/issues/192>`_ [documentation]

**Text Edits and Clarifications**

* The COUNTER_SUSHI API can now be found at `Stoplight.io <https://countermetrics.stoplight.io/docs/counter-sushi-api>`_.
* Global text changes: Report naming `#126 <https://github.com/Project-Counter/cop5/issues/126>`_ [documentation]
* Global text changes: dates changed to be current `#127 <https://github.com/Project-Counter/cop5/issues/127>`_ [documentation]
* Global text changes: lists of all reports compressed for ease of reading `#128 <https://github.com/Project-Counter/cop5/issues/128>`_ [documentation]
* Global text changes: requested elements now indicated as 'if called for' `#129 <https://github.com/Project-Counter/cop5/issues/129>`_ [documentation]
* Global text changes: report provider and report consumer in place of publisher and library `#145 <https://github.com/Project-Counter/cop5/issues/145>`_ [documentation]
* General copy-edit `#130 <https://github.com/Project-Counter/cop5/issues/130>`_ [documentation]
* Image replacements `#165 <https://github.com/Project-Counter/cop5/issues/165>`_ [documentation]
* Addition of examples for Components `#233 <https://github.com/Project-Counter/cop5/issues/233>`_ [documentation]
* Miscellaneous corrections and clarifications identified during pre-live review `#198 <https://github.com/Project-Counter/cop5/issues/198>`_ [documentation]
* Changelog for R5.1 `#152 <https://github.com/Project-Counter/cop5/issues/152>`_ [documentation]


Release 5.0.3
-------------

`List of issues on GitHub <https://github.com/Project-Counter/cop5/issues?q=is%3Aissue+milestone%3A%22Release+5.0.3%22>`_

**Corrections**

* Fix Data_Type lists and examples in COUNTER_SUSHI API Specification `#125 <https://github.com/Project-Counter/cop5/issues/125>`_ [permitted attribute values]
* Add missing ROR ID to the COUNTER_SUSHI API Specification `#209 <https://github.com/Project-Counter/cop5/issues/209>`_ [documentation]

**Clarifications**

* Clarify invocation conditions for Exception 3030 `#201 <https://github.com/Project-Counter/cop5/issues/201>`_ [documentation]

**Documentation**

* Update COUNTER contact email address `#200 <https://github.com/Project-Counter/cop5/issues/200>`_ [documentation]
* Remove postal address from Appendix C `#213 <https://github.com/Project-Counter/cop5/issues/213>`_ [documentation]
* Update change log, release information and URLs for Release 5.0.3 `#211 <https://github.com/Project-Counter/cop5/issues/211>`_ [documentation]


Release 5.0.2
-------------

`List of issues on GitHub <https://github.com/Project-Counter/cop5/issues?q=is%3Aissue+milestone%3A%22Release+5.0.2%22+>`_

**Amendments**

* Update Searches metrics definitions (amendment published 2018-12-11) `#22 <https://github.com/Project-Counter/cop5/issues/22>`_ [metric calculation]
* Add Data_Type Unspecified `#23 <https://github.com/Project-Counter/cop5/issues/23>`_ [permitted attribute values]
* Add ROR ID as institution and publisher identifier `#61 <https://github.com/Project-Counter/cop5/issues/61>`_ [permitted attribute values]
* Add Exception 2030: IP Address Not Authorized to Access Service `#73 <https://github.com/Project-Counter/cop5/issues/73>`_ [sushi]
* Add extensions for reporting open content not attributed to institutions `#100 <https://github.com/Project-Counter/cop5/issues/100>`_ [documentation]

**Corrections**

* Add missing include_parent_details parameter to COUNTER_SUSHI API path /reports/ir `#12 <https://github.com/Project-Counter/cop5/issues/12>`_ [report structure]
* Rename parameter include_item_components for COUNTER_SUSHI API path /reports/ir to include_component_details `#13 <https://github.com/Project-Counter/cop5/issues/13>`_ [report structure]
* Fix data type of Item_Parent property in COUNTER_SUSHI API object COUNTER_item_usage `#14 <https://github.com/Project-Counter/cop5/issues/14>`_ [report structure]
* Fix required properties in COUNTER_SUSHI API objects COUNTER_item_parent and COUNTER_item_component `#15 <https://github.com/Project-Counter/cop5/issues/15>`_ [report structure]
* Add missing Item_ID property to COUNTER_SUSHI API object COUNTER_database_usage `#16 <https://github.com/Project-Counter/cop5/issues/16>`_ [report structure]
* Remove Publisher and Publisher_ID properties from COUNTER_SUSHI API objects COUNTER_item_component and COUNTER_item_parent `#17 <https://github.com/Project-Counter/cop5/issues/17>`_ [report structure]
* Fix Other_Free_To_Read use in Master Title Reports `#2 <https://github.com/Project-Counter/cop5/issues/2>`_ [permitted attribute values]
* Add missing rule for marking DUL-captured usage with namespace DUL `#63 <https://github.com/Project-Counter/cop5/issues/63>`_ [permitted attribute values]
* Fix operationId for COUNTER_SUSHI API path /reports/dr `#18 <https://github.com/Project-Counter/cop5/issues/18>`_ [sushi]
* Remove Exclude_Monthly_Details values from TR_J1 filter list `#4 <https://github.com/Project-Counter/cop5/issues/4>`_ [documentation]
* Fix Article_Version description `#6 <https://github.com/Project-Counter/cop5/issues/6>`_ [documentation]
* Fix Unique_Title metric descriptions `#8 <https://github.com/Project-Counter/cop5/issues/8>`_ [documentation]
* Add missing Host_Type eJournal for Data_Type Newspaper_or_Newsletter `#10 <https://github.com/Project-Counter/cop5/issues/10>`_ [documentation]
* Fix description for the COUNTER_SUSHI API path /reports/ir_a1 `#20 <https://github.com/Project-Counter/cop5/issues/20>`_ [documentation]
* Remove Exceptions 3071 and 3080 `#45 <https://github.com/Project-Counter/cop5/issues/45>`_ [documentation]
* Update SUSHI_error_model to match the COUNTER_SUSHI API Specification `#51 <https://github.com/Project-Counter/cop5/issues/51>`_ [documentation]
* Fix examples in the glossary `#57 <https://github.com/Project-Counter/cop5/issues/57>`_ [documentation]
* Fix issues in Figures 3.b and 3.d `#69 <https://github.com/Project-Counter/cop5/issues/69>`_ [documentation]
* Restructure and update Appendix E: Audit Requirements and Tests `#75 <https://github.com/Project-Counter/cop5/issues/75>`_ [documentation]
* Fix description for the Exceptions report header `#83 <https://github.com/Project-Counter/cop5/issues/83>`_ [documentation]
* Update and fix definitions for glossary entries `#85 <https://github.com/Project-Counter/cop5/issues/85>`_ [documentation]
* Fix wrong report name, metrics and example in Appendix B `#96 <https://github.com/Project-Counter/cop5/issues/96>`_ [documentation]
* Fix and improve the sample Master Reports and Standard Views `#106 <https://github.com/Project-Counter/cop5/issues/106>`_ [documentation]

**Clarifications**

* Clarify rules for extending Master Reports and using the reserved elements `#41 <https://github.com/Project-Counter/cop5/issues/41>`_ [report structure, permitted attribute values]
* Clarify rules for using byte order marks in reports in text formats `#65 <https://github.com/Project-Counter/cop5/issues/65>`_ [report structure]
* Add missing rule for Identifier property in COUNTER_SUSHI API object COUNTER_item_contributors `#19 <https://github.com/Project-Counter/cop5/issues/19>`_ [permitted attribute values]
* Clarify that author identifiers are optional and only one identifier is permitted `#35 <https://github.com/Project-Counter/cop5/issues/35>`_ [permitted attribute values]
* Update rules for platform IDs and add guidance on how to choose a platform ID `#37 <https://github.com/Project-Counter/cop5/issues/37>`_ [permitted attribute values]
* Add HTTP status codes for COUNTER_SUSHI API `#43 <https://github.com/Project-Counter/cop5/issues/43>`_ [sushi]
* Deprecate Exceptions 3000 and 3010 `#47 <https://github.com/Project-Counter/cop5/issues/47>`_ [sushi]
* Deprecate Severity element in COUNTER_SUSHI API object SUSHI_error_model `#49 <https://github.com/Project-Counter/cop5/issues/49>`_ [sushi]
* Provide guidance on how to deal with different types of errors and multiple Exceptions `#71 <https://github.com/Project-Counter/cop5/issues/71>`_ [sushi]
* Provide guidance on how to deal with specific error conditions `#81 <https://github.com/Project-Counter/cop5/issues/81>`_ [sushi]
* Update description for Data_Type Journal `#25 <https://github.com/Project-Counter/cop5/issues/25>`_ [documentation]
* Clarify required file formats for tabular COUNTER reports `#33 <https://github.com/Project-Counter/cop5/issues/33>`_ [documentation]
* Update recommendations and add error level information for the Validation Tool `#39 <https://github.com/Project-Counter/cop5/issues/39>`_ [documentation]
* Clarify rules for using custom Exceptions `#53 <https://github.com/Project-Counter/cop5/issues/53>`_ [documentation]
* Use Requested in place of Optional for columns/elements only included when requested `#55 <https://github.com/Project-Counter/cop5/issues/55>`_ [documentation]
* Add note to appendixes that in case of conflicts the main document takes precedence `#94 <https://github.com/Project-Counter/cop5/issues/94>`_ [documentation]
* Clarify description for Institution_Name and "The World" `#98 <https://github.com/Project-Counter/cop5/issues/98>`_ [documentation]
* Clarify required elements and values and the impact of missing values `#102 <https://github.com/Project-Counter/cop5/issues/102>`_ [documentation]
* Clarify and align the rules for Institution_ID and Publisher_ID `#104 <https://github.com/Project-Counter/cop5/issues/104>`_ [documentation]

**Documentation**

* Separate columns for COUNTER_SUSHI API HTTP methods and paths `#27 <https://github.com/Project-Counter/cop5/issues/27>`_ [documentation]
* Add RFC 2119 keywords SHOULD (NOT) `#29 <https://github.com/Project-Counter/cop5/issues/29>`_ [documentation]
* Fix inconsistent Exception element names `#31 <https://github.com/Project-Counter/cop5/issues/31>`_ [documentation]
* Update notation, wording and layout in the glossary for consistency `#59 <https://github.com/Project-Counter/cop5/issues/59>`_ [documentation]
* Add transition note for Distributed Usage Logging (DUL) `#67 <https://github.com/Project-Counter/cop5/issues/67>`_ [documentation]
* Remove unused terms from the glossary `#76 <https://github.com/Project-Counter/cop5/issues/76>`_ [documentation]
* Add missing terms to the glossary `#79 <https://github.com/Project-Counter/cop5/issues/79>`_ [documentation]
* Update Section 7.1 Return Codes `#87 <https://github.com/Project-Counter/cop5/issues/87>`_ [documentation]
* Sort glossary terms alphabetically `#92 <https://github.com/Project-Counter/cop5/issues/92>`_ [documentation]
* Integrate the COUNTER_SUSHI API Specification with the Code of Practice repository `#107 <https://github.com/Project-Counter/cop5/issues/107>`_ [documentation]
* Add COUNTER logo to HTML version `#110 <https://github.com/Project-Counter/cop5/issues/110>`_ [documentation]
* Fix PDF section numbering `#111 <https://github.com/Project-Counter/cop5/issues/111>`_ [documentation]
* Miscellaneous wording, typographic and layout corrections `#116 <https://github.com/Project-Counter/cop5/issues/116>`_ [documentation]
* Add change log and release information for Release 5.0.2 `#118 <https://github.com/Project-Counter/cop5/issues/118>`_ [documentation]
