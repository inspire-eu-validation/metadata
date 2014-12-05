
# Topic Category

# Test case identifier	

md_IR231

# Test purpose	

If the type of the resource is dataset or series, at least one Topic category describing the category of the resource must be given.

# Test method	

The test first checks if at least one element of type gmd:topicCategory is given. If so, the following conditions are checked for all topic categories:
•	The topic category is of type gmd:MD_TopicCategoryCode
•	The element gmd:MD_TopicCategoryCode contains text that equals one of the categories given in B.5.27 of ISO 19115.
The value saved in the XML metadata element shall be a language neutral name.
If the type of the resource was not dataset or series, this test is omitted.

# Context

gmd:identificationInfo[1]/*

# Reference	 

INSPIRE Metadata Implementing Rules, Chap. 2.3.1
TG Req 10 & 11
ISO 19115, B.5.27

# Test type	

Automated



