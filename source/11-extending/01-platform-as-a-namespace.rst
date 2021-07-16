.. The COUNTER Code of Practice Release 5 © 2017-2021 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

Platform as a Namespace
-----------------------

Content providers and other organizations providing COUNTER reports wishing to create custom reports or introduce custom elements or values can do so by using their platform identifier (platform ID) as a namespace. For example, if EBSCO wanted to create a customized version of the “Journal Requests (Excluding OA_Gold)” Standard View for their link resolver product that includes a new Metric_Type for counting link-outs, they could do this by naming the report EBSCOhost:LR1 and creating a new Metric_Type of EBSCOhost:Total_Linkouts. Note that the platform ID is also used as a namespace for local Institution_IDs and Publisher_IDs assigned by the content provider and for Proprietary_IDs (see :numref:`formats`).

The platform ID MUST only contain ASCII letters (a–z, A–Z), digits (0–9), underscores (_), dots (.) and forward slashes (/), and the length MUST NOT exceed 17 characters. Note that the platform ID is used in various columns and therefore should be as short as possible, but still recognizable. The platform ID usually should be based on the name, a well-known unique abbreviation or the domain of the publisher or platform. A short standard identifier like GRID or ROR (without the \https://) also could be used.

COUNTER will assign the platform ID when adding the platform to their Registry of Compliance (content providers can suggest a value to be used for their platform ID). Other organizations providing COUNTER reports, such as consortia or ERM providers, may contact COUNTER to register a namespace if they desire to create extensions and customizations. COUNTER will maintain a list of approved namespaces.
