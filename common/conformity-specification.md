# Dataset conformity

**Purpose**: The metadata shall include information on the degree of conformity with the implementing 
rules on interoperability of spatial data sets.

**Prerequisites**

**Test method**

* The test first checks if there is at least one conformance [result](#Result) of type [gmd:DQ_ConformanceResult](#ConformanceResult).

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_TG_MD), 2.4.1, Req C.20

**Test type**: Automated

**Notes**
* For each specification, a separate element gmd: DQ_ConformanceResult must be used.
* The multiplicity of this element is one or more.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="result"></a> Result   | gmd:dataQualityInfo/\*/gmd:report/\*/gmd:result
<a name="ConformanceResult"></a> Conformance Result   | gmd:dataQualityInfo/\*/gmd:report/\*/gmd:result/gmd:DQ_ConformanceResult/<gmd:specification>
<a name="citation"></a> Citation  | gmd:CI_Citation/\*/gmd:report/\*/gmd:result/gmd:DQ_ConformanceResult/\*/<gmd:CI_Citation>
<a name="title"></a> Title  | gmd:title/\*/gmd:report/\*/gmd:result/gmd:DQ_ConformanceResult/\*/<gmd:CI_Citation>/<gmd:title>/text()
<a name="dateType"></a> dateType |gmd:dataQualityInfo/\*/gmd:report/\*/gmd:result/gmd:DQ_ConformanceResult/\*/<gmd:CI_Citation>/\*/<gmd:CI_Date>/\*/<gmd:CI_DateTypeCode>///gmd:CI_DateTypeCode/@codeListValue
<a name="codeListValue"></a> codeListValue | doc("http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/Codelist/gmxCodelists.xml)//gmx:CodeListDictionary[@gml:id='CI_DateTypeCode']//gml:identifier/text()

