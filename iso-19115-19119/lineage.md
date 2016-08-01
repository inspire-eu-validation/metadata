#Lineage

**Purpose**: If the type of the resource was dataset or series, exactly one explanation about the lineage of a dataset must be given

**Prerequisites**

* [Hierarchy](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/hierarchy)

**Test method**

This test case only applies to records with a [hierarchyLevel](#hierarchyLevel) value 'dataset' or 'series'.

The test first checks if a valid lineage [statement](#statement) is given and it is not an [empty characterstring](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#emptychar)
It then validates that exactly one lineage statement like the one above is given.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#ref_TG_MD) 2.7.1, Req 26


**Test type**: Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="statement"></a> statement  | gmd:dataQualityInfo/*/gmd:lineage/*/gmd:statement
