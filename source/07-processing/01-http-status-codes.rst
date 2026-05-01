.. The COUNTER Code of Practice © 2017-2024 by COUNTER Metrics
   is licensed under CC BY 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by/4.0/

HTTP Status Codes
-----------------

Only successful and valid requests MUST be counted. For web server log files successful requests are those with specific HTTP status codes (200 and 304). The standards for HTTP status codes are defined and maintained by the `IETF HTTP working group <https://datatracker.ietf.org/wg/httpbis/documents/>`_ in a series of RFCs (most notably `RFC 9110 <https://www.rfc-editor.org/rfc/rfc9110.html>`_). If key events are used, their definition MUST match the HTTP standards.

HTTP status code 302, and other redirect codes, MAY be counted if they are caused by a user interaction with an Item that redirects the user to another location (e.g. linkout). Report provders MUST NOT count 200 and 302 on a single interaction with the same Item.