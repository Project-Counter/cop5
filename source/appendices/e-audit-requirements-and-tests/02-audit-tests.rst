.. The COUNTER Code of Practice Release 5 © 2017-2021 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

E.2 Audit Tests
---------------

There are many audit tests required by the COUNTER R5 Code of Practise, detailed below.


E.2.1 Platform Reports
""""""""""""""""""""""

E.2.1.1 Master Report: PR
'''''''''''''''''''''''''

The Platform Master Report will be COUNTER-compliant if the following Standard View passes the COUNTER R5 Audit. The figures reported in the Standard View must match the figures reported in the Platform Master Report.


E.2.1.2 Standard View: PR_P1
''''''''''''''''''''''''''''

This Standard View presents platform-level usage summarized by Metric_Type.

An audit of this Standard View requires the following for all audit tests, unless otherwise specified:

* The auditor must have access to all available content on the platform of the content provider.
* All searches, including those returning 0 results, must be reported as a Searches_Platform in the PR_P1 Standard View.
* The auditor must allow at least 31 seconds between each request.
* Each time a search is conducted, the auditor will record the search term, the database searched (if applicable), and the number of results returned.
* Audit tests P1-1, P1-2 and P1-3 must take place in separate accounts so that each audit test can be separately reported.
* For each applicable audit test to achieve an audit pass, all metrics reported by the content provider in PR_P1 Standard View from the auditor’s test account must be within a -8% and +3% reliability window of the same audit metrics on the auditor’s report.

The audit test requirements may vary depending on the set up of the platform and any related database(s).


Audit Test P1-1: Searches_Platform
..................................

The auditor will perform audit tests based on the relevant option detailed below.

**Option 1**: The platform has multiple databases and the user can search: All databases, a selected subset of databases, and a single database.

The auditor must run 100 searches on the platform, including 50 searches against only 1 selected database, 25 against 2 selected databases, and 25 against all databases. Each of these searches must report 1 Searches_Platform in the PR_P1 Standard View.

**Option 2**: The platform has multiple databases and the user can search: All databases and a single database.

The auditor must run 100 searches on the platform, including 50 searches against only 1 selected database and 50 against all databases. Each of these searches must report 1 Searches_Platform in the PR_P1 Standard View.

**Option 3**: The platform has multiple databases and the user can only search all databases.

The auditor must run 100 searches. Each of these searches can only be run on all databases. Each of the searches must report 1 Searches_Platform in the PR_P1 Standard View.

**Option 4**: The platform has multiple databases and the user can search a selected single database.

The auditor must run 100 searches, each of these searches can only be run on a single database, and the testing should cover a reasonable amount of the available databases. Each of these searches must report 1 Searches_Platform in the PR_P1 Standard View.

**Option 5**: The platform has a single database.

The auditor must run 50 searches on the platform, with all 50 searches run against the 1 database. Each of these searches must report 1 Searches_Platform in the PR_P1 Standard View.


Audit Test P1-2: Total_Item_Requests, Unique_Item_Requests and Unique_Title_Requests
....................................................................................

The auditor will perform audit tests based on the relevant option detailed below.

Multiple paths should be used to make the audit requests. When possible, 50% of items requested should be via browsing the platform and 50% via searching the platform.

If browsing to items or accessing items via searching is not possible, then 100% of requested items can be accessed via the only available option.

**Option 1**: Platform has multiple databases that include books.

The auditor must make a total of 100 requests on a subset of unique items, including 50 requests against items not within books (if available) and 50 requests against items within books (if available).

If the platform only has content that is within books, then all 100 requests must be made to items within books.

The auditor requests must result in:

*  100 Total_Item_Requests and 100 Unique_Item_Requests in the PR_P1 Standard View.

Each book must have 5 items within the book requested. This will report 5 Total_Item_requests, 5 Unique_Item_Requests and 1 Unique_Title_Request.

The Unique_Title_Requests being reported in the PR_P1 Standard View will be determined by the number of unique books noted by the auditor during the testing.

**Option 2**: The Platform has multiple databases that do not include books.

The auditor must make 100 requests on a subset of the unique items available to them.

This must result in 100 Total_Item_Requests and 100 Unique_Item_Requests reported in the PR_P1 Standard View. The number of Unique_Title_Requests will be 0 and therefore not reported.

**Option 3**: Platform has a single database that includes books.

The auditor must make 50 requests on items available to them, including 25 requests against items not within books (if available) and 25 requests against items within books (if available).

If the platform only has content that is within books, then all 50 requests must be made to items within books.

This must result in 50 Total_Item_Requests being reported in the PR_P1 Standard View.

Each book must have 5 items within the book requested. This will report 5 Total_Item_Requests, 5 Unique_Item_Requests, and 1 Unique_Title_Requests.

The Unique_Title_Requests being reported in the PR_P1 Standard View will be determined by the number of unique books noted by the auditor during the testing.

**Option 4**: Platform has a single database that does not include books.

The auditor must make 50 requests on items.

This must result in 50 Total_Item_Requests and 50 Unique_Item_Requests being reported in the PR_P1 Standard View. The number of Unique_Title_Requests will be 0 and therefore not reported.


Audit Test P1-3: Total_Item_Requests and Unique_Item_Requests - 30-second filters
.................................................................................

The audit test consists of clicking links to an item twice in succession (double-clicks). If the two clicks occur within a 30-second time-span, only the second Total_Item_Requests must be recorded. If the two clicks occur with more than 30 seconds between them, then 2 Total_Item_Requests must be counted. In both cases only 1 Unique_Item_Requests will be reported.

The auditor must carry out a total of 30 tests on the platform, each test will consist of 2 requests. There are 2 types of tests that must be carried out:

* “Inside” tests (Two identical requests are made, and the second request is made within 30 seconds of the first).
* “Outside” tests (Two identical requests are made, and the second request is made more than 30 seconds after the first).

The auditor must carry out 15 **inside** tests.

This must result in:

*  15 Total_Item_Requests and 15 Unique_Item_Requests in the PR_P1 Standard View.

The auditor must carry out 15 **outside** tests.

This must result in:

*  30 Total_Item_Requests and 15 Unique_Item_Requests in the PR_P1 Standard View.


E.2.2 Database Reports
""""""""""""""""""""""

E.2.2.1 Master Report: DR
'''''''''''''''''''''''''

The Database Master Report will be COUNTER-compliant if the following Standard Views pass the COUNTER R5 audit. The figures reported in the Standard Views must match the figures reported in the Database Master Report.

Any Standard View not applicable to the content provider does not require auditing. Any exclusions must be confirmed by COUNTER prior to testing and the auditor notified.


