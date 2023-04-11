E.9 Audit Tests for Denials
---------------------------

Report providers operating platforms where turnaways or denials are in operation MUST be subject to audit tests for denials. For report providers operating multiple platforms, the audit scope as defined in :numref:`audit` MUST include platforms where turnaways or denials are in operation. Where either Limit_Exceeded or No_License denials do not apply to a report provider, auditors MUST note this in the audit report. This does not require an exemption from the COUNTER Project Director.

These audit tests apply to denial metrics across all COUNTER Reports and should represent the scope of the platform under audit. That is, where a platform is made up of a mixture of content with Data_Types Article, Multimedia and Patent, the auditor SHOULD represent each of those Data_Types proportionately in the audit test.


E.9.1 Limit_Exceeded
""""""""""""""""""""

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


E.9.2 No_Licence
""""""""""""""""

The content for which the auditor has no license MUST be declared by the report provider prior to audit testing.

The auditor MUST force 50 No_License turnaways by logging into the site and requesting an item. Each time access is refused, the auditor will record this as 1 No_License.

The test MUST result in 50 No_License.
