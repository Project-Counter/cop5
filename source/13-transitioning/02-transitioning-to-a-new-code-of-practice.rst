.. The COUNTER Code of Practice © 2017-2024 by COUNTER Metrics
   is licensed under CC BY 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by/4.0/

.. _transitioning-new-cop:

Transitioning to a New Code of Practice
---------------------------------------

New releases of the COUNTER Code of Practice will typically be assigned an effective date after which a report provider must be compliant. In such cases, a report provider may choose to implement the new release before the effective date.


Compliant Report Providers
""""""""""""""""""""""""""

New releases of the COUNTER Code of Practice may come with specific transition instructions, but, in general, report providers who are already COUNTER-compliant:

* May implement the new release prior to the effective date of the new release while continuing to offer reporting compliant with the existing release.
* Are not required to provide reports compliant with the new release for usage transacted prior to the implementation date; however, they may choose to do so at their discretion.
* MUST continue to meet the requirement to offer valid COUNTER reports for the current year plus the prior 24 months (or from the date they first became compliant, whichever is later) via a web interface and via a SUSHI server.
* MUST provide a means for customers to receive prior-release reports for usage transacted from the report provider’s transition date through to 3 full months after the effective date of the new release. For clarity, once Release 5.1 becomes effective 1 January 2025, report consumers must be able to obtain Release 5.0.3 reports for January, February and March 2025. A report provider can meet this requirement in one of the following ways:

    * Maintain two reporting systems such that usage is logged to the old and new reporting services and customers can access current-release reports on the new reporting service and prior-release reports on the old reporting service.
    * Support the prior-release reports on the new reporting service. This may involve using the metrics from the new release to produce reports formatted to the prior release; or it may involve logging additional data to the new reporting service such that the prior release reports can continue to be supported.
    * If the new release offers metrics compatible with the prior release, offer only new release reports provided customers have access to freely available tools that will automatically generate the required prior release report from an equivalent new release report and meet the requirement that these reports are available in tabular form and via the COUNTER_SUSHI API.
  
* May choose to support COUNTER reports that include a range of months that span the transition period. For example, if the new reporting service compliant with a new COUNTER release was deployed in October of 2024, a customer could request a report for January-December 2024 and receive a single report in either the new release or the previous release (see previous point on the transition period).
* When it is not practical to support a single report with date ranges that span the transition period, the report provider MUST perform the transition on the first day of a month. E.g. if the new reporting service was deployed in October 2024, a customer wanting January-December 2024 usage would request January-September 2024 from the previous reporting service and October-December 2024 from the new reporting service. For clarity, a provider MUST NOT perform the transition mid-month such that the customer is required to run reports on both the old and new reporting services for the same month and merge and sum the results to obtain actual monthly usage.

Report providers MUST alert code@countermetrics.org in advance of transitioning to a new release to ensure that the `COUNTER Registry <https://registry.countermetrics.org/>`_ remains up to date. Transition details, including the date of transition, will be noted in the specific platform record and as a notification to report consumers.


New Report Providers
""""""""""""""""""""

Report providers implementing COUNTER for the first time are encouraged to implement the new release prior to the effective date of the new release. These report providers

* Are not required to provide reports compliant with the new release for usage transacted prior to the implementation date, but may choose to do so at their discretion.
* Are not required to meet the requirement to offer valid COUNTER reports for the current year plus the prior 24 months, but may choose to do so at their discretion.
* Are not required to offer reports compliant with the prior release, but may choose to do so at their discretion.

Report providers implementing COUNTER for the first time are encouraged to contact code@countermetrics.org for advice and support and to request inclusion in the `COUNTER Registry <https://registry.countermetrics.org/>`_ per :numref:`audit`.