E.2.2.2 Standard View: DR_D1
''''''''''''''''''''''''''''

This Standard View reports on key search and request metrics needed to evaluate a database: Databases Searches and Item Usage.

An audit of this Standard View requires the following for all audit tests unless otherwise specified:

* The auditor must have access to all databases available on the platform of the content provider. Any exclusions must be agreed prior to the audit by COUNTER and communicated to the auditor.
* The auditor must allow at least 31 seconds between each request.
* Each time a search is conducted, the auditor will record the search term, the databases searched, and the number of results returned.
* All searches, including those returning 0 results, must be reported as a Searches_Regular or Searches_Automated in the DR_D1 Standard View.
* Audit tests D1-1, D1-2 and, D1-3, D1-4 and D1-5 must take place in separate accounts so that each audit test can be separately reported.
* For each applicable audit test to achieve an audit pass, all metrics reported by the content provider in DR_D1 Standard View from the auditor’s test account must be within a -8% and +3% reliability window of the same audit metric(s) on the auditor’s report.


Audit Test D1-1: Searches_Regular and Searches_Automated
........................................................

The auditor will perform audit tests based on the relevant option detailed below.

**Option 1**:The content provider has multiple databases and the user can search: All databases, a selected subset of databases, and a single database.

The auditor must run 100 searches, including 50 against only 1 selected database, 25 against 2 selected databases, and 25 against all databases.

Each of the searches on a single database must report 1 Searches_Regular in the DR_D1 Standard View.

Each of the searches over 2 auditor selected databases must report 1 Searches_Regular against each of the selected databases in the DR_D1 Standard View.

Each of the searches over all databases must report 1 Searches_Regular against each of the databases offered by the content provider in the DR_D1 Standard View.

**Option 2**: The content provider has multiple databases and the user can search: All databases and a single database.

The auditor must run 100 searches, including 50 against only 1 selected database and 50 against all databases.

Each of the searches on a single database must report 1 Searches_Regular in the DR_D1 Standard View.

Each of the searches over all databases must report 1 Searches_Regular against each of the databases offered by the content provider in the DR_D1 Standard View.

**Option 3**: The content provider has multiple databases and the user can only search all databases.

The auditor must run 100 searches. Each of these searches can only be run on all databases. Each of the searches must report 1 Searches_Automated against each of the databases offered by the content provider in the DR_D1 Standard View.

**Option 4**: The content provider has multiple databases and the user can search a single database only.

The auditor must run 100 searches, each of the searches can only be run on a single database and the testing should cover a reasonable amount of the available database.

Each of the searches must report 1 Searches_Regular in the DR_D1 Standard View.

**Option 5**: The content provider has a single database.

The auditor must run 50 searches against the single database.

Each of the searches must report 1 Searches_Regular in the DR_D1 Standard View.


Audit Test D1-2: Total_Item_Requests
....................................

The auditor must make 100 requests on a subset of available unique items.

This must result in 100 Total_Item_Requests reported in the DR_D1 Standard View.

Multiple paths should be used to make the requests. When possible, 50% of items requested should be via browsing the platform and 50% via searching the platform.

If browsing to items or accessing items via searching is not possible, then 100% of requested items can be accessed via the only available option.


Audit Test D1-3: Total_Item_Requests - 30-second filters
........................................................

The audit test consists of making an Item_Request twice in succession (double-clicks). If the two clicks occur within a 30-second time-span, only the second Total_Item_Request must be recorded. If the two clicks occur with more than 30 seconds between them, then 2 Total_Item_Requests must be counted.The auditor must carry out a total of 30 tests, and each test will consist of 2 requests. There are 2 types of tests that must be carried out:

* “Inside” tests (The 2 requests are made to the same item, and the second request is made within 30 seconds of the first).
* “Outside” tests (The 2 requests are made to the same item, and the second request is made more than 30 seconds after the first).

The auditor must carry out 15 **inside** tests.

This must result in:

* 15 Total_Item_Requests being reported in the DR_D1 Standard View.

The auditor must carry out 15 **outside** tests.

This must result in:

*  30 Total_Item_Requests being reported in the DR_D1 Standard View.


Audit Test D1-4: Total_Item_Investigations
..........................................

**IMPORTANT NOTE**: This test is required when investigations can be reported independently of a request. It is not required if all investigations have a matching request, but this must be verified during the audit. Any exclusion of tests must be confirmed by COUNTER prior to testing and the auditor notified.

The auditor must make 100 Investigations on a subset of available unique items. This must result in 100 Total_Item_Investigations.

Multiple paths should be used to make the Investigations. When possible, 50% of items Investigations should be via browsing and 50% via searching.

If either browsing to item investigations or accessing item investigations via searching is not possible, then 100% of item investigations can be made via the only available option.


Audit Test D1-5: Total_Item_Investigations - 30-second filters
..............................................................

**IMPORTANT NOTE**: This test is required when investigations can be reported independently of a request. It is not required when all investigations have a matching request. Any exclusion of tests must be confirmed by COUNTER prior to testing and the auditor notified.

The audit test consists of making an Item_Investigation twice in succession (double-clicks). If the two clicks occur within a 30-second time-span, only the second Total_Item_Investigations made must be recorded. If the two clicks occur with more than 30 seconds between, then 2 Total_Item_Investigations must be counted.

The auditor must carry out a total of 30 tests, and each test will consist of 2 item investigations. There are 2 types of tests that must be carried out:

* “Inside” tests (Two item investigations are made to the same item the second item Investigation is made within 30 seconds of the first).
* “Outside” tests (Two item investigations are made to the same item, and the second item investigation is made more than 30 seconds after the first).

The auditor must carry out 15 **inside** tests.

This must result in:

* 15 Total_Item_Investigations being reported in the DR_D1 Standard View.

The auditor must carry out 15 **outside** tests.

This must result in:

* 30 Total_Item_Investigations being reported in the DR_D1 Standard View.


E.2.2.3 Standard View: DR_D2
''''''''''''''''''''''''''''

Databases Access Denied: This Standard View reports on access-denied activity for databases where a user is denied access because simultaneous user licenses are exceeded or the institution does not have a license for the database.

An audit of this Standard View and related tests requires the following:

* The auditor must allow at least 31 seconds between each request unless otherwise specified.
* Each time a user is denied access, the auditor will record the database on which the denial was produced.
* Audit tests D2-1 and D2-2 must take place in separate accounts so that each audit test can be separately reported.
* For each applicable audit test to achieve an audit pass, all metrics reported by the content provider in DR_D2 Standard View from the auditor’s test account must be within a -8% and +3% reliability window of the same audit metrics on the auditor’s report.


