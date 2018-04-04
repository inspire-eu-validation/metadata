# Data Encoding dataset or series

**Purpose**: Evaluate encoding and the storage or transmission format for data sets and datasets.

**Prerequisites**

**Test method**

* The coding and storage or transmission format of the provided 
data sets or series of data sets through the element is tested [Distribution Format](#distributionFormat).

* The multiplicity of this element is one or more.

* It is verified that the child elementschild exist and their value is free text but not empty.

**Reference(s)**	 
* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/isdss/README#ref_TG_MD) 3.2.3.1, Req 2.6

**Test type**: Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/isdss/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| ------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | ./gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="distributionFormat"></a> Distribution Format  | ./gmd:distributionInfo/\*/gmd:distributionFormat/gmd:MD_Format
<a name="name"></a> Name  | ./gmd:distributionInfo/\*/gmd:distributionFormat/\*/gmd:name/text()
<a name="version"></a> Version  | ./gmd:distributionInfo/\*/gmd:distributionFormat/\*/gmd:version/text()
