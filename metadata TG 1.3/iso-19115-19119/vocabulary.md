# Vocabulary

**Purpose**: A keyword value reference can contain a controlled vocabulary from where it originates. This element is optional but, if given, must follow certain guidelines.

**Prerequisites**

**Test method**

The test performs the following check for each [vocabulary](#thesaurus):
* the node must contain a [title](#title) and should not be an [empty characterstring](./README#emptychar)
* the node must contain a [date](#date)
* the node must contain a [dateType](#dateType) which contains text that equals one of 'publication', 'revision' or 'creation'.

**Reference(s)**	 

* [TG MD](./README#ref_TG_MD), 2.4.2, Req 16, 17 & 18

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="thesaurus"></a> thesaurus  | gmd:identificationInfo[1]/\*/gmd:descriptiveKeywords/\*/gmd:thesaurusName
<a name="title"></a> title  | gmd:identificationInfo[1]/\*/gmd:descriptiveKeywords/\*/gmd:thesaurusName/gmd:CI_Citation/gmd:title
<a name="date"></a> date  | gmd:identificationInfo[1]/\*/gmd:descriptiveKeywords/\*/gmd:thesaurusName/gmd:CI_Citation/gmd:date/\*/gmd:date/gco:Date
<a name="dateType"></a> dateType  | gmd:identificationInfo[1]/\*/gmd:descriptiveKeywords/\*/gmd:thesaurusName//gmd:CI_Citation/gmd:date/\*/gmd:dateType
