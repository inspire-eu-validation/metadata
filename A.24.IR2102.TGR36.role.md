
# Responsible party role

**Purpose**	

Every responsible organization must name a responsible party role.

**Test method**	

The test first checks if there is at least one element at gmd:identificationInfo[1]/*/gmd:pointOfContact/*/gmd:role. It then performs the following checks for each element at gmd:identificationInfo[1]/*/gmd:pointOfContact/*/gmd:role: - The element must contain an element at gmd:CI_RoleCode[@codeListValue=x], where x is one of the values described in ISO 19115, chapter B.5.5.


**Reference(s)**	 

* IR, Chap. 2.10.2
* ISO 19115, B.5.5

**Test type:** Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name=""></a>   |

