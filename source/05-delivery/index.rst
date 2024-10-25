.. The COUNTER Code of Practice © 2017-2024 by COUNTER Metrics
   is licensed under CC BY 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by/4.0/

.. _delivery:

Delivery of COUNTER Reports
===========================

Report providers MUST make COUNTER Reports and Standard Views of the COUNTER Reports available in JSON format via the COUNTER API (formerly sushi). Report providers MUST also make tabular versions of their reports available from an administrative/reporting site accessible by members of the institution requesting the report.

* Reports MUST be provided monthly.
* Data MUST be updated within 4 weeks of the end of the reporting period.
* Usage MUST be processed for the entire month before any usage for that month can be included in reports. If usage for a given month is not available yet, the report provider MUST NOT return usage for that month and MUST include exception 3031 in the report/response to indicate that usage is not ready for requested dates.
* A minimum of the current year plus the prior 24 months of usage data MUST be available, unless the report provider is newly COUNTER compliant.
* When report providers become compliant with a new release of the Code of Practice, they begin compiling usage compliant with the new release from the time they become compliant; and they MUST continue to provide the older usage that complies with the previous release(s) of the Code of Practice to fulfil the requirement.
* The reports MUST allow the report consumer the flexibility to specify a date range, in terms of months, within the most recent 24-month period.
* Report providers should provide reports on a per-customer basis where it is possible to do so accurately. That is, if a business school has a separate customer ID from its parent university and it is possible to separately identify usage from each customer ID (e.g. there are different IP ranges for the university and the business school), the school and the university should be sent separate COUNTER reports.

.. toctree::
   :maxdepth: 1

   01-delivering-json-reports
   02-delivering-tabular-reports
   03-access-to-usage-for-consortia
