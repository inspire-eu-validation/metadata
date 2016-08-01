# Dataset spatial resolution

**Purpose**: If the type of the resource was dataset or series, Each [spatial resolution](#spatialResolution) is either an [equivalentScale](#equivalentScale) OR a ground sample [distance](#distance).

**Prerequisites**

**Test method**

Each [spatialResolution](#spatialResolution) element must contain either an [equivalentScale](#equivalentScale) or a [distance](#distance) but not both.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#ref_TG_MD) 2.7.2, Req 27

**Test type**: Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="spatialResolution"></a> spatialResolution | ./gmd:identificationInfo/*/gmd:MD_DataIdentification/*/gmd:spatialResolution
<a name="equivalentScale"></a> equivalentScale  | ./gmd:spatialResolution/gmd:MD_Resolution/gmd:equivalentScale
<a name="distance"></a> distance   | ./gmd:spatialResolution/gmd:MD_Resolution/gmd:distance
