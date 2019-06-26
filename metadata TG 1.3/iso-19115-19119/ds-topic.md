# Dataset topic

**Purpose**: If the type of the resource is dataset or series, at least one Topic category describing the category of the resource must be given.

**Prerequisites**

* [Hierarchy](./hierarchy)

**Test method**

This test case only applies to records with a [hierarchyLevel](#hierarchyLevel) value 'dataset' or 'series'.

The test first checks, if at least one element of type [topicCategory](#topic) is given. If so, the following conditions are checked for all topic categories:

* The topic category is of type [MD_TopicCategoryCode](#topic)
* The element gmd:MD_TopicCategoryCode contains text that equals one of the categories given in [B.5.27 of ISO 19115](http://inspire.ec.europa.eu/metadata-codelist/TopicCategory).
The value saved in the XML metadata element shall be a language neutral name.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.3.1, Req 10 & 11
* [B.5.27 of ISO 19115](http://inspire.ec.europa.eu/metadata-codelist/TopicCategory)

**Test type**: Automated

**Notes**

The depencency to [Hierarchy](./hierarchy) has not been implemented in the ETS as it still seems reasonable to test the available dataset (series) metadata records.  

The ETS only checks if at least one non-empty topicCategory element is given. That a topic category value is one of the enumeration values as defined by ISO 19115 is already covered by the XML Schema validation.

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="topic"></a> topicCategory  | ./gmd:identificationInfo[1]/\*/gmd:topicCategory
