# Group Keywords by CV

**Purpose**: A gmd:MD_Keywords element may only contain keywords originating from the one cited controlled vocabulary, or its version.

**Prerequisites**

**Test method**
*  Check that the keywords defined in the same source controlled vocabulary are grouped into the same [Keywords](#keywords) element will be grouped.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_TG_MD), 2.3.5 , Req c.16


**Test type**: Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="keywords"></a> Keywords  | ./gmd:identificationInfo[1]/\*/<gdm:descriptiveKeywords>/<gmd:MD_Keywords>

