#Lineage

**Purpose**: If the type of the resource was dataset or series, exactly one explanation about the lineage of a dataset must be given

**Prerequisites**

* [Hierarchy](./hierarchy)

**Test method**

This test case only applies to records with a [hierarchyLevel](#hierarchyLevel) value 'dataset' or 'series'.

The test first checks if a valid lineage [statement](#statement) is given and it is not an [empty characterstring](./README#emptychar). It then validates that exactly one lineage statement like the one above is given.

**Reference(s)**	 

* [TG MD](./README#ref_TG_MD) 2.7.1, Req 26

**Test type**: Automated

**Notes**

The depencency to [Hierarchy](./hierarchy) has not been implemented in the ETS as it still seems reasonable to test the available dataset (series) metadata records.  

The "Test method" requires to validate "that exactly one lineage statement like the one above is given" and talks about a "valid lineage statement". It is not clear if there are additional requirements on the value of a lineage statement, other than that it shall not be empty.

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="statement"></a> statement  | gmd:dataQualityInfo/\*/gmd:lineage/\*/gmd:statement
