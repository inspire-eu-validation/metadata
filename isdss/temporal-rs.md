# Temporal reference systems 'dataset' or 'series'

**Purpose**: Checks if the temporal reference system(s) used in the data set makes discovering 
data sets with temporal coordinates provided in desired reference systems possible.

**Prerequisites**

**Test method**

Check if the temporal reference system is given using element[referenceSystemInfo](#referenceSystemIdentifier).


The gmd:code child element of gmd:RS_Identifier is mandatory.

**Reference(s)**	 
* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/isdss/README#ref_TG_MD) 3.2.1.2, Req 2.3

**Test type**: Automated

**Notes**
The gmd:codeSpace child element shall be used if the [code](#codeChild) alone does not uniquely 
identify the referred coordinate reference system.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/isdss/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| ------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | ./gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="referenceSystemIdentifier"></a> referenceSystemIdentifier  | ./gmd:referenceSystemInfo/\*/gmd:referenceSystemIdentifier[1]/gmd:RS_Identifier
<a name="code"></a> codeChild  | ./gmd:referenceSystemInfo/\*/gmd:referenceSystemIdentifier[1]/\*/gmd:code/text()
