
# Metadata point of contact

**Purpose**	

At least one point of contact must be given.

**Test method**	

The test first checks if an element is given at gmd:contact. It then performs the following checks for every element at gmd:contact:
*	An element must be given at gmd:CI_ResponsibleParty/gmd:organisationName.
*	An element must be given at gmd:CI_ResponsibleParty/gmd:contactInfo/*/gmd:address/*/gmd:elec tronicMailAddress.
*	Organization name and electronic mail address must be either gco:CharacterString or gmd:PT_FreeText. In the latter case, a schema validation is performed depending on the GML version (see About schema validation).


**Reference(s)**	 

IR, Chap. 2.11.1

**Test type:** Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name=""></a>   |



