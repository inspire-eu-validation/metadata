#A.23.IR35.IR36.responsible.party.contact.info

**Purpose**: Name and contact email to a responsible party must be given for every responsible organization in the metadata.

**Prerequisites**
* [A.01.validate](A.01.validate.md) must be passed

**Test method**

The test first checks if there is at least one element at gmd:identificationInfo/*/gmd:pointOfContact. Furthermore, the following checks are performed
*	There must not be an [empty characterstring](./README.md#emptychar) at ./gmd:organisationName
*	There must not be an [empty characterstring](./README.md#emptychar) at ./gmd:contactInfo/*/gmd:address/*/gmd:electronicMailAddress. Check [electronicMailAddress](#electronicMailAddress) with the regular expresion ^[A-Z0-9._%+-]+@[A-Z0-9.-]+.[A-Z]{2,}$.
If the string does not match the regular expression, the test fails (note: regex built for case insensitive match).

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD) 2.10.1, Req 35 & 36
* [IR MD](README.md#ref_IR_MD) Part B. 3.5

**Test type:** Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="CI_ResponsibleParty"></a> CI_ResponsibleParty   | ./gmd:identificationInfo/*/gmd:pointOfContact/*/gmd:CI_ResponsibleParty
<a name="organisationName"></a> Organisation Name |./gmd:organisationName
<a name="electronicMailAddress"></a> Electronic Mail Address  |./gmd:contactInfo//gmd:address//gmd:electronicMailAddress
