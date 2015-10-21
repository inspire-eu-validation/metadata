#A.15.IR19.kws-in-vocab

**Purpose**: Keyword values originating from a single version of a single controlled vocabulary
shall be grouped in a single instance

**Prerequisites**
* [A.01.validate](A.01.validate.md) must be passed

**Test method**

In order to be consistent with ISO 19115, all the keyword values
originating from a single version of a single controlled vocabulary
shall be grouped in a single instance of the ISO 19115
descriptiveKeywords property.

For each [descriptiveKeywords](#keyword) element, the referenced controlled vocabulary should be unique

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD) Req 19
* [IR MD](README.md#ref_IR_MD) Part B. 3.2

**Test type:** Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="keyword"></a> Keyword   | gmd:identificationInfo[1]/*/gmd:descriptiveKeywords