Audit Test D2-1: Limit_Exceeded
...............................

**IMPORTANT NOTE**: This test can only be carried out if the content provider has a concurrent/simultaneous user limit. Any exclusion of tests must be confirmed by COUNTER prior to testing and the auditor notified.

The auditor will perform audit tests based on the relevant option detailed below.

The account used for this testing must have concurrent/simultaneous-user limit set at one single user. A second user attempting to access the database would be denied.

**Option 1**: The content provider denies the user access when the concurrent/simultaneous-user limit is exceeded upon login.

The auditor must force 50 Limit_Exceeded access denials.

* The auditor will log into the site causing the user limit to reach the maximum allowance. The auditor will then attempt to log into the site using a different computer.
* The second login should be refused access. Each time access is refused, the auditor will record this as 1 Limit_Exceeded.

Each of these concurrent/simultaneous turnaways must report 1 Limit_Exceeded in the DR_D2 Standard View.

**Option 2**: The content provider denies the user access when the concurrent/simultaneous user limit is exceeded upon searching or accessing a database.

The auditor must force 50 Limit_Exceeded turnaways.

* The auditor will log into the site. They will select and make a search on a database or browse to a database causing the user limit to reach the maximum allowance. The auditor will then log into the same site using a different computer. The auditor will then repeat the action made on the previous computer (select and make a search on a database or browse to a database).
* The user should then be refused access as the concurrent/simultaneous-user limit has exceeded. Each time access is refused, the auditor will record this as 1 Limit_Exceeded.

Each of these concurrent/simultaneous access denials must report 1 Limit_Exceeded in the DR_D2 Standard View.

**Option 3**: The content provider denies the user access when the concurrent/simultaneous-user limit is exceeded upon accessing an item within a database.

The auditor must force 50 Limit_Exceeded turnaways.

* The auditor will log into the site and will navigate to and request an item. This will cause the user limit to reach the maximum allowance.The auditor will log into the site again using a different computer. The auditor will then repeat the action made on the previous computer (navigate to and request an item).
* After the item has been requested the user should then be denied access. Each time access is refused, the auditor will record this as 1 Limit_Exceeded.

Each of these concurrent/simultaneous turnaways must report 1 Limit_Exceeded in the DR_D2 Standard View.


Audit Test D2-2: No_License
...........................

**IMPORTANT NOTE**: This test can only be carried out if the content provider restricts site content or if restricted content is not displayed. Any exclusion of tests must be confirmed by COUNTER prior to testing and the auditor notified.

The account used for this testing must have restricted access to content. The content the user has no license to access must be declared by the content provider prior to the testing. The auditor will attempt to access content using the account set up with restricted access. Each time access is refused, the auditor will record 1 No_License.

Each of these No_License turnaways must report 1 No_License in the DR_D2 Standard View.


E.2.3 Title Reports
"""""""""""""""""""

E.2.3.1 Master Report: TR
'''''''''''''''''''''''''

The Title Master Report will be COUNTER-compliant if the following Standard Views pass the COUNTER R5 audit. The figures reported must match the figures reported in the Title Master Report.

Any Standard View not applicable to the content provider does not require auditing. Any exclusions must be agreed prior to the audit by COUNTER.


E.2.3.2 Standard View: TR_B1
''''''''''''''''''''''''''''
Book Requests (excluding OA_Gold): Reports on full-text activity for non-Gold Open Access books as Total_Item_Requests and Unique_Title_Requests.

The Unique_Title_Requests provide comparable usage across book platforms. The Total_Item_Requests show overall activity.

An audit of this Standard View requires the following:

* The auditor must have access to all book content available by the content provider.
* The Access_Type for all requests must be Controlled and not OA_Gold.
* The auditor must allow at least 31 seconds between each request, unless otherwise specified.
* Audit tests B1-1 and B1-2 must take place in separate accounts so that each audit test can be separately reported.
* For each applicable audit test to achieve an audit pass, all metrics reported by the content provider in TR_B1 Standard View from the auditor’s test account must be within a -8% and +3% reliability window of the same audit metrics on the auditor’s report.


Audit Test B1-1: Total_Item_Requests and Unique_Title_Requests
..............................................................

The auditor must make a total of 100 requests on a subset of unique items within books.

Each book must have 5 items requested within it. This will report 5 Total_Item_Requests and 1 Unique_Title_Requests.

This must result in:

* 100 Total_Item_Requests being reported in the TR_B1 Standard View.
* 20 Unique_Title_Requests being reported in the TR_B1 Standard View.


Audit Test B1-2: Total_Item_Requests and Unique_Title_Requests - 30-second filters
..................................................................................

The audit test consists of clicking links to an item within a book twice in succession (double-clicks). If the two clicks occur within a 30-second time-span, only the second Total_Item_Requests must be recorded. If the two clicks occur with more than 30 seconds between, then 2 Total_Item_Requests must be counted. In both cases only 1 Unique_Title_Requests will be reported.

The auditor must carry out a total of 32 tests, and each test will consist of 2 requests. There are 2 types of tests that must be carried out:

* “Inside” tests (Two requests are made to the same Item, and the second request is made within 30 seconds of the first).
* “Outside” tests (Two requests are made to the same item and the second request is made more than 30 seconds after the first).

The auditor must carry out 16 **inside** tests.

Where possible, each book must have 2 item tests reporting 1 Total_Item_Requests and 1 Unique_Title_Requests.

This must result in 16 Total_Item_Requests and 8 Unique_Title_Requests in the TR_B1 Standard View.

The auditor must carry out 16 **outside** tests.

Where possible, each book must have 2 items requested reporting 2 Total_Item_Requests and 1 Unique_Title_Requests.

This must result in 32 Total_Item_Requests and 8 Unique_Title_Requests in the TR_B1 Standard View.


E.2.3.3 Standard View: TR_B2
''''''''''''''''''''''''''''

Book Access Denied: This Standard View reports on access-denied activity for books where a user is denied access because simultaneous user licenses are exceeded or their institution does not have a license for the database.

An audit of this Standard View and related tests requires the following:

* Each time a user is denied access, the auditor will record the book where the denial was produced.
* The auditor must allow at least 31 seconds between each request unless otherwise specified.
* Audit tests B2-1 and B2-2 must take place in separate accounts so that each audit test can be separately reported.
* For each applicable audit test to achieve an audit pass, all metrics reported by the content provider in TR_B2 Standard View from the auditor’s test account must be within a -8% and +3% reliability window of the same audit metrics on the auditor’s report.


Audit Test B2-1: Limit_Exceeded
...............................

