.. The COUNTER Code of Practice © 2017-2024 by COUNTER Metrics
   is licensed under CC BY 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by/4.0/

.. _api-security:

Authentication and Security for the COUNTER_SUSHI API
-----------------------------------------------------

The COUNTER_SUSHI API MUST be implemented using TLS (HTTPS).

The COUNTER_SUSHI API - excluding the public path /r51/status (see :numref:`api-paths`) - MUST be secured using one or more of the following methods:

* Combination of customer ID and requestor ID
* API key assigned to the organization harvesting the usage

All API paths (excluding the public /r51/status path) MUST be secured with the same method(s). Non-standard techniques (not specified in the Code of Practice and the COUNTER_SUSHI API specification) MUST NOT be used. This includes authorization based on IP addresses.

Report providers who would like to improve the security of their SUSHI server should consider using API keys with secure values (e.g. randomly generated UUIDs). Report providers who already use requestor IDs and/or customer IDs with secure values should consider that adding an API key would require all report consumers to update their SUSHI credentials.

If global reports are available, the customer ID 0000000000000000 should be used for "The World". The report should be available to any valid requestor ID and/or API key.
