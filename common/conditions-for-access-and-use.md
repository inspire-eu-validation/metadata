# Conditions for Access and Use

**Purpose**: Check the technical restrictions of access and use of spatial data sets and services.

**Prerequisites**

**Test method**

* Check the restrictions of access and use of the service through the element [LegalConstraints](#legalConstraints), which is used to describe the non-technical access conditions and that.

* This information will be coded by giving an instance of the element gmd:AccessConstraints or gmd:UseConstraints.

* In both cases, it will be verified that there is a child element [Restriction](#restrictionCode) with a [Code List Value](#codeListValue) defined.

* At least one instance of [Other Constraints](#otherConstraints) will also be given to describe the actual constraints from the code list [conditions-applying-to-access-and-use](#http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-interoperable/conditions-applying-to-access-and-use).

* If the conditions are unknown [Other Constraints](#otherConstraints) shall include a element pointing to the value [No Conditions Apply](#noConditionsApply) in the code list "ConditionsApplyingToAccessAndUse". 

* In other cases shall include a Non-empty Free Text Element with a textual [description](#description) of the conditions in the language of the metadata. 

* The multiplicity of this element is one or more.
**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_TG_MD), 2.3.7 , Req c.18


**Test type**: Automated

**Notes**

*This element shall not be the same one as used for describing conditions applying to [conditions-applying-to-access-and-use](#http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-interoperable/conditions-applying-to-access-and-use).
*Correct description example:

|<gmd:resourceConstraints>
||	<gmd:MD_LegalConstraints>
|||		<gmd:useConstraints>
||||			<gmd:MD_RestrictionCode codeList="http://standards.iso.org/iso/19139/resources/gmxCodelists.xml#MD_RestrictionCode" codeListValue="otherRestrictions"/>
|||		</gmd:useConstraints>
|||		<gmd:otherConstraints>
||||		<gmx:Anchor xlink:href="http://inspire.ec.europa.eu/metadata-codelist/ ConditionsApplyingToAccessAndUse/noConditionsApply">
|||||				No conditions apply to access and use 
||||			</gmx:Anchor>
|||		</gmd:otherConstraints>
||	</gmd:MD_LegalConstraints>
|</gmd:resourceConstraints>

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="legalConstraints"></a> Legal Constraints  | ./gmd:identificationInfo/\*/gmd:resourceConstraints/gmd:MD_LegalConstraints
<a name="restrictionCode"></a> Restriction Code | ./gmd:identificationInfo/\*/gmd:resourceConstraints/gmd:MD_LegalConstraints/\*/gmd:MD_RestrictionCode/@codeListValue
<a name="codeListValue"></a> Code List Value | doc("http://standards.iso.org/iso/19139/resources/gmxCodelists.xml")/gmx:CodeListDictionary[@gml:id='MD_RestrictionCode']//gml:identifier/text()
<a name="otherConstraints"></a> Other Constraints | ./gmd:identificationInfo/\*/gmd:resourceConstraints/gmd:MD_LegalConstraints/gmd:otherConstraints[1]
<a name="noConditionsApply"></a> No Conditions Apply | ./gmd:identificationInfo/\*/gmd:resourceConstraints/gmd:MD_LegalConstraints/gmd:otherConstraints[1]/gmx:Anchor/@xlink:href("http://inspire.ec.europa.eu/metadata-codelist/ConditionsApplyingToAccessAndUse/noConditionsApply")
<a name="description"></a> Description Other Constrains | ./gmd:identificationInfo/\*/gmd:resourceConstraints/gmd:MD_LegalConstraints/gmd:otherConstraints[1]/gco:CharacterString






