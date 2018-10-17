# Topic Category 

**Purpose**: Test that at least one Topic category describing the category of the resource is provided.

**Prerequisites**

* [Resource Type](./resource-type.md)

**Test method**

* Check that at least one [Topic Category](#topicCategory) element exists.

* For every [Topic Category](#topicCategory),

    * Check that [Topic Category Code](#topicCategoryCode) exists and its value is one of the [ISO 19115](http://inspire.ec.europa.eu/metadata-codelist/TopicCategory) topic category code list values.

* If any of the checks fails, the test fails.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 3.1.2.5, Req 1.7
* [B.5.27 of ISO 19115](http://inspire.ec.europa.eu/metadata-codelist/TopicCategory)

**Test type**: Automated

**Notes**

The multiplicity of this element is one or more.

Contrary to other code lists which are defined in the ISO 19139 XML Schema as references to an external code list, gmd:MD_TopicCategoryCode element is defined as a string enumeration.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:identificationInfo/gmd:MD_DataIdentification/gmd:topicCategory)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="topicCategory"></a> Topic Category  | /gmd:MD_Metadata/gmd:identificationInfo/gmd:MD_DataIdentification/gmd:topicCategory
<a name="topicCategoryCode"></a> Topic Category Code  | gmd:MD_TopicCategoryCode
