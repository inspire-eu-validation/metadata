# Metadata Point of Contact


**Purpose**: Evaluate the description of the organisation responsible for the creation and maintenance of the metadata.

**Prerequisites**

**Test method**

* Check the point of contact for the [party responsible](#partyResponsable) for the metadata.
* The multiplicity of this element is one or more.

* They have to come defined through the children elements:

* - Name of the responsible [organization](#organisationName) with a non-empty free text element content.

* - The [email address](#mailAddress) of the organization with a free text element not empty.

* - The value for the [Role](#role) coded from the [Code List Value](#codeListValue) [ISO 19139] CI_RoleCode.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_TG_MD), 2.2.3 , Req c.6


**Test type**: Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="partyResponsable"></a> Party Responsable  | ./gmd:contact/gmd:CI_ResponsibleParty[1]
<a name="organisationName"></a> Organisation Name  | ./gmd:contact/gmd:CI_ResponsibleParty[1]/gmd:organisationName/text()
<a name="mailAddress"></a> Mail Address Organisation | ./gmd:contact/gmd:CI_ResponsibleParty[1]/gmd:contactInfo/\*/gmd:address/\*/gmd:electronicMailAddress/text()
<a name="role"></a> Role  | ./gmd:contact/gmd:CI_ResponsibleParty[1]/gmd:role/gmd:CI_RoleCode/@codeListValue
<a name="codeListValue"></a> Code List Value | doc("http://standards.iso.org/iso/19139/resources/gmxCodelists.xml")//gmx:CodeListDictionary[@gml:id='CI_RoleCode']//gml:identifier/text()
