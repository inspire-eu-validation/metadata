#Responsible party role

**Purpose**: Every responsible organization must name a responsible party role.

**Prerequisites**

**Test method**

The test first checks if there is at least one [role](#role) element.

The element must contain an element at gmd:CI_RoleCode[@codeListValue=x], where x is one of the values described in [ISO 19115, chapter B.5.5](http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#CI_RoleCode).

**Reference(s)**

* ISO 19115, B.5.5
* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#ref_TG_MD), 2.10.2

**Test type**: Automated

**Notes**

* There is no explicit Implementation Requirement in [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#ref_TG_MD) for this test.

##Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="role"></a> role   | gmd:identificationInfo[1]/*/gmd:pointOfContact/*/gmd:role