**IMPORTANT NOTE**: This test can only be carried out if the content provider has a concurrent/simultaneous user limit. Any exclusion of tests must be confirmed by COUNTER prior to testing and the auditor notified.

* The auditor will log into the site and access a book item. The auditor will then log into the site using a different computer. The auditor will log into the site and access a book item.
* After the item has been requested the auditor should be refused access. Each time access is refused, the auditor will record this as 1 Limit_Exceeded.

The auditor must force 50 Limit_Exceeded turnaways during testing.

Each of these concurrent/simultaneous turnaways must report 1 Limit_Exceeded in the TR_B2 Standard View.


Audit Test B2-2: No_License
...........................

**IMPORTANT NOTE**: This test only be carried out if the content provider restricts site content or if restricted content is not displayed. Any exclusion of tests must be confirmed by COUNTER prior to testing and the auditor notified. The account used for this testing must have restricted access to book content. The book content the user has no license to access must be declared by the content provider prior to the testing.

The auditor will attempt to access book content using the account specified with no access. Each time access is refused, the auditor will record 1 No_License.

The auditor must force 50 No_License during testing. Each of these book content not licensed turnaways must report 1 No_License in the TR_B2 Standard View.


E.2.3.4 Standard View: TR_B3
''''''''''''''''''''''''''''

Book Usage by Access Type: Reports on book usage showing all applicable metric types broken down by Access_Type.

An audit of this Standard View and related tests requires the following:

* The auditor must have access to all book content made available by the content provider. Any exclusions must be confirmed by COUNTER prior to testing and the auditor notified.
* The auditor must allow at least 31 seconds between each request unless otherwise specified.
* Audit tests B3-1, B3-2, B3-3, and B3-4 must take place in separate accounts so that each audit test can be separately reported.
* The following metrics reported as a result of the B3-1 and B3-2 audit tests must match in the TR_B3 Standard View:
* Unique_Item_Requests must match Unique_Item_Investigations
* Unique_Title_Requests must match Unique_Title_Investigations
* For each applicable audit test to achieve an audit pass, all metrics reported by the content provider in TR_B3 Standard View from the auditor’s test account must be within a -8% and +3% reliability window of the same audit metrics on the auditor’s report.


Audit Test B3-1: Total_Item_Requests, Unique_Item_Requests and Unique_Title_Requests
....................................................................................

The auditor will perform audit tests based on the relevant options detailed below.

**Option 1**: Content provider offers OA_Gold items in addition to Controlled.

The auditor must make a total of 100 requests on a subset of unique items within books. There must be 50 requests to book items where the Access_Type is Controlled and 50 requests to book items where the Access_Type is OA_Gold.

Each book must have 5 items within it requested. This must report 5 Total_Item_Requests, 5 Unique_Item_Requests and 1 Unique_Title_Requests.

This must result in:

* 50 OA_Gold Total_Item_Requests and 50 Controlled Total_Item_Requests being reported in the TR_B3 Standard View.
* 50 OA_Gold Unique_Item_Requests and 50 Controlled Unique_Item_Requests being reported in the TR_B3 Standard View.
* 10 OA_Gold Unique_Title_Requests and 10 Controlled Unique_Title_Requests being reported in the TR_B3 Standard View.

**Option 2**: Content provider does not offer OA_Gold items.

The auditor must make a total of 100 requests on a subset of unique items within books.

Where the site allows, each book must have 5 items requested resulting in reporting 5 Total_Item_Requests, 5 Unique_Item_Requests, and 1 Unique_Title_Requests.

This must result in:

* 100 Controlled Total_Item_Requests being reported in the TR_B3 Standard View.
* 20 Controlled Unique_Title_Requests being reported in the TR_B3 Standard View.


Audit Test B3-2: Total_Item_Requests, Unique_Item_Requests and Unique_Title_Requests - 30-second filters
........................................................................................................

The auditor will perform audit tests based on the relevant options detailed below.

The audit test consists of clicking links to an item within a book twice in succession (double-clicks). If the two clicks occur within a 30-second time-span, only the second Total_Item_Requests must be recorded. If the two clicks occur with more than 30 seconds between, then 2 Total_Item_Requests must be counted. In both cases, only 1 Unique_Item_Requests and 1 Unique_Title_Requests will be reported.

**Option 1**: Content provider offers OA_Gold items in addition to Controlled items.

The auditor must carry out a total of 32 tests, each test will consist of 2 requests. There are 2 types of tests that must be carried out:

* “Inside” tests (Two requests are made to the same book item, and the second request is made within 30 seconds of the first).
* “Outside” tests (Two requests are made to the same book item, and the second request is made over 30 seconds after the first).

The auditor must carry out 16 **inside** tests.

* 8 tests to book items where the Access_Type is Controlled and 8 tests to book items where the Access_Type is OA_Gold.
* Where the site allows, each book must have 2 item tests. This will report 2 Total_Item_Requests, 2 Unique_Item_Requests, and 1 Unique_Title_Requests.

This must result in

* 8 Controlled Total_Item_Requests and 8 OA_Gold Total_Item_Requests in the TR_B3 Standard View.
* 8 Controlled Unique_Item_Requests and 8 OA_Gold Unique_Item_Requests in the TR_B3 Standard View.
* 4 Controlled Unique_Title_Requests and 4 OA_Gold Unique_Title_Requests in the TR_B3 Standard View.

The auditor must carry out 16 **outside** tests.

* 8 tests to book items where the Access_Type is Controlled and 8 tests to book items where the Access_Type is OA_Gold.
* Where the site allows, each book must have 2 item tests. This will report 4 Total_Item_Requests, 2 Unique_Item_Requests, and 1 Unique_Title_Requests.

This must result in:

* 16 Controlled Total_Item_Requests and 16 OA_Gold Total_Item_Requests in the TR_B3 Standard View.
* 8 Controlled Unique_Item_Requests and 8 OA_Gold Unique_Item_Requests in the TR_B3 Standard View.
* 4 Controlled Unique_Title_Requests and 4 OA_Gold Unique_Title_Requests in the TR_B3 Standard View.

**Option 2**: Content provider does not offer OA_Gold items.

The auditor must carry out a total of 32 tests, and each test will consist of 2 requests. There are 2 types of tests that must be carried out:

* “Inside” tests (Two requests are made to the same book item and the second request is made within 30 seconds of the first).
* “Outside” tests (Two requests are made to the same book item, and the second request is made over 30 seconds after the first).

The auditor must carry out 16 **inside** tests.

* Where the site allows, each book must have 2 item tests. This will report 2 Total_Item_Requests and 2 Unique_Item_Requests and 1 Unique_Title_Requests.

This must result in:

* 16 Controlled Total_Item_Requests in the TR_B3 Standard View.
* 16 Controlled Unique_Item_Requests in the TR_B3 Standard View.
* 8 Controlled Unique_Title_Requests in the TR_B3 Standard View.

The auditor must carry out 16 **outside** tests.

* Where the site allows, each book must have 2 item tests. This will report 4 Total_Item_Requests, 2 Unique_Item_Requests, and 1 Unique_Title_Requests.

This must result in:

* 32 Controlled Total_Item_Requests in the TR_B3 Standard View.
* 16 Controlled Unique_Item_Requests in the TR_B3 Standard View.
* 8 Controlled Unique_Title_Requests in the TR_B3 Standard View.


Audit Test B3-3: Total_Item_Investigations, Unique_Item_Investigations, and Unique_Title_Investigations
.......................................................................................................

**IMPORTANT NOTE**: This test is required when investigations can be reported independently of a request. It is not required when all investigations have a matching request. Any exclusion of tests must be confirmed by COUNTER prior to testing and the auditor notified.

The auditor will perform audit tests based on the relevant options detailed below.

**Option 1**: Content provider offers OA_Gold items in addition to Controlled.

The auditor must make a total of 50 item investigations within a subset of books. There must be 25 Investigations of items within a book where the Access_Type is Controlled and 25 investigations of items within a book where the Access_Type is OA_Gold.

* Each book must have 5 investigations of unique items. This will report 5 Total_Item_Investigations, 5 Unique_Item_Investigations, and 1 Unique_Title_Investigations.

This must result in:

* 25 OA_Gold Total_Item_Investigations and 25 Controlled Total_Item_Investigations being reported in the TR_B3 Standard View.
* 25 OA_Gold Unique_Item_Investigations and 25 Controlled Unique_Item_Investigations being reported in the TR_B3 Standard View.
* 5 OA_Gold Unique_Title_Investigations and 5 Controlled Unique_Title_Investigations being reported in the TR_B3 Standard View.

**Option 2**: Content provider does not offer OA_Gold items.

The auditor must make a total of 50 Investigations within a subset of books.

* Each book must have 5 investigations of unique items. This will report 5 Total_Item_Investigations, 5 Unique_Item_Investigations, and 1 Unique_Title_Investigations.

This must result in:

* 50 Controlled Total_Item_Investigations being reported in the TR_B3 Standard View.
* 50 Controlled Unique_Item_Investigations being reported in the TR_B3 Standard View.
* 10 Controlled Unique_Title_Investigations being reported in the TR_B3 Standard View.


Audit Test B3-4: Total_Item_Investigations, Unique_Item_Investigations, and Unique_Title_Investigations - 30-second filters
...........................................................................................................................

**IMPORTANT NOTE**: This test is required when investigations can be reported independently of a request. It is not required when all investigations have a matching request. Any exclusion of tests must be confirmed by COUNTER prior to testing and the auditor notified.

The auditor will perform audit tests based on the relevant options detailed below.

The audit test consists of clicking links to an investigation of an item within a book twice in succession (double-clicks). If the two clicks occur within a 30-second time-span, only the second Total_Item_Investigations must be recorded. If the two clicks occur with more than 30 seconds between, then 2 Total_Item_Investigations must be counted. In both cases only 1 Unique_Item_Investigations and 1 Unique_Title_Investigations will be reported.

**Option 1**: Content provider offers OA_Gold items in addition to Controlled.

The auditor must carry out a total of 32 tests. Each test will consist of 2 item investigations. There are 2 types of tests that must be carried out:

* “Inside” tests (Two investigations are made to the same book item, and the second investigation is made within 30 seconds of the first).
* “Outside” tests (Two investigations are made to the same book item, and the second investigation is made more than 30 seconds after the first).

The auditor must carry out 16 **inside** tests. This requires 8 Investigations to book items where the Access_Type is Controlled and 8 investigations to book items where the Access_Type is OA_Gold.

Each book must have 2 item tests. This will report 2 Total_Item_Investigations, 2 Unique_Item_Investigations, and 1 Unique_Title_Investigations.

This must result in:

* 8 Controlled Total_Item_Investigations and 8 OA_Gold Total_Item_Investigations in the TR_B3 Standard View.
* 8 Controlled Unique_Item_Investigations and 8 OA_Gold Unique_Item_Investigations in the TR_B3 Standard View.
* 4 Controlled Unique_Title_Investigations and 4 OA_Gold Unique_Title_Investigations in the TR_B3 Standard View.

The auditor must carry out 16 **outside** tests. This requires 8 tests to book items where the Access_Type is Controlled and 8 tests to book items where the Access_Type is OA_Gold.

Each book must have 2 item tests. This will report 4 Total_Item_Investigations, 2 Unique_Item_Investigations, and 1 Unique_Title_Investigations.

This must result in:

* 16 Controlled Total_Item_Investigations and 16 OA_Gold Total_Item_Investigations in the TR_B3 Standard View.
* 8 Controlled Unique_Item_Investigations and 8 OA_Gold Unique_Item_Investigations in the TR_B3 Standard View.
* 4 Controlled Unique_Title_Investigations and 4 OA_Gold Unique_Title_Investigations in the TR_B3 Standard View.

**Option 2**: Content provider does not offer OA_Gold items.

The auditor must carry out a total of 32 tests. Each test will consist of 2 item investigations. There are 2 types of tests that must be carried out:

* “Inside” tests (Two investigations are made to the same book item, and the second investigation is made within 30 seconds of the first).
* “Outside” tests (Two investigations are made to the same book item, and the second investigation is made more than 30 seconds after the first).

The auditor must carry out 16 **inside** tests.

Each book must have 2 item tests. This will report 2 Total_Item_Investigations, 2 Unique_Item_Investigations, and 1 Unique_Title_Investigations.

This must result in:

* 16 Controlled Total_Item_Investigations in the TR_B3 Standard View.
* 16 Controlled Unique_Item_Investigations in the TR_B3 Standard View.
* 8 Controlled Unique_Title_Investigations in the TR_B3 Standard View.

The auditor must carry out 16 **outside** tests.

Each book must have 2 item tests. This will report 4 Total_Item_Investigations, 2 Unique_Item_Investigations, and 1 Unique_Title_Investigations.

This must result in:

* 32 Controlled Total_Item_Investigations in the TR_B3 Standard View.
* 16 Controlled Unique_Item_Investigations in the TR_B3 Standard View.
* 8 Controlled Unique_Title_Investigations in the TR_B3 Standard View.


E.2.3.5 Standard View: TR_J1
''''''''''''''''''''''''''''

