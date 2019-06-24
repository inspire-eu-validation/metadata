# Dataset temporal

**Purpose**: INSPIRE provides 4 types of temporal reference, which are all conditional elements on their own. However, at least one of them must be provided. To be compliant with ISO 19115 it is necessary to use at least one among date of publication, date of last revision, or the date of creation.

**Prerequisites**

**Test method**

The four types of which one must be provided are Temporal extent, Date of publication, Date of last revision and Date of creation. This test performs the following checks:
* Check if a [TimePeriod](#period) element exists and if it contains gml:beginPosition and gml:endPosition or gml:begin/gml:timeInstant/gml:timePosition x 2 or gml:begin/gml:timeInstant/gml:timePosition and gml:endPosition or gml:beginPosition and gml:begin/gml:timeInstant/gml:timePosition
* Check if a temporal reference with [dateType](#dateType)='publication' exists
* Check if a temporal reference with [dateType](#dateType)='revision' exists
* Check if a temporal reference with [dateType](#dateType)='creation' exists

The test case will fail if the results to steps 2, 3 and 4 all equal false.

**Reference(s)**

* [ISO 19108](./README.md#ref_ISO_19108)
* [ISO 8601](./README.md#ref_ISO_8601)
* [TG MD](./README.md#ref_TG_MD) Chap. 2.6, Req 22 & 23

**Test type**: Automated

**Notes**

The test method does not explicitly state, if the test applies only to datasets, dataset series, or also services. TG MD is not clear on this point, either. For example, section 2.6 mostly talks about "resource" in general. In 2.6.1, however, the definition of "Temporal Extent" is: "Time period covered by the content of the dataset".  Nevertheless, in the detailed mapping sections 3.3.1 (spatial dataset and spatial dataset series) and 3.3.2 (service resources) the Temporal Extent is listed as an optional element of the identification section (in both cases, a reference to 2.6.1 is made).

In the ETS, the test has therefore been implemented as a common test and checks that a temporal reference with gml:TimePeriod uses gml:begin and gml:end elements with gml:TimeInstant given inline. The possible combinations of gml:begin, gml:beginPosition, gml:end, and gml:endPosition are already covered by the XML Schema validation.

The 'extent' property is not part of the gmd:AbstractMD_Identification_Type and therefore defined in two different namespaces: 'gmd' and 'srv' (the XPath below only uses 'gmd').

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="period"></a> TimePeriod   | gmd:identificationInfo[1]/\*/gmd:extent/\*/gmd:temporalElement/\*/gmd:extent/gml:TimePeriod
<a name="date"></a> date   | gmd:identificationInfo[1]/\*/gmd:citation/\*/gmd:date
<a name="dateType"></a> dateType   | gmd:identificationInfo[1]/\*/gmd:citation/\*/gmd:date/\*/gmd:dateType
