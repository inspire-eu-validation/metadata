# Coordinates reference systems Interoperable Spatial Data Services

**Purpose**: Checks the coordinate reference system identifiers used must originate from a common register.

**Prerequisites**

* [resource-type](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/resource-type)

**Test method**
It is checked that only the [identifiers](#referenceSystemIdentifier) contained in a common record will be used 
to refer to the coordinate reference systems of a interoperable 'service' .
When the gmd:code does not uniquely identify the referenced coordinate reference system, the value of the child element gmd: codeSpace is checked also.

The multiplicity of this element is one or more.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-interoperable/README#ref_TG_MD) 4.4.1.1, Req 6.1

**Test type**: Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-interoperable/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| ------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | ./gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="referenceSystemIdentifier"></a> referenceSystemIdentifier  | ./gmd:referenceSystemInfo/\*/gmd:referenceSystemIdentifier[1]/gmd:RS_Identifier[]