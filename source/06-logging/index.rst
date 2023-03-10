.. The COUNTER Code of Practice Release 5 © 2017-2023 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

.. _logging:

Logging Usage
=============

Usage data can be generated in a number of ways, and COUNTER does not prescribe which approach should be taken. The two most common approaches are:

* Log file analysis, which reads the log files containing the web server records of all its transactions
* Page tagging, which uses JavaScript on each page to notify a third-party server when a page is rendered by a web browser.

Other options are to leverage Distributed Usage Logging (DUL) to capture content activity that happens on other websites. Each of these approaches has advantages and disadvantages, summarised below.

.. toctree::
   :maxdepth: 1

   01-log-file-analysis
   02-page-tagging
   03-distributed-usage-logging
