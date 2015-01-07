
# Keyword for datasets

**Purpose**	

If the resource is a dataset or a dataset series, at least one keyword must originate from the INSPIRE theme of the GEMET Thesaurus

**Test method**	

Checks for every [keyword](#keyword) if it is not an [empty characterstring](./README.md#emptychar).  The text content for every keyword
can be found in either the indicated language or english version of the [INSPIRE GEMET Thesaurus](http://inspire.ec.europa.eu/theme). 
If at least one keyword from that source is found, the test succeeds, otherwise it will fail.
If the type of the resource is not dataset or series, this test is omitted.

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
 
