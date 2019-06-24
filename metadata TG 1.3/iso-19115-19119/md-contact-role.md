# Metadata contact role

**Purpose**: The role information of the responsible party serving as metadata point of contact is mandatory by the ISO 19115. Role code "pointOfContact" must be used.

**Prerequisites**

**Test method**

* Check that the metadata record contains the [RoleCode](#roleCode) element under contact.
* Check that the attribute [codeListValue](#codeListValue) has the string value "pointOfContact".

**Reference(s)**

* [TG MD](./README#ref_TG_MD) 2.11.1, Req 38
* [ISO 19115](./README#ref_ISO_19115)

**Test type**: Automated

**Notes**

It is not entirely clear, if each and every gmd:MD_Metadata/gmd:contact must have role 'pointOfContact', or if one is sufficient. This should be clarified.

It is also not clear, if the abstract test "md-contact" should only apply to contact information with role 'pointOfContact'. TG MD section 2.11.1 is all about the "metadata point of contact". Therefore it looks like the ETS should test that there is at least one (or exactly one?) gmd:MD_Metadata/gmd:contact with role 'pointOfContact' and that it has an organisation name and email address. In that case the tests md-contact and md-contact-role could be merged.

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="roleCode"></a> RoleCode  | ./gmd:contact/gmd:CI_ResponsibleParty/gmd:role/gmd:CI_RoleCode
<a name="codeList"></a> codeList   | ./gmd:contact/gmd:CI_ResponsibleParty/gmd:role/gmd:CI_RoleCode@codeList
<a name="codeListValue"></a> codeListValue   | ./gmd:contact/gmd:CI_ResponsibleParty/gmd:role/gmd:CI_RoleCode@codeListValue
