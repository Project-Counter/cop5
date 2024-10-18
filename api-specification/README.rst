COUNTER_SUSHI API Specification
===============================

Starting with R5.1, the specification for the RESTful COUNTER_SUSHI API uses JSON schema for the JSON format, and OpenAPI 3.1 for the API. The COUNTER_SUSHI API Specification is now maintained by COUNTER on Stoplight.io:

https://countermetrics.stoplight.io/docs/counter-sushi-api

The COUNTER_SUSHI API Specification is contained in a single OpenAPI 3.1/JSON schema file (COUNTER_SUSHI_API.json, included in this directory in the version corresponding to the repository branch) which is used by Stoplight.io for presenting the information about the API paths and the JSON responses. It is expected that report providers will use only the parts relevant to them, or export the file and make local tailored copies relevant to their particular circumstances, for example by removing API paths and models detailing reports they do not support. Note that it is also possible to export the JSON schemas for the JSON reports and other API responses and use them with a JSON schema validator.

The COUNTER_SUSHI API Specification for R5.1 is more detailed and precise than the specification for R5, but it is not self-contained, since it is not possible to express all rules in the COUNTER Code of Practice in JSON schema. So the rules in the Code of Practice still apply, and in the case of any conflicts with the COUNTER_SUSHI API Specification the Code of Practice takes precedence.
