# Spatial Resolution

**Purpose**: Test that a spatial resolution restriction is provided being mandatory when there is a restriction on the spatial resolution for the service.

**Prerequisites**

* [Resource Type](./resource-type.md)

**Test method**

* For services with restriction on the spatial resolution, for each Spatial Resolution Element,

    * Check if the spatial resolution restriction text includes either

        * an equivalent scale as integer valued scale denominator
        
        * a resolution distance using a numerical length value and a unit of length.

* If any of the checks fails, the test fails.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 4.1.2.1, Req 3.3

**Test type**: Manual

**Notes**

The multiplicity of this element is zero or more, with the following condition: "Mandatory when there is a restriction on the spatial resolution for this service".

The test characteristics makes impossible to automate it.

According to [TG MD](./README.md#ref_TG_MD), 4.1.2.1:

"For services, it is not possible to express the restriction of a service concerning the spatial resolution in using the ISO 19139 XML Schema. This problem has been solved in the [ISO 19115-3] standard expected to be published in summer 2016. This slightly inconvenient way of declaring the Spatial resolution for Spatial Data Services shall be used until this specification has been revised to comply with XML Schema rules of [ISO 19115-3]."

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="spatialResolution"></a> Spatial Resolution | gmd:identificationInfo[1]/*/gmd:abstract
