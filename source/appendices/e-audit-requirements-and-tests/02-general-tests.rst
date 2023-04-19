.. The COUNTER Code of Practice Release 5 © 2017-2021 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

E.2 General Audit Tests
-----------------------

This section of the appendix outlines tests that MUST be run during all audits, and which are not specific to a particular COUNTER Report.


E.2.1 Validation Tool
"""""""""""""""""""""

Once reports are available for testing (i.e. up to 28 days after the end of the seeding month), auditors MUST run the COUNTER Reports and Standard Views of COUNTER Reports that are within the scope of the audit through the Validation Tool. This test must include all attributes report providers are required to support, including attributes that are included only if called for.

Where report providers have elected to follow the pre-flight preparation step outlined in Section 9 of the Code of Practice, this audit test should not result in any errors.


E.2.2 SUSHI Endpoints
"""""""""""""""""""""

The auditor MUST test the SUSHI service endpoints as follows

* The /status endpoint MUST be public (i.e. unprotected) to allow report consumers to easily check whether the service is live.
* The /reports endpoint MUST return the date range for which COUNTER Reports and the Standard Views of COUNTER Reports are available. If this is less than the required year-to-date plus two years of back data, the auditor MUST note the missing months in the audit report.

Any error messages returned by the SUSHI service in the process of audit MUST be noted in the audit report, including an indication of where these error messages deviate from those specified in  :ref:`Appendix D <appendix-d>`.


E.2.3 Audit Tests for Double-Click Filtering
""""""""""""""""""""""""""""""""""""""""""""

This audit test applies to investigations and requests metrics across all COUNTER Reports and should represent the scope of the platform. That is, where a platform is made up of a mixture of content with Data_Types Article, Multimedia and Patent, the auditor should represent each of those Data_Types proportionately in the audit test.

The test consists of making requests to an item twice in succession (double-clicks). If the two clicks occur within a 30-second time-span, only the second request MUST be recorded, resulting in 1 Total_Item_Investigation and 1 Total_Item_Request. If the two clicks occur with more than 30 seconds between them, then 2 Total_Item_Investigations and 2 Total_Item_Requests must be counted. In both cases only 1 Unique_Item_Investigation and 1 Unique_Item_Request will be reported.

The auditor MUST carry out a total of 30 tests:

* 15 “Inside” tests, whereby 2 identical requests are made and the second request is within 30 seconds of the first.
* 15 “Outside” tests, whereby 2 identical requests are made and the second request is more than 30 seconds after the first.

The “Inside” tests MUST result in 15 each of Total_Item_Investigations, Total_Item_Requests, Unique_Item_Investigations and Unique_Item_Requests, and the “Outside” tests MUST result in 30 Total_Item_Investigations, 30 Total_Item_Requests, 15 Unique_Item_Investigations and 15 Unique_Item_Requests, for a total of 45 Total_Item_Investigations, 45 Total_Item_Requests, 30 Unique_Item_Investigations and 30 Unique_Item_Requests.


E.2.4 Audit Tests for Denials
"""""""""""""""""""""""""""""

Report providers operating platforms where turnaways or denials are in operation MUST be subject to audit tests for denials. For report providers operating multiple platforms, the audit scope as defined in :numref:`audit` MUST include platforms where turnaways or denials are in operation. Where either Limit_Exceeded or No_License denials do not apply to a report provider, auditors MUST note this in the audit report. This does not require an exemption from the COUNTER Project Director.

These audit tests apply to denial metrics across all COUNTER Reports and should represent the scope of the platform under audit. That is, where a platform is made up of a mixture of content with Data_Types Article, Multimedia and Patent, the auditor SHOULD represent each of those Data_Types proportionately in the audit test.


E.2.4.1 Limit_Exceeded
''''''''''''''''''''''

Note that the account used for this testing MUST have concurrent / simultaneous-user limit (concurrency limits) set at a single user. A second user attempting to access the database would be denied.

**Option 1**: The report provider denies the user access when the concurrency limit is exceeded upon login.

The auditor MUST force 50 Limit_Exceeded access denials by logging into the site causing the user limit to reach the maximum allowance. The auditor will then attempt to log into the site using a different computer, or a different browser, which should be refused access. Each time access is refused, the auditor will record this as 1 Limit_Exceeded.

The test MUST result in 50 Limit_Exceeded.

**Option 2**: The report provider denies the user access when the concurrency limit is exceeded upon searching or accessing a database.

The auditor MUST force 50 Limit_Exceeded turnaways by logging into the site, then either selecting and searching a database or browsing to a database causing the user limit to reach the maximum allowance. The auditor will then log into the same site using a different computer, or a different browser, and repeat the action, which should be refused access. Each time access is refused, the auditor will record this as 1 Limit_Exceeded.

The test MUST result in 50 Limit_Exceeded.

**Option 3**: The report provider denies the user access when the concurrency limit is exceeded upon accessing a content item.

The auditor MUST force 50 Limit_Exceeded turnaways by logging into the site and requesting an item, causing the user limit to reach the maximum allowance. The auditor will then log into the site again using a different computer, or a different browser, and repeat the action, which should be refused access. Each time access is refused, the auditor will record this as 1 Limit_Exceeded.

The test MUST result in 50 Limit_Exceeded.


E.2.4.2 No_Licence
''''''''''''''''''

The content for which the auditor has no license MUST be declared by the report provider prior to audit testing.

The auditor MUST force 50 No_License turnaways by logging into the site and requesting an item. Each time access is refused, the auditor will record this as 1 No_License.

The test MUST result in 50 No_License.