Journal Requests (excluding OA_Gold): Reports on usage of non-Gold Open Access journal content as Total_Item_Requests and Unique_Item_Requests.

An audit of this Standard View and related tests requires the following:

* The auditor must have access to all journal content available by the content provider. Any exclusions must be confirmed by COUNTER prior to testing and the auditor notified.The Access_Type for all requests must be Controlled and not OA_Gold.
* The auditor must allow at least 31 seconds between each request unless otherwise specified.
* Audit tests J1-1 and J1-2 must take place in separate accounts so that each audit test can be separately reported.
* For each applicable audit test to achieve an audit pass, all metrics reported by the content provider in TR_J1 Standard View from the auditor’s test account must be within a -8% and +3% reliability window of the same audit metrics on the auditor’s report.


Audit Test J1-1: Total_Item_Requests and Unique_Item_Requests
.............................................................

The auditor must make a total of 100 requests on a subset of unique journal items.

This must result in:

* 100 Total_Item_Requests being reported in the TR_J1 Standard View.
* 100 Unique_Item_Requests being reported in the TR_J1 Standard View.


Audit Test J1-2: Total_Item_Requests and Unique_Item_Requests - 30-second filters
.................................................................................

The audit test consists of clicking links to a journal item twice in succession (double-clicks). If the two clicks occur within a 30-second time-span, only the second Total_Item_Requests must be recorded. If the two clicks occur with more than 30 seconds between, then 2 Total_Item_Requests must be counted. In both cases only 1 Unique_Item_Requests will be reported.

