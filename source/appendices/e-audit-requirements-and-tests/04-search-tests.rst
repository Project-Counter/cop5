.. The COUNTER Code of Practice Release 5 © 2017-2023 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

E.4 Audit Tests for Search Metrics
----------------------------------

All report providers MUST be subject to the audit tests for Searches_Platform. For report providers operating multiple platforms including one or more of Host_Type A&I_Database, Aggregated_Full_Content, Discovery_Service, eBook_Collection, Full_Content_Database or Multimedia_Collection, the audit scope as defined in :numref:`audit` MUST include one of these platforms and be subject to the audit tests for Searches_Automated and Searches_Regular. 

Audit test requirements vary depending on the set up of the platform, as indicated by the Options within the tests below.


E.4.1 Searches_Platform
"""""""""""""""""""""""

These tests are specific to the Platform Report. The PR_P1 Standard View of the Platform Report will be deemed COUNTER-compliant if the metrics match those in the Platform Report, with the appropriate aggregation.

**Option 1**: Platform has multiple databases and the user can search the whole platform, multiple selected databases, or a single database.

The auditor MUST run 100 searches on the platform

* 50 searches against only 1 selected database.
* 25 searches against 2 selected databases.
* 25 searches against all databases on the platform.

The auditor activity MUST result in 100 Searches_Platform (1 per search).

**Option 2**: Platform has multiple databases and the user can search the whole platform or a single database.

The auditor MUST run 100 searches on the platform

* 50 searches against only 1 selected database.
* 50 searches against all databases on the platform.

The auditor activity MUST result in 100 Searches_Platform (1 per search).

**Option 3**: Platform has multiple databases but the user can only search the whole platform OR the platform has just one database.

The auditor MUST run 100 searches on the platform.

The auditor activity MUST result in 100 Searches_Platform (1 per search).

**Option 4**: Platform has multiple databases but the user can only search a single database at a time.

The auditor MUST run 100 searches across at least 10% of the available databases, restricted to one database at a time.

The auditor activity MUST result in 100 Searches_Platform (1 per search).

**Option 5**: Platform does not include any databases.

The auditor MUST run 100 searches on the platform.

The auditor activity MUST result in 100 Searches_Platform (1 per search).


E.4.2 Searches_Regular and Searches_Automated
"""""""""""""""""""""""""""""""""""""""""""""

These tests are specific to the Database Report. The DR_D1 Standard View of the Database Report will be deemed COUNTER-compliant if the metrics match those in the Database Report, with the appropriate aggregation.

**Option 1**: Platform has multiple databases and the user can search the whole platform, multiple selected databases, or a single database.

The auditor MUST run 100 searches on the platform

* 50 searches against only 1 selected database, resulting in 50 Searches_Regular against that database.
* 25 searches against 2 selected databases, resulting in 25 Searches_Regular against both databases.
* 25 searches against all databases on the platform, resulting in 25 Searches_Regular against every database.

**Option 2**: Platform has multiple databases and the user can search the whole platform or a single database.

The auditor MUST run 100 searches on the platform

* 50 searches against only 1 selected database, resulting in 50 Searches_Regular against that database.
* 50 searches against all databases on the platform, resulting in 50 Searches_Regular against every database.

**Option 3**: Platform has multiple databases but the user can only search the whole platform.

The auditor MUST run 100 searches, resulting in 100 Searches_Automated (1 per search).

**Option 4**: Platform has multiple databases but the user can only search a single database at a time.

The auditor MUST run 100 searches across at least 10% of the available databases, restricted to one database at a time, resulting in 100 Searches_Regular (1 per search).

**Option 5**: Platform has only one database.

The auditor MUST run 50 searches, resulting in 50 Searches_Regular (1 per search).