# Temporal Extent


**Purpose**: 

**Prerequisites**

**Test method**
*  If a temporary reference is provided, its coding is checked through the element encoded using the element gmd:EX_Extent with one or more elements gmd:EX_TemporalExtent.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_TG_MD), 2.3.5 , Req c.15
* [ISO 8601](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#ref_ISO_8601)


**Test type**: Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="individual"></a> Individual Date   | ./gmd:identificationInfo[1]/\*/gmd:extent/\*/gmd:temporalElement/\*/gmd:extent/gml:TimeInstant/gml:timePosition 
