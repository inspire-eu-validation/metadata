
# Temporal Reference

**Purpose**	

INSPIRE provides 4 types of temporal reference, which are all conditional elements on their own. However, at least one of them must be provided.

**Test method**	

The four types of which one must be provided are Temporal extent, Date of publication, Date of last revision and Date of creation. This test performs the following checks:
*	Is a valid Temporal extend given at gmd:identificationInfo[1]/*/gmd:extent/*/gmd:temporalElement/*/gmd: extent/gml:TimePeriod and does it contain
*	gml:beginPosition and gml:endPosition or
*	gml:begin/gml:timeInstant/gml:timePosition x 2 or
*	gml:begin/gml:timeInstant/gml:timePosition and gml:endPosition or
*	gml:beginPosition and gml:begin/gml:timeInstant/gml:timePosition
*	Is a valid date of publication given at gmd:identificationInfo[1]/*/gmd:citation/*/gmd:date[./*/gmd:dateType/*/ text()='publication']/*/gmd:date
*	Is a valid date of last revision given at gmd:identificationInfo[1]/*/gmd:citation/*/gmd:date[./*/gmd:dateType/*/ text()='revision']/*/gmd:date
*	Is a valid date of creation given at gmd:identificationInfo[1]/*/gmd:citation/*/gmd:date[./*/gmd:dateType/*/ text()='creation']/*/gmd:date
The test will fail if and only if all of the above checks evaluate to false.

**Reference(s)**	 
* IR, Chap. 2.6.1 - 2.6.4
* ISO 19108
* ISO 8601
* TG Req 22 & 23
 
**Test type:** Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name=""></a>   |

