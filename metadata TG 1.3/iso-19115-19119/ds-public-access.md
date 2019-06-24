# Dataset public access

**Purpose**

Limitations on public access must be described at least once for the resource.

There shall be at least one ISO 19115 metadata element representing a limitation on public access and one ISO 19115
metadata element representing a condition applying to access and use  as part of the different instances of MD_Constraints and its subclasses

There shall be at least one instance of MD_Constraints or one of its subclasses even if there is no limitation on public access or no specific condition applies to access and use of the resource.

Limitations on public access shall be represented by at least one of these metadata elements:

* MD_LegalConstraints.accessConstraints
* MD_LegalConstraints.otherConstraints
* MD_SecurityConstraints.classification

**Prerequisites**

**Test method**

Check whether at least one of the elements available inside [gmd:resourceConstraints](#resourceConstraints) passes at least one of the following checks:
* Check whether it contains an element accessConstraints of type gmd:MD_RestrictionCode[@codeListValue=x], where x is of type MD_RestrictionCode as defined in [ISO 19115, chapter B.5.24](http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#MD_RestrictionCode).
If x is “otherRestrictions” check also whether the element inside [gmd:resourceConstraints](#resourceConstraints) contains an element otherConstraints of type CharacterString and which is not an [empty characterstring](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#emptychar). 
* Check whether it contains an element classification of type gmd:MD_ClassificationCode[@codeListValue=x], where x is of type MD_ClassificationCode as defined in [ISO 19115, chapter B.5.24](http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#MD_ClassificationCode).

If none of the elements inside [gmd:resourceConstraints](#resourceConstraints) passes at least one of the checks, the test fails.

**Reference(s)**	 

* [ISO 19115](./README#ref_ISO_19115), B.5.24
* [TG MD](./README#ref_TG_MD) 2.9.1, Req 30, 31 & 32

**Test type**: Automated

**Notes**

The test method does not state, if the test applies only to datasets, dataset series, or also services. TG MD sections 2.9 and 2.9.1 do not appear to be restricted to a specific resource type, either. ISO 19115:2003 and ISO 19119:2005 both define "resourceContraints" as optional parts of their respective identification info elements. The test has therefore been implemented as a common test in the ETS.

The Xpath to reference resource constraints has been implemented as defined by TG MD 2.9.1: identificationInfo[1]/\*/resourceConstraints/\*/otherConstraints, not as defined below.

* The use of gmd:MD_DataIdentification in the path appears to be unnecessarily restrictive
* The ATS references only ISO 19115 chapter B.5.24. For the definition of MD_ClassificationCode, it should reference ISO 19115 B.5.11

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="resourceConstraints"></a> resourceConstraints  | ./gmd:identificationInfo/\*/gmd:MD_DataIdentification/\*/gmd:resourceConstraints/\*
