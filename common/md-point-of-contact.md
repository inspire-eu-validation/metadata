# Metadata Point of Contact


**Purpose**: Test that the description of the organisation responsible for the creation and maintenance of the metadata is provided.

**Prerequisites**

**Test method**

* Check that at least one [Responsible Party](#responsibleParty) element exists.

* For every [Responsible Party](#responsibleParty) element,

    * Check that the [Organization Name](#organizationName) exists and its value is a non-empty free text element.

    * Check that the [Email Address](#emailAddress) of the organization is a non-empty free text element.

* Check that there is at least one [Responsible Party](#responsibleParty) element with "pointOfContact" as codeListValue of its [Role](#role) node.

* If any of the checks fails the test fails.

**Reference(s)**

* [TG MD](./README.md#ref_TG_MD), 2.2.3 , Req c.6
* [CI_RoleCode](http://standards.iso.org/iso/19139/resources/gmxCodelists.xml#CI_RoleCode)

**Test type**: Automated

**Notes**

The multiplicity of this element is one or more.

According to ISO/TS 19139:2007, it is also recommended that the [Role](#role) element has a non-empty free text value.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_metadata/gmd:contact/gmd:CI_ResponsibleParty)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="responsibleParty"></a> Responsible Party | /gmd:MD_metadata/gmd:contact/gmd:CI_ResponsibleParty
<a name="organizationName"></a> Organization Name | gmd:organisationName
<a name="emailAddress"></a> Email Address | gmd:contactInfo/gmd:CI_Contact/gmd:address/gmd:CI_Address/gmd:electronicMailAddress
<a name="role"></a> Role | gmd:role/gmd:CI_RoleCode
