# Abstract

**Purpose**: Validates if a resource abstract is provided

**Prerequisites**

* [Schema validation](Schema validation.md) must be passed

**Test method**

Checks if an [abstract](#abstract) is present and not an [empty characterstring](./README.md#emptychar)

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), Chap. 2.2.2


**Test type:** Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
abstract <a name="abstract"></a>   | gmd:identificationInfo[1]/*/gmd:abstract
