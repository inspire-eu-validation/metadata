# Temporal Extent


**Purpose**: If a temporary reference is provided using the temporary extension, it will be coded using an individual date or a period of time between two dates.

**Prerequisites**

**Test method**

If a temporary reference is provided, its coding is checked through the element encoded using the element gmd:EX_Extent with one or more elements gmd:EX_TemporalExtent.

The value of each of these elements can be an individual date or a period of time between two dates.

For [individual](#individual) dates, the gml:timePosition element is evaluated with the date value given in accordance with [ISO 8601]

For a period of time it must contain a TimePeriod child element that contains the start and end dates of the period:
* Check that [beginPosition](#beginPosition) does not have attribute @frame (which means that the default reference system is used) and whether the date is valid.
* Check that [endPosition](#endPosition) does not have attribute @frame (which means that the default reference system is used) and whether the date is valid.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_TG_MD), 2.3.4 , Req c.14
* [ISO 8601](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_ISO_8601)


**Test type**: Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="individual"></a> Individual Date   | ./gmd:identificationInfo[1]/\*/gmd:extent/\*/gmd:temporalElement/\*/gmd:extent/gml:TimeInstant/gml:timePosition 
<a name="period"></a> TimePeriod   | ./gmd:identificationInfo[1]/\*/gmd:extent/\*/gmd:temporalElement/\*/gmd:extent/gml:extent
<a name="beginPosition"></a> beginPosition   | ./gmd:extent/gmd:EX_Extent/gmd:temporalElement/gmd:EX_TemporalExtent/gmd:extent/gml:TimePeriod/gml:beginPosition
<a name="endPosition"></a> endPosition   | ./gmd:extent/gmd:EX_Extent/gmd:temporalElement/gmd:EX_TemporalExtent/gmd:extent/gml:TimePeriod/gml:endPosition