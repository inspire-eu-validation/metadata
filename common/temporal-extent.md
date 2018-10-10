# Temporal Extent

**Purpose**: Test if a temporal reference is provided using the temporary extension. The temporal reference will be coded using an individual date or a period of time between two dates.

**Prerequisites**

**Test method**

* If [Temporal Extent](#temporalExtent) exists using gmd:extent/gmd:EX_Extent, then for each [Temporal extent](#temporalExtent),

    * If [Time Position](#individual) exists, check that the value is accordance to [ISO 8601](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_ISO_8601)

    * Else If [Time Period](#period) exists, check that [beginPosition](#beginPosition) exists and [endPosition](#endPosition) exists and the values are accordance to [ISO 8601](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_ISO_8601)

    * Else the test fails

* If any of the checks fails, the test fails.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.3.4 , Req c.14
* [ISO 8601](./README.md#ref_ISO_8601)


**Test type**: Automated

**Notes**

The multiplicity of [Temporal extent](#temporalExtent) is zero or more.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:identificationInfo/gmd:MD_DataIdentification/gmd:extent/gmd:EX_Extent)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="temporalExtent"></a> Temporal Extent | gmd:temporalElement/gmd:EX_TemporalExtent/gmd:extent
<a name="individual"></a> Time Position | gmd:temporalElement/gmd:EX_TemporalExtent/gmd:extent/gml:TimeInstant/gml:timePosition 
<a name="period"></a> Time Period | gmd:temporalElement/gmd:EX_TemporalExtent/gmd:extent/gml:TimePeriod
<a name="beginPosition"></a> beginPosition | gmd:temporalElement/gmd:EX_TemporalExtent/gmd:extent/gml:TimePeriod/gml:beginPosition
<a name="endPosition"></a> endPosition | gmd:temporalElement/gmd:EX_TemporalExtent/gmd:extent/gml:TimePeriod/gml:endPosition