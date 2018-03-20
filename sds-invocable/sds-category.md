# Inovable Spatial Data Service category Keywords

**Purpose**: 
**Prerequisites**

* [resource-type](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds/resource-type)

**Test method**

* Check that there is at least one DQ_ConformanceResult returned from query [classification result invocable](#result_invocable).
* The multiplicity of the element  is one.

* This element shall contain a gmd:CI_Citation element for one of the three Conformance Classes for Invocable Spatial Data Service categories.
* The title of the cited Conformance Class shall be encoded using the gmd:title/gmx:Anchor element. 
**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-invocable/README#ref_TG_MD), 4.3.3.2, Req 5.4
* [ISO 19115](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-invocable/README#ref_ISO_19115)

**Test type**: Automated

**Notes**

The test method is not clear on how a specific code list is referenced in a gmd:thesaurusName.


##Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-invocable/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
<a name="result_invocable">classification result invocable</a> | gmd:dataQualityInfo/\*/gmd:report/\*/gmd:result/gmd:DQ_ConformanceResult[1]
 <a name="citation">Citation</a> | gmd:dataQualityInfo/\*/gmd:report/\*/gmd:result/gmd:DQ_ConformanceResult[1]/\*/gmd:CI_Citation
 <a name="title">Title</a> | gmd:dataQualityInfo/\*/gmd:report/\*/gmd:result/gmd:DQ_ConformanceResult[1]/\*/gmd:CI_Citation/gmd:title/gmd:Anchor