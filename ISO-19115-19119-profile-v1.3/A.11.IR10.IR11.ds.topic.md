#A.11.IR10.IR11.ds.topic

**Purpose**: If the type of the resource is dataset or series, at least one Topic category describing the category of the resource must be given.

**Prerequisites**
* [A.01.validate](A.01.validate.md) must be passed
* [A.04.IR01.IR02.hierarchy] (A.04.IR01.IR02.hierarchy.md) contains "dataset" or "series"

**Test method**

The test first checks if at least one element of type [topicCategory](#topic) is given. If so, the following conditions are checked for all topic categories:
*	The topic category is of type [MD_TopicCategoryCode](#topic)
*	The element gmd:MD_TopicCategoryCode contains text that equals one of the categories given in [B.5.27 of ISO 19115](http://inspire.ec.europa.eu/metadata-codelist/TopicCategory).
The value saved in the XML metadata element shall be a language neutral name.

If the type of the resource was not dataset or series, this test is omitted.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.3.1, Req 10 & 11
* [IR MD](README.md#ref_IR_MD) Part B. 2.1
* [B.5.27 of ISO 19115](http://inspire.ec.europa.eu/metadata-codelist/TopicCategory)

**Test type:** Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="topic"></a> topicCategory  | ./gmd:identificationInfo[1]/*/gmd:topicCategory
