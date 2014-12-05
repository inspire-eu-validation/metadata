
# Metadata point of contact

# Test case identifier	

md_2111

# Test purpose	

At least one point of contact must be given.

# Test method	

The test first checks if an element is given at gmd:contact. It then performs the following checks for every element at gmd:contact:
•	An element must be given at gmd:CI_ResponsibleParty/gmd:organisationName.
•	An element must be given at gmd:CI_ResponsibleParty/gmd:contactInfo/*/gmd:address/*/gmd:elec tronicMailAddress.
•	Organization name and electronic mail address must be either gco:CharacterString or gmd:PT_FreeText. In the latter case, a schema validation is performed depending on the GML version (see About schema validation).


# Reference	 

INSPIRE Metadata Implementing Rules, Chap. 2.11.1

# Test type	

Automated


