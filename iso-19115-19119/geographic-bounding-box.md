# Geographic bounding box

**Purpose**: A geographic bounding box must be given and it should be as small as possible

**Prerequisites**

* [Hierarchy](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/hierarchy)

**Test method**

This test case only applies to records with a [hierarchyLevel](#hierarchyLevel) value 'dataset' or 'series'.

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

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#ref_TG_MD) 2.5.1, Req 20, 21

**Test type**: Automated/Manual

**Notes**

The depencency to [Hierarchy](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/hierarchy) has not been implemented in the ETS as it still seems reasonable to test the available dataset (series) metadata records.  

##Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="extent"></a> extent  | gmd:identificationInfo[1]/\*/gmd:extent/\*/gmd:geographicElement/gmd:EX_GeographicBoundingBox
<a name="hierarchyLevel"></a> hierarchyLevel | gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
