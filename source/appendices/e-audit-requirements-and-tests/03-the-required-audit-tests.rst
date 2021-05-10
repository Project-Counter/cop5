.. The COUNTER Code of Practice Release 5 © 2017-2021 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

E.3 The Required Audit Tests
----------------------------

Stage 1. Report Format: Checking the report layout and file-format against the COUNTER Code of Practice
"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""

The auditor will confirm that each of the audit reports complies with the COUNTER Code of Practice.

The following items will be checked:

* The layout of the report (headers/footers, number of fields, field sequence, totals field, and format of reported numbers)
* The conformity of identifiers to the required standard (e.g. ISSNs must be provided as nine digits, with a hyphen as the middle digit)
* The presence of all required file formats (a Microsoft Excel file, a tab-separated value (TSV) file, or a file that can be easily imported into Microsoft Excel)
* That email alerts are set to report usage reports updated in a timely manner
* Flexibility in the reporting period so customers can specify the start and end months of data reported in the COUNTER reports
* That COUNTER usage reports are available in JSON format in accordance with the COUNTER JSON schema specified by SUSHI. (Schema may be found on the NISO/SUSHI website at: http://www.niso.org/schemas/sushi/)
* That COUNTER schema covers all the COUNTER usage reports.
* That the JSON formatted report produced via SUSHI matches the total of the relevant usage counted on the equivalent .tsv/Excel report offered by the content provider, i.e. A report should produce the same results irrespective of the format in which it is delivered.


Stage 2. Data Integrity: Checking the usage numbers as reported
"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""

The audit-test must be conducted in such a way that the auditor’s activities during the audit-test can be isolated from other activities on the content provider’s site. Depending on the site being tested, the auditor must conduct the audit-test from a computer with a unique IP address and/or using a unique account number.

The auditor must accept user/machine and session cookies when prompted.


Platform Reports
''''''''''''''''

Master Report: PR
.................

The Platform Master Report will be COUNTER-compliant if the following Standard View passes the COUNTER Audit and the figures reported within it are matching what is reported in the Master Report.


Standard View: PR_P1
....................

Platform Usage: A Standard View of the Platform Master Report offering platform-level usage summarized by Metric_Type.

An audit of this Standard View requires the following:

#. The auditor must have access to all databases as made available on the platform of the content provider.
#. Audit-test P1-1: Searches_Platform

   - *Option 1:* Platform has multiple databases, and it is possible to search over all databases, selected subset of databases, or a single database.

     The auditor must run 100 searches on the platform, including 50 searches against only 1 selected database, 25 against 2 selected databases, and 25 against all databases. Each of these searches must report 1 Searches_Platform in the PR_P1 Standard View.

     *Option 2:* Platform has multiple databases, and it is possible to search over all databases or a single database.

     The auditor must run 100 searches on the platform, including 50 searches against only 1 selected database and 50 against all databases. Each of these searches must report 1 Searches_Platform in the PR_P1 Standard View.

     *Option 3:* Platform has a single database.

     The auditor must run 50 searches on the platform, with all 50 searches run against the 1 database. Each of these searches must report 1 Searches_Platform in the PR_P1 Standard View.
   - All searches, including those returning 0 results, must be reported as a Searches_Platform in the PR_P1 Standard View.
   - The auditor must allow at least 31 seconds between each search.
   - Each time a search is conducted, the auditor will record the search term, the database searched, and the number of results returned.
   - A content provider will pass this audit test when the sum of the searches reported by the content provider in PR_P1 Standard View for the auditor’s test account is within a -8% and +3% reliability window of the sum of the searches on the auditor’s report.
  
#. Audit-test P1-2: Total_Item_Requests, Unique_Item_Requests and Unique_Title_Requests

   - *Option 1:* Platform has multiple databases that include titles.

     The auditor must make a total of 100 requests on a subset of the unique items made available to them, including 50 requests against items not within titles (if available) and 50 requests against items within titles (if available).

     If the platform does not have content that is within a title, then all 100 requests must be made to items within titles.

     Each title must have 5 Items requested within it (reporting 5 Total_Item_Requests, 5 Unique_Item_Requests, and 1 Unique_Title_Requests).

     It may not be possible to know which Title the Item being requested belongs to prior to the delivery of the Item. In this case, the titles containing the Item must be noted by the auditor upon request. This must result in 100 Total_Item_Requests and 100 Unique_Item_Requests in the PR_P1 Standard View.

     The Unique_Title_Requests being reported in the PR_P1 Standard View will be determined by the number of unique titles noted by the auditor during the testing.

     *Option 2:* Platform has multiple databases that do not include titles.

     The auditor must make 100 requests on a subset of the unique items made available to them.

     This must result in 100 Total_Item_Requests and 100 Unique_Item_Requests being reported in the PR_P1 Standard View. The number of Unique_Title_Requests being reported will be 0.

     *Option 3:* Platform has a single database, which includes titles.

     The auditor must make 50 requests on items made available to them, including 25 requests against items not within titles (if available) and 25 requests against Items within titles (if available).

     If the platform does not have content that is within a Title, then all 50 requests must be made to Items within titles.

     Each title must have 5 Items requested within it (reporting 5 Total_Item_Requests, 5 Unique_Item_Requests, and 1 Unique_Title_Requests).

     It may not be possible to know which Title the Item being requested belongs to prior to the delivery of the Item. In this case, the titles containing the Item must be noted by the auditor upon request.

     This must result in 50 Total_Item_Requests being reported in the PR_P1 Standard View.

     The Unique_Title_Requests being reported in the PR_P1 Standard View will be determined by the number of unique titles noted by the auditor during the testing.

     *Option 4:* Platform has a single database, which does not include titles.

     The auditor must make 50 requests on items made available to them.

     This must result in 50 Total_Item_Requests and 50 Unique_Item_Requests being reported in the PR_P1 Standard View. The number of Unique_Title_Requests being reported will be 0.
   - Multiple paths should be used to make the requests. When possible, 50% of items requested should be via browsing the platform and 50% via searching. If either browsing to items or accessing items via searching is not possible, then 100% of items requested can be requested via the only available option. The user may think they are browsing a list but are in fact triggering searches. For this reason, requests via browsing may deliver unexpected searches, however the end Item/Title will always be as expected.
   - The auditor must allow at least 31 seconds between each test.
   - A content provider will pass this audit test when the sum of the Total_Item_Requests and Unique_Item_Requests reported by the content provider in PR_P1 Standard View for the auditor’s test account is within a -8% and +3% reliability window of the sum of the searches on the auditor’s report.
  
#. Audit-test P1-3: Total_Item_Requests and Unique_Item_Requests 30-second filters

   - To ensure that the report is counting correctly as per the COUNTER Code of Practice, it is important that the browser cache settings of the machines used for testing are disabled. It is also important that the auditee confirms before the audit period whether or not they operate a cache server. If they do, this test will not report as the Code of Practice expects and is likely to under-report successive searches outside the double-click threshold.
   - The audit test consists of clicking links to an item twice in succession (double-clicks). If the two clicks occur within a 30-second time-span, only the second Total_Item_Requests must be recorded. If the two clicks occur with more than 30 seconds between them, then 2 Total_Item_Requests must be counted. In both cases only 1 Unique_Item_Requests will be reported.
   - The auditor must carry out a total of 30 tests on the platform, and each test will consist of 2 requests. There are 2 types of tests that must be carried out:

     - “Inside” tests (Two identical requests are made, and the second request is made within 30 seconds of the first).
     - “Outside” tests (Two identical requests are made, and the second request is made more than 30 seconds after the first).

     The auditor must carry out 15 inside tests.

     This must result in 15 Total_Item_Requests and 15 Unique_Item_Requests in the PR_P1 Standard View.

     This may not be the case if the content provider operates a cache server.

     The audit must carry out 15 outside tests.

     This must result in 30 Total_Item_Requests and 15 Unique_Item_Requests in the PR_P1 Standard View.

     This may not be the case if the content provider operates a cache server.
   - The auditor must allow at least 31 seconds between each of the 30 tests.
   - A content provider will pass this audit test when the sum of the Total_Item_Requests and Unique_Item_Requests reported by the content provider in PR_P1 Standard View for the auditor’s test account is within a -8% and +3% reliability window of the sum of the Total_Item_Requests and Unique_Item_Requests on the auditor’s report.
  
#. Audit tests P1-1, P1-2 and P1-3 must take place in separate accounts so that each audit-test can be separately reported.


Database Reports
''''''''''''''''

Master Report: DR
.................

The Database Master Report will be COUNTER-compliant if the following Standard Views pass the COUNTER audits and the figures reported within them match what is reported in the Master Report.

Any Standard View that is not applicable to the content provider does not require auditing. This must be agreed prior to the audit by COUNTER.


Standard View: DR_D1
....................

Databases Searches and Item Usage: Reports on key search and request metrics needed to evaluate a database.

An audit of this Standard View requires the following:

#. The auditor must have access to all databases available on the platform of the content provider.
#. Audit-test D1-1: Searches_Regular and Searches_Automated

   - *Option 1:* The content provider offers multiple databases, and it is possible to search over all databases, a selected subset of databases, or a single database.

     The auditor must run 100 searches, including 50 against only 1 selected database, 25 against 2 selected databases, and 25 against all databases (without actively choosing).

     Each of these searches on a single database must report 1 Searches_Regular in the DR_D1 Standard View.

     Each of these searches over 2 databases must report 1 Searches_Regular against each of the selected databases in the DR_D1 Standard View.

     Each of these searches over all databases must report 1 Searches_Automated against each of the databases offered by the content provider in the DR_D1 Standard View.

     *Option 2:* The content provider has multiple databases, and it is possible to search over all databases or a single database.

     The auditor must run 100 searches, including 50 against only 1 selected database and 50 against all databases (without actively choosing).

     Each of these searches on a single database must report 1 Searches_Regular in the DR_D1 Standard View.

     Each of these searches over all databases must report 1 Searches_Automated against each of the databases offered by the content provider in the DR_D1 Standard View.

     *Option 3:* The content provider has a single database.

     The auditor must run 50 searches against the 1 database. Each of these searches must report 1 Searches_Regular in the DR_D1 Standard View.
   - All searches, including those returning 0 results, must be reported as a Searches_Platform in the DR_D1 Standard View.
   - The auditor must allow at least 31 seconds between each search.
   - Each time a search is conducted, the auditor will record the search term, the database searched, and the number of results returned.
   - A content provider will pass this audit test when the sum of the searches reported by the content provider in DR_D1 Standard View for the auditor’s test account is within a -8% and +3% reliability window of the sum of the searches on the auditor’s report.
  
#. Audit-test D1-2: Total_Item_Requests

   - The auditor must make 100 requests on a subset of unique Items made available.

     This must result in 100 Total_Item_Requests reported in the DR_D1 Standard View.
   - Multiple paths should be used to make the requests. When possible, 50% of items requested should be via browsing and 50% via searching. If either browsing to items or accessing items via searching is not possible, then 100% of items requested can be requested via the only available option. The user may think they are browsing a list but in fact be triggering searches. For this reason, making requests via browsing may deliver unexpected searches, however the end Item/Title will always be as expected.
   - The auditor must allow at least 31 seconds between each test.
   - A content provider will pass this audit test when the sum of the Total_Item_Requests reported by the content provider in DR_D1 Standard View for the auditor’s test account is within a -8% and +3% reliability window of the sum of the Total_Item_Requests on the auditor’s report.
  
#. Audit-test D1-3: Total_Item_Requests 30-second filters

   - To ensure that the report is counting correctly as per the COUNTER Code of Practice, it is important that the browser cache settings of the machines used for testing are disabled. It is also important that the auditee confirms before the audit period whether or not they operate a cache server. If they do, this test will not report as the Code of Practice expects and is likely to under-report successive searches outside the double-click threshold.
   - The audit-test consists of making an Item Request twice in succession (double-clicks). If the two clicks occur within a 30-second time-span, only the second Total_Item_Requests must be recorded. If the two clicks occur with more than 30 seconds between them, then 2 Total_Item_Requests must be counted.
   - The auditor must carry out a total of 30 tests, and each test will consist of 2 requests. There are 2 types of tests that must be carried out:

     - “Inside” tests (The 2 requests are made to the same item, and the second request is made within 30 seconds of the first).
     - “Outside” tests (The 2 requests are made to the same item, and the second request is made more than 30 seconds after the first).

     The auditor must carry out 15 inside tests.

     This must result in 15 Total_Item_Requests being reported in the DR_D1 Standard View.

     The audit must carry out 15 outside tests.

     This must result in 30 Total_Item_Requests being reported in the DR_D1 Standard View.

     This may not be the case if the content provider operates a cache server.
   - The auditor must allow at least 31 seconds between each of the 30 tests.
   - A content provider will pass this audit test when the sum of the Total_Item_Requests reported by the content provider in DR_D1 Standard View for the auditor’s test account is within a -8% and +3% reliability window of the sum of the Total_Item_Requests on the auditor’s report.
  
#. Audit-test D1-4: Total_Item_Investigations

   IMPORTANT NOTE: This test does not need to be carried out where the content provider does not offer Investigations that are not also Requests. This must be declared to the auditor and the COUNTER Executive Committee prior to testing.

   - The auditor must make 100 Investigations on a subset of unique Items made available to them.

     This must result in 100 Total_Item_Investigations.
   - Multiple paths should be used to make the Investigations. When possible, 50% of Items Investigations should be via browsing and 50% via searching. If either browsing to item investigations or accessing item investigations via searching is not possible, then 100% of item investigations can be made via the only available option. The user may think they are browsing a list, but in fact be triggering searches. For this reason, investigations made via browsing may deliver unexpected searches, however the end Investigation will always be as expected.
   - The auditor must allow at least 31 seconds between each test.
   - A content provider will pass this audit test when the sum of the Total_Item_Investigations reported by the content provider in DR_D1 Standard View for the auditor’s test account is within a -8% and +3% reliability window of the sum of the Total_Item_Investigations on the auditor’s report.
  
#. Audit-test D1-5: Total_Item_Investigations 30-second filters

   IMPORTANT NOTE: This test does not need to be carried out where the Content provider does not offer Investigations that are not also Requests. This must be declared to the auditor and the COUNTER Executive Committee prior to testing.

   - To ensure that the report is counting correctly as per the COUNTER Code of Practice, it is important that the browser cache settings of the machines used for testing are disabled. It is also important that the auditee confirms before the audit period if they operate a cache server. If they do, this test will not report as the Code of Practice expects and is likely to under-report successive searches outside the double-click threshold.
   - The audit-test consists of making an Item Investigation twice in succession (double-clicks). If the two clicks occur within a 30-second time-span, only the second Total_Item_Investigations made must be recorded. If the two clicks occur with more than 30 seconds between, then 2 Total_Item_Investigations must be counted.
   - The auditor must carry out a total of 30 tests, and each test will consist of 2 item investigations. There are 2 types of tests that must be carried out:

     - “Inside” tests (Two item investigations are made to the same item the second Item Investigation is made within 30 seconds of the first).
     - “Outside” tests (Two item investigations are made to the same item, and the second item investigation is made more than 30 seconds after the first).

     The auditor must carry out 15 inside tests.

     This must result in 15 Total_Item_Investigations being reported in the DR_D1 Standard View.

     The audit must carry out 15 outside tests.

     This must result in 30 Total_Item_Investigations being reported in the DR_D1 Standard View.

     This may not be the case if the content provider operates a cache server.
   - The auditor must allow at least 31 seconds between each of the 30 tests.
   - A content provider will pass this audit test when the sum of the Total_Item_Requests and Total_Item_Investigations reported by the Content provider in DR_D1 Standard View for the auditor’s test account is within a -8% and +3% reliability window of the sum of the Total_Item_Requests and Total_Item_Investigations on the auditor’s report.
  
#. If the content provider does not offer investigations that are not also requests, the following figure being reported as a result of the D3-1 and D3-2 audit tests must match in the DR_D1 Standard View:

   Total_Item_Requests must match Total_Item_Investigations
#. Audit tests D1-1, D1-2 and D1-3, D1-4 and DB1-5 must take place in separate accounts so that each audit test can be separately reported.


Standard View: DR_D2
....................

Databases Access Denied: Reports on access-denied activity for databases where users were denied access because simultaneous-user licenses were exceeded, or their institution did not have a license for the database.

An audit of this Standard View requires the following:

#. Audit-test D2-1: Limit_Exceeded

   IMPORTANT NOTE: This test cannot be carried out if the content provider does not offer a concurrent/simultaneous user limit. This must be declared to the auditor and the COUNTER Executive Committee prior to testing.

   - The account used for this testing must have concurrent/simultaneous-user limit set, and the number of registered users concurrently allowed must be declared by the content provider prior to the testing. Ideally the account should allow a single active user on the site requesting access to the database. This means that a second user accessing the database would be turned away.
   - *Option 1:* The content provider turns the user away when the concurrent/simultaneous-user limit is exceeded upon login.

     The auditor will log into the site. This means that the user limit is at maximum active users.

     The auditor will then attempt to log into the site using a different computer. The auditor should then be refused access because of exceeding the concurrent/simultaneous-user limit. Each time access is refused, the auditor will record this as Limit_Exceeded.

     The auditor must force 50 Limit_Exceeded turnaways during testing.

     Each of these concurrent/simultaneous turnaways must report 1 Limit_Exceeded in the DR_D2 Standard View.

     *Option 2:* The content provider turns the user away when the concurrent/simultaneous user limit is exceeded upon searching or accessing a database.

     The auditor will log into the site. This means that the user limit is at maximum active users. The user will then select and make a search on a database (or browse to a database).

     The auditor will then log into the site using a different computer. The auditor will then repeat the action made on the previous computer (select and make a search on a database or browse to a database). After the search has been made (or database browsed to) the user should then be refused access because of exceeding the concurrent/simultaneous-user limit. Each time access is refused, the auditor will record this as Limit_Exceeded.

     The auditor must force 50 Limit_Exceeded turnaways during testing.

     Each of these concurrent/simultaneous turnaways must report 1 Limit_Exceeded in the DR_D2 Standard View.

     *Option 3:* The content provider turns the user away when the concurrent/simultaneous-user limit is exceeded upon accessing an Item within a database.

     The auditor will log into the site. This means that the user limit is at maximum active users. The user will then navigate to and request an Item.

     The auditor will then log into the site using a different computer. The auditor will then repeat the action made on the previous computer (navigate to and request an Item). After the Item has been requested the user should then be refused access because of exceeding the concurrent/simultaneous-user limit. Each time access is refused, the auditor will record this as Limit_Exceeded.

     The auditor must force 50 Limit_Exceeded turnaways during testing.

     Each of these concurrent/simultaneous turnaways must report 1 Limit_Exceeded in the DR_D2 Standard View.
   - The auditor must allow at least 31 seconds between each search.
   - Each time a turnaway is made, the auditor will record the database on which the turnaway was produced. (In the case of turning away at log in, the database will be All).
   - A content provider will pass this audit test when the sum of the turnaways reported by the content provider in DR_D2 Standard View for the auditor’s test account is within a -8% and +3% reliability window of the sum of the turnaways on the auditor’s report.
  
#. Audit-test D2-2: No_License

   IMPORTANT NOTE: This test cannot be carried out if the content provider does not restrict site content or if restricted content is not displayed. This must be declared to the auditor and the COUNTER Executive Committee prior to testing.

   - The account used for this testing must have restricted access to content, and the content for which the user has no license to access must be declared by the content provider prior to the testing. Alternatively, the content provider may declare the content that the user does have license to access.
   - The auditor will attempt to access content to which the account being used does not have access. Each time access is refused, the auditor will record No_License.

     The auditor must force 50 No_License turnaways during testing.

     Each of these “No License” turnaways must report 1 No_License in the DR_D2 Standard View.
   - The auditor must allow at least 31 seconds between each search.
   - Each time a turnaway is made, the auditor will record the database on which the turnaway was produced.
   - A content provider will pass this audit test when the sum of the turnaways reported by the content provider in DR_D2 Standard View for the auditor’s test account is within a -8% and +3% reliability window of the sum of the turnaways on the auditor’s report.
  
#. Audit tests D2-1 and D2-2 must take place in separate accounts so that each audit test can be separately reported.


Title Reports
'''''''''''''

Master Report: TR
.................

The Title Master Report will be COUNTER-compliant if the following Standard Views pass the COUNTER audits and the figures reported within them match what is reported in the Master Report.

Any Standard View that is not applicable to the content provider does not require auditing, this must be agreed prior to the audit by COUNTER.


Standard View: TR_B1
....................

Book Requests (excluding OA_Gold): Reports on full-text activity for non-Gold open access books as Total_Item_Requests and Unique_Title_Requests. The Unique_Title_Requests view provides comparable usage across book platforms. The Total_Item_Requests view shows overall activity; however, numbers between sites will vary significantly based on how the content is delivered (e.g. delivered as a complete book or by chapter.)

An audit of this Standard View requires the following:

#. The auditor must have access to all book content available by the content provider.
#. The Access_Type for all requests must be Controlled and not OA_Gold.
#. Audit-test B1-1: Total_Item_Requests and Unique_Title_Requests

   - The auditor must make a total of 100 requests on a subset of unique Items within book titles.

     Each title must have 5 Items requested within it (reporting 5 Total_Item_Requests and 1 Unique_Title_Requests).

     This must result in 100 Total_Item_Requests being reported in the TR_B1 Standard View.

     This must result in 20 Unique_Title_Requests being reported in the TR_B1 Standard View.
   - The auditor must allow at least 31 seconds between each test.
   - A content provider will pass this audit test when the sum of the Total_Item_Requests and Unique_Title_Requests reported by the content provider in TR_B1 Standard View for the auditor’s test account is within a -8% and +3% reliability window of the sum of the Total_Item_Requests and Unique_Title_Requests on the auditor’s report.
  
#. Audit-test B1-2: Total_Item_Requests and Unique_Title_Requests 30-second filters

   - To ensure that the report is counting correctly as per the COUNTER Code of Practice, it is important that the browser cache settings of the machines used for testing are disabled. It is also important that the auditee confirms before the audit period whether or not they operate a cache server. If they do, this test will not report as the Code of Practice expects and is likely to under-report successive searches outside the double-click threshold.
   - The audit test consists of clicking links to an Item within a book title twice in succession (double-clicks). If the two clicks occur within a 30-second time-span, only the second Total_Item_Requests must be recorded. If the two clicks occur with more than 30 seconds between, then 2 Total_Item_Requests must be counted. In both cases only 1 Unique_Title_Requests will be reported.
   - The auditor must carry out a total of 32 test, and each test will consist of 2 requests. There are 2 types of tests that must be carried out:

     - “Inside” tests (Two requests are made to the same Item, and the second request is made within 30 seconds of the first).
     - “Outside” tests (Two requests are made to the same Item and the second request is made more than 30 seconds after the first).

     The auditor must carry out 16 inside tests.

     Where possible, each title must have 2 Item tests within it (reporting 1 Total_Item_Requests and 1 Unique_Title_Requests).

     This must result in 16 Total_Item_Requests and 8 Unique_Title_Requests in the TR_B1 Standard View.

     This may not be the case if the content provider operates a cache server.

     The audit must carry out 16 outside tests.

     Where possible, each title must have 2 Items requested within it (reporting 2 Total_Item_Requests and 1 Unique_Title_Requests).

     This must result in 30 Total_Item_Requests and 8 Unique_Title_Requests in the TR_B1 Standard View.

     This may not be the case if the content provider operates a cache server.
   - The auditor must allow at least 32 seconds between each of the 30 tests.
   - A Content provider will pass this audit test when the sum of the Total_Item_Requests and Unique_Title_Requests reported by the Content provider in TR_B1 Standard View for the auditor’s test account is within a -8% and +3% reliability window of the sum of the Total_Item_Requests and Unique_Title_Requests on the auditor’s report.
  
#. Audit tests B1-1 and B1-2 must take place in separate accounts so that each audit test can be separately reported.


Standard View: TR_B2
....................

Book Access Denied: Reports on access denied activity for books where users were denied access because simultaneous-user licenses were exceeded, or their institution did not have a license for the book.

An audit of this Standard View requires the following:

#. Audit-test B2-1: Limit_Exceeded

   IMPORTANT NOTE: This test cannot be carried out if the content provider does not offer a concurrent/simultaneous user limit. This must be declared to the auditor and the COUNTER Executive Committee prior to testing.

   - The account used for this testing must have concurrent/simultaneous-user limit set for book title/items and the number of registered users concurrently allowed must be declared by the content provider prior to the testing. Ideally the account should allow a single active user to access books. (This means that a second user accessing books will be turned away).
   - The content provider turns the user away when the concurrent/simultaneous-user limit is exceeded for books.
   - The auditor will log into the site and access a book item, this means that the user limit is at maximum active users.

     The auditor will then log into the site using a different computer. The auditor will then repeat the action made on the previous computer (access a book item). After the item has been requested the user should then be refused access because of exceeding the concurrent/simultaneous user limit. Each time access is refused, the auditor will record this as Limit_Exceeded.

     The auditor must force 50 Limit_Exceeded turnaways during testing.

     Each of these concurrent/simultaneous turnaways must report 1 Limit_Exceeded in the TR_B2 Standard View.
   - The auditor must allow at least 31 seconds between each request.
   - A content provider will pass this audit test when the sum of the Limit_Exceeded turnaways reported by the content provider in TR_B2 Standard View for the auditor’s test account is within a -8% and +3% reliability window of the sum of the Limit_Exceeded turnaways on the auditor’s report.
  
#. Audit-test B2-2: No_License

   IMPORTANT NOTE: This test cannot be carried out if the content provider does not restrict site content or where restricted content is not displayed. This must be declared to the auditor and the COUNTER Executive Committee prior to testing.

   - The account used for this testing must have restricted access to book content, and the book content that the user has no license to access must be declared by the content provider prior to the testing. Alternatively, the content provider may declare the content to which the user does have license to access.
   - The auditor will attempt to access book content that the account being used does not have access to. Each time access is refused, the auditor will record No_License.
   - The auditor must force 50 No_License during testing.

     Each of these Book content not licensed turnaways must report 1 No_License in the TR_B2 Standard View.
   - The auditor must allow at least 31 seconds between each search.
   - A content provider will pass this audit test when the sum of the No_License turnaways reported by the content provider in TR_B2 Standard View for the auditor’s test account is within a -8% and +3% reliability window of the sum of the No_License turnaways on the auditor’s report.
  
#. Audit tests B2-1 and B2-2 must take place in separate accounts so that each audit test can be separately reported.


Standard View: TR_B3
....................

Book Usage by Access Type: Reports on book usage showing all applicable metric types broken down by Access_Type

An audit of this Standard View requires the following:

#. The auditor must have access to all book content available by the content provider.
#. Audit-test B3-1: Total_Item_Requests, Unique_Item_Requests and Unique_Title_Requests

   - *Option 1:* content provider offers OA_Gold Items in addition to Controlled.

     The auditor must make a total of 100 requests on a subset of unique Items within book titles (50 requests to book Items where the Access_Type is Controlled, and 50 requests to book items where the Access_Type is OA_Gold).

     Each title must have 5 items requested within it (reporting 5 Total_Item_Requests, 5 Unique_Item_Requests and 1 Unique_Title_Requests).

     This must result in 50 OA_Gold Total_Item_Requests and 50 Controlled Total_Item_Requests being reported in the TR_B3 Standard View.

     This must result in 50 OA_Gold Unique_Item_Requests and 50 Controlled Unique_Item_Requests being reported in the TR_B3 Standard View.

     This must result in 10 OA_Gold Unique_Title_Requests and 10 Controlled Unique_Title_Requests being reported in the TR_B3 Standard View.

     *Option 2:* Content provider does not offer OA_Gold items.

     The auditor must make a total of 100 requests on a subset of unique Items within book titles.

     Where possible, each title must have 5 items requested within it (reporting 5 Total_Item_Requests, 5 Unique_Item_Requests, and 1 Unique_Title_Requests).

     This must result in 100 Controlled Total_Item_Requests being reported in the TR_B3 Standard View.

     This must result in 100 Controlled Unique_Item_Requests being reported in the TR_B3 Standard View.

     This must result in 20 Controlled Unique_Title_Requests being reported in the TR_B3 Standard View.
   - The auditor must allow at least 31 seconds between each test.
   - A content provider will pass this audit test when the sum of the Total_Item_Requests, Unique_Item_Requests, and Unique_Title_Requests reported by the content provider in TR_B3 Standard View for the auditor’s test account is within a -8% and +3% reliability window of the sum of the Total_Item_Requests, Unique_Item_Requests, and Unique_Title_Requests on the auditor’s report.
  
#. Audit-test B3-2: Total_Item_Requests, Unique_Item_Requests and Unique_Title_Requests 30-second filters

   - To ensure that the report is counting correctly as per the COUNTER Code of Practice, it is important that the browser cache settings of the machines used for testing are disabled. It is also important that the auditee confirms before the audit period whether or not they operate a cache server. If they do, this test will not report as the Code of Practice expects and is likely to under-report successive searches outside the double-click threshold.
   - The audit-test consists of clicking links to an Item within a book title twice in succession (double-clicks). If the two clicks occur within a 30-second time-span, only the second Total_Item_Requests must be recorded. If the two clicks occur with more than 30 seconds between, then 2 Total_Item_Requests must be counted. In both cases only 1 Unique_Item_Requests and Unique_Title_Requests will be reported.
   - *Option 1:* Content provider offers OA_Gold items in addition to Controlled items.

     The auditor must carry out a total of 32 tests, and each test will consist of 2 requests. There are 2 types of tests that must be carried out:

     - “Inside” tests (Two requests are made to the same book item, and the second request is made within 30 seconds of the first).
     - “Outside” tests (Two requests are made to the same book item, and the second request is made over 30 seconds after the first).

     The auditor must carry out 16 inside tests (8 tests to book items where the Access_Type is Controlled and 8 tests to book items where the Access_Type is OA_Gold).

     Where possible, each title must have 2 book item tests within it (reporting 2 Total_Item_Requests, 2 Unique_Item_Requests, and 1 Unique_Title_Requests).

     This must result in 8 Controlled Total_Item_Requests and 8 OA_Gold Total_Item_Requests in the TR_B3 Standard View.

     This must result in 8 Controlled Unique_Item_Requests and 8 OA_Gold Unique_Item_Requests in the TR_B3 Standard View.

     This must result in 4 Controlled Unique_Title_Requests and 4 OA_Gold Unique_Title_Requests in the TR_B3 Standard View.

     (This may not be the case if the content provider operates a cache server.)

     The auditor must carry out 16 outside tests (8 tests to book items where the Access_Type is Controlled and 8 tests to book items where the Access_Type is OA_Gold).

     Where possible, each title must have 2 book item tests within it (reporting 4 Total_Item_Requests, 2 Unique_Item_Requests, and 1 Unique_Title_Requests).

     This must result in 16 Controlled Total_Item_Requests and 16 OA_Gold Total_Item_Requests in the TR_B3 Standard View.

     This must result in 8 Controlled Unique_Item_Requests and 8 OA_Gold Unique_Item_Requests in the TR_B3 Standard View.

     This must result in 4 Controlled Unique_Title_Requests and 4 OA_Gold Unique_Title_Requests in the TR_B3 Standard View.

     (This may not be the case if the content provider operates a cache server.)

     *Option 2:* Content provider does not offer OA_Gold Items.

     The auditor must carry out a total of 32 tests, and each test will consist of 2 requests. There are 2 types of tests that must be carried out:

     - “Inside” tests (Two requests are made to the same book item and the second request is made within 30 seconds of the first).
     - “Outside” tests (Two requests are made to the same book item, and the second request is made over 30 seconds after the first).

     The auditor must carry out 16 inside tests.

     Where possible, each title must have 2 book item tests within it (reporting 2 Total_Item_Requests and 2 Unique_Item_Requests and 1 Unique_Title_Requests).

     This must result in 16 Controlled Total_Item_Requests in the TR_B3 Standard View.

     This must result in 16 Controlled Unique_Item_Requests in the TR_B3 Standard View.

     This must result in 8 Controlled Unique_Title_Requests in the TR_B3 Standard View.

     (This may not be the case if the Content provider operates a cache server.)

     The auditor must carry out 16 outside tests.

     Each title must have 2 book item tests within it (reporting 4 Total_Item_Requests, 2 Unique_Item_Requests, and 1 Unique_Title_Requests).

     This must result in 32 Controlled Total_Item_Requests in the TR_B3 Standard View.

     This must result in 16 Controlled Unique_Item_Requests in the TR_B3 Standard View.

     This must result in 8 Controlled Unique_Title_Requests in the TR_B3 Standard View.

     (This may not be the case if the content provider operates a cache server.)
   - The auditor must allow at least 31 seconds between each of the 30 tests.
   - A content provider will pass this audit test when the sum of the Total_Item_Requests, Unique_Item_Requests, and Unique_Title_Requests reported by the content provider in TR_B3 Standard View for the auditor’s test account is within a -8% and +3% reliability window of the sum of the Total_Item_Requests, Unique_Item_Requests, and Unique_Title_Requests on the auditor’s report.
  
#. Audit-test B3-3: Total_Item_Investigations, Unique_Item_Investigations, and Unique_Title_Investigations

   IMPORTANT NOTE: This test does not need to be carried out if the content provider does not offer investigations that are not also requests. This must be declared to the auditor and the COUNTER Executive Committee prior to testing.

   - *Option 1:* Content provider offers OA_Gold Items in addition to Controlled.

     The auditor must make a total of 50 item investigations within a subset of book titles (25 Investigations of items within a book where the Access_Type is Controlled, and 25 investigations of items within a book where the Access_Type is OA_Gold).

     Each title must have 5 investigations to unique Items within it (reporting 5 Total_Item_Investigations, 5 Unique_Item_Investigations, and 1 Unique_Title_Investigations).

     This must result in 25 OA_Gold Total_Item_Investigations and 25 Controlled Total_Item_Investigations being reported in the TR_B3 Standard View.

     This must result in 25 OA_Gold Unique_Item_Investigations and 25 Controlled Unique_Item_Investigations being reported in the TR_B3 Standard View.

     This must result in 5 OA_Gold Unique_Title_Investigations and 5 Controlled Unique_Title_Investigations being reported in the TR_B3 Standard View.

     *Option 2:* Content provider does not offer OA_Gold Items.

     The auditor must make a total of 50 Investigations within a subset of book titles.

     Each title must have 5 investigations to unique items within it (reporting 5 Total_Item_Investigations, 5 Unique_Item_Investigations, and 1 Unique_Title_Investigations).

     This must result in 50 Controlled Total_Item_Investigations being reported in the TR_B3 Standard View.

     This must result in 50 Controlled Unique_Item_Investigations being reported in the TR_B3 Standard View.

     This must result in 10 Controlled Unique_Title_Investigations being reported in the TR_B3 Standard View.
   - The auditor must allow at least 31 seconds between each test.
   - A content provider will pass this audit test when the sum of the Total_Item_Investigations, Unique_Item_Investigations, and Unique_Title_Investigations reported by the content provider in TR_B3 Standard View for the auditor’s test account is within a -8% and +3% reliability window of the sum of the Total_Item_Investigations, Unique_Item_Investigations, and Unique_Title_Investigations on the auditor’s report.
  
#. Audit test B3-4: Total_Item_Investigations, Unique_Item_Investigations, and Unique_Title_Investigations 30-second filters

   IMPORTANT NOTE: This test does not need to be carried out if the content provider does not offer investigations that are not also requests. This must be declared to the auditor and the COUNTER Executive Committee prior to testing.

   - To ensure that the report is counting correctly as per the COUNTER Code of Practice, it is important that the browser cache settings of the machines used for testing are disabled. It is also important that the auditee confirms before the audit period whether or not they operate a cache server. If they do, this test will not report as the Code of Practice expects and is likely to under-report successive searches outside the double-click threshold.
   - The audit test consists of clicking links to an investigation of an item within a book title twice in succession (double-clicks). If the two clicks occur within a 30-second time-span, only the second Total_Item_Investigations must be recorded. If the two clicks occur with more than 30 seconds between, then 2 Total_Item_Investigations must be counted. In both cases only 1 Unique_Item_Investigations and Unique_Title_Investigations will be reported.
   - *Option 1:* Content provider offers OA_Gold Items in addition to Controlled.

     The auditor must carry out a total of 32 tests, and each test will consist of 2 item investigations. There are 2 types of tests that must be carried out:

     - “Inside” tests (Two investigations are made to the same book item, and the second investigation is made within 30 seconds of the first).
     - “Outside” tests (Two investigations are made to the same book item, and the second investigation is made more than 30 seconds after the first).

     The auditor must carry out 16 inside tests (8 Investigations to book items where the Access_Type is Controlled and 8 investigations to book items where the Access_Type is OA_Gold).

     Each title must have 2 book item tests within it (reporting 2 Total_Item_Investigations, 2 Unique_Item_Investigations, and 1 Unique_Item_Investigations).

     This must result in 8 Controlled Total_Item_Investigations and 8 OA_Gold Total_Item_Investigations in the TR_B3 Standard View.

     This must result in 8 Controlled Unique_Item_Investigations and 8 OA_Gold Unique_Item_Investigations in the TR_B3 Standard View.

     This must result in 4 Controlled Unique_Title_Investigations and 4 OA_Gold Unique_Title_Investigations in the TR_B3 Standard View.

     This may not be the case if the content provider operates a cache server.

     The auditor must carry out 16 outside tests (8 tests to book items where the Access_Type is Controlled and 8 tests to book items where the Access_Type is OA_Gold).

     Each title must have 2 book item tests within it (reporting 4 Total_Item_Investigations, 2 Unique_Item_Investigations, and 1 Unique_Title_Investigations).

     This must result in 16 Controlled Total_Item_Investigations and 16 OA_Gold Total_Item_Investigations in the TR_B3 Standard View.

     This must result in 8 Controlled Unique_Item_Investigations and 8 OA_Gold Unique_Item_Investigations in the TR_B3 Standard View.

     This must result in 4 Controlled Unique_Title_Investigations and 4 OA_Gold Unique_Title_Investigations in the TR_B3 Standard View.

     This may not be the case if the content provider operates a cache server.

     *Option 2:* Content provider does not offer OA_Gold items.

     The auditor must carry out a total of 32 tests, and each test will consist of 2 item investigations. There are 2 types of tests that must be carried out:

     - “Inside” tests (Two investigations are made to the same book item, and the second investigation is made within 30 seconds of the first).
     - “Outside” tests (Two investigations are made to the same book item, and the second investigation is made more than 30 seconds after the first).

     The auditor must carry out 16 inside tests.

     Each title must have 2 book item tests within it (reporting 2 Total_Item_Investigations, 2 Unique_Item_Investigations, and 1 Unique_Title_Investigations).

     This must result in 16 Controlled Total_Item_Investigations in the TR_B3 Standard View.

     This must result in 16 Controlled Unique_Item_Investigations in the TR_B3 Standard View.

     This must result in 8 Controlled Unique_Title_Investigations in the TR_B3 Standard View.

     This may not be the case if the content provider operates a cache server.

     The auditor must carry out 16 outside tests.

     Each title must have 2 book item tests within it (reporting 4 Total_Item_Investigations, 2 Unique_Item_Investigations, and 1 Unique_Title_Investigations).

     This must result in 32 Controlled Total_Item_Investigations in the TR_B3 Standard View.

     This must result in 16 Controlled Unique_Item_Investigations in the TR_B3 Standard View.

     This must result in 8 Controlled Unique_Title_Investigations in the TR_B3 Standard View.

     This may not be the case if the content provider operates a cache server.
   - The auditor must allow at least 31 seconds between each of the 30 tests.
   - A content provider will pass this audit test when the sum of the Total_Item_Investigations, Unique_Item_Investigations, and Unique_Title_Investigations reported by the content provider in TR_B3 Standard View for the auditor’s test account is within a -8% and +3% reliability window of the sum of the Total_Item_Investigations, Unique_Item_Investigations, and Unique_Title_Investigations on the auditor’s report.
  
#. If the content provider does not offer Investigations that are not also requests, the following figure being reported as a result of the B3-1 and B3-2 audit tests must match in the TR_B3 Standard View:

   Total_Item_Requests must match Total_Item_Investigations

   Unique_Item_Requests must match Unique_Item_Investigations

   Unique_Title_Requests must match Unique_Title_Investigations
#. Audit tests B3-1, B3-2, B3-3, and B3-4 must take place in separate accounts so that each audit test can be separately reported.


Standard View: TR_J1
....................

Journal Requests (excluding OA_Gold): Reports on usage of non-Gold open access journal content as Total_Item_Requests and Unique_Item_Requests. The Unique_Item_Requests provides comparable usage across journal platform by reducing the inflationary effect that occurs when an HTML full text automatically displays and the user then accesses the PDF version. The Total_Item_Requests shows overall activity.

An audit of this Standard View requires the following:

#. The auditor must have access to all journal content available by the content provider.
#. The Access_Type for all requests must be Controlled and not OA_Gold.
#. Audit-test J1-1: Total_Item_Requests and Unique_Item_Requests

   - The auditor must make a total of 100 requests on a subset of unique Journal Items.

     This must result in 100 Total_Item_Requests being reported in the TR_J1 Standard View.

     This must result in 100 Unique_Item_Requests being reported in the TR_J1 Standard View.
   - The auditor must allow at least 31 seconds between each test.
   - A content provider will pass this audit test when the sum of the Total_Item_Requests and Unique_Item_Requests reported by the content provider in TR_J1 Standard View for the auditor’s test account is within a -8% and +3% reliability window of the sum of the Total_Item_Requests and Unique_Item_Requests on the auditor’s report.
  
#. Audit-test J1-2: Total_Item_Requests and Unique_Item_Requests 30-second filters

   - To ensure that the report is counting correctly as per the COUNTER Code of Practice, it is important that the browser cache settings of the machines used for testing are disabled. It is also important that the auditee confirms before the audit period whether or not they operate a cache server. If they do, this test will not report as the Code of Practice expects and is likely to under-report successive searches outside the double-click threshold.
   - The audit-test consists of clicking links to a journal item twice in succession (double-clicks). If the two clicks occur within a 30-second time-span, only the second Total_Item_Requests must be recorded. If the two clicks occur with more than 30 seconds between, then 2 Total_Item_Requests must be counted. In both cases only 1 Unique_Item_Requests will be reported.
   - The auditor must carry out a total of 30 tests, and each test will consist of 2 requests. There are 2 types of tests that must be carried out:

     - “Inside” tests (Two requests are made to the same journal item, and the second request is made within 30 seconds of the first).
     - “Outside” tests (Two requests are made to the same journal item, and the second request is made over 30 seconds after the first).

     The auditor must carry out 15 inside tests.

     This must result in 15 Total_Item_Requests and 15 Unique_Item_Requests in the TR_J1 Standard View.

     This may not be the case if the content provider operates a cache server.

     The audit must carry out 15 outside tests.

     This must result in 30 Total_Item_Requests and 15 Unique_Item_Requests in the TR_J1 Standard View.

     This may not be the case if the content provider operates a cache server.
   - The auditor must allow at least 31 seconds between each of the 30 tests.
   - A content provider will pass this audit test when the sum of the Total_Item_Requests and Unique_Item_Requests reported by the content provider in TR_J1 Standard View for the auditor’s test account is within a -8% and +3% reliability window of the sum of the Total_Item_Requests and Unique_Item_Requests on the auditor’s report.
  
#. Audit tests J1-1 and J1-2 must take place in separate accounts so that each audit test can be separately reported.


Standard View: TR_J2
....................

Journal Accessed Denied: Reports on Access Denied activity for journal content where users were denied access because simultaneous-user licenses were exceeded, or their institution did not have a license for the title.

An audit of this Standard View requires the following:

#. Audit-test J2-1: Limit_Exceeded

   IMPORTANT NOTE: This test cannot be carried out where the content provider does not offer a concurrent/simultaneous-user limit. This must be declared to the auditor and the COUNTER Executive Committee prior to testing.

   - The account used for this testing must have a concurrent/simultaneous-user limit set for journal items, and the number of registered users concurrently allowed must be declared by the content provider prior to the testing. Ideally, the account should allow a single active user to access journals. This means that a second user accessing journals will be turned away.
   - The content provider turns the user away when the concurrent/simultaneous-user limit is exceeded for journals.

     The auditor will log into the site and access a journal item. This means that the user limit is at maximum active users.

     The auditor will then log into the site using a different computer. The auditor will then repeat the action made on the previous computer (access a journal item). After the Item has been requested, the user should then be refused access because of exceeding the concurrent/simultaneous-user limit. Each time access is refused, the auditor will record this as Limit_Exceeded.

     The auditor must force 50 Limit_Exceeded turnaways during testing.

     Each of these concurrent/simultaneous turnaways must report 1 Limit_Exceeded in the TR_J2 Standard View.
   - The auditor must allow at least 31 seconds between each request.
   - A content provider will pass this audit test when the sum of the Limit_Exceeded turnaways reported by the content provider in TR_J2 Standard View for the auditor’s test account is within a -8% and +3% reliability window of the sum of the Limit_Exceeded turnaways on the auditor’s report.
  
#. Audit-test J2-2: No_License

   IMPORTANT NOTE: This test cannot be carried out if the content provider does not restrict site content or where restricted content is not displayed. This must be declared to the auditor and the COUNTER Executive Committee prior to testing.

   - The account used for this testing must have restricted access to journal content, and the journal content that the user has no license to access must be declared by the content provider prior to the testing. Alternatively, the content provider may declare the content that the user does have license to access.
   - The auditor will attempt to access journal content that the account being used does not have access to. Each time access is refused, the auditor will record No_License.

     The auditor must force 50 No_License turnaways during testing.

     Each of these journal content not licensed turnaways must report 1 No_License in the TR_J2 Standard View.
   - The auditor must allow at least 31 seconds between each search.
   - A content provider will pass this audit test when the sum of the No_License turnaways reported by the content provider in TR_J2 Standard View for the auditor’s test account is within a -8% and +3% reliability window of the sum of the No_License turnaways on the auditor’s report.
  
#. Audit tests J2-1 and J2-2 must take place in separate accounts so that each audit test can be separately reported.


Standard View: TR_J3
....................

Journal Usage by Access Type: Reports on usage of journal content for all metric types broken down by access type.

An audit of this Standard View requires the following:

#. The auditor must have access to all journal content available by the content provider.
#. Audit-test J3-1: Total_Item_Requests and Unique_Item_Requests

   - *Option 1:* Content provider offers OA_Gold items in addition to Controlled.

     The auditor must make a total of 100 requests on a subset of unique journal Items (50 requests to journal Items where the Access_Type is Controlled and 50 requests to journal items where the Access_Type is OA_Gold).

     This must result in 50 OA_Gold Total_Item_Requests and 50 Controlled Total_Item_Requests being reported in the TR_J3 Standard View.

     This must result in 50 OA_Gold Unique_Item_Requests and 50 Controlled Unique_Item_Requests being reported in the TR_J3 Standard View.

     *Option 2:* Content provider does not offer OA_Gold Items.

     The auditor must make a total of 100 requests on a subset of unique journal Items.

     This must result in 100 Controlled Total_Item_Requests being reported in the TR_J3 Standard View.

     This must result in 100 Controlled Unique_Item_Requests being reported in the TR_J3 Standard View.
   - The auditor must allow at least 31 seconds between each test.
   - A content provider will pass this audit test when the sum of the Total_Item_Requests and Unique_Item_Requests reported by the content provider in TR_J3 Standard View for the auditor’s test account is within a -8% and +3% reliability window of the sum of the Total_Item_Requests and Unique_Item_Requests on the auditor’s report.
  
#. Audit-test J3-2: Total_Item_Requests and Unique_Item_Requests 30-second filters

   - To ensure that the report is counting correctly as per the COUNTER Code of Practice, it is important that the browser cache settings of the machines used for testing are disabled. It is also important that the auditee confirms before the audit period whether or not they operate a cache server. If they do, this test will not report as the Code of Practice expects and is likely to under-report successive searches outside the double-click threshold.
   - The audit-test consists of clicking links to a journal item twice in succession (double-clicks). If the two clicks occur within a 30-second time-span, only the second Total_Item_Requests must be recorded. If the two clicks occur with more than 30 seconds between them, then 2 Total_Item_Requests must be counted. In both cases only 1 Unique_Item_Requests will be reported.
   - *Option 1:* Content provider offers OA_Gold Items in addition to Controlled.

     The auditor must carry out a total of 30 tests, and each test will consist of 2 requests. There are 2 types of tests that must be carried out:

     - “Inside” tests (Two requests are made to the same journal item, and the second request is made within 30 seconds of the first).
     - “Outside” tests (Two requests are made to the same journal item and the second request is made over 30 seconds after the first).

     The auditor must carry out 15 inside tests (8 tests to journal items where the Access_Type is Controlled and 7 tests to journal items where the Access_Type is OA_Gold).

     This must result in 8 Controlled Total_Item_Requests and 7 OA_Gold Total_Item_Requests in the TR_J3 Standard View.

     This must result in 8 Controlled Unique_Item_Requests and 7 OA_Gold Unique_Item_Requests in the TR_J3 Standard View.

     This may not be the case if the content provider operates a cache server.

     The auditor must carry out 15 outside tests (8 tests to journal items where the Access_Type is Controlled and 7 tests to journal items where the Access_Type is OA_Gold).

     This must result in 16 Controlled Total_Item_Requests and 14 OA_Gold Total_Item_Requests in the TR_J3 Standard View.

     This must result in 8 Controlled Unique_Item_Requests and 7 OA_Gold Unique_Item_Requests in the TR_J3 Standard View.

     This may not be the case if the content provider operates a cache server.

     *Option 2:* Content provider does not offer OA_Gold Items.

     The auditor must carry out a total of 30 tests, and each test will consist of 2 requests. There are 2 types of tests that must be carried out:

     - “Inside” tests (Two requests are made to the same journal item, and the second request is made within 30 seconds of the first).
     - “Outside” tests (Two requests are made to the same journal item, and the second request is made more than 30 seconds after the first).

     The auditor must carry out 15 inside tests.

     This must result in 15 Controlled Total_Item_Requests in the TR_J3 Standard View.

     This must result in 15 Controlled Unique_Item_Requests in the TR_J3 Standard View.

     This may not be the case if the content provider operates a cache server.

     The auditor must carry out 15 outside tests.

     This must result in 30 Controlled Total_Item_Requests in the TR_J3 Standard View.

     This must result in 15 Controlled Unique_Item_Requests in the TR_J3 Standard View.

     This may not be the case if the content provider operates a cache server.
   - The auditor must allow at least 31 seconds between each of the 30 tests.
   - A content provider will pass this audit test when the sum of the Total_Item_Requests and Unique_Item_Requests reported by the content provider in TR_J3 Standard View for the auditor’s test account is within a -8% and +3% reliability window of the sum of the Total_Item_Requests and Unique_Item_Requests on the auditor’s report.
  
#. Audit-test J3-3: Total_Item_Investigations and Unique_Item_Investigations

   - *Option 1:* Content provider offers OA_Gold Items in addition to Controlled.

     The auditor must make a total of 50 investigations to a subset of unique journal items (25 Investigations of journal items where the Access_Type is Controlled and 25 Investigations of journal items where the Access_Type is OA_Gold).

     This must result in 25 OA_Gold Total_Item_Investigations and 25 Controlled Total_Item_Investigations being reported in the TR_J3 Standard View.

     This must result in 25 OA_Gold Unique_Item_Investigations and 25 Controlled Unique_Item_Investigations being reported in the TR_J3 Standard View.

     *Option 2:* Content provider does not offer OA_Gold Items.

     The auditor must make a total of 50 investigations to a subset of unique Journal Items.

     This must result in 50 Controlled Total_Item_Investigations being reported in the TR_J3 Standard View.

     This must result in 50 Controlled Unique_Item_Investigations being reported in the TR_J3 Standard View.
   - The auditor must allow at least 31 seconds between each test.
   - A content provider will pass this audit test when the sum of the Total_Item_Investigations and Unique_Item_Investigations reported by the content provider in TR_J3 Standard View for the auditor’s test account is within a -8% and +3% reliability window of the sum of the Total_Item_Investigations and Unique_Item_Investigations on the auditor’s report.
  
#. Audit-test J3-4: Total_Item_Investigations and Unique_Item_Investigations 30-second filters

   - To ensure that the report is counting correctly as per the COUNTER Code of Practice, it is important that the browser cache settings of the machines used for testing are disabled. It is also important that the auditee confirms before the audit period whether or not they operate a cache server. If they do, this test will not report as the Code of Practice expects and is likely to under-report successive searches outside the double-click threshold.
   - The audit-test consists of clicking links to an Investigation of a Journal Item twice in succession (double-clicks). If the two clicks occur within a 30-second time-span, only the second Total_Item_Requests must be recorded. If the two clicks occur with more than 30 seconds between them, then 2 Total_Item_Requests must be counted. In both cases only 1 Unique_Item_Requests and Unique_Title_Requests will be reported.
   - *Option 1:* Content provider offers OA_Gold Items in addition to Controlled.

     The auditor must carry out a total of 30 tests, and each test will consist of 2 Investigations. There are 2 types of tests that must be carried out:

     - “Inside” tests (Two investigations are made to the same journal item, and the second investigation is made within 30 seconds of the first).
     - “Outside” tests (Two investigations are made to the same journal item, and the second investigation is made more than 30 seconds after the first).

     The auditor must carry out 15 inside tests (8 tests to journal items where the Access_Type is Controlled and 7 tests to journal items where the Access_Type is OA_Gold).

     This must result in 8 Controlled Total_Item_Investigations and 7 OA_Gold Total_Item_Investigations in the TR_J3 Standard View.

     This must result in 8 Controlled Unique_Item_Investigations and 7 OA_Gold Unique_Item_Investigations in the TR_J3 Standard View.

     This may not be the case if the content provider operates a cache server.

     The auditor must carry out 15 outside tests (8 tests to journal items where the Access_Type is Controlled and 7 tests to journal items where the Access_Type is OA_Gold).

     This must result in 16 Controlled Total_Item_Investigations and 14 OA_Gold Total_Item_Investigations in the TR_J3 Standard View.

     This must result in 8 Controlled Unique_Item_Investigations and 7 OA_Gold Unique_Item_Investigations in the TR_J3 Standard View.

     This may not be the case if the content provider operates a cache server.

     *Option 2:* Content provider does not offer OA_Gold Items.

     The auditor must carry out a total of 30 tests, and each test will consist of 2 Investigations. There are 2 types of tests that must be carried out:

     - “Inside” tests (Two investigations are made to the same book item, and the second investigation is made within 30 seconds of the first).
     - “Outside” tests (Two investigations are made to the same book item, and the second investigation is more than 30 seconds after the first).

     The auditor must carry out 15 inside tests.

     This must result in 15 Controlled Total_Item_Investigations in the TR_J3 Standard View.

     This must result in 15 Controlled Unique_Item_Investigations in the TR_J3 Standard View.

     This may not be the case if the content provider operates a cache server.

     The auditor must carry out 15 outside tests.

     This must result in 30 Controlled Total_Item_Investigations in the TR_J3 Standard View.

     This must result in 15 Controlled Unique_Item_Investigations in the TR_J3 Standard View.

     This may not be the case if the content provider operates a cache server.
   - The auditor must allow at least 31 seconds between each of the 30 tests.
   - A content provider will pass this audit test when the sum of the Total_Item_Investigations and Unique_Item_Investigations reported by the content provider in TR_J3 Standard View for the auditor’s test account is within a -8% and +3% reliability window of the sum of the Total_Item_Investigations and Unique_Item_Investigations on the auditor’s report.
  
#. Audit tests J3-1, J3-2, J3-3, and J3-4 must take place in separate accounts so that each audit test can be separately reported.


Standard View: TR_J4
....................

Journal Requests by YOP (excluding OA_Gold): Breaks down the usage of non-Gold pen Access journal content by year of publication (YOP) providing counts for the metric types Total_Item_Requests and Unique_Item_Requests. Provides the details necessary to analyze usage of content in backfiles or covered by perpetual access agreement. Note: COUNTER reports do not provide access model or perpetual access rights details.

An audit of this Standard View requires the following:

#. The auditor must have access to all journal content available by the content provider.
#. The Access_Type for all requests must be Controlled and not OA_Gold.
#. The auditor must record the Year of Publication (YOP) of every item accessed during audit testing.
#. The auditor must ensure that some full-text articles from different years of the same journal are requested during the J4-1 and J4-2 tests. Hence, the auditor should know the numbers expected to appear against each Year of Publication (YOP) in the TR_J4 report.
#. Audit-test J4-1: Total_Item_Requests and Unique_Item_Requests

   - The auditor must make a total of 100 requests on a subset of unique Journal Items.

     This must result in 100 Total_Item_Requests being reported in the TR_J4 Standard View.

     This must result in 100 Unique_Item_Requests being reported in the TR_J4 Standard View.
   - The auditor must allow at least 31 seconds between each test.
   - A content provider will pass this audit test when the sum of the Total_Item_Requests and Unique_Item_Requests reported by the content provider in TR_J4 Standard View for the auditor’s test account is within a -8% and +3% reliability window of the sum of the Total_Item_Requests and Unique_Item_Requests on the auditor’s report.
   - The auditor must confirm the Year of Publication (YOP) of articles covered in J4-1 with appropriate and proportionate spot checks, unless the article is “YOP unknown”.
  
#. Audit-test J4-2: Total_Item_Requests and Unique_Item_Requests 30-second filters

   - To ensure that the report is counting correctly as per the COUNTER Code of Practice, it is important that the browser cache settings of the machines used for testing are disabled. It is also important that the auditee confirms before the audit period whether or not they operate a cache server. If they do, this test will not report as the Code of Practice expects and is likely to under-report successive searches outside the double-click threshold.
   - The audit-test consists of clicking links to a Journal Item twice in succession (double-clicks). If the two clicks occur within a 30-second time-span, only the second Total_Item_Requests must be recorded. If the two clicks occur with more than 30 seconds between, then 2 Total_Item_Requests must be counted. In both cases only 1 Unique_Item_Requests will be reported.
   - The auditor must carry out a total of 30 tests, and each test will consist of 2 requests. There are 2 types of tests that must be carried out:

     - “Inside” tests (Two Item requests are made to the same journal item and the second request is made within 30 seconds of the first).
     - “Outside” tests (Two item requests are made to the same journal item, and the second request is made more than 30 seconds after the first).

     The auditor must carry out 15 inside tests.

     This must result in 15 Total_Item_Requests and 15 Unique_Item_Requests in the TR_J4 Standard View.

     This may not be the case if the content provider operates a cache server.

     The audit must carry out 15 outside tests.

     This must result in 30 Total_Item_Requests and 15 Unique_Item_Requests in the TR_J4 Standard View.

     This may not be the case if the content provider operates a cache server.
   - The auditor must allow at least 31 seconds between each of the 30 tests.
   - A content provider will pass this audit test when the sum of the Total_Item_Requests and Unique_Item_Requests reported by the content provider in TR_J1 Standard View for the auditor’s test account is within a -8% and +3% reliability window of the sum of the Total_Item_Requests and Unique_Item_Requests on the auditor’s report.
   - The auditor must confirm the Year of Publication (YOP) of articles covered in J4-2 with appropriate and proportionate spot checks, unless the article is “YOP unknown”.
  
#. Audit tests J4-1 and J4-2 must take place in separate accounts so that each audit test can be separately reported.


Item Reports
''''''''''''

Master Report: IR
.................

The Item Master Report will be COUNTER compliant if the following Standard Views pass the COUNTER audits and the figures reported within them match what is reported in the Master Report.

Any Standard View that is not applicable to the content provider does not require auditing. This must be agreed prior to the audit by COUNTER.


Standard View: IR_A1
....................

Reports on journal article requests at the article level. This report is limited to content with a Data_Type of Journal, Section_Type of article, and metric types of Total_Item_Requests.

An audit of this Standard View requires the following:

#. The auditor must have access to all journal article content available by the content provider.
#. Audit-test A1-1: Total_Item_Requests

   - The auditor must make a total of 100 requests on a subset of journal article Items.

     This must result in 100 Total_Item_Requests being reported in the IR_A1 Standard View.
   - The auditor must allow at least 31 seconds between each test.
   - A content provider will pass this audit test when the sum of the Total_Item_Requests reported by the content provider in IR_A1 Standard View for the auditor’s test account is within a -8% and +3% reliability window of the sum of the Total_Item_Requests on the auditor’s report.
  
#. Audit-test A1-2: Total_Item_Requests 30-second filters

   - To ensure that the report is counting correctly as per the COUNTER Code of Practice, it is important that the browser cache settings of the machines used for testing are disabled. It is also important that the auditee confirms before the audit period whether or not they operate a cache server. If they do, this test will not report as the Code of Practice expects and is likely to under-report successive searches outside the double-click threshold.
   - The audit-test consists of clicking links to a Journal Article Item twice in succession (double-clicks). If the two clicks occur within a 30-second time-span, only the second Total_Item_Requests must be recorded. If the two clicks occur with more than 30 seconds between, then 2 Total_Item_Requests must be counted.
   - The auditor must carry out a total of 30 tests, and each test will consist of 2 requests. There are 2 types of tests that must be carried out:

     - “Inside” tests (Two requests are made to the same journal article item, and the second request is made within 30 seconds of the first).
     - “Outside” tests (Two requests are made to the same journal article item, and the second request is made more than 30 seconds after the first).

     The auditor must carry out 15 inside tests.

     This must result in 15 Total_Item_Requests in the IR_A1 Standard View.

     This may not be the case if the content provider operates a cache server.

     The audit must carry out 15 outside tests.

     This must result in 30 Total_Item_Requests in the IR_A1 Standard View.

     This may not be the case if the content provider operates a cache server.
   - The auditor must allow at least 31 seconds between each of the 30 tests.
   - A content provider will pass this audit test when the sum of the Total_Item_Requests reported by the content provider in IR_A1 Standard View for the auditor’s test account is within a -8% and +3% reliability window of the sum of the Total_Item_Requests on the auditor’s report.
  
#. Audit tests A1-1 and A1-2 must take place in separate accounts so that each audit test can be separately reported.


Standard View: IR_M1
....................

Reports on multimedia requests at the item level.

An audit of this Standard View requires the following:

#. The auditor must have access to all multimedia content available by the content provider.
#. Audit-test M1-1: Total_Item_Requests

   - The auditor must make a total of 100 requests on a subset of multimedia items.

     This must result in 100 Total_Item_Requests being reported in the IR_M1 Standard View.
   - The auditor must allow at least 31 seconds between each test.
   - A content provider will pass this audit test when the sum of the Total_Item_Requests reported by the content provider in IR_M1 Standard View for the auditor’s test account is within a -8% and +3% reliability window of the sum of the Total_Item_Requests on the auditor’s report.
  
#. Audit-test M1-2: Total_Item_Requests 30-second filters

   - To ensure that the report is counting correctly as per the COUNTER Code of Practice, it is important that the browser cache settings of the machines used for testing are disabled. It is also important that the auditee confirms before the audit period if they operate a cache server. If they do, this test will not report as the Code of Practice expects and is likely to under-report successive searches outside the double-click threshold.
   - The audit-test consists of clicking links to a multimedia item twice in succession (double-clicks). If the two clicks occur within a 30-second time-span, only the second Total_Item_Requests must be recorded. If the two clicks occur with more than 30 seconds between, then 2 Total_Item_Requests must be counted.
   - The auditor must carry out a total of 30 tests, and each test will consist of 2 requests). There are 2 types of tests that must be carried out:

     - “Inside” tests (Two requests are made to the same multimedia item and the second request is made within 30 seconds of the first).
     - “Outside” tests (Two requests are made to the same multimedia item, and the second request is made more than30 seconds after the first).

     The auditor must carry out 15 inside tests.

     This must result in 15 Total_Item_Requests in the IR_M1 Standard View.

     This may not be the case if the content provider operates a cache server.

     The audit must carry out 15 outside tests.

     This must result in 30 Total_Item_Requests in the IR_M1 Standard View.

     This may not be the case if the content provider operates a cache server.
   - The auditor must allow at least 31 seconds between each of the 30 tests.
   - A content provider will pass this audit test when the sum of the Total_Item_Requests reported by the content provider in IR_M1 Standard View for the auditor’s test account is within a -8% and +3% reliability window of the sum of the Total_Item_Requests on the auditor’s report.
  
#. Audit tests M1-1 and M1-2 must take place in separate accounts so that each audit test can be separately reported.


Stage 3. Report Delivery: Checking delivery of the reports
""""""""""""""""""""""""""""""""""""""""""""""""""""""""""

In addition to verifying the delivery of reports in a tabular format, the auditor will check that the COUNTER reports are downloadable using the SUSHI protocol. This may be tested using the COUNTER Report Validation Tool, an open-source tool that provides a series of web-forms and guidance to take users through the steps and parameters needed to connect successfully to SUSHI servers and download content provider reports. The COUNTER Report Validation Tool may be found at: https://www.projectcounter.org/validation-tool/.

A content provider will only pass an audit test if the JSON-formatted report produced via SUSHI matches the total of the relevant usage counted on the equivalent tabular report offered by the content provider. In other words, a report should produce the same results irrespective of the format in which it is delivered.
