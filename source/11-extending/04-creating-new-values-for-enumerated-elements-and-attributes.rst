.. The COUNTER Code of Practice Release 5 © 2017-2021 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

Creating New Values for Enumerated Elements and Attributes
----------------------------------------------------------

Several report elements and attributes in COUNTER reports include a controlled list of possible values. On occasion, a content provider may want to introduce additional values that better reflects their content and platform. The element value lists can be extended by including additional values in the form of *{namespace}*:*{element value}*. An example of a custom Metric_Type could be ebscohost:Total_Linkouts. The following is the list of elements that can be extended in this manner:

* Data_Type
* Section_Type
* Access_Type
* Access_Method
* Metric_Type

Note that values for identifier fields (Institution_ID, Publisher_ID, etc.) MUST also include the namespace for these identifiers. For proprietary identifiers that are platform-specific, the platform ID should be used as the namespace.
