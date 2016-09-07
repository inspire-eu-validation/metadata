# Keywords in vocabulary

**Purpose**: Keyword values originating from a single version of a single controlled vocabulary
shall be grouped in a single instance

**Prerequisites**

**Test method**

1. For each [descriptiveKeywords](#keyword) element, the referenced controlled vocabulary should be unique 
2. Each referenced controlled vocabulary must appear in at most one [descriptiveKeywords](#keyword) element

Use the vocabulary [title](#title) in comparisons.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#ref_TG_MD) 2.4.2, Req 19

**Test type**: Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="keyword"></a> Keyword   | gmd:identificationInfo[1]/\*/gmd:descriptiveKeywords
<a name="title"></a> title  | gmd:identificationInfo[1]/\*/gmd:descriptiveKeywords/\*/gmd:thesaurusName/gmd:CI_Citation/gmd:title
