
# Conformity

**Purpose**	

For every conformity statement, one conformance result indicated by a boolean value must be given.

**Test method**	

The test first checks if there is at least one conformance result of type gco:Boolean at gmd:dataQualityInfo/*/gmd:report/*/gmd:result. It then performs the following actions for every element at gmd:dataQualityInfo/*/gmd:report/*/gmd:result:
*	If the element has an element /*/gmd:pass, it must contain a value of type gco:Boolean.


**Reference(s)**	 

IR, Chap. 2.8.1
TG Req 28
 
**Test type:** Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name=""></a>   |

