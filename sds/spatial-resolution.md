# Spatial resolution services.

**Purpose**:
Check the level of detail of the data set, both gridded type data and imagery-derived products,
how to maps or map products.
For services, it is not possible to express the restriction of a service concerning the spatial 
resolution in using the ISO 19139 XML Schema.

**Prerequisites**

**Test method**
The spatial resolution restriction text shall include either an equivalent scale as integer valued scale denominator
 or a resolution distance using a numerical length value and with a unit of length.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds/README#ref_TG_MD) 4.1.2.1, Req 3.3

**Test type**: Automated

**Notes**
The spatial resolution restriction text shall include either an equivalent scale as integer valued scale
 denominator or a resolution distance using a numerical length value and with a unit of length.
 
##Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="spatialResolution"></a> spatialResolution | ./gmd:identificationInfo[1]/\*/gmd:abstract

