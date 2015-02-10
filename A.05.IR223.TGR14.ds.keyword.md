
# Keyword for datasets

**Purpose**	

If the resource is a dataset or a dataset series, at least one keyword must originate from the INSPIRE theme of the GEMET Thesaurus

**Test method**	
If the type of the resource is not dataset or series, this test is omitted.

The test should check for each descriptiveKeywords block if it references either http://www.eionet.europa.eu/gemet/inspire_themes or any duplicate of that thesaurus (eg http://inspire.ec.europa.eu/theme). If a block is referencing that thesaurus the test should check if at least one [keyword](#keyword) is available and it matches with a concept in the thesaurus.

If a keyword from that source is found, the test succeeds, otherwise it will fail.


**Reference(s)**	 

* [IR](./README.md#IR), Chap. 2.2.3
* http://inspire.ec.europa.eu/theme
* [TG](./README.md#TG) Req 14

**Test type:** Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="keyword"></a> keyword   | gmd:identificationInfo[1]/*/gmd:descriptiveKeywords/*/gmd:keyword
 
