# Dataset conformity specifications

**Purpose**: Check that the DQ_ConformanceResult element is correctly specified through a citation of the INSPIRE Implementing Rule
and a specification document or Conformance Class using CI_Citation element: including its official title and the date of publication of the document.

**Prerequisites**

**Test method**

The test first checks if there is at least one conformance [result](#Result) of type [gmd:DQ_ConformanceResult](#ConformanceResult).

* The [title](#title) shall be given using the gmd:title child element of the citation element with a Non-empty Free Text Element content.
* The publication date of the cited document shall be given using gmd:date child element.
* The [date](#date) value shall be expressed in accordance with [ISO 8601](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_ISO_8601) with only the date part included.
* The [Date Type Code](#dateTypeCode) element shall be given and it shall point to the value "publication" of the ISO 19139 [codeList](#codeListValue) CI_DateTypeCode30

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_TG_MD), 2.4.1, Req C.21
* [ISO 8601](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_ISO_8601)
* [ISO 19139](http://standards.iso.org/iso/19139/resources/gmxCodelists.xml#CI_DateTypeCode) Date Type Code


**Test type**: Automated

**Notes**
* For each specification, a separate element gmd:DQ_ConformanceResult must be used.
* For the INSPIRE Implementation Rule documents the value of the title element shall match exactly the official title of the cited document in the language of the metadata.


## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="result"></a> Result   | gmd:dataQualityInfo/\*/gmd:report/\*/gmd:result
<a name="ConformanceResult"></a> Conformance Result   | gmd:dataQualityInfo/\*/gmd:report/\*/gmd:result/gmd:DQ_ConformanceResult/<gmd:specification>
<a name="citation"></a> Citation  | gmd:CI_Citation/\*/gmd:report/\*/gmd:result/gmd:DQ_ConformanceResult/\*/<gmd:CI_Citation>
<a name="title"></a> Title  | gmd:title/\*/gmd:report/\*/gmd:result/gmd:DQ_ConformanceResult/\*/<gmd:CI_Citation>/<gmd:title>/text()
<a name="date"></a> Date |gmd:dataQualityInfo/\*/gmd:report/\*/gmd:result/gmd:DQ_ConformanceResult/\*/<gmd:CI_Citation>/\*/<gmd:CI_Date>/\*/<gmd:CI_DateTypeCode>///gmd:CI_DateTypeCode/@codeListValue
<a name="dateTypeCode"></a> Date Type Code | doc('http://standards.iso.org/iso/19139/resources/gmxCodelists.xml#CI_DateTypeCode')/gmx:CodeListDictionary[@gml:id='CI_DateTypeCode']//gml:identifier/text()

