
# Spatial data service type

**Purpose**	

If the type of the resource was service, exactly one name describing the type of service must be given.

**Test method**	

If the type of the resource is service, exactly one name describing the type of service must be given. 
The test first checks if a service type element is given at [serviceType](#serviceType) and if it is 
unique throughout the document. The test then checks if the element [serviceType](#serviceType) contains text that equals one of 
the types given in http://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType (IR, Chap. 1.3.1.)

If the type of the resource was not service, this test is omitted.

**Reference(s)**	
 
* [IR](./README.md#IR), Annex B. 2.2
* [TG](./README.md#TG), Req 12
* http://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType

**Test type:** Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
serviceType <a name="serviceType"></a>   | ./gmd:identificationInfo[1]/*/srv:serviceType


