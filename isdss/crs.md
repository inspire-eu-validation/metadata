# Coordinates reference systems 'dataset' or 'series'

**Purpose**: Checks the coordinate reference system identifiers used must originate from a common register.

**Prerequisites**

**Test method**
* It is checked that only the [identifiers](#referenceSystemIdentifier) contained in a common record will be used 
to refer to the coordinate reference systems of a  'dataset' or 'series'.

* The multiplicity of this element is one or more.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/isdss/README#ref_TG_MD) 3.2.1.1, Req 2.1

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/isdss/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| ------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | ./gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="referenceSystemIdentifier"></a> referenceSystemIdentifier  | ./gmd:referenceSystemInfo/\*/gmd:referenceSystemIdentifier[1]/gmd:RS_Identifier