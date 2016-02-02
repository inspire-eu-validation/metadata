#A.09.IR04.srv.linkage

**Purpose**: If a linkage for a service is available, the Resource Locator shall be a
valid URL providing one of the following:
* a link to a web with further instructions
* a link to a service capabilities document
* a link to the service WSDL document (SOAP Binding)
* a link to a client application that directly accesses the service

**Prerequisites**
* [A.01.validate](A.01.validate.md) must be passed

**Test method**

If the type of the resource is not service, this test is omitted.

Any of the onlineresources should be checked if it [resolves](./README.md#resolve)
* if wm(t)s/wfs/wcs; in one of the featuretypes/layers in the capabilities there should be a link back to the metadata, it should be the same metadata.
* if atom: ... <!-- todo: -->
* if soap: ... <!-- todo: -->

Either a link to a web with further instructions or a link to a client application are not machine testable

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.2.4, Req 4
* [IR MD](README.md#ref_IR_MD) Part B. 1.4

**Test type:** Automated

**Notes**

##Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="linkage"></a> Linkage   | distributionInfo/*/transferOptions/*/onLine/*/linkage