The auditor must carry out a total of 30 tests. Each test will consist of 2 requests.

There are 2 types of tests that must be carried out:

* “Inside” tests (Two requests are made to the same journal item, and the second request is made within 30 seconds of the first).
* “Outside” tests (Two requests are made to the same journal item, and the second request is made over 30 seconds after the first).

The auditor must carry out 15 **inside** tests.

This must result in:

* 15 Total_Item_Requests and 15 Unique_Item_Requests in the TR_J1 Standard View.

The auditor must carry out 15 **outside** tests.

This must result in:

*  30 Total_Item_Requests and 15 Unique_Item_Requests in the TR_J1 Standard View.


E.2.3.6 Standard View: TR_J2
''''''''''''''''''''''''''''

Journal Access Denied: This Standard View reports on access denied activity for journal content. A user is denied access because simultaneous-user licenses are exceeded, or their institution does not have a license for the journal.

An audit of this Standard View and related tests requires the following:

* The auditor must allow at least 31 seconds between each request unless otherwise specified.
* Each time a user is denied access, the auditor will record the journal on which the denial was produced.
* Audit tests J2-1 and J2-2 must take place in separate accounts so that each audit test can be separately reported.
* For each applicable audit test to achieve an audit pass, all metrics reported by the content provider in TR_J2 Standard View from the auditor’s test account must be within a -8% and +3% reliability window of the same audit metrics on the auditor’s report.


Audit Test J2-1: Limit_Exceeded
...............................

**IMPORTANT NOTE**: This test can only be carried out where the content provider offers a concurrent/simultaneous-user limit. Any exclusion of tests must be confirmed by COUNTER prior to testing and the auditor notified.

The account used for this testing must have a concurrent/simultaneous-user limit set for journal items. The account should allow a single active user to access journals. A second user accessing journals will be turned away. The number of registered users concurrently allowed must be declared by the content provider prior to the testing.

The content provider denies the user access when the concurrent/simultaneous-user limit is exceeded for journals.

* The auditor will log into the site and access a journal item. The user limit is at maximum active users.
* The auditor will then log into the site using a different computer and repeat the action of accessing a journal.
* The user should be refused access.
* Each time access is refused, the auditor will record this as 1 Limit_Exceeded.

The auditor must force 50 Limit_Exceeded turnaways during testing.

Each of these concurrent/simultaneous access denials must report 1 Limit_Exceeded in the TR_J2 Standard View.


Audit Test J2-2: No_License
...........................

**IMPORTANT NOTE**: This test can only be carried out if the content provider restricts site content or where restricted content is not displayed. Any exclusion of tests must be confirmed by COUNTER prior to testing and the auditor notified.

The account used for this testing must have restricted access to journal content. The content provider must declare the content the user does not have license to access.

The auditor will attempt to access the restricted journal content. Each time access is refused, the auditor will record 1 No_License.

The auditor must force 50 No_License turnaways during testing.

Each of these journal content not licensed denials must report 1 No_License in the TR_J2 Standard View.


E.2.3.7 Standard View: TR_J3
''''''''''''''''''''''''''''

Journal Usage by Access Type: This Standard View reports on usage of journal content for all metric types broken down by access type.

An audit of this Standard View and related tests requires the following:

* The auditor must have access to all journal content made available by the content provider. Any exclusions must be confirmed by COUNTER prior to testing and the auditor notified.
* The auditor must allow at least 31 seconds between each request unless otherwise specified.
* Audit tests J3-1, J3-2, J3-3, and J3-4 must take place in separate accounts so that each audit test can be separately reported.
* For each applicable audit test to achieve an audit pass, all metrics reported by the content provider in TR_J3 Standard View from the auditor’s test account must be within a -8% and +3% reliability window of the same audit metrics on the auditor’s report.


Audit Test J3-1: Total_Item_Requests and Unique_Item_Requests
.............................................................

The auditor will perform audit tests based on the relevant options detailed below.

**Option 1**: Content provider offers OA_Gold items in addition to Controlled.

The auditor must make a total of 100 requests on a subset of unique journal items. 50 requests to journal items where the Access_Type is Controlled and 50 requests to journal items where the Access_Type is OA_Gold.

This must result in:

* 50 OA_Gold Total_Item_Requests and 50 Controlled Total_Item_Requests being reported in the TR_J3 Standard View.
* 50 OA_Gold Unique_Item_Requests and 50 Controlled Unique_Item_Requests being reported in the TR_J3 Standard View.

**Option 2**: Content provider does not offer OA_Gold items.

The auditor must make a total of 100 requests on a subset of unique journal items.

This must result in:

* 100 Controlled Total_Item_Requests being reported in the TR_J3 Standard View.
* 100 Controlled Unique_Item_Requests being reported in the TR_J3 Standard View.


Audit Test J3-2: Total_Item_Requests and Unique_Item_Requests - 30-second filters
.................................................................................

The auditor will perform audit tests based on the relevant options detailed below.

