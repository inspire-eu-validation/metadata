# Srv type

**Purpose**: If the type of the resource was service, exactly one name describing the type of service must be given.

**Prerequisites**
* [Schema validation](Schema validation.md) must be passed
* [Hierarchy](Hierarchy.md) should contain "service"

**Test method**

If the type of the resource is service, exactly one name describing the type of service must be given.
First, a check is performed to establish whether the [serviceType](#serviceType) element occurs exactly once in the document. The test then checks if the element [serviceType](#serviceType) contains text that equals one of
the types given in http://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType ([TG MD](./README.md#ref_TG_MD) Chap. 1.3.1.)

If the type of the resource was not service, this test is omitted.

**Reference(s)**

* [TG MD](./README.md#ref_TG_MD), 1.3.1 & 2.3.2, Req 12
* http://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType

**Test type**: Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
serviceType <a name="serviceType"></a>   | ./gmd:identificationInfo[1]/*/srv:serviceType
