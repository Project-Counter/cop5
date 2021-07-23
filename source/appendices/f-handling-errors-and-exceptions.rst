.. The COUNTER Code of Practice Release 5 © 2017-2021 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

|clearpage|

.. _appendix-f:

Appendix F: Handling Errors and Exceptions
==========================================

As a rule, the structure of the SUSHI response will be governed by the SUSHI schema; therefore, any error conditions that can be reported will be specified within the SUSHI response. The following is a definition of from the COUNTER_SUSHI API Specification that shows the format of the exception.

.. code-block:: json-object

   “SUSHI_error_model”: {
     “type”: “object”,
     “description”: “Generalized format for presenting errors and warnings.”,
     “required”: [ “Code”, “Severity”, “Message” ],
     “properties”: {
       “Code”: {
         “type”: “integer”,
         “format”: “int32”,
         “description”: “Exception Code. See Table F.1 in the Code of Practice, Appendix F.”,
         “example”: 3031
       },
       “Severity”: {
         “type”: “string”,
         “description”: “Severity of the Exception (deprecated).”,
         “example”: “Warning”,
         “enum”: [ “Warning”, “Error”, “Fatal”, “Debug”, “Info” ]
       },
       “Message”: {
         “type”: “string”,
         “description”: “Exception Message. See Table F.1 in the Code of Practice, Appendix F.”,
         “example”: “Usage Not Ready for Requested Dates”
       },
       “Help_URL”: {
         “type”: “string”,
         “description”: “URL to a help page that explains the Exception in more detail.”
       },
       “Data”: {
         “type”: “string”,
         “description”: “Additional data provided by the server to clarify the Exception.”,
         “example”: “Request was for 2016-01-01 to 2016-12-31; however, usage is only available to 2016-08-31.”
       }
     }
   }

As indicated in the JSON code above, multiple exceptions can be returned and the exceptions have the following elements:

* **Code**: is a numeric exception number that identifies the exception. See table F.1 for permissible values.
* **Severity:** In Release 4 the Severity element was used to indicate the severity of the Exception (Fatal, Error, Warning, Info or Debug). The RESTful COUNTER_SUSHI API in Release 5 instead uses HTTP status codes to indicate if the response is a (fatal) error (non-200 HTTP status code) or not (HTTP status code 200). The Severity element therefore is deprecated and will be removed in the next major release. SUSHI clients should stop relying on Severity and use the HTTP status code and Exception Code instead.
* **Message**: textual description of the exception. For exception Codes &gt; 999 the Message must exactly match column 1 in table F.1.
* **Data:** additional optional data that further describes the error. Example: for “Partial Data Returned” exception, the Data could state “You requested 2017-01-01 to 2017-12-31; however, only 2017-01-01 to 2017-06-30 were available.”
* **Help_URL**: an optional variable that includes the URL to a help message that explains the exception in more detail.

Table F.1 provides a list of possible exceptions that may occur for the COUNTER_SUSHI API. Note that some of the exceptions also may occur for tabular reports.

Table F.1 (below): Exceptions

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.21}|>{\raggedright\arraybackslash}\Y{0.11}|>{\raggedright\arraybackslash}\Y{0.12}|>{\raggedright\arraybackslash}\Y{0.09}|>{\parskip=\tparskip}\Y{0.47}|

