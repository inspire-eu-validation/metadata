# Metadata contact

**Purpose**: At least one point of contact must be given.

**Prerequisites**

**Test method**

The test first checks if a [contact](#contact) element is given. It then performs the following checks for every element at gmd:contact:
*	There must not be an [empty characterstring](./README#emptychar) at ./gmd:organisationName
*	There must not be an [empty characterstring](./README#emptychar) at ./gmd:contactInfo/\*/gmd:address/\*/gmd:electronicMailAddress. Check [electronicMailAddress](#electronicMailAddress) with the regular expresion ^[A-Z0-9._%+-]+@[A-Z0-9.-]+.[A-Z]{2,}$.
If the string does not match the regular expression, the test fails (note: regex built for case insensitive match).

**Reference(s)**	 

* [TG MD](./README#ref_TG_MD) 2.11.1, Req 37

**Test type**: Automated

**Notes**

In the ETS, an updated regex '^[a-zA-Z0-9\._%\+-]+@[a-zA-Z0-9\.-]+\.[a-zA-Z]{2,}$' has been used (regex are case sensitive and special characters like "." and "+" have to be escaped).

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="contact"></a> Contact   | ./gmd:contact/gmd:CI_ResponsibleParty
<a name="organisationName"></a> Organisation Name |./gmd:organisationName
<a name="electronicMailAddress"></a> Electronic Mail Address  |./gmd:contactInfo//gmd:address//gmd:electronicMailAddress
