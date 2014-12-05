
# Lineage

# Test case identifier	

md_IR271

# Test purpose	

If the type of the resource was dataset or series, exactly one explanation about the lineage of a dataset must be given

# Test method	

The test first checks if a valid lineage statement is given at gmd:dataQualityInfo/*/gmd:lineage/*/gmd:statement 
and if the statement type is either gco:CharacterString or gmd:PT_FreeText. In the latter case, a schema validation 
is performed depending on the GML version (seeAbout schema validation). It then validates that exactly one lineage statement like the one above is given.

# Reference	 

INSPIRE Metadata Implementing Rules, Chap. 2.7.1

# Test type	

Automated


