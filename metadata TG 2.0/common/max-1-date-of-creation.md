# Max One Date of Creation


**Purpose**: Test that not more than one date of creation for the metadata is given.

**Prerequisites**

[Temporal reference](./temporal-reference.md)

**Test method**

* Check that at most one [Date Type](#dateType) element with attribute codeListValue equal 'creation' exists.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.3.4 , Req c.12
* [ISO 8601](./README.md#ref_ISO_8601)

**Test type**: Automated

**Notes**

The multiplicity of the element is zero or one.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:identificationInfo/*/gmd:citation/gmd:CI_Citation)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="dateType"></a> Date Type | gmd:date/gmd:CI_Date/gmd:dateType/gmd:CI_DateTypeCode
