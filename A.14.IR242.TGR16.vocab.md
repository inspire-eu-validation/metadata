
# Originating controlled vocabulary

# Test case identifier	

md_IR242

# Test purpose	

A keyword value (see md_241) can give a controlled vocalbulary from where it originates from. This element is optional but, if given, must follow certain guidelines.

# Test method	

The test performs the following check for each element at gmd:identificationInfo[1]/*/gmd:descriptiveKeywords/*/gmd:thesaurusName:
•	the node must contain a title at ./gmd:CI_Citation/gmd:title
•	the node must contain a date at /gmd:CI_Citation/gmd:date/*/gmd:date/gco:Date
•	the node must contain a dateType element at /gmd:CI_Citation/gmd:date/*/gmd:dateType which contains text that equals one of publication, revision or creation.
•	the type of the title must be either gco:CharacterString or gmd:PT_FreeText. In the latter case, a schema validation is performed depending on the GML version (see About schema validation).

Validating if the keyword is actually available in the indicated vocabulary is a challenge, since the vocabulary is usually not referenced by a URL. 
If a vocabulary is indicated that is available to the validator, then this check can be performed.

# Reference	 

INSPIRE Metadata Implementing Rules, Chap. 2.4.2 
TG Req 16, 17 & 18

# Test type	

Automated


