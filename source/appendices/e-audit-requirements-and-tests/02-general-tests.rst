.. The COUNTER Code of Practice Release 5 © 2017-2023 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

E.2 General Audit Tests
-----------------------

This section of the appendix outlines tests that MUST be run during all audits, and which are not specific to a particular COUNTER Report.


E.2.1 Validation Tool
"""""""""""""""""""""

Once reports are available for testing (i.e. up to 28 days after the end of the seeding month), auditors MUST run the COUNTER Reports and Standard Views of COUNTER Reports that are within the scope of the audit through the Validation Tool. This test must include all attributes report providers are required to support, including attributes that are included only if called for.

Where report providers have elected to follow the pre-flight preparation step outlined in :numref:`audit` of the Code of Practice, this audit test should not result in any errors.


E.2.2 COUNTER API Endpoints
"""""""""""""""""""""

The auditor MUST test the COUNTER API (formerly sushi) server endpoints as follows

* The /status endpoint MUST be public (i.e. unprotected) to allow report consumers to easily check whether the service is live.
* The /reports endpoint MUST return the date range for which COUNTER Reports and the Standard Views of COUNTER Reports are available. If this is less than the required year-to-date plus two years of back data, the auditor MUST note the missing months in the audit report.
* The /members endpoint MUST return the auditor's customer details.

Any error messages returned by the COUNTER API server in the process of audit MUST be noted in the audit report, including an indication of where these error messages deviate from those specified in  :ref:`Appendix D <appendix-d>`.


E.2.3 Audit Tests for Double-Click Filtering
""""""""""""""""""""""""""""""""""""""""""""

This audit test applies to investigations and requests metrics across all COUNTER Reports and should represent the scope of the platform. That is, where a platform is made up of a mixture of content with Data_Types Article, Multimedia and Patent, the auditor should represent each of those Data_Types proportionately in the audit test.

The test consists of making requests to an item twice in succession (double-clicks). If the two clicks occur within a 30-second time-span, only the second request MUST be recorded, resulting in 1 Total_Item_Investigations and 1 Total_Item_Requests. If the two clicks occur with more than 30 seconds between them, then 2 Total_Item_Investigations and 2 Total_Item_Requests must be counted. In both cases only 1 Unique_Item_Investigations and 1 Unique_Item_Requests will be reported.

The auditor MUST carry out a total of 30 tests:

* 15 Inside tests, whereby 2 identical requests are made and the second request is within 30 seconds of the first.
* 15 Outside tests, whereby 2 identical requests are made and the second request is more than 30 seconds after the first.

The Inside tests MUST result in 15 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and the Outside tests MUST result in 30 Total_Item_Investigations, 30 Total_Item_Requests, 15 Unique_Item_Investigations and 15 Unique_Item_Requests, for a total of 45 Total_Item_Investigations, 45 Total_Item_Requests, 30 Unique_Item_Investigations and 30 Unique_Item_Requests.

Note that in the specific case of platforms offering Books and/or Reference_Works as whole-title downloads where Book_Segments and/or Reference_Items can be identified, the metric counts will deviate from those specified. The auditor MUST note the number of Book_Segments and/or Reference_Items in the titles subject to double-click tests, and the number of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests must reflect the number of Book_Segments and/or Reference_Items in addition to any other items tested.
