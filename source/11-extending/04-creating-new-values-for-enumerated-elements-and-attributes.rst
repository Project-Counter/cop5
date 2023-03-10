.. The COUNTER Code of Practice Release 5 © 2017-2021 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

Creating Custom Values for Enumerated Elements
----------------------------------------------

Several elements in COUNTER reports include a controlled list of possible values. On occasion, content providers may want to introduce additional custom values that better reflect their content and platform. For Master reports (PR, DR, TR, IR) and custom reports the element value lists can be extended by including additional custom values in the form of *{namespace}*:*{element value}*. An example would be a custom Metric_Type value EBSCOhost:Total_Linkouts. The following is the list of elements that can be extended in this manner:

* Data_Type
* Section_Type
* Access_Type
* Access_Method
* Metric_Type

Custom values MUST only be included in Master Reports if called for, and if included they MUST be listed in the corresponding report filters in the Report_Filters or Metric_Types header.
