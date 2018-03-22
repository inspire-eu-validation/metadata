# Keyword Originating CV

**Purpose**: Provide the citation of the source controlled vocabulary when giving the value of a keyword.

**Prerequisites**

**Test method**
*  The controlled vocabulary of origin of a keyword must be cited using [Citation](#citation) element, and its children elements:

*  - The vocabulary title will be given using the [title](#title), and will be free text not empty.

*  - The date of publication of the vocabulary will be given through the [Date](#date) elements and the [code](#codeListValue) for the [Date Type](#dateType).

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_TG_MD), 2.3.5 , Req c.15
* [ISO 8601](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#ref_ISO_8601)


**Test type**: Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="citation"></a> Date  | ./gmd:identificationInfo[1]/\*/descriptiveKeywords/\*/gmd:thesaurusName/gmd:CI_Citation
<a name="title"></a> Date  | ./gmd:identificationInfo[1]/\*/descriptiveKeywords/\*/gmd:thesaurusName/gmd:CI_Citation/gmd:title
<a name="date"></a> Date  | ./gmd:identificationInfo[1]/\*/descriptiveKeywords/\*/gmd:thesaurusName/\*/gmd:date/gmd:CI_Date/gmd:date[1]/gco:Date
<a name="dateType"></a> Date Type | ./gmd:identificationInfo[1]/\*/descriptiveKeywords/\*/gmd:date/gmd:CI_Date/gmd:date[1]/\*/gmd:dateType/gmd:CI_DateTypeCode/@codeListValue
<a name="codeListValue"></a> Code List Value | doc("http://standards.iso.org/iso/19139/resources/gmxCodelists.xml)//gmx:CodeListDictionary[@gml:id='CI_DateTypeCode']//gml:identifier/text()
