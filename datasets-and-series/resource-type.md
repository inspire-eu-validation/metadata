# Resource Type 'dataset' or 'series'

**Purpose**: Checks that a resource type is provided as a dataset or series.

**Prerequisites**

**Test method**
Check if a resource type is provided ([hierarchyLevel](#hierarchyLevel)) and its value is taken from the list of [code List Value](#codeListValue).
This value must be declared as 'dataset' or 'series'.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/README#ref_TG_MD),3.1.1.1, Req 1.1
* [ISO 19115](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/README#ref_ISO_19115) table B.5.25 MD_ScopeCode 

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| ------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | ./gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="codeListValue"></a> code List Value | doc("http://standards.iso.org/iso/19139/resources/gmxCodelists.xml)//gmx:CodeListDictionary[@gml:id='MD_ScopeCode']//gml:identifier/text()