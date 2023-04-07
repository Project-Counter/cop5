.. The COUNTER Code of Practice Release 5 © 2017-2023 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

Text and Data Mining
--------------------

Text and data mining (TDM) is a computational process whereby text or datasets are crawled by software that recognizes entities, relationships, and actions. (`STM Statement on Text and Data Mining <https://www.stm-assoc.org/2012_03_15_STM_Summary_Statement_Text_Data_Mining_final.pdf>`_)

TDM does NOT include straightforward information retrieval, straightforward information extraction, abstracting and summarizing activity, automated translation, or summarizing query-response systems.

A key feature of TDM is the discovery of unknown associations based on categories that will be revealed as a result of computational and linguistic analytical tools.


.. rubric:: Principles for reporting usage:

* COUNTER metrics do not record TDM itself, as most of this activity takes place after an article has been downloaded. Instead, metrics represent the count of articles downloaded for the purposes of mining.
* Usage associated with TDM activity (e.g. articles downloaded for the purpose of TDM) MUST be tracked by assigning an Access_Method of TDM.
* Usage associated with TDM activity MUST be reported using the Title, Database, and Platform Reports by identifying such usage as Access_Method=TDM.
* Usage associated with TDM activity MUST NOT be reported in Standard Views of the COUNTER Reports (TR_J1, TR_B1, etc.).


.. rubric:: Detecting activity related to TDM:

TDM activity typically requires a prior agreement between the report provider and the individual or organization downloading the content for the purpose of text mining. The report provider can isolate TDM-related traffic using techniques like:

* Providing a dedicated end-point that is specifically for TDM data harvesting.
* Requiring the use of a special account or profile for TDM data harvesting.
* Assigning an API key that would be used for the harvesting.
* Registering the IP address of the machine harvesting content.

Harvesting of content for TDM without permission or without using the endpoint or protocol supplied by the report provider MUST be treated as robot or crawler traffic and MUST be excluded from all COUNTER reports.
