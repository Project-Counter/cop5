.. The COUNTER Code of Practice Release 5 © 2017-2021 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

.. _transitioning-new-cop:

Transitioning to a New Code of Practice
---------------------------------------

New releases of the COUNTER Code of Practice will typically be assigned an effective date after which a content provider must be compliant. In such cases, a content provider may choose to implement the new release before the effective date. New releases of the COUNTER Code of Practice may come with specific transition instructions, but, in general, content providers:

* May implement the new release prior to the effective date of the new release.
* Are not required to release reports for usage transacted prior to the implementation date; however, they may choose to do so at their discretion.
* MUST continue to meet the requirement to offer valid COUNTER reports for the current year plus the prior 24 months (or from the date they first became compliant, whichever is later) via a web interface and via a SUSHI server.
* MUST provide a means for customers to receive prior-release reports for usage transacted from the content provider’s transition date through to 3 full months after the effective date of the new release. For clarity, if a new release becomes effective 1 February 2019 and a content provider implements the new release 1 October 2018, a customer must be able to obtain the prior-release usage reports for usage prior to the transition period as well as for usage that occurred in October 2018 to April 2019. A content provider can meet this requirement in one of the following ways:

    * Maintain two reporting systems such that usage is logged to the old and new reporting services and customers can access current-release reports on the new reporting service and prior-release reports on the old reporting service.
    * Support the prior-release reports on the new reporting service. This may involve using the metrics from the new release to produce reports formatted to the prior release; or it may involve logging additional data to the new reporting service such that the prior release reports can continue to be supported.
    * If the new release offers metrics compatible with the prior release, offer only new release reports provided customers have access to freely available tools that will automatically generate the required prior release report from an equivalent new release report and meet the requirement that these reports are available in tabular form and via the COUNTER_SUSHI API.
  
* May choose to support COUNTER reports that include a range of months that span the transition period. E.g. if the new reporting service compliant with a new COUNTER release was deployed in October of 2018, a customer could request a report for January-December 2018 and receive a single report in either the new release or the previous release (see previous point on the transition period).
* When it is not practical to support a single report with date ranges that span the transition period, the content provider MUST perform the transition on the first day of a month. E.g. if the new reporting service was deployed in October 2018, a customer wanting January-December 2018 usage would request January-September 2018 from the previous reporting service and October-December 2018 from the new reporting service. For clarity, a provider MUST NOT perform the transition mid-month such that the customer is required to run reports on both the old and new reporting services for the same month and merge and sum the results to obtain actual monthly usage.
