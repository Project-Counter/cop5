.. The COUNTER Code of Practice Release 5 © 2017-2023 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

Distributed Usage Logging
-------------------------

Distributed Usage Logging (DUL) was an initiative sponsored by Crossref that provides a framework for publishers to capture usage of DOI-identified content items that occurs on other websites, such as aggregators, repositories, and scholarly information-sharing sites. The premise behind DUL was that publishers could register a DUL usage logging end-point with Crossref, which was then mapped to all of the publisher’s DOIs. A content site, such as a repository, could use a content item’s DOI to look up where the publisher wants a transaction to be logged, then use the standard DUL message structure to log the activity. Using DUL could allow a publisher to capture a more complete picture of content usage. The following points cover how DUL may be used with COUNTER statistical reporting:

* DUL is not a replacement for log file analysis or page-tagging approaches. DUL can supplement a publisher’s normal usage logging mechanisms, but not replace them.
* DUL-captured usage MUST NOT appear on Standard Views.
* DUL-captured usage may appear on Master Reports.
* DUL-captured usage that appears on Master Reports MUST be reported under the platform name where the transaction occurred.
* The platform name MUST include the namespace DUL (i.e. MUST be in the format of DUL:*{platform name}*), so that DUL-captured usage can be identified and excluded when creating a Standard View from a Master Report.
* An organization that supplies usage transactions using DUL MUST include their platform ID with each transaction, and their platform MUST be registered with COUNTER.
* Reporting usage through DUL is OPTIONAL.
* The publisher receiving transactions through DUL is responsible for performing COUNTER processing to eliminate double-clicks, eliminate robot/crawler or other rogue usage, and perform the actions to identify unique items and unique titles.
* Publishers that plan to include usage reported through DUL in their COUNTER Master Reports are responsible for ensuring that DUL-reported usage is included in the audit.

The Crossref project has terminated but this process could be used by content providers to capture usage activity related to their content that happens on sites other than their own.
