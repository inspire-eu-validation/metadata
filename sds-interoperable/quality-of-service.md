# Minimum estimated Quality of Service 

**Purpose**: The purpose is to describe the minimum provided service level for a Spatial Data Service.

**Prerequisites**

**Test method**

*The minimum values for each of the quality of service criteria are evaluated using a [Conceptual Consistency](#conceptualConsistency) element within the gmd element: DQ_DataQuality, with scope for the entire service.
*These elements of a measurement will also be tested:

* - The [name](#nameMeasurement) of the measurement.
* - A description of the encoded measurement under the gmd: measureDescription element.
* - The measurement [result](#resultMeasurement) value.
* - The [unit](#) of measurement.

**Reference(s)**

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-interoperable/README#ref_TG_MD) 4.4.3.1, Req 6.5
* [Quality Of Service Criteria Code](http://inspire.ec.europa.eu/metadatacodelist/QualityOfServiceCriteriaCode)
**Test type**: Automated

**Notes**

* These values should reflect the true Quality of Service of the particular service evaluated in realistic test scenarios rather than the expected goals to reach for these criteria. 

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
<a name="conceptualConsistency"></a> Conceptual Consistency | ./gmd:dataQualityInfo/\*/gmd:report/gmd:DQ_ConceptualConsistency
<a name="nameMeasurement"></a> Name Measurement | ./gmd:dataQualityInfo/\*/gmd:report/gmd:DQ_ConceptualConsistency/gmd:nameOfMeasure/gmd:Anchor/@xlink:href='http://inspire.ec.europa.eu/metadatacodelist/QualityOfServiceCriteriaCode'
<a name="descriptionMeasurement"></a> Description Measurement | ./gmd:dataQualityInfo/\*/gmd:report/gmd:DQ_ConceptualConsistency/gmd:measureDescription
<a name="resultMeasurement"></a> Result Measurement | ./gmd:dataQualityInfo/\*/gmd:report/gmd:DQ_ConceptualConsistency/gmd:result/gmd:DQ_QuantitativeResult
<a name="unitMeasurement"></a> Unit Measurement | ./gmd:dataQualityInfo/\*/gmd:report/gmd:DQ_ConceptualConsistency/gmd:valueUnit
