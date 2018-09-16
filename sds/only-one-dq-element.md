# Only One Data Quality Info Element

**Purpose**: For every conformity statement, one citation of the product specification or user requirement against which data is being evaluated must be given.

**Prerequisites**

* [Resource Type](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds/resource-type)

**Test method**

This test case only applies to records with a [hierarchyLevel](#hierarchyLevel) value 'service'.

The test first checks that shall be exactly one [dataQualityInfo](#dataquality) element scoped to the entire described services. 

**Reference(s)**

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds/README#ref_TG_MD), 4.1.4.1, Req 3.8

**Test type**: Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="hierarchyLevel"></a> Hierarchy Level | ./gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="dataquality"></a> dataQuality    | ./gmd:dataQualityInfo[count(gmd:DQ_DataQuality)=1]
<a name="scopeCode"></a> scopeCode    | ./gmd:dataQualityInfo[1]/\*/gmd:scope/\*/gmd:level/gmd:MD_ScopeCode/@codeListValue
<a name="codeListValue"></a> codeListValue | doc("http://standards.iso.org/iso/19139/resources/gmxCodelists.xml)//gmx:CodeListDictionary[@gml:id='MD_ScopeCode']///gml:identifier/text()
