#A.17.IR22.IR23.ds.temporal

**Purpose**: INSPIRE provides 4 types of temporal reference, which are all conditional elements on their own. However, at least one of them must be provided.

**Prerequisites**
* [A.01.validate](A.01.validate.md) must be passed

**Test method**

The four types of which one must be provided are Temporal extent, Date of publication, Date of last revision and Date of creation. This test performs the following checks:
*	Is a valid [TimePeriod](#period) and does it contain gml:beginPosition and gml:endPosition or gml:begin/gml:timeInstant/gml:timePosition x 2 or gml:begin/gml:timeInstant/gml:timePosition and gml:endPosition or gml:beginPosition and gml:begin/gml:timeInstant/gml:timePosition
*	Is a valid [date](#date) of publication given at [dateType](#dateType)='publication'
*	Is a valid [date](#date) of last revision given at [dateType](#dateType)='revision'
*	Is a valid [date](#date) of creation given at [dateType](#dateType)='creation'

The test will fail if and only if at least one check among date of publication, date of last revision or date of creation doesn’t evaluate to true.

**Reference(s)**

* [ISO 19108](README.md#ref_ISO_19108)
* [ISO 8601](README.md#ref_ISO_8601)
* [TG MD](./README.md#ref_TG_MD) Chap. 2.6.1 - 2.6.4, Req 22 & 23
* [IR MD](README.md#ref_IR_MD) Part B. 5.1

**Test type:** Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="period"></a> TimePeriod   | gmd:identificationInfo[1]/*/gmd:extent/*/gmd:temporalElement/*/gmd:extent/gml:TimePeriod
<a name="date"></a> date   | gmd:identificationInfo[1]/*/gmd:citation/*/gmd:date
<a name="dateType"></a> dateType   | gmd:identificationInfo[1]/*/gmd:citation/*/gmd:date/*/gmd:dateType
