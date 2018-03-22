# Coupled resource

**Purpose**: If the resource is a spatial data service, this metadata element refers to the
target spatial data set(s) of the service. It is implemented by reference, i.e. through a URL that
points to the metadata record of the data on which the service operates.

**Prerequisites**

**Test method**

This test case only applies to records with a [hierarchyLevel](#hierarchyLevel) value 'service'.

The operatesOn element in the [SV_ServiceIdentification](#SV_ServiceIdentification) element should be a HTTP URI that when retrieved using 
HTTP GET should return the metadata document describing the dataset exposed by this service.

The multiplicity of this element is 0 or more.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds/README#ref_TG_MD) 4.1.2.4, Req 3.6

**Test type**: Automated

**Notes**


##Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | ./gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="coupling"></a> SV_ServiceIdentification   | ./gmd:identificationInfo/\*/srv:operatesOn
