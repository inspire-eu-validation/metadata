#A.13.IR13.keyword

**Purpose**: At least one [keyword](#keyword) must be given to describe the subject.

**Prerequisites**
* [A.01.validate](A.01.validate.md) must be passed

**Test method**

The test checks if one keyword element is given and not .

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.4.1, Req 13

**Test type:** Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="keyword"></a> Keyword  | gmd:identificationInfo[1]/*/gmd:descriptiveKeywords/*/gmd:keyword
