#A.14.IR16.IR17.IR18.vocab

**Purpose**: A [keyword value](A.13.IR13.keyword.md) reference can contain a [controlled vocabulary](#thesaurus) from where it originates. This element is optional but, if given, must follow certain guidelines.

**Prerequisites**
* [A.01.validate](A.01.validate.md) must be passed

**Test method**

The test performs the following check for each vocabulary:
* the node must contain a title at ./gmd:CI_Citation/gmd:title and should not be an [empty characterstring](./README.md#emptychar)
* the node must contain a date at /gmd:CI_Citation/gmd:date/*/gmd:date/gco:Date
* the node must contain a dateType element at /gmd:CI_Citation/gmd:date/*/gmd:dateType which contains text that equals one of publication, revision or creation.

Validating if the keyword is actually available in the indicated vocabulary is a challenge, since the vocabulary is usually not referenced by a URL.
If a vocabulary is indicated that is available to the validator, then this check can be performed.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.4.2, Req 16, 17 & 18
* [IR MD](README.md#ref_IR_MD) Part B. 3.2

**Test type:** Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="thesaurus"></a> thesaurus  | gmd:identificationInfo[1]/*/gmd:descriptiveKeywords/*/gmd:thesaurusName
