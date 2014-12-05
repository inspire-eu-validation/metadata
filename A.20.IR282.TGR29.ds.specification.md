
# Specification

**Purpose**	

For every conformity statement, one citation of the product specification or user requirement against which data is being evaluated must be given.

**Test method**	

The test first checks if there is at least one specification at gmd:dataQualityInfo/*/gmd:report/*/gmd:result/*/specification. In case there is none, a warning is thrown. It then performs the following checks for every element at gmd:dataQualityInfo/*/gmd:report/*/gmd:result/*/gmd:specification:
*	The specification must contain an element of type gmd:CI_Citation.
*	The specification must contain an element of type gmd:CI_Citation/gmd:title.
*	The specification must contain an element of type gmd:CI_Citation/gmd:date[./*/gmd:dateType/*/text()='x']/*/gmd:date, where x is one of creation, revision and publication.
*	the type of the title must be either gco:CharacterString or gmd:PT_FreeText. In the latter case, a schema validation is performed depending on the GML version (see About schema validation).

**Reference(s)**	 

IR, Chap. 2.8.2
TG Req 29

**Test type:** Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name=""></a>   |

