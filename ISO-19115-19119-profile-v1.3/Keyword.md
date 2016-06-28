# Keyword

**Purpose**: At least one [keyword](#keyword) must be given to describe the subject.

**Prerequisites**
* [Schema validation](Schema validation.md) must be passed

**Test method**

The test checks if at least one [keyword](#keyword) element is provided and it is not an [empty characterstring](./README.md#emptychar)

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.4, Req 13


**Test type:** Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="keyword"></a> keyword  | gmd:identificationInfo[1]/*/gmd:descriptiveKeywords/*/gmd:keyword
