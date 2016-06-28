#Ds public access

**Purpose**

Limitations on public access must be described at least once for the resource.

There shall be at least one ISO 19115 metadata element representing
a limitation on public access and one ISO 19115
metadata element representing a condition applying to access and
use  as part of the different instances of MD_Constraints
and its subclasses

There shall be at least one instance of MD_Constraints or one of its
subclasses even if there is no limitation on
public access or no specific condition applies to access and use of
the resource.

Limitations on public access shall be represented by at least one of
these metadata elements:
* MD_LegalConstraints.accessConstraints
* MD_LegalConstraints.otherConstraints
* MD_SecurityConstraints.classification

**Prerequisites**
* [Schema validation](schema-validation.md) must be passed

**Test method**

Check whether at least one of the elements available inside [gmd:resourceConstraints](#resourceConstraints) passes at least one of the following checks:
* Check whether it contains an element accessConstraints of type gmd:MD_RestrictionCode[@codeListValue=x], where x is of type MD_RestrictionCode as defined in [ISO 19115, chapter B.5.24](http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#MD_RestrictionCode).
If x is “otherRestrictions” check also whether the element inside [gmd:resourceConstraints](#resourceConstraints) contains an element otherConstraints of type CharacterString and which is not an [empty characterstring](./README.md#emptychar). 
* Check whether it contains an element classification of type gmd:MD_ClassificationCode[@codeListValue=x], where x is of type MD_ClassificationCode as defined in [ISO 19115, chapter B.5.24](http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#MD_ClassificationCode).

If none of the elements inside [gmd:resourceConstraints](#resourceConstraints) passes at least one of the checks, the test fails.

**Reference(s)**	 

* [ISO 19115](./README.md#ref_ISO_19115), B.5.24
* [TG MD](./README.md#ref_TG_MD) 2.9.1, Req 30, 31 & 32

**Test type:** Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="resourceConstraints"></a> resourceConstraints  | ./gmd:identificationInfo/*/gmd:MD_DataIdentification/*/gmd:resourceConstraints/*
