# Metadata date

**Purpose**

A metadata date must be given.

**Test method**

The test checks if there is an element of type gco:Date at [dateStamp](#dateStamp).

**Reference(s)**

* [IR](./README.md#IR), Annex B. 10.2

**Test type:** Automated

**Notes**

The metadata date is not explicitly a requirement in the TG, but it's still mentioned as "Mandatory" INSPIRE element(?).

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="dateStamp"></a> dateStamp   | ./gmd:dateStamp
