# Temporal Reference


**Purpose**: A metadata must have information about the temporal dimension of the data to which it refers.

**Prerequisites**

**Test method**

* The information on the temporal dimension of the data will be described by a set of dates referring to a temporary reference system and will be expressed in accordance with [ISO 8601](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_ISO_8601).

* The default reference system will be the Gregorian calendar.
* For this there must be at least one [date](#date) element.

* - To specify the value of the [date precision](#datePrecision), the gco element will be used: Date

* - To specify the value of the [date and time precision](#dateTimePrecision), the gco element will be used: DateTime

* - The date type will be specified through the [Date Type](#dateType) element with a corresponding value from the [Code List Value](#codeListValue) [ISO 19139].

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_TG_MD), 2.3.4 , Req c.11
* [ISO 8601](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_ISO_8601)

**Test type**: Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="date"></a> Date  | ./gmd:identificationInfo[1]/\*/gmd:citation/\*/gmd:date/gmd:CI_Date/gmd:date[1]
<a name="datePrecision"></a> Date Precision  | ./gmd:identificationInfo[1]/\*/gmd:citation/\*/gmd:date/gmd:CI_Date/gmd:date[1]/gco:Date
<a name="dateTimePrecision"></a> DateTime Precision  | ./gmd:identificationInfo[1]/\*/gmd:citation/\*/gmd:date/gmd:CI_Date/gmd:date[1]/gco:DateTime
<a name="dateType"></a> Date Type | ./gmd:identificationInfo[1]/\*/gmd:citation/\*/gmd:date/gmd:CI_Date/gmd:date[1]/\*/gmd:dateType/gmd:CI_DateTypeCode/@codeListValue
<a name="codeListValue"></a> Code List Value | doc("http://standards.iso.org/iso/19139/resources/gmxCodelists.xml)//gmx:CodeListDictionary[@gml:id='CI_DateTypeCode']//gml:identifier/text()
