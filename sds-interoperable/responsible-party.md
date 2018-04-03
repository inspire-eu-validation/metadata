# Responsible Party

**Purpose**: Verify whether the interoperable spatial data service metadata contains information about the responsible party in the role of the custodian.

The party responsible for the care and maintenance of the service needs to be discoverable both for evaluating the reliability of the 
service and for reporting the possible technical or interoperability issues.

**Prerequisites**

**Test method**
This information is verified through the element [Point Of Contact](#pointOfContact). Its multiplicity is from one or more.

This element shall be coded through the following child elements:
* The value "custodian" of ISO 19139 code list CI_RoleCode [Role Code](#codeListValue).
* The name of the organisation as the value of [organisation name](#organisationName) element with a Non-empty Free Text Element content. 
* The email address of the organisation as the value of [electronic mail adress](#electronicMailAddress) element with a Non-empty Free Text Element

**Reference(s)**

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds/README#ref_TG_MD),4.4.2.2 , Req 6.4

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
---------------------------------------------------------- | -------------------------------------------------------------------------
<a name="custodian">Point Of Contact</a>   | ./gmd:identificationInfo/\*/gmd:pointOfContact/gmd:CI_ResponsibleParty[1]
<a name="custodian">pointOfContact</a>   | ./gmd:identificationInfo/\*/gmd:pointOfContact/gmd:CI_ResponsibleParty[1]/\*/gmd:CI_RoleCode/@codeList 
<a name="codeListValue"></a> code List Value | doc("http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml)//gmx:CodeListDictionary[@gml:id='CI_RoleCode']//gml:identifier/text()
<a name="organisationName">Name Organisation</a>   | /gmd:identificationInfo/\*/gmd:pointOfContact/gmd:CI_ResponsibleParty[1]/<gmd:organisationName>/text()
<a name="electronicMailAddress">Electronic Mail Adress</a>   | /gmd:identificationInfo/\*/gmd:pointOfContact/gmd:CI_ResponsibleParty[1]/gmd:contactInfo/\*/gmd:address/\*/gmd:electronicMailAddress/text()

