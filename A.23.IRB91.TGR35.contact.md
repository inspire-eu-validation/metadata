
# Responsible party

**Purpose**	

Name and contact email to a responsible party must be given for every responsible organization in the metadata.

**Test method**	

The test first checks if there is at least one element at gmd:identificationInfo/*/gmd:pointOfContact. Furthermore, the following checks are performed
*	There must not be an [empty characterstring](./README.md#emptychar) at ./gmd:organisationName
*	There must not be an [empty characterstring](./README.md#emptychar) at ./gmd:contactInfo/*/gmd:address/*/gmd:electronicMailAddress 

**Reference(s)**	 

* [IR](./README.md#IR), Annex B. 3.5
* [TG](./README.md#TG) Req 35

**Test type:** Automated
	
**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------

<a name="CI_ResponsibleParty"></a> CI_ResponsibleParty   | ./gmd:identificationInfo/*/gmd:pointOfContact/*/gmd:CI_ResponsibleParty

