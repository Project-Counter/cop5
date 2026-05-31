.. The COUNTER Code of Practice © 2017-2024 by COUNTER Metrics
   is licensed under CC BY 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by/4.0/

.. _reserved-values:

Reserved Values Available for Extending Reports
-------------------------------------------------

COUNTER's `Best Practice on Generative and Agentic AI Usage <https://www.countermetrics.org/code-of-practice/best-practice/bp-ai/>`_ created a new Access_Method and new Metric_Types specifically for reporting AI usage. These values are OPTIONAL extensions for inclusion in COUNTER Reports only when called for.


.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.17}|>{\raggedright\arraybackslash}\Y{0.26}|>{\parskip=\tparskip}\Y{0.46}|>{\raggedright\arraybackslash}\Y{0.11}|

.. list-table::
   :class: longtable
   :widths: 15 22 51 12
   :header-rows: 1

   * - Element Name
     - Value
     - Description
     - Reports

   * - Access_Method
     - Agent
     - Content and metadata accessed by an AI system.
     - PR, DR, TR, IR

   * - Metric_Type
     - AI_Responses_Generated
     - A response delivered by an AI system in response to a user prompt. The response is likely to be text, but may include images or other multimedia. Each response MUST only be counted once regardless of the number of queries initiated by the AI system. Subsequent prompts within the same user session MUST be counted as a new AI_Responses_Generated.
     - PR

   * - Metric_Type
     - Total_AI_Investigations
     - Total number of times within a user session that a chunk from an Item or information related to an Item was included by an AI system in generating a response to a user prompt.
     - PR, DR, TR, IR


   * - Metric_Type
     - Unique_AI_Investigations
     - Unique count of times within a user session that a chunk from an Item or information related to an Item was included by an AI system in generating a response to a user prompt.
     - PR, DR, TR, IR


   * - Metric_Type
     - Total_AI_Requests
     - Total number of times within a user session that a chunk from an Item was requested (i.e. the full text or content was accessible to the AI system) in generating a response to a user prompt, during a user session.
     - PR, DR, TR, IR


   * - Metric_Type
     - Unique_AI_Requests
     - Unique count of times within a user session that a chunk from an Item was requested (i.e. the full text or content was accessible to the AI system) in generating a response to a user prompt.
     - PR, DR, TR, IR



Access_Method Agent is an OPTIONAL extension. Where report providers make Access_Method Agent available, it MUST only be included in COUNTER Reports. Where report providers make Access_Method Agent available, it MUST only be included in COUNTER Reports when called for by report consumers. Where Access_Method Agent is included in COUNTER Reports, it MUST be reported against AI Metric_Types.

The new AI Metric_Types are all OPTIONAL extensions. Where report providers make these AI Metric_Types available, they MUST only be included in COUNTER Reports. Where report providers make these AI Metric_Types available, they MUST only be included in COUNTER Reports when called for by report consumers. Where AI Metric_Types are included in COUNTER Reports, they MUST be reported against Access_Method Agent.
