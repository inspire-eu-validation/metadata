
# Spatial data service type

# Test case identifier	

md_IR232

# Test purpose	

If the type of the resource was service, exactly one name describing the type of service must be given.

# Test method	

If the type of the resource was service, exactly one name describing the type of service must be given. 
The test first checks if a service type element is given at gmd:identificationInfo[1]/*/srv:serviceType and if it is 
unique throughout the document. The test then checks if the element srv:serviceType contains text that equals one of 
the types given in INSPIRE Metadata Implementing Rules, Chap. 1.3.1. (in INSPIRE registry at http://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType)

If the type of the resource was not service, this test is omitted.

# Reference	 

INSPIRE Metadata Implementing Rules, Chap. 2.3.2
INSPIRE Metadata Implementing Rules, Chap. 1.3.1
TG Req 12
# Test type	

Automated

