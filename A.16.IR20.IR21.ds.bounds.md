#A.16.IR20.IR21.ds.bounds

**Purpose**: A geographic bounding box must be given and it should be as small as possible

**Prerequisites**
* [A.01.validate](A.01.validate.md) must be passed

**Test method**

Check if it's a valid geographic [extend](#extent). It is described by 4 elements: westBoundLongitude, eastBoundLongitude, southBoundLatitude and northBoundLatitude. The test performs the following checks on them:
*	Is a correctly formatted westBoundLongitude given at gmd:westBoundLongitude/gco:Decimal.
*	Is the following constraint given: -180.00 = westBoundLongitude = 180.00
*	Is a correctly formatted eastBoundLongitude given at gmd:eastBoundLongitude/gco:Decimal.
*	Is the following constraint given: -180.00 = eastBoundLongitude = 180.00
*	Is a correctly formatted southBoundLongitude given at gmd:southBoundLongitude/gco:Decimal.
*	Is the following constraint given: -90.00 = southBoundLatitude = northBoundLatitude
*	Is a correctly formatted northBoundLongitude given at gmd:northBoundLongitude/gco:Decimal.
*	Is the following constraint given: southBoundLatitude = northBoundLatitude = 90.00;

The bounding box shall be as small as possible. Quite hard to honour. Data should be downloaded and a minimal bounds could be calculated and compared to the indicated bounds.

The bounding box shall be expressed in decimal degree with a precision of at least 2 decimals.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD) 2.5.1, Req 20 & 21

**Test type:** Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="extent"></a> extent  | gmd:identificationInfo[1]/*/gmd:extent/*/gmd:geographicElement/*/
