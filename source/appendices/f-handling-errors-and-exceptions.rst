.. The COUNTER Code of Practice Release 5 © 2017-2023 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

|clearpage|

.. _appendix-f:

Appendix F: Handling Errors and Exceptions
==========================================

Note: The main Code of Practice document takes precedence in the case of any conflicts between it and this appendix.

Exceptions are used both for reporting errors that occur while responding to a COUNTER_SUSHI API call and, when generating a report, for indicating that the report differs from what might be expected. While the COUNTER_SUSHI API Specification (see :numref:`sushi`) defines the API methods and the JSON response formats, including the format for Exceptions (SUSHI_error_model), this appendix defines the permissible Exceptions, that is the Exception Codes, the corresponding Exception Messages and HTTP status codes, and how these Exceptions are expected to be used. Some of the Exceptions also can occur when generating tabular reports at an administrative/reporting site.

There are four types of errors that can occur while responding to COUNTER_SUSHI API calls:

* The base URL, for example the release, or the method is wrong, resulting in an invalid path. In this case the SUSHI server MUST respond with HTTP status code 404. The Exceptions 3000 and 3010 used in Release 4 for indicating that the report or report version isn't supported still exist, but they are deprecated and will be removed in the next major release.
* While processing a COUNTER_SUSHI API call an error occurs that usually prohibits generating the requested report, report list, consortium member list or server status. The SUSHI server MUST respond with the appropriate non-200 HTTP status code and a single Exception in JSON format (see below).
* The SUSHI server detects errors in a report request that can be ignored and processing can continue. The SUSHI server SHOULD continue processing the request and return HTTP status code 200 and the report in JSON format with the appropriate Exceptions in the report header.
* The report differs from what might be expected, for example the report is empty because there was no usage. In this case the report in JSON format MUST be returned with the appropriate Exceptions in the report header.

When requesting a tabular report at an administrative/reporting site, only the last type of error should occur and be included in a report. The website is expected to gracefully handle other errors that might occur while generating the report.

While only a single Exception can be returned for a non-200 HTTP status code, the Exceptions element in the report header allows to return multiple Exceptions with HTTP status code 200, both in JSON and tabular reports. If the SUSHI server detects multiple errors, including some with a non-200 HTTP status code, it MUST only return a single Exception with a non-200 HTTP status code, preferably the one with the lowest Exception Code.

The COUNTER_SUSHI API Specification defines the JSON format for Exceptions as follows:

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
         “example”: “Request was for 2024-01-01 to 2024-12-31; however, usage is only available to 2024-08-31.”
       }
     }
   }

For tabular reports the format for the Exceptions header is defined in :numref:`report-header` of the Code of Practice, Table 3.f, as "*{Exception Code}*: *{Exception Message}* (*{Data}*)" with multiple Exceptions separated by semicolon-space ("; ").

As indicated in the code above, Exceptions in JSON format have the following elements:

* **Code**: The Code is a number that identifies the Exception. See Table F.1 below for permissible values.
* **Severity:** In Release 4 the Severity element was used to indicate the severity of the Exception (Fatal, Error, Warning, Info or Debug). The RESTful COUNTER_SUSHI API in Release 5 instead uses HTTP status codes to indicate if the response is a (fatal) error (non-200 HTTP status code) or not (HTTP status code 200). The Severity element therefore is deprecated and will be removed in the next major release. SUSHI clients should stop relying on Severity and use the HTTP status code and Exception Code instead.
* **Message**: The Message element contains a textual description of the Exception. For standard Exceptions with Codes > 999 the Message MUST exactly match the Message in Table F.1 below.
* **Data:** The Data element contains additional information that further describes the Exception. For some Exceptions this additional information MUST be provided (as indicated in Table F.1 below), for other Exceptions it is optional.
* **Help_URL**: An optional element that contains an URL to a help page that explains the Exception in more detail.

