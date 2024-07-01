.. The COUNTER Code of Practice Release 5 © 2017-2023 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

Delivering JSON Reports
-----------------------

* JSON reports MUST be formatted in accordance with the COUNTER API (specification (see :numref:`counterapi`).
* The reports MUST be encoded using UTF-8. JSON reports and other COUNTER API server responses MUST NOT include a byte order mark (according to `RFC 8259, Section 8.1 <https://datatracker.ietf.org/doc/html/rfc8259#section-8.1>`_).
* JSON Reports MUST be "minimal", i.e. information that can be included in a single objects MUST NOT be split into multiple objects:

  * all Items with the same Parent MUST be included in a single Parent_Item object (Item Reports only, avoids duplicate Parent metadata)
  * all Attribute_Performance objects for the same Item/Title/Database/Platform MUST be included in a single Report_Item object (avoids duplicate item metadata)
  * all Performance for the same Attribute combination MUST be included in a single Attribute_Performance object (avoids duplicate Attribute combinations)

* The reports SHOULD not include unnecessary whitespace.
* COUNTER API servers SHOULD use HTTP Compression if the client supports it.
* JSON Reports MUST be available for harvesting via the COUNTER API within 4 weeks of the end of the reporting period.
