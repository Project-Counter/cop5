
.. The COUNTER Code of Practice Release 5 © 2017-2023 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

|clearpage|

.. _appendix-b:

Appendix B: Changes from Release 5
==================================

Note: The main Code of Practice document takes precedence in the case of any conflicts between it and this appendix.

Starting with Release 5.0.2 the COUNTER Code of Practice Release 5 is maintained in the GitHub repository `Project-Counter/cop5 <https://github.com/Project-Counter/cop5>`_, and all changes are tracked with GitHub issues and linked pull requests. The `change log <https://github.com/Project-Counter/cop5/blob/5.1/CHANGELOG.rst>`_ lists all changes by type and impact of the change.


Primary changes between R5 and R5.1
"""""""""""""""""""""""""""""""""""

* **Item becoming the unit of reporting** - Improved OA reporting is one of the major objectives of R5.1, which requires reporting at the level of the item. This impacts on reporting of book usage: under R5.1, usage of each Book_Segment (e.g. chapter) MUST be reported as a separate item investigation or request, with multiple item investigations or requests rolled up to 1 title investigation or request per book.
* **Data_Type** - Many publishers reported difficulties with the restricted list of Data_Types provided in R5, so the list has been expanded and the definitions and use of each Data_Type clarified.
* **Section_Type** - The impact of the above changes means Section_Type is removed in R5.1.
* **Access_Type** - R5.1 clarifies where and how COUNTER Access_Types apply. R5.1 also introduced revised definitions for Access_Types to better facilitate reporting of open and free materials.
* **Components** - Required for the Item Report in R5, Components are optional in R5.1 to simplify delivery of Item Reports.
* **Report headers** - R5.1 added a link to the `COUNTER Registry <https://registry.countermetrics.org>`_ to the standard report header in both JSON and tabular reports.


SUSHI changes between R5 and R5.1
"""""""""""""""""""""""""""""""""

* **COUNTER_SUSHI API** - The COUNTER_SUSHI API can now be found at `Stoplight.io <https://countermetrics.stoplight.io/docs/counter-sushi-api>`_.
* **SUSHI URLs** - Starting with Release 5.1, the release version number will need to be included in the SUSHI URL path.
* **SUSHI authentication** - R5.1 removes support for IP-based authentication in the COUNTER_SUSHI API. API key may be used if a replacement is desired.
* **SUSHI paths** - The /r51/status path is public to allow report consumers to easily check whether a service is live. The /r51/reports endpoint is extended to return information about the first and last months for which data are available. We are also introducing separate parameters for common extensions.


JSON changes between R5 and R5.1
""""""""""""""""""""""""""""""""

* **Compact** - to avoid problems with large reports, and easier to process:

  * Parent_Items include Report_Items to avoid duplicate parent metadata.
  * Report_Items include an Attribute_Performance object to avoid duplicate item metadata.
  * Performance is more compact and easier to read.

* **Reflect all other changes**

  * Changes in the Code of Practice.
  * Changes related to the COUNTER_SUSHI API.

* **JSON** - format updated to be more in line with standard JSON and thus easier to work with.
* **Alignment** - removed deviations between the JSON and tabular reports.



Smaller and optional changes
""""""""""""""""""""""""""""

* **Global Reports** - R5 introduced the concept of “The World” reporting - that is, a report showing total global usage of content, wherever it comes from (institutional or otherwise). R5.1 recommends that all report providers should provide reports at the global level.
* **Item Reports** - Other changes introduced in R5.1 (e.g. optional Components) simplify delivery of Item Reports. All Host_Types are therefore encouraged to offer the IR.
* **Global Item Reports** - All Host_Types are encouraged to provide a Global Item Report.
* **Report naming** - R5.1 uses the terms COUNTER Reports and Standard Views of COUNTER Reports in place of Master Reports and Standard Views.
* **Audits** - The audit process is clarified and the audit scripts rationalised in R5.1 compared with R5.
* **Versioning** - We have clarified the versioning process for future Code of Practice releases.