Table F.1 lists all Exceptions permissible for the COUNTER_SUSHI API. Note that the standard Exceptions with Code > 999 MUST be used for the indicated invocation conditions, it is neither permitted to use custom Exceptions with Code <= 999 instead nor to define custom Exceptions with Code > 999.

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

   * - *{Info or Debug Message}*
     - Info\ |br|\ |lb|
       Debug
     - 0
     - 200
     - Any. These Messages will never be standardized and service providers can design them as they see fit.

   * - *{Warning Message}*
     - Warning
     - 1-999
     - 200
     - Any. This range is reserved for the use of service providers to supply their own custom warnings.

   * - Service Not Available
     - Fatal
     - 1000
     - 503
     - The service is executing a request, but due to internal errors cannot complete the request. If possible, the server should provide an explanation in the additional Data element.

   * - Service Busy
     - Fatal
     - 1010
     - 503
     - The service is too busy to execute the incoming request. The client should retry the request after some reasonable time.

   * - Report Queued for Processing
     - Warning
     - 1011
     - 202
     - Services queueing incoming report requests must return a response with this Exception and no payload to inform the client about the processing status. The client should retry the request after some reasonable time.

       Note: This Exception was included in the `amendments published on 11 December 2018 <https://www.projectcounter.org/amendments-clarifications-code-practice-release-5/>`__ but initially was missing from Release 5.0.1.

   * - Client has made too many requests
     - Fatal
     - 1020
     - 429
     - If the service sets a limit on the number of requests a client can make within a given timeframe, the server will return this Exception when the client exceeds that limit. The server would provide an explanation of the limit in the additional Data element (e.g. “Client has made too many requests. This server allows only 5 requests per day per requestor_id and customer_id.”).

   * - Insufficient Information to Process Request
     - Fatal
     - 1030
     - 400
     - There is insufficient data in the request to begin processing (e.g. missing requestor_id, no customer_id, etc.).

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
     - The service requires a valid APIKey to access usage data and the key provided was not valid or not authorized for the data being requested.

   * - IP Address Not Authorized to Access Service
     - Error
     - 2030
     - 401
     - The service requires IP authorization, and the IP address used by the client is not authorized. The server MUST include information on how this issue can be resolved in the Data element or include a Help_URL that points to the information.

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
     - The requested version of the report is not supported by the service.

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
     - The service did not find any data for the date range specified.

       Note: If the usage for a requested month either hasn’t been processed yet or is no longer available, only Exception 3031 or 3032 must be returned for that month.

   * - Usage Not Ready for Requested Dates
     - Error, Warning
     - 3031
     - 200
     - The service has not yet processed the usage for one or more of the requested months, if some months are available that data should be returned. The Exception should include the months not processed in the additional Data element.

       Note: If the requested begin_date is the current or a future month, the server should return Exception 3020. If the requested end_date is the current or a future month, the server may continue processing the request and include Exception 3031, the End_Date Report_Filter then should be set to the previous month (the last month that could have been processed).

   * - Usage No Longer Available for Requested Dates
     - Warning
     - 3032
     - 200
     - The service does not have the usage for one or more of the requested months because the requested begin_date is earlier than the available data. If some months are available that data should be returned. The Exception should include the months not processed in the additional Data element.

       Note: This Exception was included in the `amendments published on 11 December 2018 <https://www.projectcounter.org/amendments-clarifications-code-practice-release-5/>`__ but initially was missing from Release 5.0.1.

   * - Partial Data Returned
     - Warning
     - 3040
     - 200
     - The request could not be fulfilled in its entirety, since some of the requested data is missing. The server should return the available data and provide an explanation in the additional Data element.

       Note: This Exception is not intended for the conditions already covered by Exceptions 3030, 3031 and 3032. A use case for this Exception for example would be that usage data is missing because the logging has failed. Usually this Exception indicates a permanent error.

   * - Parameter Not Recognized in this Context
     - Warning
     - 3050
     - 200
     - The request contained one or more parameters that are not recognized by the server in the context of the report being serviced. The server should list the names of unsupported parameters in the additional Data element.

       Note: The server is expected to ignore unsupported parameters and continue to process the request, returning data that is available without the parameter being applied.

       Note: This Exception is only applicable for report requests. For report list, member list and server status requests parameters not recognized by the server should be ignored.

   * - Invalid ReportFilter Value
     - Warning\ |br|\ |lb|
       Error
     - 3060
     - 200
     - The request contained one or more filter values that are not supported by the server. The server should list the names of unsupported filter values in the additional Data element.

       Note: The server is expected to ignore unsupported filters and continue to process the request, returning data that is available without the filter being applied.

       Note: If the begin_date or end_date value is invalid, the server must return Exception 3020. If the service requires a platform parameter, and the platform value is invalid, the server should return Exception 1030.

   * - Incongruous ReportFilter Value
     - Warning\ |br|\ |lb|
       Error
     - 3061
     - 200
     - A filter element includes multiple values in a pipe-delimited list; however, the supplied values are not all of the same scope (e.g., item_id filter includes article level DOIs and journal level DOIs or ISSNs).

       Note: The server is expected to ignore the invalid filters and continue to process the request, returning data that is available without the filter being applied.

   * - Invalid ReportAttribute Value
     - Warning\ |br|\ |lb|
       Error
     - 3062
     - 200
     - The request contained one or more report attribute values that are not supported by the server. The server should list the names of unsupported report attribute values in the additional Data element.

       Note: The server is expected to ignore unsupported report attributes and continue to process the request, returning data that is available without the report attribute being applied.

   * - Required ReportFilter Missing
     - Warning\ |br|\ |lb|
       Error
     - 3070
     - 200
     - A required filter was not included in the request. Which filters are required will depend on the report and the service being called. The server should list the names of the missing filters in the additional Data element.

       Note: If begin_date or end_date is missing, the server must return Exception 1030. If the service requires a platform parameter, and platform is missing, the server also should return Exception 1030.

       Note: Currently there are no other required report filters, so this Exception should not occur.
