# Conformity to Technical Specifications

**Purpose**: The metadata element will contain technical specifications to which the invokable spatial data service must be fully adjusted. 
To do this, it must provide all a series of technical elements necessary to allow its invocation.

**Prerequisites**

* [conformity](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/conformity)

**Test method**
* Verify that the service fully complies with at least one technical specification that provides all the technical elements necessary to 
invoke the service and allow its use.
*This is tested from the DQ_ConformanceResult element (according to TG Requirement C.20). In addition, it must contain an [citation](#citation) for the coded technical specification according to requirement TG.C.21 [conformity-specification](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/conformity-specification).

*The multiplicity of the element is one or more.

**Reference(s)**

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-invocable/README#ref_TG_MD) 4.3.3.3, Req 5.5

**Test type**: Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-invocable/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="citation"></a> Citation  | gmd:CI_Citation/\*/gmd:report/\*/gmd:result/gmd:DQ_ConformanceResult/\*/<gmd:CI_Citation>
<a name="title"></a> Title  | gmd:title/\*/gmd:report/\*/gmd:result/gmd:DQ_ConformanceResult/\*/<gmd:CI_Citation>/<gmd:title>/text()
<a name="dateType"></a> dateType |gmd:dataQualityInfo/\*/gmd:report/\*/gmd:result/gmd:DQ_ConformanceResult/\*/<gmd:CI_Citation>/\*/<gmd:CI_Date>/\*/<gmd:CI_DateTypeCode>///gmd:CI_DateTypeCode/@codeListValue
<a name="codeListValue"></a> codeListValue | doc("http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/Codelist/gmxCodelists.xml)//gmx:CodeListDictionary[@gml:id='CI_DateTypeCode']//gml:identifier/text()

