# Metadata contact role

**Purpose**: The role information of the responsible party serving as metadata point of contact is mandatory by the ISO 19115. Role code "pointOfContact" must be used.

**Prerequisites**

**Test method**

* Check that the metadata record contains the [RoleCode](#roleCode) element under contact.
* Check that the attribute [codeListValue](#codeListValue) has the string value "pointOfContact".

**Reference(s)**

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#ref_TG_MD) 2.11.1, Req 38
* [ISO 19115](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#ref_ISO_19115)

**Test type**: Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="roleCode"></a> RoleCode  | ./gmd:contact/gmd:CI_ResponsibleParty/gmd:role/gmd:CI_RoleCode
<a name="codeList"></a> codeList   | ./gmd:contact/gmd:CI_ResponsibleParty/gmd:role/gmd:CI_RoleCode@codeList
<a name="codeListValue"></a> codeListValue   | ./gmd:contact/gmd:CI_ResponsibleParty/gmd:role/gmd:CI_RoleCode@codeListValue
