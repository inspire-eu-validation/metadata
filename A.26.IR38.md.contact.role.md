#A.26.IR38.md.contact.role

**Purpose**: The role information of the responsible party serving as metadata point of contact is mandatory by the ISO 19115. Role code "pointOfContact" must be used.

**Prerequisites**
* [A.01.validate](A.01.validate.md) must be passed

**Test method**

* Check that the metadata record contains the [RoleCode](#roleCode) element under contact.
* Check that the attribute [codeListValue](#codeListValue) has value "pointOfContact".

**Reference(s)**

* [TG MD](./README.md#ref_TG_MD) 2.11.1, Req 38
* [ISO 19115](README.md#ref_ISO_19115)

**Test type:** Automated

**Notes**

The TG Requirement 38 is not clear: The requirement text says that "the default value is
pointOfContact", but it refers to SC16, which seems to mandate a fixed value:

    SC16.The value of MD_Metadata.contact[1].CI_ResponsibleParty.role.CI_RoleCode shall be pointOfContact.

Open questions:

* The the codeList URL above the only approved way to refer to the CI_RoleCode codelist?
* Does the string value of the [RoleCode](#roleCode) element have any significance? Does it have to also be "pointOfContact" or can it be missing entirely?

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="roleCode"></a> RoleCode  | ./gmd:contact/gmd:CI_ResponsibleParty/gmd:role/gmd:CI_RoleCode
<a name="codeList"></a> codeList   | ./gmd:contact/gmd:CI_ResponsibleParty/gmd:role/gmd:CI_RoleCode@codeList
<a name="codeListValue"></a> codeListValue   | ./gmd:contact/gmd:CI_ResponsibleParty/gmd:role/gmd:CI_RoleCode@codeListValue
