# Conditions applying to access and use 

**Purpose**: Check the technical restrictions of access and use of an interoperable spatial data service specified in the metadata.

**Prerequisites**

* [resource-type](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/resource-type)

**Test method**
* Check the restrictions of access and use of the service through the element [LegalConstraints](#legalConstraints), which is used to describe the non-technical access conditions and that.

* The multiplicity of this element is one or more.

* This information will be coded by giving an instance of the element gmd:AccessConstraints or gmd:UseConstraints.
In both cases, it will be verified that there is a child element [Restriction](#Restriction) with a [Code List Value](#codeListValue) defined.

* At least one instance of [Other Constraints](#otherConstraints) will also be given to describe the actual constraints from the code list ConditionsApplyingToAccessAndUse.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-interoperable/README#ref_TG_MD) 4.4.1.1, Req 6.1
* [ISO 19115](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-interoperable/README#ref_ISO_19115) table B.8 MD_RestrictionCode

**Test type**: Automated

**Notes**
This element shall not be the same used for describing limitations on public access.

## Contextual XPath references

The namespace prefixes used as described in [README.md](#README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| ------------------------------------------------------------------
<a name="LegalConstraints"></a> LegalConstraints |  ./gmd:identificationInfo/\*/gmd:resourceConstraints/gmd:MD_LegalConstraints[1]
<a name="Restriction"></a> Restriction |  ./gmd:identificationInfo/\*/gmd:resourceConstraints/gmd:MD_LegalConstraints[1]/\*/<gmd:MD_RestrictionCode>/@codeListValue
<a name="codeListValue"></a> code List Value | doc("http://standards.iso.org/iso/19139/resources/gmxCodelists.xml)//gmx:CodeListDictionary[@gml:id='MD_RestrictionCode']//gml:identifier/text()
<a name="otherConstraints"></a> Other Constraints | ./gmd:identificationInfo/\*/gmd:resourceConstraints/gmd:MD_LegalConstraints/gmd:otherConstraints/gmx:Anchor/@xlink:href='http://inspire.ec.europa.eu/metadata-
codelist/LimitationsOnPublicAccess/INSPIRE_Directive_Article13_1a'