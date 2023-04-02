.. The COUNTER Code of Practice Release 5 © 2017-2023 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

.. _sushi:

SUSHI for Automated Report Harvesting
=====================================

The COUNTER_SUSHI API is designed to simplify the gathering of usage statistics by report consumers, and report providers MUST support automatic harvesting of COUNTER reports via the COUNTER_SUSHI API. The specification for the RESTful COUNTER_SUSHI API is maintained by COUNTER on SwaggerHub:

`<https://app.swaggerhub.com/apis/COUNTER/counter-sushi_5_0_api/>`

The Swagger files are a comprehensive reference version that contains a detailed description of the entire COUNTER_SUSHI API. It is expected that reporting services will use only the parts relevant to them, or make local tailored copies relevant to their particular circumstances, for example by removing methods detailing reports they don't support.

.. toctree::
   :maxdepth: 1

   01-counter-sushi-api-paths-to-support
   02-authentication-and-security-for-counter-sushi-api
   03-report-filters-and-report-attributes
   04-errors-and-exceptions
