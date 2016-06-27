#Ds access use

**Purpose**: Conditions applying to access and use must be described at least once for the resource.

**Prerequisites**
* [Schema validation](Schema validation.md) must be passed

**Test method**

The test checks if a [useLimitation](#useLimitation) element is provided and it is not an [empty characterstring](./README.md#emptychar).

If no conditions apply to the access and use of the resource, "no
conditions apply" shall be used. If conditions are unknown, "conditions
unknown" shall be used.

Descriptions of terms and conditions, including where applicable, the
corresponding fees shall be provided through this element or a link
(URL) where these terms and conditions are described. The content will need to be checked manually.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.9.2, Req 33,34

**Test type:** Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="useLimitation"></a> useLimitation  | ./gmd:identificationInfo/*/gmd:resourceConstraints/*/gmd:useLimitation
