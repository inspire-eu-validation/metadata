# INSPIRE Theme Keyword

**Purpose**: Test that the INSPIRE Data Themes, which the data belongs to, are declared using at least one keyword from the INSPIRE Spatial Data Themes vocabulary.

**Prerequisites**

**Test method**

* Check that at least one of the [MD_Keywords](#mdKeywords) elements has a [Title](#title) child element with value "GEMET - INSPIRE themes, version 1.0". Then,

    * For every [MD_Keywords](#mdKeywords) which title child is "GEMET - INSPIRE themes, version 1.0":

        * Check that a [Keyword](#keyword) with the title of theme is included as a non-empty free text referencing the INSPIRE Spatial Data Themes vocabulary of the general environmental multilingual thesaurus [GEMET](http://www.eionet.europa.eu/gemet/en/inspire-themes/).

* If any of the checks fails, the test fails.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 3.1.2.2, Req 1.4
* [ISO 19115](./README.md#ref_ISO_19115) table B.5.25 MD_ScopeCode 
* [GEMET](http://www.eionet.europa.eu/gemet/en/inspire-themes/)

**Test type**: Automated

**Notes**

The multiplicity of this element is one or more.


## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:identificationInfo/gmd:MD_DataIdentification)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="mdKeywords"></a> MD_Keywords | gmd:descriptiveKeywords/gmd:MD_Keywords
<a name="title"></a> Title | gmd:descriptiveKeywords/gmd:MD_Keywords/gmd:thesaurusName/gmd:CI_Citation/gmd:title
<a name="keyword"></a> Keyword | gmd:descriptiveKeywords/gmd:MD_Keywords/gmd:keyword
