
# Service Identification

**Purpose**	

If the resource is a spatial data service, this metadata element refers to the
target spatial data set(s) of the service. It is implemented by reference, i.e. through a URL that
points to the metadata record of the data on which the service operates

**Test method**	

The operatesOn element in the [SV_ServiceIdentification](#SV_ServiceIdentification) element should [resolve](./README.md#resolve) to the metadata document describing the dataset exposed by this service. 

<!-- todo: to validate this is the proper identification, the identification used in capabilities might be required -->

**Reference(s)**	 

* [IR](./README.md#IR), Annex B. 1.6
* [TG](./README.md#TG), req 7 

**Test type:** Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="coupling"></a> SV_ServiceIdentification   | ./gmd:identificationInfo/srv:SV_ServiceIdentification/srv:operatesOn


