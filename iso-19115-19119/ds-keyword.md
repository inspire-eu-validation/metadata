# Dataset keyword

**Purpose**: Ds keyword. If the resource is a dataset or a dataset series, at least one keyword must originate from the INSPIRE theme of the GEMET Thesaurus

**Prerequisites**

* [Hierarchy](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/hierarchy) 
* [Keyword](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/keyword)

**Test method**

This test case only applies to records with a [hierarchyLevel](#hierarchyLevel) value 'dataset' or 'series'.

The test should check for each descriptiveKeywords block if it references either http://www.eionet.europa.eu/gemet/inspire_themes or any duplicate of that thesaurus, e.g. http://inspire.ec.europa.eu/theme. If a block is referencing that thesaurus the test should check if at least one [keyword](#keyword) is available and it matches with a concept in the thesaurus.

If a keyword from that source is found, the test succeeds, otherwise it will fail.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#ref_TG_MD) Chap. 2.2.3, Req 14
* http://inspire.ec.europa.eu/theme

**Test type**: Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="keyword"></a> keyword   | gmd:identificationInfo[1]/*/gmd:descriptiveKeywords/*/gmd:keyword
