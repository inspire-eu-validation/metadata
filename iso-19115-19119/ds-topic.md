# Dataset topic

**Purpose**: If the type of the resource is dataset or series, at least one Topic category describing the category of the resource must be given.

**Prerequisites**

* [Hierarchy](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/hierarchy)

**Test method**

This test case only applies to records with a [hierarchyLevel](#hierarchyLevel) value 'dataset' or 'series'.

The test first checks, if at least one element of type [topicCategory](#topic) is given. If so, the following conditions are checked for all topic categories:

* The topic category is of type [MD_TopicCategoryCode](#topic)
* The element gmd:MD_TopicCategoryCode contains text that equals one of the categories given in [B.5.27 of ISO 19115](http://inspire.ec.europa.eu/metadata-codelist/TopicCategory).
The value saved in the XML metadata element shall be a language neutral name.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#ref_TG_MD), 2.3.1, Req 10 & 11
* [B.5.27 of ISO 19115](http://inspire.ec.europa.eu/metadata-codelist/TopicCategory)

**Test type**: Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="topic"></a> topicCategory  | ./gmd:identificationInfo[1]/*/gmd:topicCategory
