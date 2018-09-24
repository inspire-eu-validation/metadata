# Metadata Date


**Purpose**: indicate the date which specifies when the metadata record was created or updated.

**Prerequisites**

**Test method**

Shall be especificated the last update date of each metadata record from the [dateStamp](#date).

* If no updates have been made, the creation date of the metadata will be used.

* The multiplicity of this element is one or more.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_TG_MD), 2.2.4 , Req c.7
* [ISO 8601](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_ISO_8601)


**Test type**: Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="date"></a> Date Stamp  | ./gmd:dateStamp[1]

