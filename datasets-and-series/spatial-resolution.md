# Spatial resolution

**Purpose**:
Check the level of detail of the data set, both gridded type data and imagery-derived products,
how to maps or map products.

**Prerequisites**

* [Resource Type](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/resource-type)

**Test method**
This test case only applies to records with a [hierarchyLevel](#hierarchyLevel) value 'dataset' or 'series'.

* Each [spatialResolution](#spatialResolution) element must contain either:
* [equivalentScale](#equivalentScale).
* Or [distance](#distance) but not both.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/README#ref_TG_MD) 3.1.2.3, Req 1.5

**Test type**: Automated

**Notes**

This test is already covered by the XML Schema validation (the content of an MD_Resolution element is a choice between an 'equivalentScale' or 'distance').

The Xpath references for equivalentScale and distance shown below are misleading. They should show the full path starting from MD_Metadata.

##Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="hierarchyLevel"></a> Hierarchy Level | ./gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="spatialResolution"></a> spatialResolution | ./gmd:identificationInfo[1]/\*/gmd:spatialResolution
<a name="equivalentScale"></a> equivalentScale  | ./gmd:spatialResolution/\*/gmd:equivalentScale
<a name="distance"></a> distance   | ./gmd:spatialResolution/\*/gmd:distance
