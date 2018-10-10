# Temporal Reference

**Purpose**: Test that there is at least one temporal reference and it is codified correctly.

**Prerequisites**

**Test method**

* Check that there is at least one [date](#date) element. If it does, for every [date](#date) element,

    * Check that one of [date precision](#datePrecision) or [date and time precision](#dateTimePrecision) exists and that it is codified correctly according with [ISO 8601](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_ISO_8601).

    * Check that [Date Type](#dateType) element exists. If it does,

        * Check that the [Date Type](#dateType) has an attribute named codeList which value is "http://standards.iso.org/iso/19139/resources/gmxCodelists.xml#CI_DateTypeCode"

        * Check that the [Date Type](#dateType) has an attribute named codeListValue which value is "publication", "revision" or "creation".

* If any of the checks fails, the test fails.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.3.4 , Req c.11
* [ISO 8601](./README.md#ref_ISO_8601)
* [ISO 19139](http://standards.iso.org/iso/19139/resources/gmxCodelists.xml#CI_DateTypeCode) Date Type Code

**Test type**: Automated

**Notes**

The multiplicity of [date](#date) is one or more.

The default reference system will be the Gregorian calendar.

The profile of ISO 8601, the International Standard for the representation of dates and times, describes a large number of date/time formats:

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

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:identificationInfo/*/gmd:citation/gmd:CI_Citation)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="date"></a> Date  | gmd:date/gmd:CI_Date/gmd:date
<a name="datePrecision"></a> Date Precision  | gmd:date/gmd:CI_Date/gmd:date/gco:Date
<a name="dateTimePrecision"></a> DateTime Precision  | gmd:date/gmd:CI_Date/gmd:date/gco:DateTime
<a name="dateType"></a> Date Type | gmd:date/gmd:CI_Date/gmd:dateType/gmd:CI_DateTypeCode
