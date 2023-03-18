.. The COUNTER Code of Practice Release 5 © 2017-2023 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

Authentication and Security for COUNTER_SUSHI API
-------------------------------------------------

The COUNTER_SUSHI API MUST be implemented using TLS (HTTPS).

The API MUST be secured using one or more of the following methods:

* Combination of customer ID and requestor ID
* IP address of the SUSHI client
* API key assigned to the organization harvesting the usage

Non-standard techniques for authentication (techniques not specified in the COUNTER_SUSHI API specification) MUST NOT be used.

If IP address authentication is implemented, it MUST allow the same SUSHI client (a single IP address) to harvest usage for multiple customer accounts (e.g. hosted ERM services).

If global reports are available, the customer ID 0000000000000000 should be used for "The World". The report should be available to any valid requestor ID and/or API key.