The audit test consists of clicking links to a journal item twice in succession (double-clicks). If the two clicks occur within a 30-second time-span, only the second Total_Item_Requests must be recorded. If the two clicks occur with more than 30 seconds between them, then 2 Total_Item_Requests must be counted. In both cases only 1 Unique_Item_Requests will be reported.

**Option 1**: Content provider offers OA_Gold items in addition to Controlled.

The auditor must carry out a total of 30 tests, and each test will consist of 2 requests. There are 2 types of tests that must be carried out:

* “Inside” tests (Two requests are made to the same journal item, and the second request is made within 30 seconds of the first).
* “Outside” tests (Two requests are made to the same journal item and the second request is made over 30 seconds after the first).

The auditor must carry out 15 **inside** tests.

8 tests to journal items where the Access_Type is Controlled and 7 tests to journal items where the Access_Type is OA_Gold.

This must result in:

* 8 Controlled Total_Item_Requests and 7 OA_Gold Total_Item_Requests in the TR_J3 Standard View.
* 8 Controlled Unique_Item_Requests and 7 OA_Gold Unique_Item_Requests in the TR_J3 Standard View.

The auditor must carry out 15 **outside** tests.

8 tests to journal items where the Access_Type is Controlled and 7 tests to journal items where the Access_Type is OA_Gold).

This must result in:

* 16 Controlled Total_Item_Requests and 14 OA_Gold Total_Item_Requests in the TR_J3 Standard View.
* 8 Controlled Unique_Item_Requests and 7 OA_Gold Unique_Item_Requests in the TR_J3 Standard View.

**Option 2**: Content provider does not offer OA_Gold items.

The auditor must carry out a total of 30 tests, and each test will consist of 2 requests. There are 2 types of tests that must be carried out:

* “Inside” tests (Two requests are made to the same journal item, and the second request is made within 30 seconds of the first).
* “Outside” tests (Two requests are made to the same journal item, and the second request is made more than 30 seconds after the first).

The auditor must carry out 15 **inside** tests.

This must result in:

* 15 Controlled Total_Item_Requests in the TR_J3 Standard View.
* 15 Controlled Unique_Item_Requests in the TR_J3 Standard View.

The auditor must carry out 15 **outside** tests.

This must result in:

* 30 Controlled Total_Item_Requests in the TR_J3 Standard View.
* 15 Controlled Unique_Item_Requests in the TR_J3 Standard View.


Audit Test J3-3: Total_Item_Investigations and Unique_Item_Investigations
.........................................................................

The auditor will perform audit tests based on the relevant options detailed below.

**Option 1**: Content provider offers OA_Gold items in addition to Controlled.

The auditor must make a total of 50 investigations to a subset of unique journal items. Where the site allows, there must be 25 Investigations of journal items where the Access_Type is Controlled and 25 Investigations of journal items where the Access_Type is OA_Gold.

This must result in:

* 25 OA_Gold Total_Item_Investigations and 25 Controlled Total_Item_Investigations being reported in the TR_J3 Standard View.
* 25 OA_Gold Unique_Item_Investigations and 25 Controlled Unique_Item_Investigations being reported in the TR_J3 Standard View.

**Option 2**: Content provider does not offer OA_Gold items.

The auditor must make a total of 50 investigations to a subset of unique journal items.

This must result in:

* 50 Controlled Total_Item_Investigations being reported in the TR_J3 Standard View.
* 50 Controlled Unique_Item_Investigations being reported in the TR_J3 Standard View.


Audit Test J3-4: Total_Item_Investigations and Unique_Item_Investigations - 30-second filters
.............................................................................................

The audit test consists of clicking links to an Investigation of a journal item twice in succession (double-clicks). If the two clicks occur within a 30-second time-span, only the second Total_Item_Requests must be recorded. If the two clicks occur with more than 30 seconds between them, then 2 Total_Item_Requests must be counted. In both cases only 1 Unique_Item_Requests will be reported.

**Option 1**: Content provider offers OA_Gold items in addition to Controlled.

The auditor must carry out a total of 30 tests. Each test will consist of 2 Investigations. There are 2 types of tests that must be carried out:

* “Inside” tests (Two investigations are made to the same journal item, and the second investigation is made within 30 seconds of the first).
* “Outside” tests (Two investigations are made to the same journal item, and the second investigation is made more than 30 seconds after the first).

The auditor must carry out 15 **inside** tests.

8 tests to journal items where the Access_Type is Controlled and 7 tests to journal items where the Access_Type is OA_Gold.

This must result in:

* 8 Controlled Total_Item_Investigations and 7 OA_Gold Total_Item_Investigations in the TR_J3 Standard View.
* 8 Controlled Unique_Item_Investigations and 7 OA_Gold Unique_Item_Investigations in the TR_J3 Standard View.

The auditor must carry out 15 **outside** tests.

8 tests to journal items where the Access_Type is Controlled and 7 tests to journal items where the Access_Type is OA_Gold.

This must result in:

* 16 Controlled Total_Item_Investigations and 14 OA_Gold Total_Item_Investigations in the TR_J3 Standard View.
* 8 Controlled Unique_Item_Investigations and 7 OA_Gold Unique_Item_Investigations in the TR_J3 Standard View.

**Option 2**: Content provider does not offer OA_Gold items.

The auditor must carry out a total of 30 tests. Each test will consist of 2 Investigations.

There are 2 types of tests that must be carried out:

* “Inside” tests (Two investigations are made to the same journal item, and the second investigation is made within 30 seconds of the first).
* “Outside” tests (Two investigations are made to the same journal item, and the second investigation is more than 30 seconds after the first).

The auditor must carry out 15 **inside** tests.

This must result in:

* 15 Controlled Total_Item_Investigations in the TR_J3 Standard View.
* 15 Controlled Unique_Item_Investigations in the TR_J3 Standard View.

The auditor must carry out 15 **outside** tests.

This must result in:

* 30 Controlled Total_Item_Investigations in the TR_J3 Standard View.
* 15 Controlled Unique_Item_Investigations in the TR_J3 Standard View.


