.. The COUNTER Code of Practice Release 5 © 2017-2023 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

Log File Analysis
-----------------

Log files are text files representing individual HTTP requests, including the user host name or IP address, the date and time of the request, the requested file name, the HTTP response status and size, the referring URL and the browser information. HTTP requests are what happen when a user tries to access a web page, while an HTTP response is the delivery of that page to the user’s browser.

Most web servers produce log files by default in a pre-defined format which may differ by server type. The log file data needed for a COUNTER implementation should be available without changes to the platform.

As log file data is held on servers in a standard format, report providers can use a variety of analytics programmes and receive consistent results over time. Log files are also independent of users’ web browsers, meaning report providers can reliably track all activity for the purposes of COUNTER reporting.

Report providers wishing to learn more about log files should read the Amazon Web Service documentation (https://docs.aws.amazon.com/).

Other things to note in respect of log file analysis are:

* Log files contain information on visits from spiders and robots. Although these MUST NOT be reported as part of user activity, it is useful information for search engine optimization.
* Log files require no additional DNS lookups. Thus, there are no external server calls which can slow page load speeds or result in uncounted page views.
* Cached pages are not requested from the server and therefore do not appear in log file analysis, although cached pages can account for a sizeable proportion of usage.
