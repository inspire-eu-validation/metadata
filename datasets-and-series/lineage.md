# Lineage

**Purpose**: Test that exactly one explanation about the lineage of a dataset is provided.

**Prerequisites**

* [Resource Type](./resource-type.md)

**Test method**

* Check that exactly one [Lineage](#lineage) element exists.

    * Check that content of every [Statement](#statement) is a non-empty free text.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD) 3.1.4.3, Req 1.11

**Test type**: Automated

**Notes**

The multiplicity of this element is one.

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:dataQualityInfo/gmd:DQ_DataQuality)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="lineage"></a>Lineage | /gmd:MD_Metadata/gmd:dataQualityInfo/gmd:DQ_DataQuality/gmd:lineage
<a name="statement"></a> Statement | gmd:lineage/gmd:LI_Lineage/gmd:statement
