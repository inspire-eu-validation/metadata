# Dataset access use

**Purpose**: Conditions applying to access and use must be described at least once for the resource.

**Prerequisites**

**Test method**

The test checks if a [useLimitation](#useLimitation) element is provided and it is not an [empty characterstring](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#emptychar).

If no conditions apply to the access and use of the resource, "no conditions apply" shall be used. If conditions are unknown, "conditions unknown" shall be used.

Descriptions of terms and conditions, including where applicable, the corresponding fees shall be provided through this element or a link (URL) where these terms and conditions are described. The content will need to be checked manually.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#ref_TG_MD), 2.9.2, Req 33,34

**Test type**: Automated/Manual

**Notes**

According to TG MD 2.9.2 this appears to be a common test, not one specific for datasets and series. The test description also does not state such a restriction. The test has therefore been implemented as a "common" test in the ETS.

##Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="useLimitation"></a> useLimitation  | ./gmd:identificationInfo/\*/gmd:resourceConstraints/\*/gmd:useLimitation
