
# Resource Language

# Test case identifier	

md_IR227

# Test purpose	

If the type of the resource was dataset or series and the resource contains textual information, a resource language must be given.

# Test method	

The test first checks if a gmd:LanguageCode object is given at gmd:identificationInfo[1]/*/gmd:language/gmd:LanguageCode and contains a codeList and codeListValue attribute. It is then checked if the codeListValue attribute contains a valid 3-letter language code according to ISO/TS 19139.
If the type of the resource is not dataset or series, this test is omitted.

# Reference	 

INSPIRE Metadata Implementing Rules, Chap. 2.2.7
ISO 639-2

# Test type	

Automated

