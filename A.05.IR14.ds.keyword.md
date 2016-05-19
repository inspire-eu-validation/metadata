#A.05.IR14.ds.keyword

**Purpose**: Keyword for datasets. If the resource is a dataset or a dataset series, at least one keyword must originate from the INSPIRE theme of the GEMET Thesaurus

**Prerequisites**
* [A.01.validate](A.01.validate.md) must be passed
* [A.13.IR13.keyword](A.13.IR13.keyword.md) must be passed

**Test method**
If the type of the resource is not dataset or series, this test is omitted.

The test should check for each descriptiveKeywords block if it references either http://www.eionet.europa.eu/gemet/inspire_themes or any duplicate of that thesaurus (eg http://inspire.ec.europa.eu/theme). If a block is referencing that thesaurus the test should check if at least one [keyword](#keyword) is available and it matches with a concept in the thesaurus.

If a keyword from that source is found, the test succeeds, otherwise it will fail.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD) Chap. 2.2.3, Req 14
* [IR MD](README.md#ref_IR_MD) Part B. 3.1
* http://inspire.ec.europa.eu/theme


**Test type:** Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="keyword"></a> keyword   | gmd:identificationInfo[1]/*/gmd:descriptiveKeywords/*/gmd:keyword
