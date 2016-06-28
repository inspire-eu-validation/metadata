#Md contact

**Purpose**: At least one point of contact must be given.

**Prerequisites**
* [Schema validation](schema-validation.md) must be passed

**Test method**

The test first checks if a [contact](#contact) element is given. It then performs the following checks for every element at gmd:contact:
*	There must not be an [empty characterstring](./README.md#emptychar) at ./gmd:organisationName
*	There must not be an [empty characterstring](./README.md#emptychar) at ./gmd:contactInfo/*/gmd:address/*/gmd:electronicMailAddress. Check [electronicMailAddress](#electronicMailAddress) with the regular expresion ^[A-Z0-9._%+-]+@[A-Z0-9.-]+.[A-Z]{2,}$.
If the string does not match the regular expression, the test fails (note: regex built for case insensitive match).

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD) 2.11.1, Req 37

**Test type:** Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="contact"></a> Contact   | ./gmd:contact/gmd:CI_ResponsibleParty
<a name="organisationName"></a> Organisation Name |./gmd:organisationName
<a name="electronicMailAddress"></a> Electronic Mail Address  |./gmd:contactInfo//gmd:address//gmd:electronicMailAddress
