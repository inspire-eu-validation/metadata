
# Conformity

# Test case identifier	

md_IR281

# Test purpose	

For every conformity statement, one conformance result indicated by a boolean value must be given.

# Test method	

The test first checks if there is at least one conformance result of type gco:Boolean at gmd:dataQualityInfo/*/gmd:report/*/gmd:result. It then performs the following actions for every element at gmd:dataQualityInfo/*/gmd:report/*/gmd:result:
•	If the element has an element /*/gmd:pass, it must contain a value of type gco:Boolean.


# Reference	 

INSPIRE Metadata Implementing Rules, Chap. 2.8.1
TG Req 28
 
# Test type	

Automated