.. list-table::
   :class: longtable
   :widths: 20 9 10 7 54
   :header-rows: 1

   * - Exception Message
     - Severity
     - Exception Code
     - HTTP Status Code
     - Invocation Conditions

   * - Info or Debug
     - Info\ |br|\ |lb|
       Debug
     - 0
     - 200
     - Any. These Messages will never be standardized and service providers can design them as they see fit.

   * - Warnings
     - Warning
     - 1-999
     - 200
     - Any. This range is reserved for the use of service providers to supply their own custom warnings.

   * - Service Not Available
     - Fatal
     - 1000
     - 503
     - Service is executing a request, but due to internal errors cannot complete the request.

   * - Service Busy
     - Fatal
     - 1010
     - 503
     - Service is too busy to execute the incoming request. Client should retry the request after some reasonable time.

   * - Report Queued for Processing
     - Warning
     - 1011
     - 202
     - Services queuing incoming report requests must return a response with this exception and no payload to inform the client about the processing status. Client should retry the request after some reasonable time.

       Note: This Exception was included in the `amendments published on 11 December 2018 <https://www.projectcounter.org/amendments-clarifications-code-practice-release-5/>`__ but initially was missing from Release 5.0.1.

   * - Client has made too many requests
     - Fatal
     - 1020
     - 429
     - If the server sets a limit on the number of requests a client can make within a given timeframe, the server will return this error when the client exceeds that limit. The server would provide an explanation of the limit in the additional Data element (e.g., “Client has made too many requests. This server allows only 5 requests per day per requestor_id and customer_id.”).

   * - Insufficient Information to Process Request
     - Fatal
     - 1030
     - 400
     - There is insufficient data in the request to begin processing (e.g., missing requestor_id, no customer_id, etc.).

   * - Requestor Not Authorized to Access Service
     - Error
     - 2000
     - 401
     - If requestor_id is not recognized or not authorized by the service.

   * - Requestor is Not Authorized to Access Usage for Institution
     - Error
     - 2010
     - 403
     - If requestor_id has not been authorized to harvest usage for the institution identified by the customer_id, or if the customer_id is not recognized.

   * - APIKey Invalid
     - Error
     - 2020
     - 401
     - The service being called requires a valid APIKey to access usage data and the key provided was not valid or not authorized for the data being requested.

   * - Report Not Supported
     - Error
     - 3000
     - 404
     - The requested report name, or other means of identifying a report that the service can process is not matched against the supported reports.

       In Release 5 the requested report is part of the URL path, and for RESTful APIs the HTTP status code 404 is used to signal that a path isn’t supported. Therefore this Exception is deprecated and will be removed in the next major release. SUSHI clients should stop relying on this Exception and use the HTTP status code instead.

   * - Report Version Not Supported
     - Error
     - 3010
     - 404
     - Requested version of the report is not supported by the service.

       In Release 5 the requested report version is part of the URL path, and for RESTful APIs the HTTP status code 404 is used to signal that a path isn’t supported. Therefore this Exception is deprecated and will be removed in the next major release. SUSHI clients should stop relying on this Exception and use the HTTP status code instead.

   * - Invalid Date Arguments
     - Error
     - 3020
     - 400
     - Any format or logic errors involving date computations (e.g., end_date cannot be less than begin_date).

   * - No Usage Available for Requested Dates
     - Error
     - 3030
     - 200
     - Service did not find any data for the date range specified.

   * - Usage Not Ready for Requested Dates
     - Error, Warning
     - 3031
     - 200
     - Service has not yet processed the usage for one or more of the requested months, if some months are available that data should be returned. The exception should include the months not processed in the additional Data element.

   * - Usage No Longer Available for Requested Dates
     - Warning
     - 3032
     - 200
     - Service does not have the usage for one or more of the requested months because the requested Begin_Date is earlier than the available data. If some months are available that data should be returned. The Exception should include the months not processed in the additional Data element.

       Note: This Exception was included in the `amendments published on 11 December 2018 <https://www.projectcounter.org/amendments-clarifications-code-practice-release-5/>`__ but initially was missing from Release 5.0.1.

   * - Partial Data Returned
     - Warning
     - 3040
     - 200
     - Request could not be fulfilled in its entirety. Data that was available was returned.

   * - Parameter Not Recognized in this Context
     - Warning
     - 3050
     - 200
     - Request contained one or more parameters that are not recognized by the server in the context of the report being serviced. The server should list the names of unsupported parameters in the additional Data element of the exception.

       Note: The server is expected to ignore unsupported parameters and continue to process the request, returning data that is available without the parameter being applied.

   * - Invalid ReportFilter Value
     - Warning\ |br|\ |lb|
       Error
     - 3060
     - 200
     - Request contained one or more filter values that are not supported by the server. The server should list the names of unsupported filter values in the additional Data element of the exception.

       Note: The server is expected to ignore unsupported filters and continue to process the request, returning data that is available without the filter being applied.

   * - Incongruous ReportFilter Value
     - Warning\ |br|\ |lb|
       Error
     - 3061
     - 200
     - A filter element includes multiple values in a pipe-delimited list; however, the supplied values are not all of the same scope (e.g., item_id filter includes article level DOIs and journal level DOIs or ISSNs).

   * - Invalid ReportAttribute Value
     - Warning\ |br|\ |lb|
       Error
     - 3062
     - 200
     - Request contained one or more report attribute values that are not supported by the server. The server should list the names of unsupported report attribute values in the additional Data element of the exception.

       Note: The server is expected to ignore unsupported report attributes and continue to process the request, returning data that is available without the report attribute being applied.

   * - Required ReportFilter Missing
     - Warning\ |br|\ |lb|
       Error
     - 3070
     - 200
     - A required filter was not included in the request. Which filters are required will depend on the report and the service being called. For example, if the service requires that the request define the Platform name and no Platform filter is included, an exception would be returned. In general, the omission of a required filter would be viewed as an <em>Error</em>; however, if the service is able to process the request using a default value then a <em>Warning</em> can be returned. The additional Data element of the exception should name the missing filter.

   * - Required ReportAttribute Missing
     - Warning\ |br|\ |lb|
       Error
     - 3071
     - 
     - A required report attribute was not included in the request. For example, if the service requires that the request define the Platform name and no Platform filter is included, an exception would be returned. In general, the omission of a required attribute would be viewed as an <em>Error</em>; however, if the service is able to process the request using a default value, then a <em>Warning</em> can be returned. The additional Data element of the exception should name the missing filter.

   * - Limit Requested Greater than Maximum Server Limit
     - Warning
     - 3080
     - 
     - The requested value for limit (number of items to return) exceeds the server limit. The server is expected to return data in the response (up to the limit). The Message element of the exception should indicate the server limit.

Note 1: An Error does not interrupt completion of the transaction (in the sense of a programmatic failure), although it may not return the expected report for the reason that is identified. A Fatal exception does not complete the transaction; the problem may be temporary and a retry could be successful.

Note 2: Optional response: Service may respond with the additional exception of Info level and include additional information in the Message. For example, if the client is requesting data for a date range where the begin_date is before what the service offers, the service might include a HelpURL that can provide more information about supported dates.

Note 3: If multiple exceptions are discovered, each exception should be returned in its own element.

Note 4: Clarifying details about an exception (e.g., the filter that was missing or deemed invalid should be added to the Data element or, for custom warnings, the Message element of the exception so that the caller knows what to correct).

Note 5: If the caller gets the baseURL, the version, or method wrong, the expectation is that they will receive an HTTP 404 error since the specified path is not valid.
