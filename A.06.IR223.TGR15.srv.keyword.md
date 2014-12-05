
# Keywords for Resource type Service

# Test case identifier	

md_IR223_service

# Test purpose	

If the resource is a service, the type of service should be specified

# Test method	

If the resource is a service, at least one keyword must originate from EU commission regulation No. 1205/2008, Annex part D, No. 4.
The codelist is duplicated in the INSPIRE registry http://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceCategory
Checks for every gmd:keyword found at gmd:identificationInfo[1]/*/gmd:descriptiveKeywords/*/ if it is formatted as either gco:CharacterString or gmd:PT_FreeText. 
In the latter case, a schema validation is performed depending on the GML version (see About schema validation). It the checks for every keyword if its text content 
can be found among the keywords given in EU commission regulation No. 1205/2008, Annex part D, No. 4. If at least one keyword from that source is found, the test succeeds, otherwise it will fail.
If the type of the resource is not service, this test is omitted. 

# Reference	 

INSPIRE Metadata Implementing Rules, Chap. 2.2.3
Article 4, part D of the EU commission regulation No 1205/2008
TG Req 15

# Test type	

Automated
