# Quality of Service 

**Purpose**: Test that Quality of Service is provided correctly.

**Prerequisites**

**Test method**

* Check that at least three [Conceptual Consistency](#conceptualConsistency) elements exists.

* For every [Conceptual Consistency](#conceptualConsistency),

    * Check that [Measurement Name](#measurementName) element exists and it has an attribute xlink:href with URL value starting with "http://inspire.ec.europa.eu/metadata-codelist/QualityOfServiceCriteriaCode/" and postfixed with one of values of code list QualityOfServiceCriteriaCode, see [Annex D.4 TG](./README.md#ref_TG_MD).

    * Check that [Measurement Description](#measurementDescription) element exists.

    * Check that [Measurement Result](#measurementResult) element exists.

    * Check that [Measurement Unit](#measurementUnit) element exists.

    * Check that [Record](#record) element exists and it has an atttribute "xsi:type".

* If any of the checks fails, the test fails.

**Reference(s)**

* [TG MD](./README.md#ref_TG_MD) 4.4.3.1, Req 6.5
* [Quality Of Service Criteria Code](http://inspire.ec.europa.eu/metadatacodelist/QualityOfServiceCriteriaCode)

**Test type**: Automated

**Notes**

The multiplicity of this element is three or more.

These values should reflect the true Quality of Service of the particular service evaluated in realistic test scenarios rather than the expected goals to reach for these criteria. 

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /gmd:MD_Metadata/gmd:dataQualityInfo/gmd:DQ_DataQuality/gmd:report)
---------------------------------------------------------- | -------------------------------------------------------------------------
<a name="conceptualConsistency"></a> Conceptual Consistency | gmd:DQ_ConceptualConsistency
<a name="measurementName"></a> Measurement Name | gmd:DQ_ConceptualConsistency/gmd:nameOfMeasure/gmd:Anchor
<a name="measurementDescription"></a> Measurement Description | gmd:DQ_ConceptualConsistency/gmd:measureDescription
<a name="measurementResult"></a> Measurement Result | gmd:DQ_ConceptualConsistency/gmd:result/gmd:DQ_QuantitativeResult
<a name="measurementUnit"></a> Measurement Unit | gmd:DQ_ConceptualConsistency/gmd:result/gmd:DQ_QuantitativeResult/gmd:valueUnit
<a name="record"></a> Record | gmd:DQ_ConceptualConsistency/gmd:result/gmd:DQ_QuantitativeResult/gmd:value/gco:Record
