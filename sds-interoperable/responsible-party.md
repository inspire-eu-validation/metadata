# Responsible Party

**Purpose**: 
Test that the interoperable spatial data service metadata contains information about the responsible party in the role of the custodian.

**Prerequisites**

**Test method**

* Check that at least one [Responsible Party](#responsibleParty) element exists.

* For every [Responsible Party](#responsibleParty),

    * Check that [Role Code](#roleCode) element exists and it has an attribute codeList with value "http://standards.iso.org/iso/19139/resources/gmxCodelists.xml#CI_RoleCode" and an attribute codeListValue with "custodian" value.

**Reference(s)**

* [TG MD](./README.md#ref_TG_MD), 4.4.2.2 , Req 6.4

**Test type**: Automated

**Notes**

The multiplicity of this element is one or more.

The specification for this requirement is defined in [Responsible organisation](../common/responsible-organisation.md) requirement from [Common Requirements](../common/README.md).

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:identificationInfo/gmd:MD_DataIdentification)
---------------------------------------------------------- | -------------------------------------------------------------------------
<a name="responsibleParty"></a> Responsible Party | gmd:pointOfContact/gmd:CI_ResponsibleParty
<a name="roleCode"></a> Role Code | gmd:pointOfContact/gmd:CI_ResponsibleParty/gmd:role/gmd:CI_RoleCode
