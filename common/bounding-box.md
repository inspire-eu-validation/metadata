# Bounding Box

**Purpose**: Test that the extent of the resource in the geographic space is specified using a geometric bounding box.

**Prerequisites**

**Test method**

* If the codeListValue attribute of [Scope Code](#scopeCode) is 'dataset' or 'series',

    * Check that at least one [Extent](#extent) element exists.

* If [Extent](#extent) element exists, then,

    * Check that [West Bound Longitude](#west) exists. If it does,
        * Check its value is valid according with EX_GeographicBoundingBox class of the [ISO 19115](https://www.iso.org/standard/53798.html), and it has a precision of at least two decimals.
    
    * Check that [East Bound Longitude](#east) exists. If it does,
        * Check its value is valid according with EX_GeographicBoundingBox class of the [ISO 19115](https://www.iso.org/standard/53798.html), and it has a precision of at least two decimals.
    
    * Check that [South Bound Latitude](#south) exists. If it does,
        * Check its value is valid according with EX_GeographicBoundingBox class of the [ISO 19115](https://www.iso.org/standard/53798.html), and it has a precision of at least two decimals.
    
    * Check that [North Bound Latitude](#north) exists. If it does,
        * Check its value is valid according with EX_GeographicBoundingBox class of the [ISO 19115](https://www.iso.org/standard/53798.html), and it has a precision of at least two decimals.

* If any of the checks fails the test fails.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.3.8 , Req c.19
* [ISO 19115](https://www.iso.org/standard/53798.html)


**Test type**: Automated

**Notes**

For datasets and series, the multiplicity of this element is one or more.

For services, the multiplicity of this element is zero or more.


## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:identificationInfo/gmd:MD_DataIdentification/gmd:extent)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="scopeCode"></a> Scope Code | /gmd:MD_Metadata/gmd:hierarchyLevel/gmd:MD_ScopeCode
<a name="extent"></a> Extent | gmd:EX_Extent/gmd:geographicElement/gmd:EX_GeographicBoundingBox
<a name="west"></a> West Bound Longitude | gmd:EX_Extent/gmd:geographicElement/gmd:EX_GeographicBoundingBox/gmd:westBoundLongitude/gco:Decimal
<a name="east"></a> East Bound Longitude | gmd:EX_Extent/gmd:geographicElement/gmd:EX_GeographicBoundingBox/gmd:eastBoundLongitude/gco:Decimal
<a name="south"></a> South Bound Latitude | gmd:EX_Extent/gmd:geographicElement/gmd:EX_GeographicBoundingBox/gmd:southBoundLatitude/gco:Decimal
<a name="north"></a> North Bound Latitude | gmd:EX_Extent/gmd:geographicElement/gmd:EX_GeographicBoundingBox/gmd:northBoundLatitude/gco:Decimal
