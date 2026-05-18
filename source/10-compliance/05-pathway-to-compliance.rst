.. The COUNTER Code of Practice © 2017-2024 by COUNTER Metrics
   is licensed under CC BY 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by/4.0/

.. _compliance-pathway:

Pathway to Compliance
---------------------

For smaller publishers, full COUNTER compliance can be a major technical challenge. This section identifies incremental steps for non-compliant publishers to make their usage reporting easier to access and more valuable to report consumers.


Eligibility
"""""""""""

Small publishers who are not compliant with R5.1, and who were not compliant with the older R5, may apply to COUNTER for inclusion in the `COUNTER Registry <https://registry.countermetrics.org/>`_ under the terms of the Pathway To Compliance.

For the purposes of the Pathway, a small publisher is one with a single platform, where that platform includes up to 150 books OR 15 journals OR one database. This aligns with the definition of small publishers eligible for alternate year audits in :numref:`alternate-year-audits`.

Publishers who join the Pathway MUST

* Be members of COUNTER.
* Comply with the requirements defined in this section.
* Commit to reaching full compliance as and when COUNTER migrates to a future Release 5.2 (not before January 2030).


Requirements
""""""""""""

Data
''''

Publishers on the Pathway MUST process their raw usage data in compliance with the requirements of the Code of Practice, specifically :numref:`processing`.


Reports
'''''''

.. rubric:: Required Reports

Publishers on the Pathway are only REQUIRED to provide the Platform Report, plus the Database, Title and/or Item Reports as relevant.

Standard Views derived from the COUNTER Reports are optional.

The Executive Director is available to help publishers identify which COUNTER Reports are required based on the publisher’s Host_Type.

.. rubric:: Report Filters and Attributes

Per :numref:`filters-attributes`, customized views are created by applying report filters and report attributes to the COUNTER Reports. Report attributes define the columns (elements) and report filters the rows (values) included in the reports. Publishers on the Pathway who are technically able to support the full COUNTER filter options for each report SHOULD do so. That is:

* Filtering the Platform Report by all of Data_Type, Access_Method, Metric_Type, and Exclude_Monthly_Details.
* Filtering the Database Report by all of Data_Type, Access_Method, Metric_Type, and Exclude_Monthly_Details.
* Filtering the Title Report by all of Data_Type, YOP, Access_Type, Access_Method, Metric_Type, and Exclude_Monthly_Details.
* Filtering the Item Report by all of Data_Type, YOP, Access_Type, Access_Method, Metric_Type, Include_Parent_Details, Include_Component_Details, and Exclude_Monthly_Details.

Where publishers on the Pathway allow the full set of filter options, they MUST specify which attributes are included in the report via Attributes_To_Show.

Publishers on the Pathway who cannot support the full COUNTER filter options for each report MUST include all attributes in all reports by default.

.. rubric:: Report Format

Publishers on the Pathway MUST provide their reports in standard COUNTER formats, as described in :numref:`formats`.

* Delivery of both tabular and JSON formats is preferred.
* Where only one format is available, publishers on the Pathway SHOULD provide reports in JSON format.
* Where JSON is not an option, tabular reports in TSV or Excel format are acceptable.

.. rubric:: Report Frequency and Granularity

Publishers on the Pathway MUST provide at least one set of reports each year, showing the Reporting_Period_Total usage for the calendar year (e.g. January to December 2026). More regular (quarterly or monthly) reports are preferred, but we acknowledge this may not be viable for the smallest publishers.

Publishers on the Pathway MUST offer month-by-month breakdowns within their reports, in line with :numref:`formats`.

.. rubric:: Report Delivery

Publishers on the Pathway SHOULD facilitate report delivery through the COUNTER API (formerly sushi) for automated report harvesting.

Publishers who are unable to create a COUNTER API due to lack of technical resources MUST make it possible for librarians to set up an alternative automated report delivery system. The minimum requirement is to allow librarians to register once to receive a regular delivery of their reports via email.


Metrics
'''''''

.. rubric:: Usage

Publishers on the Pathway MUST provide COUNTER usage metrics:

* Total_Item_Investigations
* Unique_Item_Investigations
* Total_Item_Requests
* Unique_Item_Requests
* Unique_Title_Investigations (for platforms including Books and/or Reference_Works)
* Unique_Title_Requests (for platforms including Books and/or Reference_Works).

.. rubric:: Denials

Publishers on the Pathway SHOULD provide denial metrics where these are relevant (for example, OA publishers will not have denial metrics):

* No_License
* Limit_Exceeded

.. rubric:: Search

Publishers on the Pathway with a database Host_Type SHOULD provide Searches_Regular in the Database Report. That includes these Host_Types:

* A&I_Database
* Aggregated_Full_Content
* Discovery_Service
* eBook_Collection
* Full_Content_Database
* Multimedia_Collection

As publishers on the Pathway will only ever have one database on the platform, the Searches_Platform metric would always be identical to the Searches_Regular and SHOULD also be provided in the Platform Report.

Search metrics are OPTIONAL for all other publishers on the Pathway (e.g. eJournal and eBook Host_Types).

.. rubric:: Non-COUNTER Metrics

Publishers on the Pathway MUST NOT include any non-COUNTER metrics in their COUNTER Reports except as outlined in :numref:`extending`.


Transparency and Verification
"""""""""""""""""""""""""""""

.. _pathway-technical-validity:

Technical Validity
''''''''''''''''''

Publishers on the Pathway, like all publishers, are RECOMMENDED to use the free `COUNTER Validator <https://validator.countermetrics.org/>`_ regularly to make sure their reports remain technically accurate.

* Where they are available, tabular reports from publishers on the Pathway MUST pass the checks included in the Validator.
* Where they are available, JSON reports from publishers on the Pathway MUST pass the checks included in the Validator.
* Where it is available, the COUNTER API from publishers on the Pathway MUST pass the checks included in the Validator.

Publishers on the Pathway MUST share a complete set of Validator results with COUNTER annually to demonstrate technical validity. A complete set of Validator results is defined as including

* Results for at least two iterations versions of each COUNTER Report with all attributes the publisher MUST deliver (e.g. two Platform Reports sent to two different institutions) in each format (tabular and/or JSON)
* Results for at least two iterations versions of each report the publisher COULD deliver (e.g. if Standard Views are offered) in each format.
* Results of tests for each COUNTER API endpoint.


Audit and Manual Assessment
'''''''''''''''''''''''''''

Publishers on the Pathway To Compliance are not subject to formal audits per :numref:`audit`.

If errors are reported by more than three report consumers in one calendar month, or by more than six report consumers over a rolling three-month period, COUNTER will trigger an investigation into the report provider's compliance status. This will include

* Seeking additional feedback from other libraries via the COUNTER listserv.
* Requiring a repeat technical assessment as described in :numref:`pathway-technical-validity`.


Fixing Issues
'''''''''''''

Where issues are identified, either during the annual Technical Validity checks or through the Manual Assessment mechanism, publishers on the Pathway will have six months to fix the problem. This is in line with the maximum period for fixing issues identified during a formal audit.

At the end of the fix period, COUNTER will re-test as described in Technical Validity. Publishers on the Pathway who fail to pass the checks after the fix period expires will be delisted from the COUNTER Registry.
