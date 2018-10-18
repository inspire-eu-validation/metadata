# Conditions for Access and Use

**Purpose**: Test the technical restrictions of access and use of spatial data sets and services.

**Prerequisites**

**Test method**

* Check that if [Access Constraints](#accessConstraints) and/or [Use Constraints](#useConstraints) elements exists they belong to the same [Legal Constraints](#legalConstraints) parent node.

    * If [Access Constraints](#accessConstraints) element exists,

        * Check that the attribute codeList is "http://standards.iso.org/iso/19139/resources/gmxCodelists.xml" and attribute codeListValue is "otherRestrictions".

    * If [Use Constraints](#useConstraints) element exists,

        * Check that the attribute codeList is "http://standards.iso.org/iso/19139/resources/gmxCodelists.xml" and attribute codeListValue is "otherRestrictions".

    * Check that at least one [Other Constraints](#otherConstraints) child element exists.

        * If gmx:Anchor child element exists, check that it has an attribute xlink:href with URL value "http://inspire.ec.europa.eu/metadata-codelist/ConditionsApplyingToAccessAndUse/noConditionsApply" or with URL value "http://inspire.ec.europa.eu/metadata-codelist/ConditionsApplyingToAccessAndUse/conditionsUnknown".

        * Else, check that a non-empty free text element exist.

* If any of the checks fails, the test fails.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.3.7 , Req c.18


**Test type**: Automated

**Notes**

The multiplicity of this element is one or more.

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

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:identificationInfo/gmd:MD_DataIdentification/gmd:resourceConstraints)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="legalConstraints"></a> Legal Constraints | gmd:MD_LegalConstraints
<a name="accessConstraints"></a> Access Constraints | gmd:MD_LegalConstraints/gmd:accessConstraints
<a name="useConstraints"></a> Use Constraints | gmd:MD_LegalConstraints/gmd:useConstraints
<a name="otherConstraints"></a> Other Constraints | gmd:MD_LegalConstraints/gmd:otherConstraints
