
# Resource abstract

# Test case identifier	

md_IR222

# Test purpose	

Validates if a resource abstract is provided 

# Test method	

Checks if an abstract is provided (not empty string)  for each of the advertised languages and is provided as either gco:CharacterString, gmx:Anchor or gmd:PT_FreeText. 
In case of gmx:Anchor, the anchor should resolve to a document (not status 404/500)
In case of PT_FreeText, a schema validation is performed depending on the GML version 

# Context

gmd:identificationInfo[1]/*

# Reference	 

INSPIRE Metadata Implementing Rules, Chap. 2.2.2

# Test type	

Automated
	
