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

The test method is not clear on how a specific code list is referenced in a gmd:thesaurusName. The ETS assumes that the gmd:thesaurusName/\*/gmd:title/\*/text() equals 'GEMET - INSPIRE themes, version 1.0'. 

The TG MD requirement 14 does not require that each and every descriptiveKeywords block that references the INSPIRE themes code list must have at least one code from that code list. It states that "If only one keyword is used" - which is ambiguous. The requirement may need to be reworded. The ETS checks each and every descriptiveKeywords block that references the INSPIRE themes code list.

TG MD requirement 14 states that the keyword shall be expressed in one of the official INSPIRE languages or a language neutral term "such as a URI". The ETS retrieves the Atom feeds of the code list from the INSPIRE registry, for each of the following languages: 'bg','cs','da','de','et','el','en','es','fr','hr','it','lv','lt','hu','mt','nl','pl','pt','ro','sk','sl','fi','sv'. In addition, the language independent code values are parsed from the Ids of the feed entries. A keyword is compared against this set of strings. However, at the moment, no comparison against a full URI is made.

The depencency to [Hierarchy](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/hierarchy) has not been implemented in the ETS as it still seems reasonable to test the available dataset (series) metadata records.  

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="keyword"></a> keyword   | gmd:identificationInfo[1]/\*/gmd:descriptiveKeywords/\*/gmd:keyword
