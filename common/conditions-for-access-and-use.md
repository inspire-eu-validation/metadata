# Conditions for Access and Use

**Purpose**: Test the technical restrictions of access and use of spatial data sets and services.

**Prerequisites**

**Test method**

* Check that it exists exactly one [Legal Constraints](#legalConstraints) element with the following features:

     * Exactly one [Access Constraints](#accessConstraints) or one [Use Constraints](#useConstraints) element.

          * The gmd:MD_RestrictionCode child element of either [Access Constraints](#accessConstraints) or [Use Constraints](#useConstraints) has attribute codeListValue with value "otherRestrictions".

     * At least one [Other Constraints](#otherConstraints) element with:

          * One [Anchor](#anchor) element which xlink:href attribute is a URL starting with "http://inspire.ec.europa.eu/metadata-codelist/ConditionsApplyingToAccessAndUse/" and postfixed with one of values of code list ConditionsApplyingToAccessAndUse of the [TG MD](./README.md#ref_TG_MD) Annex D.2.

          * Or, a non-empty free text element. 

* If any of the checks fails, the test fails. 

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.3.7 , Req c.18


**Test type**: Automated

**Notes**

The multiplicity of [Legal Constraints](#legalConstraints) is one to n. But only one shall exists for describing the 'conditions for access and use' with the features described above.

According to ISO/TS 19139:2007, it is also recommended that the [Access Constraints](#accessConstraints) or [Use Constraints](#useConstraints) element has a non-empty free text value.

This element shall not be the same one as used for describing conditions applying to [conditions-applying-to-access-and-use](#http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-interoperable/conditions-applying-to-access-and-use).

Correct description example:

     <gmd:resourceConstraints>
          <gmd:MD_LegalConstraints>
               <gmd:useConstraints>
                    <gmd:MD_RestrictionCode codeList="http://standards.iso.org/iso/19139/resources/gmxCodelists.xml#MD_RestrictionCode" codeListValue="otherRestrictions"/>
               </gmd:useConstraints>
               <gmd:otherConstraints>
                    <gmx:Anchor xlink:href="http://inspire.ec.europa.eu/metadata-codelist/ ConditionsApplyingToAccessAndUse/noConditionsApply">
                         No conditions apply to access and use 
                    </gmx:Anchor>
               </gmd:otherConstraints>
          </gmd:MD_LegalConstraints>
     </gmd:resourceConstraints>

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:identificationInfo/*/gmd:resourceConstraints)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="legalConstraints"></a> Legal Constraints | gmd:MD_LegalConstraints
<a name="accessConstraints"></a> Access Constraints | gmd:MD_LegalConstraints/gmd:accessConstraints
<a name="useConstraints"></a> Use Constraints | gmd:MD_LegalConstraints/gmd:useConstraints
<a name="otherConstraints"></a> Other Constraints | gmd:MD_LegalConstraints/gmd:otherConstraints
<a name="anchor"></a> Anchor | gmd:MD_LegalConstraints/gmd:otherConstraints/gmx:Anchor
