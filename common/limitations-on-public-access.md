# Limitations on Public Sccess 

**Purpose**: Provide information on the existence of some limitation of public access to spatial data sets and spatial data services.

**Prerequisites**

**Test method**

Check the information about the existence and its reasons in the limitations of public access to the data set. To do this, the element [Legal Constraints](#legalConstraints) will be used.
* The limitations (or lack thereof) will include both specifications of the restriction:

* An [Restriction Code](#restrictionCode) element will be given with a value from the "otherRestrictions" [Code List Value](#codeListValue)

* And at least one instance [Other Constraints](#otherConstraints) that points to one of the values in the code list for "LimitationsOnPublicAccess26". In the case of no access limitations, this element must point to the value of the "noLimitations" code list.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_TG_MD), 2.3.6 , Req c.17


**Test type**: Automated

**Notes**

*This element shall not be the same one as used for describing conditions applying to [conditions-applying-to-access-and-use](#http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-interoperable/conditions-applying-to-access-and-use).

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="legalConstraints"></a> Legal Constraints  | ./gmd:identificationInfo/\*/gmd:resourceConstraints/gmd:MD_LegalConstraints
<a name="restrictionCode"></a> Restriction Code | ./gmd:identificationInfo/\*/gmd:resourceConstraints/gmd:MD_LegalConstraints/gmd:accessConstraints/gmd:MD_RestrictionCode/@codeListValue
<a name="codeListValue"></a> Code List Value | doc("http://standards.iso.org/iso/19139/resources/gmxCodelists.xml)//gmx:CodeListDictionary[@gml:id='MD_RestrictionCode']//gml:identifier/text()

<a name="otherConstraints"></a> Other Constraints | ./gmd:identificationInfo/\*/gmd:resourceConstraints/gmd:MD_LegalConstraints/gmd:otherConstraints/gmx:Anchor/@xlink:href='http://inspire.ec.europa.eu/metadata-
codelist/LimitationsOnPublicAccess/INSPIRE_Directive_Article13_1a'





