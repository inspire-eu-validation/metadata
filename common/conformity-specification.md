# Dataset Conformity Specifications

**Purpose**: Test that the DQ_ConformanceResult element is correctly specified through a citation of the INSPIRE Implementing Rule and a specification document or Conformance Class using CI_Citation element: including its official title and the date of publication of the document.

**Prerequisites**

[Conformity](./conformity.md)

**Test method**

* For every [Result](#result) element,

    * Checks that at least one [Citation](#citation) exists, then for every [Citation](#citation),

        * Check that [Title](#title) element exists and its content is a Non-empty Free Text Element.

        * Check that [Date](#date) element exists and its value is in accordance with [ISO 8601](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_ISO_8601) with only the date part included.

            * Check that [Date Type Code](#dateTypeCode) exists, its attribute codeList is "http://standards.iso.org/iso/19139/resources/gmxCodelists.xml#CI_DateTypeCode" and its attribute codeListValue is "publication".

* If any of the checks fails, the test fails.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.4.1, Req C.21
* [ISO 8601](./README.md#ref_ISO_8601)
* [ISO 19139](http://standards.iso.org/iso/19139/resources/gmxCodelists.xml#CI_DateTypeCode) Date Type Code


**Test type**: Automated

**Notes**

The multiplicity of this element is one or more.

For each specification, a separate element gmd:DQ_ConformanceResult must be used.

For the INSPIRE Implementation Rule documents the value of the title element shall match exactly the official title of the cited document in the language of the metadata.


## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:dataQualityInfo/gmd:DQ_DataQuality/gmd:report)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="result"></a> Result | gmd:DQ_DomainConsistency/gmd:result
<a name="citation"></a> Citation | gmd:DQ_DomainConsistency/gmd:result/gmd:specification/gmd:CI_Citation
<a name="title"></a> Title | gmd:DQ_DomainConsistency/gmd:result/gmd:specification/gmd:CI_Citation/gmd:title
<a name="date"></a> Date | gmd:DQ_DomainConsistency/gmd:result/gmd:specification/gmd:CI_Citation/gmd:date
<a name="dateTypeCode"></a> Date Type Code | gmd:DQ_DomainConsistency/gmd:result/gmd:specification/gmd:CI_Citation/gmd:date/gmd:CI_Date/gmd:dateType/gmd:CI_DateTypeCode
