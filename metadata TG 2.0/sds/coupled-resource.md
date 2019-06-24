# Coupled Resource

**Purpose**: Test that an operatesOn element refers to the target spatial data set(s) of the service, being implemented by reference.

**Prerequisites**

**Test method**

* Check if the operatesOn element in the [SV_ServiceIdentification](#SV_ServiceIdentification) element is a HTTP URI that when retrieved using HTTP GET returns the metadata document describing the dataset exposed by the service.

* Check if the property is implemented by reference. It means that the xlink:href attribute of each operatesOn element contains a URI pointing to the gmd:MD_DataIdentification element of the metadata record of the provided data set or data set series.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD) 4.1.2.4, Req 3.6

**Test type**: Automated

**Notes**

The multiplicity of this element is zero or more with the following condition: "Mandatory if linkage to data sets on which the service operates are available".

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="SV_ServiceIdentification"></a> SV_ServiceIdentification   | gmd:identificationInfo/srv:SV_ServiceIdentification/srv:operatesOn
