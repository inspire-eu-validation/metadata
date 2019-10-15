# Responsible Organization

**Purpose**: Test that the responsible organization metadata is provided.

**Prerequisites**

**Test method**

* Check that at least one [organisation responsible](#organisationResponsible) element exists.

* For every [organisation responsible](#organisationResponsible) element,

    * Check that the [Organization Name](#organisationName) exists and its value is a non-empty free text element.

    * Check that the [Email Address](#emailAddress) of the organization is a non-empty free text element.

    * Check that the attribute codeListValue of the [Role](#role) node is the most relevant value of ISO 19139.

* If any of the checks fails the test fails.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.3.3 , Req c.10


**Test type**: Automated

**Notes**

The multiplicity of [organisation responsible](#organisationResponsible) is one or more.

According to ISO/TS 19139:2007, it is also recommended that the [Role](#role) element has a non-empty free text value.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:identificationInfo/*/gmd:pointOfContact/gmd:CI_ResponsibleParty)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="organisationResponsible"></a> Organisation Responsible | /gmd:MD_Metadata/gmd:identificationInfo/*/gmd:pointOfContact/gmd:CI_ResponsibleParty
<a name="organisationName"></a> Organisation Name |gmd:organisationName
<a name="emailAddress"></a> Email Address Organisation | gmd:contactInfo/gmd:CI_Contact/gmd:address/gmd:CI_Address/gmd:electronicMailAddress
<a name="role"></a> Role | gmd:role/gmd:CI_RoleCode
