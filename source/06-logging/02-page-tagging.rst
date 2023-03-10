.. The COUNTER Code of Practice Release 5 © 2017-2023 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

Page Tagging
------------

The main advantages of page tagging over log file analysis are:

* Counting is activated by opening the page, not requesting it from the server. If a page is cached it will not be counted by the server. Cached pages can account for a significant proportion of page views.
* Data is gathered via a component (tag) in the page, usually written in JavaScript although Java can also be used. JQuery and AJAX can also be used in conjunction with a server-side scripting language (such as PHP) to manipulate and store it in a database, allowing complete control over how the data is represented.
* The script may have access to additional information on the web client or on the user, not sent in the query.
* Page tagging can report on events that do not involve a request to the web server.
* Page tagging is available to companies who do not have access to their own web servers.
* The page-tagging service manages the process of assigning cookies to visitors; with log file analysis, the server must be configured to do this.
* Recently page tagging has become a standard in web analytics.
* Log file analysis is almost always performed in-house. Page tagging can be done in-house, but is more often provided as a third-party service. The cost differences between these two models can also be a consideration.
