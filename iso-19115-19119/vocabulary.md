# Vocabulary

**Purpose**: A keyword value reference can contain a controlled vocabulary from where it originates. This element is optional but, if given, must follow certain guidelines.

**Prerequisites**

**Test method**

The test performs the following check for each [vocabulary](#thesaurus):
* the node must contain a [title](#title) and should not be an [empty characterstring](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#emptychar)
* the node must contain a [date](#date)
* the node must contain a [dateType](#dateType) which contains text that equals one of 'publication', 'revision' or 'creation'.
* if the [title](#title) is 'GEMET - INSPIRE themes, version 1.0' the [date](#date) shall be '2008-06-01' and [dateType](#dateType) shall be 'publication'.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#ref_TG_MD), 2.4.2, Req 16, 17 & 18

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="thesaurus"></a> thesaurus  | gmd:identificationInfo[1]/\*/gmd:descriptiveKeywords/\*/gmd:thesaurusName
<a name="title"></a> title  | gmd:identificationInfo[1]/\*/gmd:descriptiveKeywords/\*/gmd:thesaurusName/gmd:CI_Citation/gmd:title
<a name="date"></a> date  | gmd:identificationInfo[1]/\*/gmd:descriptiveKeywords/\*/gmd:thesaurusName/gmd:CI_Citation/gmd:date/\*/gmd:date/gco:Date
<a name="dateType"></a> dateType  | gmd:identificationInfo[1]/\*/gmd:descriptiveKeywords/\*/gmd:thesaurusName//gmd:CI_Citation/gmd:date/\*/gmd:dateType
