# Metadata Structure and Encoding: Root Element

**Purpose**: The encoding of the metadata must be encoded from a specific root element, MD_Metadata.

**Prerequisites**

**Test method**

* The metadata for an INSPIRE data set, data set or service should be encoded using the [root element](#rootElement) MD_Metadata.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_TG_MD), 2.1 , Req c.2
* [ISO 19115](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_ISO_19115)
* [ISO 19119](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_ISO_19119)

**Test type**: Automated

**Notes**

It must be taken into account that the use of these lines guarantees that the metadata does not conflict with [ISO 19115](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_ISO_19115) or [ISO 19119](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_ISO_19119). But at the same time, full compliance with [ISO 19115] is necessary for additional elements that are not required by the INSPIRE Implementation Rules, that is, beyond the scope of this specification.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="rootElement">Root Element</a>   | <gmd:MD_Metadata>
