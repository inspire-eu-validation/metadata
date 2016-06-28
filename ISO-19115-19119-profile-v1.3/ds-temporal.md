#Ds temporal

**Purpose**: INSPIRE provides 4 types of temporal reference, which are all conditional elements on their own. However, at least one of them must be provided. To be compliant with ISO 19115 it is necessary to use at least one among date of publication, date of last revision, or the date of creation.

**Prerequisites**
* [Schema validation](schema-validation.md) must be passed

**Test method**

The four types of which one must be provided are Temporal extent, Date of publication, Date of last revision and Date of creation. This test performs the following checks:
* Check if a [TimePeriod](#period) element exists and if it contains gml:beginPosition and gml:endPosition or gml:begin/gml:timeInstant/gml:timePosition x 2 or gml:begin/gml:timeInstant/gml:timePosition and gml:endPosition or gml:beginPosition and gml:begin/gml:timeInstant/gml:timePosition
* Check if a temporal reference with [dateType](#dateType)='publication' exists
* Check if a temporal reference with [dateType](#dateType)='revision' exists
* Check if a temporal reference with [dateType](#dateType)='creation' exists

The test case will fail if the results to steps 2, 3 and 4 all equal false.

**Reference(s)**

* [ISO 19108](README.md#ref_ISO_19108)
* [ISO 8601](README.md#ref_ISO_8601)
* [TG MD](./README.md#ref_TG_MD) Chap. 2.6.1 - 2.6.4, Req 22 & 23

**Test type:** Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="period"></a> TimePeriod   | gmd:identificationInfo[1]/*/gmd:extent/*/gmd:temporalElement/*/gmd:extent/gml:TimePeriod
<a name="date"></a> date   | gmd:identificationInfo[1]/*/gmd:citation/*/gmd:date
<a name="dateType"></a> dateType   | gmd:identificationInfo[1]/*/gmd:citation/*/gmd:date/*/gmd:dateType
