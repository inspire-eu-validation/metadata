
# Responsible party

# Test case identifier	

md_2101

# Test purpose	

Name and contact to a responsible party must be given for every responsible organization in the metadata.

# Test method	

The test first checks if there is at least one element at gmd:identificationInfo[1]/*/gmd:pointOfContact. Furthermore, the following checks are performed for every element at gmd:identificationInfo[1]/*/gmd:pointOfContact:
*	There must be an element gmd:CI_ResponsibleParty.
*	There must be an organization name at gmd:CI_ResponsibleParty/gmd:organisationName.
*	There must be a mail address of type gco:CharacterString at gmd:CI_ResponsibleParty/gmd:contactInfo/*/gmd:address/*/gmd:electronicMailAddress
*	The type of the organization name must be either gco:CharacterString or gmd:PT_FreeText. In the latter case, a schema validation is performed depending on the GML version (see About schema validation).

# Reference	 

INSPIRE Metadata Implementing Rules, Chap. 2.10.1 

# Test type	

Automated
	
