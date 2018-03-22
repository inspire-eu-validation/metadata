# Coordinates reference systems 'dataset' or 'series'

**Purpose**: Checks the coordinate reference system identifiers used must originate from a common register.

**Prerequisites**

* [referenceSystemIdentifier](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/crs)

**Test method**
Check if the coordinate reference system is listed in the Default Coordinate Reference System Identifiers table in [Part D.4].
Then the value of the HTTP URI Identifier column will be used as the value of [code](#code).

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/isdss/README#ref_TG_MD) 3.2.1.1, Req 2.2

**Test type**: Automated

**Notes**
The gmd:codeSpace element shall not be used in this case.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/isdss/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| ------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | ./gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="code"></a> code  | ./gmd:referenceSystemInfo/\*/gmd:referenceSystemIdentifier[1]/\*/gmd:code
