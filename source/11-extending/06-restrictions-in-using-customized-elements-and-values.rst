.. The COUNTER Code of Practice © 2017-2024 by COUNTER Metrics
   is licensed under CC BY 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by/4.0/

Restrictions in Using Custom Elements and Values
------------------------------------------------

Extensions MUST only be used with COUNTER Reports and custom reports, they MUST NOT be used with Standard Views of the COUNTER Reports. Note, however, that a report with extensions that is similar to a Standard View of the COUNTER Reports can be created by applying the Standard View’s filters and attributes to the corresponding COUNTER Report and adding the extensions.

Custom elements and values MUST only be included in COUNTER Reports if called for. So for reports requested via the COUNTER_SUSHI API, custom elements MUST only be included if requested via attributes_to_show, and custom values MUST only be included if requested via the corresponding report filters (e.g. metric_type or data_type). On the administrative/reporting site the custom elements and values can be preselected for COUNTER Reports, but the user MUST have the option to exclude the custom elements and values from the COUNTER Reports.
