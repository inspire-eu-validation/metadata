# Ds temporal date

**Purpose**: 

Test whether dates are expressed in accordance with ISO 8601 (yyyy-mm-dd).

**Prerequisites**
* [Schema validation](schema-validation.md) must be passed
* [Ds temporal](ds-temporal.md) must be passed

**Test method**

* If a [TimePeriod](#period) element exists, check whether all child elements contain a valid date.
* If a [date](#date) of publication is given at [dateType](#dateType)='publication', check whether the date is valid
* If a [date](#date) of publication is given at [dateType](#dateType)='revision', check whether the date is valid
* If a [date](#date) of publication is given at [dateType](#dateType)='creation', check whether the date is valid
*  Check that [beginPosition](#beginPosition) does not have attribute @frame (which means that the default reference system is used) and whether the date is valid 
*  Check that [endPosition](#endPosition) does not have attribute @frame (which means that the default reference system is used) and whether the date is valid

The test case fails if any of the above steps returns false.

**Reference(s)**

* [ISO 19115](README.md#ref_ISO_19115)
* [ISO 19108](README.md#ref_ISO_19108)
* [ISO 8601](README.md#ref_ISO_8601)
* [TG MD](./README.md#ref_TG_MD) Chap. 2.6.1 - 2.6.4, Req 24


**Test type:** Automated

**Notes**

The following regular expression can be used to check the validity of the date ^[0-9]{4}-[0-9]{2}-[0-9]{2}(T.*)?

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="period"></a> TimePeriod   | gmd:identificationInfo[1]/*/gmd:extent/*/gmd:temporalElement/*/gmd:extent/gml:TimePeriod
<a name="date"></a> date   | gmd:identificationInfo[1]/*/gmd:citation/*/gmd:date
<a name="dateType"></a> dateType   | gmd:identificationInfo[1]/*/gmd:citation/*/gmd:date/*/gmd:dateType
<a name="beginPosition"></a> beginPosition   | gmd:extent/gmd:EX_Extent/gmd:temporalElement/gmd:EX_TemporalExtent/gmd:extent/gml:TimePeriod/gml:beginPosition
<a name="endPosition"></a> endPosition   | gmd:extent/gmd:EX_Extent/gmd:temporalElement/gmd:EX_TemporalExtent/gmd:extent/gml:TimePeriod/gml:endPosition
