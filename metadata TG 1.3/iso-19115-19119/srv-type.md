# Srv type

**Purpose**: If the type of the resource was service, exactly one name describing the type of service must be given.

**Prerequisites**

* [Hierarchy](./hierarchy)

**Test method**

This test case only applies to records with a [hierarchyLevel](#hierarchyLevel) value 'service'.

If the type of the resource is service, exactly one name describing the type of service must be given.
First, a check is performed to establish whether the [serviceType](#serviceType) element occurs exactly once in the document. The test then checks if the element [serviceType](#serviceType) contains text that equals one of
the types given in http://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType ([TG MD](./README#ref_TG_MD) Chap. 1.3.1.)

**Reference(s)**

* [TG MD](./README#ref_TG_MD), 1.3.1 & 2.3.2, Req 12
* http://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType

**Test type**: Automated

**Notes**

The test method does not mention that the language independent codes should be used. TG MD 1.3.1 and 2.3.2 do say so.

The depencency to [Hierarchy](./hierarchy) has not been implemented in the ETS as it still seems reasonable to test the available service metadata records.  

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
serviceType <a name="serviceType"></a>   | ./gmd:identificationInfo[1]/\*/srv:serviceType
