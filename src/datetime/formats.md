Supported Date and Time Formats
===============================

**目录**

-   [Time Formats](/datetime/formats.html#Time%20Formats)
-   [Date Formats](/datetime/formats.html#Date%20Formats)
-   [Compound Formats](/datetime/formats.html#Compound%20Formats)
-   [Relative Formats](/datetime/formats.html#Relative%20Formats)

This section describes all the different formats that the <span
class="classname">DateTimeImmutable</span>, <span
class="classname">DateTime</span>, <span
class="function">date\_create</span>, <span
class="function">date\_create\_immutable</span>, and <span
class="function">strtotime</span> parser understands. The formats are
grouped by section. In most cases formats from different sections,
separated by whitespace, comma or dot, can be used in the same date/time
string. For each of the supported formats, one or more examples are
given, as well as a description for the format. Characters in single
quotes in the formats are case-insensitive (*'t'* could be *t* or *T*),
characters in double quotes are case-sensitive (*"T"* is only *T*).

Time Formats
------------

This page describes the different date/time formats that the <span
class="classname">DateTimeImmutable</span>, <span
class="classname">DateTime</span>, <span
class="function">date\_create</span>, <span
class="function">date\_create\_immutable</span>, and <span
class="function">strtotime</span> parser understands.

| Description    | Formats                                                               | Examples                                           |
|----------------|-----------------------------------------------------------------------|----------------------------------------------------|
| *frac*         | . \[0-9\]+                                                            | ".21342", ".85"                                    |
| *hh*           | "0"?\[1-9\] \| "1"\[0-2\]                                             | "04", "7", "12"                                    |
| *HH*           | \[01\]\[0-9\] \| "2"\[0-4\]                                           | "04", "07", "19"                                   |
| *meridian*     | \[AaPp\] .? \[Mm\] .? \[\\0\\t \]                                     | "A.m.", "pM", "am."                                |
| *MM*           | \[0-5\]\[0-9\]                                                        | "00", "12", "59"                                   |
| *II*           | \[0-5\]\[0-9\]                                                        | "00", "12", "59"                                   |
| *space*        | \[ \\t\]                                                              |                                                    |
| *tz*           | "("? \[A-Za-z\]{1,6} ")"? \| \[A-Z\]\[a-z\]+(\[\_/\]\[A-Z\]\[a-z\]+)+ | "CEST", "Europe/Amsterdam", "America/Indiana/Knox" |
| *tzcorrection* | "GMT"? \[+-\] *hh* ":"? *MM*?                                         | "+0400", "GMT-07:00", "-07:00"                     |

| Description                                                                        | Format                                            | Examples                    |
|------------------------------------------------------------------------------------|---------------------------------------------------|-----------------------------|
| Hour only, with meridian                                                           | *hh* *space*? *meridian*                          | "4 am", "5PM"               |
| Hour and minutes, with meridian                                                    | *hh* \[.:\] *MM* *space*? *meridian*              | "4:08 am", "7:19P.M."       |
| Hour, minutes and seconds, with meridian                                           | *hh* \[.:\] *MM* \[.:\] *II* *space*? *meridian*  | "4:08:37 am", "7:19:19P.M." |
| MS SQL (Hour, minutes, seconds and fraction with meridian), PHP 5.3 and later only | *hh* ":" *MM* ":" *II* \[.:\] \[0-9\]+ *meridian* | "4:08:39:12313am"           |

| Description                         | Format                                                                | Examples                                         |
|-------------------------------------|-----------------------------------------------------------------------|--------------------------------------------------|
| Hour and minutes                    | 't'? *HH* \[.:\] *MM*                                                 | "04:08", "19.19", "T23:43"                       |
| Hour and minutes, no colon          | 't'? *HH* *MM*                                                        | "0408", "t1919", "T2343"                         |
| Hour, minutes and seconds           | 't'? *HH* \[.:\] *MM* \[.:\] *II*                                     | "04.08.37", "t19:19:19"                          |
| Hour, minutes and seconds, no colon | 't'? *HH* *MM* *II*                                                   | "040837", "T191919"                              |
| Hour, minutes, seconds and timezone | 't'? *HH* \[.:\] *MM* \[.:\] *II* *space*? ( *tzcorrection* \| *tz* ) | "040837CEST", "T191919-0700"                     |
| Hour, minutes, seconds and fraction | 't'? *HH* \[.:\] *MM* \[.:\] *II* *frac*                              | "04.08.37.81412", "19:19:19.532453"              |
| Time zone information               | *tz* \| *tzcorrection*                                                | "CEST", "Europe/Amsterdam", "+0430", "GMT-06:00" |

Date Formats
------------

This page describes the different date formats that the <span
class="function">strtotime</span>, <span
class="classname">DateTime</span> and <span
class="function">date\_create</span> parser understands.

| Description | Format                                                                                                                                                                                                                                                                                                                                                                 | Examples                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| *daysuf*    | "st" \| "nd" \| "rd" \| "th"                                                                                                                                                                                                                                                                                                                                           |                               |
| *dd*        | (\[0-2\]?\[0-9\] \| "3"\[01\]) *daysuf*?                                                                                                                                                                                                                                                                                                                               | "7th", "22nd", "31"           |
| *DD*        | "0" \[0-9\] \| \[1-2\]\[0-9\] \| "3" \[01\]                                                                                                                                                                                                                                                                                                                            | "07", "31"                    |
| *m*         | 'january' \| 'february' \| 'march' \| 'april' \| 'may' \| 'june' \| 'july' \| 'august' \| 'september' \| 'october' \| 'november' \| 'december' \| 'jan' \| 'feb' \| 'mar' \| 'apr' \| 'may' \| 'jun' \| 'jul' \| 'aug' \| 'sep' \| 'sept' \| 'oct' \| 'nov' \| 'dec' \| "I" \| "II" \| "III" \| "IV" \| "V" \| "VI" \| "VII" \| "VIII" \| "IX" \| "X" \| "XI" \| "XII" |                               |
| *M*         | 'jan' \| 'feb' \| 'mar' \| 'apr' \| 'may' \| 'jun' \| 'jul' \| 'aug' \| 'sep' \| 'sept' \| 'oct' \| 'nov' \| 'dec'                                                                                                                                                                                                                                                     |                               |
| *mm*        | "0"? \[0-9\] \| "1"\[0-2\]                                                                                                                                                                                                                                                                                                                                             | "0", "04", "7", "12"          |
| *MM*        | "0" \[0-9\] \| "1"\[0-2\]                                                                                                                                                                                                                                                                                                                                              | "00", "04", "07", "12"        |
| *y*         | \[0-9\]{1,4}                                                                                                                                                                                                                                                                                                                                                           | "00", "78", "08", "8", "2008" |
| *yy*        | \[0-9\]{2}                                                                                                                                                                                                                                                                                                                                                             | "00", "08", "78"              |
| *YY*        | \[0-9\]{4}                                                                                                                                                                                                                                                                                                                                                             | "2000", "2008", "1978"        |

| Description                                               | Format                                        | Examples                                       |
|-----------------------------------------------------------|-----------------------------------------------|------------------------------------------------|
| American month and day                                    | *mm* "/" *dd*                                 | "5/12", "10/27"                                |
| American month, day and year                              | *mm* "/" *dd* "/" *y*                         | "12/22/78", "1/17/2006", "1/17/6"              |
| Four digit year, month and day with slashes               | *YY* "/" *mm* "/" *dd*                        | "2008/6/30", "1978/12/22"                      |
| Four digit year and month (GNU)                           | *YY* "-" *mm*                                 | "2008-6", "2008-06", "1978-12"                 |
| Year, month and day with dashes                           | *y* "-" *mm* "-" *dd*                         | "2008-6-30", "78-12-22", "8-6-21"              |
| Day, month and four digit year, with dots, tabs or dashes | *dd* \[.\\t-\] *mm* \[.-\] *YY*               | "30-6-2008", "22.12.1978"                      |
| Day, month and two digit year, with dots or tabs          | *dd* \[.\\t\] *mm* "." *yy*                   | "30.6.08", "22\\t12.78"                        |
| Day, textual month and year                               | *dd* (\[ \\t.-\])\* *m* (\[ \\t.-\])\* *y*    | "30-June 2008", "22DEC78", "14 III 1879"       |
| Textual month and four digit year (Day reset to 1)        | *m* (\[ \\t.-\])\* *YY*                       | "June 2008", "DEC1978", "March 1879"           |
| Four digit year and textual month (Day reset to 1)        | *YY* (\[ \\t.-\])\* *m*                       | "2008 June", "1978-XII", "1879.MArCH"          |
| Textual month, day and year                               | *m* (\[ .\\t-\])\* *dd* \[,.stndrh\\t \]+ *y* | "July 1st, 2008", "April 17, 1790", "May.9,78" |
| Textual month and day                                     | *m* (\[ .\\t-\])\* *dd* \[,.stndrh\\t \]\*    | "July 1st,", "Apr 17", "May.9"                 |
| Day and textual month                                     | *d* (\[ .\\t-\])\* *m*                        | "1 July", "17 Apr", "9.May"                    |
| Month abbreviation, day and year                          | *M* "-" *DD* "-" *y*                          | "May-09-78", "Apr-17-1790"                     |
| Year, month abbreviation and day                          | *y* "-" *M* "-" *DD*                          | "78-Dec-22", "1814-MAY-17"                     |
| Year (and just the year)                                  | *YY*                                          | "1978", "2008"                                 |
| Textual month (and just the month)                        | *m*                                           | "March", "jun", "DEC"                          |

| Description                                       | Format                         | Examples                                   |
|---------------------------------------------------|--------------------------------|--------------------------------------------|
| Eight digit year, month and day                   | *YY* *MM* *DD*                 | "15810726", "19780417", "18140517"         |
| Four digit year, month and day with slashes       | *YY* "/" *MM* "/" *DD*         | "2008/06/30", "1978/12/22"                 |
| Two digit year, month and day with dashes         | *yy* "-" *MM* "-" *DD*         | "08-06-30", "78-12-22"                     |
| Four digit year with optional sign, month and day | \[+-\]? *YY* "-" *MM* "-" *DD* | "-0002-07-26", "+1978-04-17", "1814-05-17" |

> **Note**:
>
> For the *y* and *yy* formats, years below 100 are handled in a special
> way when the *y* or *yy* symbol is used. If the year falls in the
> range 0 (inclusive) to 69 (inclusive), 2000 is added. If the year
> falls in the range 70 (inclusive) to 99 (inclusive) then 1900 is
> added. This means that "00-01-01" is interpreted as "2000-01-01".

> **Note**:
>
> The "Day, month and two digit year, with dots or tabs" format (*dd*
> \[.\\t\] *mm* "." *yy*) only works for the year values 61 (inclusive)
> to 99 (inclusive) - outside those years the *time format* "*HH* \[.:\]
> *MM* \[.:\] *SS*" has precedence.

> **Note**:
>
> The "Year (and just the year)" format only works if a time string has
> already been found -- otherwise this format is recognised as *HH*
> *MM*.

> **Note**:
>
> It is possible to over- and underflow the *dd* and *DD* format. Day 0
> means the last day of previous month, whereas overflows count into the
> next month. This makes "2008-08-00" equivalent to "2008-07-31" and
> "2008-06-31" equivalent to "2008-07-01" (June only has 30 days).
>
> Note that as of PHP 5.1.0 the day range is restricted to 0-31 as
> indicated by the regular expression above. Thus "2008-06-32" is not a
> valid date string, for instance.
>
> It is also possible to underflow the *mm* and *MM* formats with the
> value 0. A month value of 0 means December of the previous year. As
> example "2008-00-22" is equivalent to "2007-12-22".
>
> If you combine the previous two facts and underflow both the day and
> the month, the following happens: "2008-00-00" first gets converted to
> "2007-12-00" which then gets converted to "2007-11-30". This also
> happens with the string "0000-00-00", which gets transformed into
> "-0001-11-30" (the year -1 in the ISO 8601 calendar, which is 2 BC in
> the proleptic Gregorian calendar).

Compound Formats
----------------

This page describes the different compound date/time formats that the
<span class="function">strtotime</span>, <span
class="classname">DateTime</span> and <span
class="function">date\_create</span> parser understands.

| Description    | Formats                                                                                                            | Examples                          |
|----------------|--------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| *DD*           | "0" \[0-9\] \| \[1-2\]\[0-9\] \| "3" \[01\]                                                                        | "02", "12", "31"                  |
| *doy*          | "00"\[1-9\] \| "0"\[1-9\]\[0-9\] \| \[1-2\]\[0-9\]\[0-9\] \| "3"\[0-5\]\[0-9\] \| "36"\[0-6\]                      | "001", "012", "180", "350", "366" |
| *frac*         | . \[0-9\]+                                                                                                         | ".21342", ".85"                   |
| *hh*           | "0"?\[1-9\] \| "1"\[0-2\]                                                                                          | "04", "7", "12"                   |
| *HH*           | \[01\]\[0-9\] \| "2"\[0-4\]                                                                                        | "04", "07", "19"                  |
| *meridian*     | \[AaPp\] .? \[Mm\] .? \[\\0\\t \]                                                                                  | "A.m.", "pM", "am."               |
| *ii*           | \[0-5\]\[0-9\]                                                                                                     | "04", "8", "59"                   |
| *II*           | \[0-5\]\[0-9\]                                                                                                     | "04", "08", "59"                  |
| *M*            | 'jan' \| 'feb' \| 'mar' \| 'apr' \| 'may' \| 'jun' \| 'jul' \| 'aug' \| 'sep' \| 'sept' \| 'oct' \| 'nov' \| 'dec' |                                   |
| *MM*           | \[0-1\]\[0-9\]                                                                                                     | "00", "12"                        |
| *space*        | \[ \\t\]                                                                                                           |                                   |
| *ss*           | \[0-5\]\[0-9\]                                                                                                     | "04", "8", "59"                   |
| *SS*           | \[0-5\]\[0-9\]                                                                                                     | "04", "08", "59"                  |
| *W*            | "0"\[1-9\] \| \[1-4\]\[0-9\] \| "5"\[0-3\]                                                                         | "05", "17", "53"                  |
| *tzcorrection* | "GMT"? \[+-\] *hh* ":"? *II*?                                                                                      | "+0400", "GMT-07:00", "-07:00"    |
| *YY*           | \[0-9\]{4}                                                                                                         | "2000", "2008", "1978"            |

| Description                       | Format                                                                   | Examples                                                 |
|-----------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------|
| Common Log Format                 | *dd* "/" *M* "/" *YY* : *HH* ":" *II* ":" *SS* *space* *tzcorrection*    | "10/Oct/2000:13:55:36 -0700"                             |
| EXIF                              | *YY* ":" *MM* ":" *DD* " " *HH* ":" *II* ":" *SS*                        | "2008:08:07 18:11:31"                                    |
| ISO year with ISO week            | *YY* "-"? "W" *W*                                                        | "2008W27", "2008-W28"                                    |
| ISO year with ISO week and day    | *YY* "-"? "W" *W* "-"? \[0-7\]                                           | "2008W273", "2008-W28-3"                                 |
| MySQL                             | *YY* "-" *MM* "-" *DD* " " *HH* ":" *II* ":" *SS*                        | "2008-08-07 18:11:31"                                    |
| PostgreSQL: Year with day-of-year | *YY* "."? *doy*                                                          | "2008.197", "2008197"                                    |
| SOAP                              | *YY* "-" *MM* "-" *DD* "T" *HH* ":" *II* ":" *SS* *frac* *tzcorrection*? | "2008-07-01T22:35:17.02", "2008-07-01T22:35:17.03+08:00" |
| Unix Timestamp                    | "@" "-"? \[0-9\]+                                                        | "@1215282385"                                            |
| XMLRPC                            | *YY* *MM* *DD* "T" *hh* ":" *II* ":" *SS*                                | "20080701T22:38:07", "20080701T9:38:07"                  |
| XMLRPC (Compact)                  | *YY* *MM* *DD* 't' *hh* *II* *SS*                                        | "20080701t223807", "20080701T093807"                     |
| WDDX                              | *YY* "-" *mm* "-" *dd* "T" *hh* ":" *ii* ":" *ss*                        | "2008-7-1T9:3:37"                                        |

> **Note**:
>
> The "W" in the "ISO year with ISO week" and "ISO year with ISO week
> and day" formats is case-sensitive, you can only use the upper case
> "W".
>
> The "T" in the SOAP, XMRPC and WDDX formats is case-sensitive, you can
> only use the upper case "T".
>
> The "Unix Timestamp" format sets the timezone to UTC.

Relative Formats
----------------

This page describes the different relative date/time formats that the
<span class="function">strtotime</span>, <span
class="classname">DateTime</span> and <span
class="function">date\_create</span> parser understands.

| Description | Format                                                                                                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *dayname*   | 'sunday' \| 'monday' \| 'tuesday' \| 'wednesday' \| 'thursday' \| 'friday' \| 'saturday' \| 'sun' \| 'mon' \| 'tue' \| 'wed' \| 'thu' \| 'fri' \| 'sat'                                |
| *daytext*   | 'weekday' \| 'weekdays'                                                                                                                                                                |
| *number*    | \[+-\]?\[0-9\]+                                                                                                                                                                        |
| *ordinal*   | 'first' \| 'second' \| 'third' \| 'fourth' \| 'fifth' \| 'sixth' \| 'seventh' \| 'eighth' \| 'ninth' \| 'tenth' \| 'eleventh' \| 'twelfth' \| 'next' \| 'last' \| 'previous' \| 'this' |
| *reltext*   | 'next' \| 'last' \| 'previous' \| 'this'                                                                                                                                               |
| *space*     | \[ \\t\]+                                                                                                                                                                              |
| *unit*      | (('sec' \| 'second' \| 'min' \| 'minute' \| 'hour' \| 'day' \| 'fortnight' \| 'forthnight' \| 'month' \| 'year') 's'?) \| 'weeks' \| *daytext*                                         |

| Format                                   | Description                                                                                                          | Examples                                                                                     |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| 'yesterday'                              | Midnight of yesterday                                                                                                | "yesterday 14:00"                                                                            |
| 'midnight'                               | The time is set to 00:00:00                                                                                          |                                                                                              |
| 'today'                                  | The time is set to 00:00:00                                                                                          |                                                                                              |
| 'now'                                    | Now - this is simply ignored                                                                                         |                                                                                              |
| 'noon'                                   | The time is set to 12:00:00                                                                                          | "yesterday noon"                                                                             |
| 'tomorrow'                               | Midnight of tomorrow                                                                                                 |                                                                                              |
| 'back of' *hour*                         | 15 minutes past the specified hour                                                                                   | "back of 7pm", "back of 15"                                                                  |
| 'front of' *hour*                        | 15 minutes before the specified hour                                                                                 | "front of 5am", "front of 23"                                                                |
| 'first day of'                           | Sets the day of the first of the current month. This phrase is best used together with a month name following it.    | "first day of January 2008"                                                                  |
| 'last day of'                            | Sets the day to the last day of the current month. This phrase is best used together with a month name following it. | "last day of next month"                                                                     |
| *ordinal* *space* *dayname* *space* 'of' | Calculates the *x*-th week day of the current month.                                                                 | "first sat of July 2008"                                                                     |
| 'last' *space* *dayname* *space* 'of'    | Calculates the *last* week day of the current month.                                                                 | "last sat of July 2008"                                                                      |
| *number* *space*? (*unit* \| 'week')     | Handles relative time items where the value is a number.                                                             | "+5 weeks", "12 day", "-7 weekdays"                                                          |
| *ordinal* *space* *unit*                 | Handles relative time items where the value is text.                                                                 | "fifth day", "second month"                                                                  |
| 'ago'                                    | Negates all the values of previously found relative time items.                                                      | "2 days ago", "8 days ago 14:00", "2 months 5 days ago", "2 months ago 5 days", "2 days ago" |
| *dayname*                                | Moves to the next day of this name.                                                                                  | "Monday"                                                                                     |
| *reltext* *space* 'week'                 | Handles the special format "weekday + last/this/next week".                                                          | "Monday next week"                                                                           |

> **Note**:
>
> Relative statements are always processed *after* non-relative
> statements. This makes "+1 week july 2008" and "july 2008 +1 week"
> equivalent.
>
> Exceptions to this rule are: "yesterday", "midnight", "today", "noon"
> and "tomorrow". Note that "tomorrow 11:00" and "11:00 tomorrow" are
> different. Considering today's date of "July 23rd, 2008" the first one
> produces "2008-07-24 11:00" where as the second one produces
> "2008-07-24 00:00". The reason for this is that those five statements
> directly influence the current time.

> **Note**:
>
> Observe the following remarks when the current day-of-week is the same
> as the day-of-week used in the date/time string. The current
> day-of-week could have been (re-)calculated by non-relative parts of
> the date/time string however.
>
> 1.  <span class="simpara"> "*dayname*" does *not* advance to another
>     day. (Example: "Wed July 23rd, 2008" means "2008-07-23"). </span>
> 2.  <span class="simpara"> "*number* *dayname*" does *not* advance to
>     another day. (Example: "1 wednesday july 23rd, 2008" means
>     "2008-07-23"). </span>
> 3.  <span class="simpara"> "*number* week *dayname*" will first add
>     the number of weeks, but does *not* advance to another day. In
>     this case "*number* week" and "*dayname*" are two distinct blocks.
>     (Example: "+1 week wednesday july 23rd, 2008" means "2008-07-30").
>     </span>
> 4.  <span class="simpara"> "*ordinal* *dayname*" *does* advance to
>     another day. (Example "first wednesday july 23rd, 2008" means
>     "2008-07-30"). </span>
> 5.  <span class="simpara"> "*number* week *ordinal* *dayname*" will
>     first add the number of weeks, and then *advances* to another day.
>     In this case "*number* week" and "*ordinal* *dayname*" are two
>     distinct blocks. (Example: "+1 week first wednesday july 23rd,
>     2008" means "2008-08-06"). </span>
> 6.  <span class="simpara"> "*ordinal* *dayname* 'of' " does *not*
>     advance to another day. (Example: "first wednesday of july 23rd,
>     2008" means "2008-07-02" because the specific phrase with 'of'
>     resets the day-of-month to '1' and the '23rd' is ignored here).
>     </span>
>
> Also observe that the "of" in "*ordinal* *space* *dayname* *space*
> 'of' " and "'last' *space* *dayname* *space* 'of' " does something
> special.
>
> 1.  <span class="simpara"> It sets the day-of-month to 1. </span>
> 2.  <span class="simpara"> "*ordinal* *dayname* 'of' " does *not*
>     advance to another day. (Example: "first tuesday of july 2008"
>     means "2008-07-01"). </span>
> 3.  <span class="simpara"> "*ordinal* *dayname* " *does* advance to
>     another day. (Example: "first tuesday july 2008" means
>     "2008-07-08", see also point 4 in the list above). </span>
> 4.  <span class="simpara"> "'last' *dayname* 'of' " takes the last
>     *dayname* of the current month. (Example: "last wed of july 2008"
>     means "2008-07-30") </span>
> 5.  <span class="simpara"> "'last' *dayname*" takes the last *dayname*
>     from the current day. (Example: "last wed july 2008" means
>     "2008-06-25"; "july 2008" first sets the current date to
>     "2008-07-01" and then "last wed" moves to the previous Wednesday
>     which is "2008-06-25"). </span>

> **Note**:
>
> Relative month values are calculated based on the length of months
> that they pass through. An example would be "+2 month 2011-11-30",
> which would produce "2012-01-30". This is due to November being 30
> days in length, and December being 31 days in length, producing a
> total of 61 days.

> **Note**:
>
> *number* is an *integer* number; if a decimal number is given, the dot
> (or comma) is likely interpreted as delimiter. For instance, *'+1.5
> hours'* is parsed like *'+1 5 hours'*, not as *'+1 hour +30 minutes'*.

### 更新日志

| 版本          | 说明                                                                                                                                                     |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 5.6.23, 7.0.8 | Weeks always start on monday. Formerly, sunday would also be considered to start a week.                                                                 |
| 5.3.3         | "first day" and "last day" changed to behave has "+1 day" and "-1 day", respectively. Previously, the behaviour was as "first day of" and "last day of". |