E.2.3.8 Standard View: TR_J4
''''''''''''''''''''''''''''

Journal Requests by YOP (excluding OA_Gold): Breaks down the usage of non-Gold Open Access journal content by year of publication (YOP) providing counts for the metric types Total_Item_Requests and Unique_Item_Requests. Note: COUNTER reports do not provide access model or perpetual access rights details.

An audit of this Standard View requires the following:

* The auditor must have access to all journal content available by the content provider. Any exclusions must be confirmed by COUNTER prior to testing and the auditor notified.
* The Access_Type for all requests must be Controlled and not OA_Gold.
* The auditor must record the Year of Publication (YOP) of every item accessed during audit testing.
* The auditor must confirm the Year of Publication (YOP) of articles covered in J4-1 with appropriate and proportionate spot checks, unless the article is “YOP unknown”, then check that YOP is 0001.
* Audit tests J4-1 and J4-2 must take place in separate accounts so that each audit test can be separately reported.
* The auditor must ensure that some full-text articles from different years of the same journal are requested during the J4-1 and J4-2 tests. The auditor should know the numbers expected to appear against each Year of Publication (YOP) in the TR_J4 report.
* The auditor must allow at least 31 seconds between each request unless otherwise specified.
* For each applicable audit test to achieve an audit pass, all metrics reported by the content provider in TR_J4 Standard View from the auditor’s test account must be within a -8% and +3% reliability window of the same audit metrics on the auditor’s report.


Audit Test J4-1: Total_Item_Requests and Unique_Item_Requests
.............................................................

The auditor must make a total of 100 requests on a subset of unique journal items.

This must result in:

* 100 Total_Item_Requests being reported in the TR_J4 Standard View.
* 100 Unique_Item_Requests being reported in the TR_J4 Standard View.


Audit Test J4-2: Total_Item_Requests and Unique_Item_Requests - 30-second filters
.................................................................................

The audit test consists of clicking links to a journal item twice in succession (double-clicks). If the two clicks occur within a 30-second time-span, only the second Total_Item_Requests must be recorded. If the two clicks occur with more than 30 seconds between, then 2 Total_Item_Requests must be counted. In both cases only 1 Unique_Item_Requests will be reported.

The auditor must carry out a total of 30 tests. Each test will consist of 2 requests. There are 2 types of tests that must be carried out:

* “Inside” tests (Two item requests are made to the same journal item and the second request is made within 30 seconds of the first).
* “Outside” tests (Two item requests are made to the same journal item, and the second request is made more than 30 seconds after the first).

The auditor must carry out 15 **inside** tests.

This must result in:

* 15 Total_Item_Requests and 15 Unique_Item_Requests in the TR_J4 Standard View.

The auditor must carry out 15 **outside** tests.

This must result in:

* 30 Total_Item_Requests and 15 Unique_Item_Requests in the TR_J4 Standard View.


E.2.4 Item Reports
""""""""""""""""""

E.2.4.1 Master Report: IR
'''''''''''''''''''''''''

The Item Master Report will be COUNTER compliant if the following Standard Views pass the COUNTER R5 audit. The figures reported in the Standard Views must match the figures reported in the Item Master Report.

Any Standard View not applicable to the content provider does not require auditing. Any exclusions must be agreed prior to the audit by COUNTER.


E.2.4.2 Standard View: IR_A1
''''''''''''''''''''''''''''

This Standard View reports on journal article requests at the article level. This report is limited to content with a Parent_Data_Type of Journal, Data_Type of Article, and metric types of Total_Item_Requests and Unique_Item_Requests.

An audit of this Standard View requires the following:

* The auditor must have access to all journal article content available by the content provider. Any exclusions must be confirmed by COUNTER prior to testing and the auditor notified.
* The auditor must allow at least 31 seconds between each request, unless otherwise specified.
* Audit tests A1-1 and A1-2 must take place in separate accounts so that each audit test can be separately reported.
* An audit pass requires all metrics reported by the content provider in IR_A1 Standard View for the auditor’s test account to be within a -8% and +3% reliability window of the same metrics on the auditor’s report.


Audit Test A1-1: Total_Item_Requests and Unique_Item_Requests
.............................................................

The auditor must make a total of 100 requests on a subset of journal article items.

This must result in:

* 100 Total_Item_Requests being reported in the IR_A1 Standard View.
* 100 Unique_Item_Requests being reported in the IR_A1 Standard View.


Audit Test A1-2: Total_Item_Requests and Unique_Item_Requests - 30-second filters
.................................................................................

The audit test consists of clicking links to a journal article item twice in succession (double-clicks). If the two clicks occur within a 30-second time-span, only the second Total_Item_Requests must be recorded. If the two clicks occur with more than 30 seconds between, then 2 Total_Item_Requests must be counted. In both cases, only 1 Unique_Item_Request will be reported.

The auditor must carry out a total of 30 tests, and each test will consist of 2 requests. There are 2 types of tests that must be carried out:

* “Inside” tests (Two requests are made to the same journal article item, and the second request is made within 30 seconds of the first).
* “Outside” tests (Two requests are made to the same journal article item, and the second request is made more than 30 seconds after the first).

The auditor must carry out 15 **inside** tests.

This must result in:

* 15 Total_Item_Requests and 15 Unique_Item_Requests in the IR_A1 Standard View.

The auditor must carry out 15 **outside** tests.

This must result in:

* 30 Total_Item_Requests and 15 Unique_Item_Requests  in the IR_A1 Standard View.


E.2.4.3 Standard View: IR_M1
''''''''''''''''''''''''''''

Reports on multimedia requests at the item level.

An audit of this Standard View requires the following:

* The auditor must have access to all multimedia content available by the content provider.
* The auditor must allow at least 31 seconds between each request, unless otherwise specified.
* Audit tests M1-1 and M1-2 must take place in separate accounts so that each audit test can be separately reported.
* For each applicable audit test to achieve an audit pass, all metrics reported by the content provider in IR_M1 Standard View from the auditor’s test account must be within a -8% and +3% reliability window of the same audit metrics on the auditor’s report.


Audit Test M1-1: Total_Item_Requests
....................................

The auditor must make a total of 100 requests on a subset of multimedia items.

This must result in:

* 100 Total_Item_Requests being reported in the IR_M1 Standard View.


Audit Test M1-2: Total_Item_Requests - 30-second filters
........................................................

The audit test consists of clicking links to a multimedia item twice in succession (double-clicks). If the two clicks occur within a 30-second time-span, only the second Total_Item_Requests must be recorded. If the two clicks occur with more than 30 seconds between, then 2 Total_Item_Requests must be counted.

The auditor must carry out a total of 30 tests, and each test will consist of 2 requests. There are 2 types of tests that must be carried out:

* “Inside” tests (Two requests are made to the same multimedia item and the second request is made within 30 seconds of the first).
* “Outside” tests (Two requests are made to the same multimedia item, and the second request is made more than 30 seconds after the first).

The auditor must carry out 15 **inside** tests.

This must result in:

* 15 Total_Item_Requests in the IR_M1 Standard View.

The auditor must carry out 15 **outside** tests.

This must result in:

*  30 Total_Item_Requests in the IR_M1 Standard View.
