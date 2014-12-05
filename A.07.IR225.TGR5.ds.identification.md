

# Unique resource identifier

# Test case identifier	

md_IR225

# Test purpose	

If the type of the resource was dataset or series, a unique identifier identifying the resource must be given.

# Test method	

The test first checks if a unique identifier is given as gmd:identifier and if it is of type MD_Identifier or RS_Identifier. 
The contained code element may not be empty.
If the type of the resource is not dataset or series, this test is omitted.

# Context

gmd:identificationInfo[1]/*/gmd:citation/*

# Reference	 

INSPIRE Metadata Implementing Rules, Chap. 2.2.5
TG Req 5 & 6
ISO 19115, B.2.7.3

# Test type	

Automated


