# Temporal Reference


**Purpose**: A metadata must have information about the temporal dimension of the data to which it refers.

**Prerequisites**

**Test method**

The information on the temporal dimension of the data will be described by a set of dates referring 
to a temporary reference system and will be expressed in accordance with [ISO 8601](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_ISO_8601).

The default reference system will be the Gregorian calendar.
For this there must be at least one [date](#date) element.

* To specify the value of the [date precision](#datePrecision), the gco element will be used: Date

* To specify the value of the [date and time precision](#dateTimePrecision), the gco element will be used: DateTime

* The date type will be specified through the [Date Type](#dateType) element with a corresponding value from the [Code List Value](#codeListValue) of [ISO 19139](http://standards.iso.org/iso/19139/resources/gmxCodelists.xml#CI_DateTypeCode).


**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_TG_MD), 2.3.4 , Req c.11
* [ISO 8601](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_ISO_8601)
* [ISO 19139](http://standards.iso.org/iso/19139/resources/gmxCodelists.xml#CI_DateTypeCode) Date Type Code

**Test type**: Automated

**Notes**
The profile of ISO 8601, the International Standard for the representation of dates and times,
describes a large number of date/time formats:

     Year:
     YYYY (eg 1997)

     Year and month:
     YYYY-MM (eg 1997-07)

     Complete date:
     YYYY-MM-DD (eg 1997-07-16)

     Complete date plus hours and minutes:
     YYYY-MM-DDThh:mmTZD (eg 1997-07-16T19:20+01:00)

     Complete date plus hours, minutes and seconds:
     YYYY-MM-DDThh:mm:ssTZD (eg 1997-07-16T19:20:30+01:00)

     Complete date plus hours, minutes, seconds and a decimal fraction of a second
     YYYY-MM-DDThh:mm:ss.sTZD (eg 1997-07-16T19:20:30.45+01:00)

where:

     YYYY = four-digit year
     MM   = two-digit month (01=January, etc.)
     DD   = two-digit day of month (01 through 31)
     hh   = two digits of hour (00 through 23) (am/pm NOT allowed)
     mm   = two digits of minute (00 through 59)
     ss   = two digits of second (00 through 59)
     s    = one or more digits representing a decimal fraction of a second
     TZD  = time zone designator (Z or +hh:mm or -hh:mm)


## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="date"></a> Date  | ./gmd:identificationInfo[1]/\*/gmd:citation/\*/gmd:date/gmd:CI_Date/gmd:date[1]
<a name="datePrecision"></a> Date Precision  | ./gmd:identificationInfo[1]/\*/gmd:citation/\*/gmd:date/gmd:CI_Date/gmd:date[1]/gco:Date
<a name="dateTimePrecision"></a> DateTime Precision  | ./gmd:identificationInfo[1]/\*/gmd:citation/\*/gmd:date/gmd:CI_Date/gmd:date[1]/gco:DateTime
<a name="dateType"></a> Date Type | ./gmd:identificationInfo[1]/\*/gmd:citation/\*/gmd:date/gmd:CI_Date/gmd:date[1]/\*/gmd:dateType/gmd:CI_DateTypeCode/@codeListValue
<a name="codeListValue"></a> Code List Value | doc("http://standards.iso.org/iso/19139/resources/gmxCodelists.xml#CI_DateTypeCode")/gmx:CodeListDictionary[@gml:id='CI_DateTypeCode']//gml:identifier/text()
