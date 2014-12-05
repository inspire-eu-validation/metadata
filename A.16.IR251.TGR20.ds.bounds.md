
# Geographic bounding box

# Test case identifier	

md_IR251

# Test purpose	

If the type of the resource was dataset or series or if the type was service, a geographic bounding box must be given.

# Test method	

Check if it's a valid geographic extend. It is described by 4 elements: westBoundLongitude, eastBoundLongitude, southBoundLatitude and northBoundLatitude. The test performs the following checks on them:
*	Is a correctly formatted westBoundLongitude given at gmd:identificationInfo[1]/*/gmd:extent/*/gmd:geographicElement/*/gm d:westBoundLongitude/gco:Decimal.
*	Is the following constraint given: -180.00 = westBoundLongitude = 180.00
*	Is a correctly formatted eastBoundLongitude given at gmd:identificationInfo[1]/*/gmd:extent/*/gmd:geographicElement/*/gm d:eastBoundLongitude/gco:Decimal.
*	Is the following constraint given: -180.00 = eastBoundLongitude = 180.00
*	Is a correctly formatted southBoundLongitude given at gmd:identificationInfo[1]/*/gmd:extent/*/gmd:geographicElement/*/gm d:southBoundLongitude/gco:Decimal.
*	Is the following constraint given: -90.00 = southBoundLatitude = northBoundLatitude
*	Is a correctly formatted northBoundLongitude given at gmd:identificationInfo[1]/*/gmd:extent/*/gmd:geographicElement/*/gm d:northBoundLongitude/gco:Decimal.
*	Is the following constraint given: southBoundLatitude = northBoundLatitude = 90.00;

The bounding box shall be as small as possible. Quite hard to honour. Data should be downloaded and a minimal bounds could be calculated and compared to the indicated bounds.

The bounding box shall be expressed in decimal degree with a precision of at least 2 decimals.


# Reference	 

INSPIRE Metadata Implementing Rules, Chap. 2.5.1 
TG Req 20 & 21 

# Test type	

Automated


