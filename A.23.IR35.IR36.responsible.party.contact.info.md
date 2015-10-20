#A.23.IR35.IR36.responsible.party.contact.info

**Purpose**: Name and contact email to a responsible party must be given for every responsible organization in the metadata.

**Prerequisites**
* [A.01.validate](A.01.validate.md) must be passed

**Test method**

The test first checks if there is at least one element at gmd:identificationInfo/*/gmd:pointOfContact. Furthermore, the following checks are performed
*	There must not be an [empty characterstring](./README.md#emptychar) at ./gmd:organisationName
*	There must not be an [empty characterstring](./README.md#emptychar) at ./gmd:contactInfo/*/gmd:address/*/gmd:electronicMailAddress

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD) 2.10.1, Req 35

**Test type:** Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------

<a name="CI_ResponsibleParty"></a> CI_ResponsibleParty   | ./gmd:identificationInfo/*/gmd:pointOfContact/*/gmd:CI_ResponsibleParty
