# Dataset topic

**Purpose**: If the type of the resource is dataset or series, at least one Topic category describing the category of the resource must be given.

**Prerequisites**

* [resource-type](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/resource-type)

**Test method**

This test case only applies to records with a [hierarchyLevel](#hierarchyLevel) value 'dataset' or 'series'.

The test first checks, if at least one element of type [topicCategory](#topic) is given. If so, the following conditions are checked for all topic categories:

* The topic category is of type [MD_TopicCategoryCode](#topic)
* The element gmd:MD_TopicCategoryCode contains text that equals one of the categories given in [B.5.27 of ISO 19115](http://inspire.ec.europa.eu/metadata-codelist/TopicCategory).
The value saved in the XML metadata element shall be a language neutral name.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/topic-category/README#ref_TG_MD), 3.1.2.5, Req 1.7
* [B.5.27 of ISO 19115](http://inspire.ec.europa.eu/metadata-codelist/TopicCategory)

**Test type**: Automated

**Notes**

That contrary to many other code lists which are defined in the ISO 19139 XML Schema as references to an external code list, gmd:MD_TopicCategoryCode element is defined as a string enumeration.

##Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="topic"></a> topicCategory  | ./gmd:identificationInfo[1]/\*/gmd:topicCategory/gmd:MD_TopicCategoryCode
