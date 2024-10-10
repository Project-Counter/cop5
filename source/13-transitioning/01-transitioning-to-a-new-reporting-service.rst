.. The COUNTER Code of Practice Release 5 © 2017-2023 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

Transitioning to a New Reporting Service
----------------------------------------

When a report provider implements a new reporting service, underlying logging system, or approach, they MUST continue to meet the requirement to offer valid COUNTER reports for the current year plus the prior 24 months (or from the date they first became compliant, whichever is later). At a minimum, these reports MUST be available in tabular format with all Attributes via the new reporting service's web interface. The reports SHOULD also be available in JSON via a SUSHI server.


Availability of Previous Reports
""""""""""""""""""""""""""""""""

Report providers SHOULD offer a single report with date ranges that span the transition period. That is, if the new reporting service was deployed in August of 2024 a customer could request a report for January-December 2024 and receive a single report.

When it is not practical to support a single report with date ranges that span the transition period, the report provider SHOULD perform the transition on the first day of a month. If the new reporting service was deployed in August 2024, a customer wanting January-December 2024 usage would request January-July 2024 from the previous reporting service and August-December 2024 from the new reporting service. 

COUNTER Metrics is aware that it is not always possible to transition on the first day of a month (e.g. where a platform is moving from one service provider to another). Where a report provider has no option but to perform the transition mid-month, such that the customer is required to run reports on both the old and new reporting services for the same month, the report provider MUST provide clear guidance about merging and summing the results to obtain actual monthly usage.

Report providers MUST alert code@countermetrics.org in advance of platforms transitioning to a new reporting service to ensure that the `COUNTER Registry <https://registry.countermetrics.org/>`_ remains up to date. Where a platform is migrating from or to a third-party report provider, it is the responsibility of that report provider to ensure that COUNTER is notified. Transition details, including the date of transition, will be noted in the specific platform record and as a notification to report consumers.


Dual Running of Reporting Systems
"""""""""""""""""""""""""""""""""

Report providers have two options in respect of delivering previous reports, where they are unable to offer a single report with date ranges that span the transition period. 

* Support two reporting systems, such that reports on usage dating prior to transition are held in the old reporting service. In this case report consumers will access post-transition reports on the new reporting service and pre-transition reports on the old reporting service.
* Support the pre-transition reports on the new reporting service.
