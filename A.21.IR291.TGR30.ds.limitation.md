
# Limitations on public access

# Test case identifier	

md_IR291

# Test purpose	

Limitations on public access must be described at least once for the resource.

# Test method	

Three types of resources may occur: gmd:accessConstraints (1), gmd:otherConstraints (2), gmd:classification (3) and gdm:useLimitation (4). The following action are performed for each one of the possible types:
•	(1) The element must have an element at gmd:MD_RestrictionCode[@codeListValue=x], where x is of type MD_RestrictionCode as defined in ISO 19115, chapter B.5.24.
•	(2) The element is free text, it must be of type gco:CharacterString or gmd:PT_Freetext.
•	(3) The element must have an element at gmd:MD_ClassificationCode[@codeListValue=x], where x is of type MD_ClassificationCode as defined in ISO 19115, chapter B.5.24.
•	(4) The element is free text, not further tests are performed.
If none of the four elements is found, the test fails.

# Reference	 

INSPIRE Metadata Implementing Rules, Chap. 2.9.1
ISO 19115, B.5.24
TG Req 30, 31 & 32

# Test type	

Automated

