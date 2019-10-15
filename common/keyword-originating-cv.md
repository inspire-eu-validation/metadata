# Keyword Originating CV

**Purpose**: Test that the citation of the source controlled vocabulary when giving the value of a keyword is provided correctly.

**Prerequisites**

**Test method**

* For every [Citation](#citation) element,

    * Check that the [title](#title) element exists and it is a non-empty free text.

    * Check that the [Date](#date) element exists.

    * Check that the [Date Type](#dateType) element exists and it has an attribute codeList with "http://standards.iso.org/iso/19139/resources/gmxCodelists.xml#CI_DateTypeCode" and an attribute codeListValue with value "publication".

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.3.5 , Req c.15
* [ISO 8601](./README.md#ref_ISO_8601)


**Test type**: Automated

**Notes**

The multiplicity of [Citation](#citation) is zero or more.

According to ISO/TS 19139:2007, it is also recommended that the [Date Type](#dateType) element has a non-empty free text value.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:identificationInfo/*)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="citation"></a> Citation  | gmd:descriptiveKeywords/gmd:MD_Keywords/gmd:thesaurusName/gmd:CI_Citation
<a name="title"></a> Title  | gmd:descriptiveKeywords/gmd:MD_Keywords/gmd:thesaurusName/gmd:CI_Citation/gmd:title
<a name="date"></a> Date  | gmd:descriptiveKeywords/gmd:MD_Keywords/gmd:thesaurusName/gmd:CI_Citation/gmd:date/gmd:CI_Date/gmd:date/gco:Date
<a name="dateType"></a> Date Type | gmd:descriptiveKeywords/gmd:MD_Keywords/gmd:thesaurusName/gmd:CI_Citation/gmd:date/gmd:CI_Date/gmd:date/gmd:dateType/gmd:CI_DateTypeCode
