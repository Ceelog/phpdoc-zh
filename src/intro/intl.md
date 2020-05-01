Internationalization extension (further is referred as Intl) is a
wrapper for
<a href="http://www.icu-project.org/" class="link external">» ICU</a>
library, enabling PHP programmers to perform various locale-aware
operations including but not limited to formatting, transliteration,
encoding conversion, calendar operations,
<a href="http://www.unicode.org/reports/tr10/" class="link external">» UCA</a>-conformant
collation, locating text boundaries and working with locale identifiers,
timezones and graphemes,

It tends to closely follow ICU APIs, so that people having experience
working with ICU in either C/C++ or Java could easily use the PHP API.
Also, this way ICU documentation would be useful to understand various
ICU functions.

Intl consists of several modules, each of them exposes the corresponding
ICU API:

-   <span class="simpara"> Collator: provides string comparison
    capability with support for appropriate locale-sensitive sort
    orderings. </span>
-   <span class="simpara"> Number Formatter: allows to display number
    according to the localized format or given pattern or set of rules,
    and to parse strings into numbers. </span>
-   <span class="simpara"> Message Formatter: allows to create messages
    incorporating data (such as numbers or dates) formatted according to
    given pattern and locale rules, and parse messages extracting data
    from them. It can handle plurals, locale-aware numbers, currencies,
    conditions and much more. </span>
-   <span class="simpara"> Normalizer: provides a function to transform
    text into one of the Unicode normalization forms, and provides a
    routine to test if a given string is already normalized. </span>
-   <span class="simpara"> Locale: provides interaction with locale
    identifiers in the form of functions to get subtags from locale
    identifier; parse, compose, match(lookup and filter) locale
    identifiers. </span>
-   <span class="simpara"> Calendar: provides a class which could be
    used for locale-aware calendar operations and getting various
    information such as timezone for locale chosen, first day of week or
    if it's daylight saving time now. </span>
-   <span class="simpara"> Timezone: provides a wrapper around the
    <a href="http://www.iana.org/time-zones" class="link external">» "Olson" database</a>
    which has information about all the timezones around the world.
    </span>
-   <span class="simpara"> Date formatter: allows to display date and
    time according to the localized format or given pattern or set of
    rules, and to parse strings into date and time. </span>
-   <span class="simpara"> Transliterator: allows getting latin
    representation of strings in various languages. </span>

Links
-----

-   <a href="http://site.icu-project.org/docs/" class="link external">» Miscellaneous ICU docs</a>

-   <a href="http://www.icu-project.org/userguide/" class="link external">» ICU User Guide</a>

-   <a href="http://www.unicode.org/reports/tr10/" class="link external">» Unicode Collation Algorithm</a>
