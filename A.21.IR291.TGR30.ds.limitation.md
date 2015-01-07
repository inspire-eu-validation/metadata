
# Limitations on public access

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
* MD_LegalConstraints. accessConstraints
* MD_LegalConstraints. otherConstraints
* MD_SecurityConstraints. classification

**Test method**	

Four types of [constraints](#resourceConstraints) may occur: gmd:accessConstraints (1), gmd:otherConstraints (2), gmd:classification (3) and gmd:useLimitation (4). The following actions are performed for each one of the possible types:
* The element must have an element at gmd:MD_RestrictionCode[@codeListValue=x], where x is of type MD_RestrictionCode as defined in [ISO 19115, chapter B.5.24](http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#MD_RestrictionCode). 
* The element is free text and not [empty characterstring](./README.md#emptychar) 
* The element must have an element at gmd:MD_ClassificationCode[@codeListValue=x], where x is of type MD_ClassificationCode as defined in [ISO 19115, chapter B.5.24](http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#MD_ClassificationCode).

If none of the four elements is found, the test fails.

**Reference(s)**	 

* [IR](./README.md#IR), Chap. 2.9.1
* [ISO 19115](./README.md#ISO19115), B.5.24
* [TG](./README.md#TG) Req 30, 31 & 32

**Test type:** Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="resourceConstraints"></a> resourceConstraints  | ./gmd:identificationInfo/*/gmd:MD_DataIdentification/*/gmd:resourceConstraints/*

