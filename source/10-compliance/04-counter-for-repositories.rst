.. The COUNTER Code of Practice © 2017-2026 by COUNTER Metrics
   is licensed under CC BY 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by/4.0/

.. _compliance-repositories:

COUNTER Reporting for Repositories
----------------------------------

The COUNTER Code of Practice for Research Data (CRD) was a milestone in data evaluation practices, making it possible to report comparable usage counts across repositories and other data platforms. The development of the CRD drew from COUNTER’s experience with standards for usage metrics for scholarly resources, and its recommendations aligned as much as possible with Release 5 of the COUNTER Code of Practice.

Repository infrastructure has developed substantially in the years since the release of the CRD. Release 5.1 of the COUNTER Code of Practice extended the type of outputs for which usage can be reported. Make Data Count and COUNTER therefore recommend that repositories and other data platforms should follow R5.1 instead of the CRD. This section lays out the similarities and differences between R5.1 and the CRD.


Attributes
""""""""""

Key attributes outlined in :numref:`common-attributes-and-elements` are used the same way in R5.1 as they were in the CRD:

* Host_Types Data_Repository and Repository
* Data_Type Dataset
* Access_Method Regular
* YOP (year of publication)

Two further aspects are functionally the same, but with slightly different naming conventions. Access_Method TDM replaces Access_Method Machine in the CRD. Metric_Types use "Item" in place of "Dataset" in the CRD:

* Total_Item_Investigations in place of Total_Dataset_Investigations
* Unique_Item_Investigations in place of Unique_Dataset_Investigations
* Total_Item_Requests in place of Total_Dataset_Requests
* Unique_Item_Requests in place of Unique_Dataset_Requests

The Access_Type attribute is required in R5.1 but does not appear in the CRD.


Required Reports
""""""""""""""""

R5.1 requires Data_Repository and Repository Host_Types to deliver the Platform Report (PR) and Item Report (IR), together with the Standard Views of those reports. The IR maps closely to the Dataset Report specified in the CRD.

The Platform field in the PR and IR MUST be used to supply the repository name.

Three elements are required in IR but do not appear in the CRD: ISBN, Print_ISSN and Online_ISSN. These are not applicable to research data but may apply where repositories include archived journal and book content. Where the information is not relevant, the fields MUST remain empty in the tabular version of the IR. These elements are optional in JSON reports and MUST be omitted when no value is available.

There are also fields from the CRD which appear in R5.1 under different names:

* Item in place of Dataset_Title
* Authors in place of Creators
* Article_Version in place of Dataset_Version
* Proprietary_ID in place of Other_ID


Using Components within the IR
""""""""""""""""""""""""""""""

An aspect of R5.1 that may be particularly helpful for repositories is Components, which allow for Items to have multiple subunits. In this model, the dataset https://doi.org/10.18739/A2P55DH4M represents an R5.1 Item, while each file within the dataset (e.g. Heatmap_Family.png) is a Component. Using this structure would allow repositories to report on usage of the dataset as a whole, or to be more granular and report usage of each Component.


Mapping COUNTER Data_Types to Datacite Resource Types
""""""""""""""""""""""""""""""""""""""""""""""""""""""

The CRD only permits Data_Type Dataset. The R5.1 IR allows comprehensive reporting on multiple Data_Types. For Data_Repository Host_Types, Dataset remains the default. For mixed-content repositories, the full list of COUNTER Data_Types as described at :numref:`data-types` is available.

Many COUNTER Data_Types map exactly to the Datacite metadata schema resource types:

* Audiovisual
* Book
* Dataset
* Image
* Journal
* Other
* Report
* Software
* Sound
* Standard

Some COUNTER Data_Types use different terms from the Datacite metadata schema resource types. A mapping is provided in Table 10.a for quick reference.

Table 10.a (below): COUNTER Data_Types mapped to Datacite resource types

.. only:: latex

   .. tabularcolumns:: |>{\raggedright\arraybackslash}\Y{0.28}|>{\raggedright\arraybackslash}\Y{0.25}|

.. list-table::
   :class: longtable
   :widths: 31 31
   :header-rows: 1

   * - COUNTER Data_Type
     - Datacite Resource Type

   * - Article
     - JournalArticle

   * - Book_Segment
     - BookChapter

   * - Conference
     - ConferenceProceeding

   * - Conference_Item
     - ConferencePaper

   * - Interactive_Resource
     - InteractiveResource

   * - Multimedia
     - Other

   * - News_Item
     - Text

   * - Newspaper_or_Newsletter
     - Text

   * - Patent
     - Other

   * - Reference_Item
     - Text

   * - Reference_Work
     - Text

   * - Thesis_or_Dissertation
     - Dissertation

   * - Unspecified
     - Other
