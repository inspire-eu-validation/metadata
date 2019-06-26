# Schema validation

**Purpose**: Performs a schema validation of the document.

**Prerequisites**

**Test method**

The document shall pass schema validation without errors using the following XML schema definitions:

* `encoding` = `CSW ISO AP 1.0.0`: http://schemas.opengis.net/csw/2.0.2/profiles/apiso/1.0.0/apiso.xsd
* `encoding` = `ISO/TS 19139`: http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/gmd/gmd.xsd or http://schemas.opengis.net/iso/19139/20070417/gmd/gmd.xsd

If no parameter is provided, the encoding is determined by inspecting the [schemaLocation](#schemaLocation) based on the schema documents used for the "gmd" namespace. If this information cannot be determined, assume `CSW ISO AP 1.0`. 

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.1.2

**Test type**: Automated

**Notes**

The schemas above are only sufficient, if a single metadata record is validated. If the metadata record is part of another document, e.g. a response to a CSW GetRecords request, validation will fail. 

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README#namespaces).

Abbreviation                                     |  XPath expression												|  Parameter  value
------------------------------------------------ | ---------------------------------------------------------------	| ---------------------------------------------------------------
schemaLocation <a name="schemaLocation"></a>   | /*/@xsi:schemaLocation
