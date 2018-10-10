# Root Element

**Purpose**: Test that the specification of a metadata is encoded through a root element MD_Metadata.

**Prerequisites**

**Test method**

* Check that exactly one [Root Element](#rootElement) MD_Metadata exists.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.1 , Req c.2
* [ISO 19115](./README.md#ref_ISO_19115)
* [ISO 19119](./README.md#ref_ISO_19119)

**Test type**: Automated

**Notes**

The multiplicity of [root element](#rootElement) is one.

It must be taken into account that the use of these lines guarantees that the metadata does not conflict with [ISO 19115](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_ISO_19115) or [ISO 19119](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_ISO_19119). But at the same time, full compliance with [ISO 19115] is necessary for additional elements that are not required by the INSPIRE Implementation Rules, that is, beyond the scope of this specification.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression
-----------------------------------------------| -------------------------------------------------------------------------
<a name="rootElement">Root Element</a>   | /gmd:MD_Metadata
