#Lineage

**Purpose**: If the type of the resource was dataset or series, exactly one explanation about the
lineage of a dataset must be given

**Prerequisites**

* [resource-type](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/resource-type)

**Test method**

This test case only applies to records with a [hierarchyLevel](#hierarchyLevel) value 'dataset' or 'series'.

The test first checks if a valid lineage [statement](#statement) is given and it is not an [empty characterstring](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/README#emptychar). 
It then validates that exactly one lineage statement like the one above is given.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/lineage/README#ref_TG_MD) 3.1.4.3, Req 1.11

**Test type**: Automated

**Notes**

The "Test method" requires to validate "that exactly one lineage statement like the one above is given" and talks about a "valid lineage statement". It is not clear if there are additional requirements on the value of a lineage statement, other than that it shall not be empty.

##Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | ./gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="statement"></a> statement  | ./gmd:dataQualityInfo/\*/gmd:lineage/\*/gmd:statement
