# Bounding Box

**Purpose**: Specify the extent of the resource in the geographic space, given as a geometric bounding box..

**Prerequisites**

**Test method**
Check if it's a valid geographic [extend](#extent). It is described by 4 elements: westBoundLongitude, eastBoundLongitude, southBoundLatitude and northBoundLatitude. The test performs the following checks on them:
*	Is a correctly formatted westBoundLongitude given at gmd:westBoundLongitude/gco:Decimal.
*	Is the following constraint given: -180.00 ≤ westBoundLongitude ≤ 180.00
*	Is a correctly formatted eastBoundLongitude given at gmd:eastBoundLongitude/gco:Decimal.
*	Is the following constraint given: -180.00 ≤ eastBoundLongitude ≤ 180.00
*	Is a correctly formatted southBoundLongitude given at gmd:southBoundLongitude/gco:Decimal.
*	Is the following constraint given: -90.00 ≤ southBoundLatitude ≤ northBoundLatitude
*	Is a correctly formatted northBoundLongitude given at gmd:northBoundLongitude/gco:Decimal.
*	Is the following constraint given: southBoundLatitude ≤ northBoundLatitude ≤ 90.00;

The bounding box shall be expressed in decimal degree with a precision of at least 2 decimals.

The bounding box shall be as small as possible. This requires a manual check.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_TG_MD), 2.3.8 , Req c.19


**Test type**: Automated

**Notes**

*The multiplicity of this element is one or more for data sets and data set series, and zero or more for services. 

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="extent"></a> extent  | gmd:identificationInfo[1]/\*/gmd:extent/\*/gmd:geographicElement/gmd:EX_GeographicBoundingBox





