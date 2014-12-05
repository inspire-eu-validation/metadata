
# Lineage

**Purpose**	

If the type of the resource was dataset or series, exactly one explanation about the lineage of a dataset must be given

**Test method**	

The test first checks if a valid lineage statement is given at gmd:dataQualityInfo/*/gmd:lineage/*/gmd:statement 
and if the statement type is either gco:CharacterString or gmd:PT_FreeText. In the latter case, a schema validation 
is performed depending on the GML version (seeAbout schema validation). It then validates that exactly one lineage statement like the one above is given.

**Reference(s)**	 

IR, Chap. 2.7.1

**Test type:** Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name=""></a>   |



