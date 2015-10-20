#A.18.IR26.lineage

**Purpose**: If the type of the resource was dataset or series, exactly one explanation about the lineage of a dataset must be given

**Prerequisites**
* [A.01.validate](A.01.validate.md) must be passed

**Test method**

The test first checks if a valid lineage [statement](#statement) is given and it is not an [empty characterstring](./README.md#emptychar)
It then validates that exactly one lineage statement like the one above is given.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD) 2.7.1, Req 26

**Test type:** Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="statement"></a> statement  | gmd:dataQualityInfo/*/gmd:lineage/*/gmd:statement
