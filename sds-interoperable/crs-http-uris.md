# Coordinates reference systems Interoperable Spatial Data Services

**Purpose**: For interoperability reasons, if appropriate for the offered datasets, the INSPIRE SDS should provide their data using a subset of the well-known
2D and 3D coordinate reference systems listed in TG Annex D.4 of [INT SDS](#README.md#ref_TG_MD). The list of the
supported CRSes for a service shall be given as a list in the service metadata record to make it easier to discover them.

**Prerequisites**

* [resource-type](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/resource-type)

**Test method**
It is checked that the value of the HTTP URI Identifier column is used as the value of [referenceSystemIdentifier](#referenceSystemIdentifier) element.

The gmd:codeSpace element shall not be used in this case.

**Reference(s)**	 

* [TG MD](#README.md#ref_TG_MD) 4.4.1.1, Req 6.2
* [Default CRS Identifiers](#README.md#ref_TG_MD) Annex D.4

**Test type**: Automated

**Notes**
* The list of the allowed INSPIRE CRS identifiers is only given as a recommendation, so it's not possible to automatically validate if the CRSes provided fulfill the 
INSPIRE CRS criteria (ETRS89 based for data inside Europe, ITRS based otherwise).


## Contextual XPath references

The namespace prefixes used as described in [README.md](#README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| ------------------------------------------------------------------
<a name="referenceSystemIdentifier"></a> referenceSystemIdentifier  | gmd:referenceSystemInfo/\*/gmd:referenceSystemIdentifier[1]/\*/gmd:code/(gmx:Anchor/@xlink:href&#124;gco:CharacterString)