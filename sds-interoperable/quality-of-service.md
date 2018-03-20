# Minimum estimated Quality of Service 

**Purpose**: It is verified that each of the quality criteria of the services comply with minimum values.

**Prerequisites**

**Test method**

Check that the [availability statement](#availability_statement) for availability is given. If so, pass the test. Otherwise fail the test.

**Reference(s)**

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-interoperable/README#ref_TG_MD) 4.4.3.1, Req 6.5

**Test type**: Automated

**Notes**

* Identifying the INSPIRE QoS indicator just be a specific ```gco:CharacterString``` value ```Availability``` is not sufficient, as there may be other conceptual consistency reports with measures with the same name. There should be reference to the definition of this indicator in the INSPIRE context.
* The units of the measure must be identified in order to avoid misinterpretations, like whether the availability number should be interpreted as a percentage (0-100) or fraction (0 - 1).
* The type of the ```gco:Record``` is not defined in GML. There should be clear guidance on the content for this element in [TG SDS](README.md#ref_TG_SDS) in order to harmonize it's use.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
availability statement <a name="availability_statement"></a> | /gmd:MD_Metadata/gmd:dataQualityInfo/gmd:DQ_DataQuality/gmd:report/gmd:DQ_ConceptualConsistency[child::gmd:nameOfMeasure/gco:CharacterString='Availability' and child::gmd:result/gmd:DQ_QualitativeResult/gmd:value/gco:Record]
