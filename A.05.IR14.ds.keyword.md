#A.05.IR14.ds.keyword

**Purpose**: If the resource is a dataset or a dataset series, it checks that at least one keyword originating from the INSPIRE theme of the GEMET Thesaurus is provided

**Prerequisites**
* [A.01.validate](A.01.validate.md) must be passed
* [A.13.IR13.keyword](A.13.IR13.keyword.md) must be passed
* [A.15.IR19.kws-in-vocab](A.15.IR19.kws-in-vocab.md) must be passed
* [A.26.IR39.language](A.26.IR39.language.md) must be passed

**Test method**

If the resource type is not dataset or series, this test is omitted.

The test should check whether a descriptiveKeywords block exists which references http://www.eionet.europa.eu/gemet/inspire_themes. If a block is referencing that thesaurus the test should check if at least one [keyword](#keyword) is available and it matches with a concept in the thesaurus, in the language of the metadata OR using a language neutral URI. 

If at least one descriptiveKeywords block references INSPIRE GEMET and at least one keyword from that source is found in this block, the test succeeds, otherwise it will fail.


**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD) Chap. 2.4, Req 14
* [IR MD](README.md#ref_IR_MD) Part B. 3.1
* http://inspire.ec.europa.eu/theme


**Test type:** Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="keyword"></a> keyword   | gmd:identificationInfo[1]/*/gmd:descriptiveKeywords/*/gmd:keyword
