# Topological consistency descriptive results
**Purpose**: Evaluate the type of spatial representation of the data.

**Prerequisites**

**Test method**
Checks so type of spatial representation is given using an element [spatialRepresentationTypeCode](#spatialRepresentationTypeCode).
One of the code list values "vector", "grid", "tin" or "textTable".

**Reference(s)**	 
* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/isdss/spatial-representation-type/README#ref_TG_MD) 3.2.2.1, Req 2.4

**Test type**: Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/isdss/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| ------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="spatialRepresentationTypeCode"></a> spatialRepresentationTypeCode  | gmd:referenceSystemInfo/\*/gmd:spatialRepresentationType/gmd:MD_SpatialRepresentationTypeCode/@codeListValue
<a name="codeListValue"></a> codeListValue  | doc("http://standards.iso.org/iso/19139/resources/gmxCodelists.xml")//gmx:CodeListDictionary[@gml:id='MD_SpatialRepresentationTypeCode ']//gml:identifier/text()
