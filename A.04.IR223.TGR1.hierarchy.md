
# Resource type

# Test case identifier	

md_IR223

# Test purpose	

Type of the cited resource must be provided

# Test method	

Checks if a resource type is provided and is formatted as MD_ScopeCode object.
To be relevant for INSPIRE the value should be either 'dataset', 'service' or 'series'
  
  <sch:assert test="gmd:hierarchyLevel/*/@codeListValue='dataset'
    or gmd:hierarchyLevel/*/@codeListValue='series'
    or gmd:hierarchyLevel/*/@codeListValue='service'">

# Context 

//gmd:metadata/gmd:identificationInfo[1]/* <!-- todo: check context -->

# Reference	 

IR Chap. 2.2.3
TG Requirement 1 <!-- todo: check pagenr -->
TG Requirement 2

# Test type	

Automated
