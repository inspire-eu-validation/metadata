# Dataset identification

**Purpose**: Unique resource identifier. If the type of the resource was dataset or series, a unique identifier identifying the resource must be given.

**Prerequisites**

* [resource-type](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/resource-type)

**Test method**

* This test case only applies to records with a [hierarchyLevel](#hierarchyLevel) value 'dataset' or 'series'.
* The test first checks if a unique [identifier](#identifier) is given and if it is of type MD_Identifier or RS_Identifier.

TThe container of the CODE element is free text but should not be empty.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/README#ref_TG_MD), 3.1.2.1, Req 1.3
* [ISO 19115](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/README#ref_ISO_19115) table B.5.25 MD_ScopeCode 

**Test type**: Automated

**Notes**

* The [ISO 19139] xml schemas allow the use of either the MD_Identifier type or its sub-type RS_Identifier, which, in addition to the mandatory code property, also contains an optional codeSpace property.
* It is strongly recommended to use the MD_Identifier instead of the the RS_Identifier type and to encode the complete URI in the code element.

##Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="identifier"></a> identifier   | gmd:identificationInfo[1]/\*/gmd:citation/\*/gmd:identifier/\*/gmd:code
