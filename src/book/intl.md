Internationalization Functions
==============================

**目录**

-   [简介](/intro/intl.html)
-   [安装／配置](/intl/setup.html)
    -   [需求](/intl/setup.html#需求)
    -   [安装](/intl/setup.html#安装)
    -   [运行时配置](/intl/setup.html#运行时配置)
    -   [资源类型](/intl/setup.html#资源类型)
-   [预定义常量](/intl/constants.html)
-   [范例](/intl/examples.html)
    -   [Basic usage of this
        extension](/intl/examples.html#Basic%20usage%20of%20this%20extension)
-   [Collator](/class/collator.html) — The Collator class
    -   [Collator::asort](/class/collator.html#Collator::asort) — Sort
        array maintaining index association
    -   [Collator::compare](/class/collator.html#Collator::compare) —
        Compare two Unicode strings
    -   [Collator::\_\_construct](/class/collator.html#Collator::__construct)
        — Create a collator
    -   [Collator::create](/class/collator.html#Collator::create) —
        Create a collator
    -   [Collator::getAttribute](/class/collator.html#Collator::getAttribute)
        — Get collation attribute value
    -   [Collator::getErrorCode](/class/collator.html#Collator::getErrorCode)
        — Get collator's last error code
    -   [Collator::getErrorMessage](/class/collator.html#Collator::getErrorMessage)
        — Get text for collator's last error code
    -   [Collator::getLocale](/class/collator.html#Collator::getLocale)
        — Get the locale name of the collator
    -   [Collator::getSortKey](/class/collator.html#Collator::getSortKey)
        — Get sorting key for a string
    -   [Collator::getStrength](/class/collator.html#Collator::getStrength)
        — Get current collation strength
    -   [Collator::setAttribute](/class/collator.html#Collator::setAttribute)
        — Set collation attribute
    -   [Collator::setStrength](/class/collator.html#Collator::setStrength)
        — Set collation strength
    -   [Collator::sortWithSortKeys](/class/collator.html#Collator::sortWithSortKeys)
        — Sort array using specified collator and sort keys
    -   [Collator::sort](/class/collator.html#Collator::sort) — Sort
        array using specified collator
-   [NumberFormatter](/class/numberformatter.html) — The NumberFormatter
    class
    -   [NumberFormatter::create](/class/numberformatter.html#NumberFormatter::create)
        — Create a number formatter
    -   [NumberFormatter::formatCurrency](/class/numberformatter.html#NumberFormatter::formatCurrency)
        — Format a currency value
    -   [NumberFormatter::format](/class/numberformatter.html#NumberFormatter::format)
        — Format a number
    -   [NumberFormatter::getAttribute](/class/numberformatter.html#NumberFormatter::getAttribute)
        — Get an attribute
    -   [NumberFormatter::getErrorCode](/class/numberformatter.html#NumberFormatter::getErrorCode)
        — Get formatter's last error code
    -   [NumberFormatter::getErrorMessage](/class/numberformatter.html#NumberFormatter::getErrorMessage)
        — Get formatter's last error message
    -   [NumberFormatter::getLocale](/class/numberformatter.html#NumberFormatter::getLocale)
        — Get formatter locale
    -   [NumberFormatter::getPattern](/class/numberformatter.html#NumberFormatter::getPattern)
        — Get formatter pattern
    -   [NumberFormatter::getSymbol](/class/numberformatter.html#NumberFormatter::getSymbol)
        — Get a symbol value
    -   [NumberFormatter::getTextAttribute](/class/numberformatter.html#NumberFormatter::getTextAttribute)
        — Get a text attribute
    -   [NumberFormatter::parseCurrency](/class/numberformatter.html#NumberFormatter::parseCurrency)
        — Parse a currency number
    -   [NumberFormatter::parse](/class/numberformatter.html#NumberFormatter::parse)
        — Parse a number
    -   [NumberFormatter::setAttribute](/class/numberformatter.html#NumberFormatter::setAttribute)
        — Set an attribute
    -   [NumberFormatter::setPattern](/class/numberformatter.html#NumberFormatter::setPattern)
        — Set formatter pattern
    -   [NumberFormatter::setSymbol](/class/numberformatter.html#NumberFormatter::setSymbol)
        — Set a symbol value
    -   [NumberFormatter::setTextAttribute](/class/numberformatter.html#NumberFormatter::setTextAttribute)
        — Set a text attribute
-   [Locale](/class/locale.html) — The Locale class
    -   [Locale::acceptFromHttp](/class/locale.html#Locale::acceptFromHttp)
        — Tries to find out best available locale based on HTTP
        "Accept-Language" header
    -   [Locale::canonicalize](/class/locale.html#Locale::canonicalize)
        — Canonicalize the locale string
    -   [Locale::composeLocale](/class/locale.html#Locale::composeLocale)
        — Returns a correctly ordered and delimited locale ID
    -   [Locale::filterMatches](/class/locale.html#Locale::filterMatches)
        — Checks if a language tag filter matches with locale
    -   [Locale::getAllVariants](/class/locale.html#Locale::getAllVariants)
        — Gets the variants for the input locale
    -   [Locale::getDefault](/class/locale.html#Locale::getDefault) —
        Gets the default locale value from the INTL global
        'default\_locale'
    -   [Locale::getDisplayLanguage](/class/locale.html#Locale::getDisplayLanguage)
        — Returns an appropriately localized display name for language
        of the inputlocale
    -   [Locale::getDisplayName](/class/locale.html#Locale::getDisplayName)
        — Returns an appropriately localized display name for the input
        locale
    -   [Locale::getDisplayRegion](/class/locale.html#Locale::getDisplayRegion)
        — Returns an appropriately localized display name for region of
        the input locale
    -   [Locale::getDisplayScript](/class/locale.html#Locale::getDisplayScript)
        — Returns an appropriately localized display name for script of
        the input locale
    -   [Locale::getDisplayVariant](/class/locale.html#Locale::getDisplayVariant)
        — Returns an appropriately localized display name for variants
        of the input locale
    -   [Locale::getKeywords](/class/locale.html#Locale::getKeywords) —
        Gets the keywords for the input locale
    -   [Locale::getPrimaryLanguage](/class/locale.html#Locale::getPrimaryLanguage)
        — Gets the primary language for the input locale
    -   [Locale::getRegion](/class/locale.html#Locale::getRegion) — Gets
        the region for the input locale
    -   [Locale::getScript](/class/locale.html#Locale::getScript) — Gets
        the script for the input locale
    -   [Locale::lookup](/class/locale.html#Locale::lookup) — Searches
        the language tag list for the best match to the language
    -   [Locale::parseLocale](/class/locale.html#Locale::parseLocale) —
        Returns a key-value array of locale ID subtag elements
    -   [Locale::setDefault](/class/locale.html#Locale::setDefault) —
        Sets the default runtime locale
-   [Normalizer](/class/normalizer.html) — The Normalizer class
    -   [Normalizer::getRawDecomposition](/class/normalizer.html#Normalizer::getRawDecomposition)
        — Gets the Decomposition\_Mapping property for the given UTF-8
        encoded code point
    -   [Normalizer::isNormalized](/class/normalizer.html#Normalizer::isNormalized)
        — Checks if the provided string is already in the specified
        normalization form
    -   [Normalizer::normalize](/class/normalizer.html#Normalizer::normalize)
        — Normalizes the input provided and returns the normalized
        string
-   [MessageFormatter](/class/messageformatter.html) — The
    MessageFormatter class
    -   [MessageFormatter::create](/class/messageformatter.html#MessageFormatter::create)
        — Constructs a new Message Formatter
    -   [MessageFormatter::formatMessage](/class/messageformatter.html#MessageFormatter::formatMessage)
        — Quick format message
    -   [MessageFormatter::format](/class/messageformatter.html#MessageFormatter::format)
        — Format the message
    -   [MessageFormatter::getErrorCode](/class/messageformatter.html#MessageFormatter::getErrorCode)
        — Get the error code from last operation
    -   [MessageFormatter::getErrorMessage](/class/messageformatter.html#MessageFormatter::getErrorMessage)
        — Get the error text from the last operation
    -   [MessageFormatter::getLocale](/class/messageformatter.html#MessageFormatter::getLocale)
        — Get the locale for which the formatter was created
    -   [MessageFormatter::getPattern](/class/messageformatter.html#MessageFormatter::getPattern)
        — Get the pattern used by the formatter
    -   [MessageFormatter::parseMessage](/class/messageformatter.html#MessageFormatter::parseMessage)
        — Quick parse input string
    -   [MessageFormatter::parse](/class/messageformatter.html#MessageFormatter::parse)
        — Parse input string according to pattern
    -   [MessageFormatter::setPattern](/class/messageformatter.html#MessageFormatter::setPattern)
        — Set the pattern used by the formatter
-   [IntlCalendar](/class/intlcalendar.html) — The IntlCalendar class
    -   [IntlCalendar::add](/class/intlcalendar.html#IntlCalendar::add)
        — Add a (signed) amount of time to a field
    -   [IntlCalendar::after](/class/intlcalendar.html#IntlCalendar::after)
        — Whether this objectʼs time is after that of the passed object
    -   [IntlCalendar::before](/class/intlcalendar.html#IntlCalendar::before)
        — Whether this objectʼs time is before that of the passed object
    -   [IntlCalendar::clear](/class/intlcalendar.html#IntlCalendar::clear)
        — Clear a field or all fields
    -   [IntlCalendar::\_\_construct](/class/intlcalendar.html#IntlCalendar::__construct)
        — Private constructor for disallowing instantiation
    -   [IntlCalendar::createInstance](/class/intlcalendar.html#IntlCalendar::createInstance)
        — Create a new IntlCalendar
    -   [IntlCalendar::equals](/class/intlcalendar.html#IntlCalendar::equals)
        — Compare time of two IntlCalendar objects for equality
    -   [IntlCalendar::fieldDifference](/class/intlcalendar.html#IntlCalendar::fieldDifference)
        — Calculate difference between given time and this objectʼs time
    -   [IntlCalendar::fromDateTime](/class/intlcalendar.html#IntlCalendar::fromDateTime)
        — Create an IntlCalendar from a DateTime object or string
    -   [IntlCalendar::get](/class/intlcalendar.html#IntlCalendar::get)
        — Get the value for a field
    -   [IntlCalendar::getActualMaximum](/class/intlcalendar.html#IntlCalendar::getActualMaximum)
        — The maximum value for a field, considering the objectʼs
        current time
    -   [IntlCalendar::getActualMinimum](/class/intlcalendar.html#IntlCalendar::getActualMinimum)
        — The minimum value for a field, considering the objectʼs
        current time
    -   [IntlCalendar::getAvailableLocales](/class/intlcalendar.html#IntlCalendar::getAvailableLocales)
        — Get array of locales for which there is data
    -   [IntlCalendar::getDayOfWeekType](/class/intlcalendar.html#IntlCalendar::getDayOfWeekType)
        — Tell whether a day is a weekday, weekend or a day that has a
        transition between the two
    -   [IntlCalendar::getErrorCode](/class/intlcalendar.html#IntlCalendar::getErrorCode)
        — Get last error code on the object
    -   [IntlCalendar::getErrorMessage](/class/intlcalendar.html#IntlCalendar::getErrorMessage)
        — Get last error message on the object
    -   [IntlCalendar::getFirstDayOfWeek](/class/intlcalendar.html#IntlCalendar::getFirstDayOfWeek)
        — Get the first day of the week for the calendarʼs locale
    -   [IntlCalendar::getGreatestMinimum](/class/intlcalendar.html#IntlCalendar::getGreatestMinimum)
        — Get the largest local minimum value for a field
    -   [IntlCalendar::getKeywordValuesForLocale](/class/intlcalendar.html#IntlCalendar::getKeywordValuesForLocale)
        — Get set of locale keyword values
    -   [IntlCalendar::getLeastMaximum](/class/intlcalendar.html#IntlCalendar::getLeastMaximum)
        — Get the smallest local maximum for a field
    -   [IntlCalendar::getLocale](/class/intlcalendar.html#IntlCalendar::getLocale)
        — Get the locale associated with the object
    -   [IntlCalendar::getMaximum](/class/intlcalendar.html#IntlCalendar::getMaximum)
        — Get the global maximum value for a field
    -   [IntlCalendar::getMinimalDaysInFirstWeek](/class/intlcalendar.html#IntlCalendar::getMinimalDaysInFirstWeek)
        — Get minimal number of days the first week in a year or month
        can have
    -   [IntlCalendar::getMinimum](/class/intlcalendar.html#IntlCalendar::getMinimum)
        — Get the global minimum value for a field
    -   [IntlCalendar::getNow](/class/intlcalendar.html#IntlCalendar::getNow)
        — Get number representing the current time
    -   [IntlCalendar::getRepeatedWallTimeOption](/class/intlcalendar.html#IntlCalendar::getRepeatedWallTimeOption)
        — Get behavior for handling repeating wall time
    -   [IntlCalendar::getSkippedWallTimeOption](/class/intlcalendar.html#IntlCalendar::getSkippedWallTimeOption)
        — Get behavior for handling skipped wall time
    -   [IntlCalendar::getTime](/class/intlcalendar.html#IntlCalendar::getTime)
        — Get time currently represented by the object
    -   [IntlCalendar::getTimeZone](/class/intlcalendar.html#IntlCalendar::getTimeZone)
        — Get the objectʼs timezone
    -   [IntlCalendar::getType](/class/intlcalendar.html#IntlCalendar::getType)
        — Get the calendar type
    -   [IntlCalendar::getWeekendTransition](/class/intlcalendar.html#IntlCalendar::getWeekendTransition)
        — Get time of the day at which weekend begins or ends
    -   [IntlCalendar::inDaylightTime](/class/intlcalendar.html#IntlCalendar::inDaylightTime)
        — Whether the objectʼs time is in Daylight Savings Time
    -   [IntlCalendar::isEquivalentTo](/class/intlcalendar.html#IntlCalendar::isEquivalentTo)
        — Whether another calendar is equal but for a different time
    -   [IntlCalendar::isLenient](/class/intlcalendar.html#IntlCalendar::isLenient)
        — Whether date/time interpretation is in lenient mode
    -   [IntlCalendar::isSet](/class/intlcalendar.html#IntlCalendar::isSet)
        — Whether a field is set
    -   [IntlCalendar::isWeekend](/class/intlcalendar.html#IntlCalendar::isWeekend)
        — Whether a certain date/time is in the weekend
    -   [IntlCalendar::roll](/class/intlcalendar.html#IntlCalendar::roll)
        — Add value to field without carrying into more significant
        fields
    -   [IntlCalendar::set](/class/intlcalendar.html#IntlCalendar::set)
        — Set a time field or several common fields at once
    -   [IntlCalendar::setFirstDayOfWeek](/class/intlcalendar.html#IntlCalendar::setFirstDayOfWeek)
        — Set the day on which the week is deemed to start
    -   [IntlCalendar::setLenient](/class/intlcalendar.html#IntlCalendar::setLenient)
        — Set whether date/time interpretation is to be lenient
    -   [IntlCalendar::setMinimalDaysInFirstWeek](/class/intlcalendar.html#IntlCalendar::setMinimalDaysInFirstWeek)
        — Set minimal number of days the first week in a year or month
        can have
    -   [IntlCalendar::setRepeatedWallTimeOption](/class/intlcalendar.html#IntlCalendar::setRepeatedWallTimeOption)
        — Set behavior for handling repeating wall times at negative
        timezone offset transitions
    -   [IntlCalendar::setSkippedWallTimeOption](/class/intlcalendar.html#IntlCalendar::setSkippedWallTimeOption)
        — Set behavior for handling skipped wall times at positive
        timezone offset transitions
    -   [IntlCalendar::setTime](/class/intlcalendar.html#IntlCalendar::setTime)
        — Set the calendar time in milliseconds since the epoch
    -   [IntlCalendar::setTimeZone](/class/intlcalendar.html#IntlCalendar::setTimeZone)
        — Set the timezone used by this calendar
    -   [IntlCalendar::toDateTime](/class/intlcalendar.html#IntlCalendar::toDateTime)
        — Convert an IntlCalendar into a DateTime object
-   [IntlGregorianCalendar](/class/intlgregoriancalendar.html) — The
    IntlGregorianCalendar class
    -   [IntlGregorianCalendar::\_\_construct](/class/intlgregoriancalendar.html#IntlGregorianCalendar::__construct)
        — Create the Gregorian Calendar class
    -   [IntlGregorianCalendar::getGregorianChange](/class/intlgregoriancalendar.html#IntlGregorianCalendar::getGregorianChange)
        — Get the Gregorian Calendar change date
    -   [IntlGregorianCalendar::isLeapYear](/class/intlgregoriancalendar.html#IntlGregorianCalendar::isLeapYear)
        — Determine if the given year is a leap year
    -   [IntlGregorianCalendar::setGregorianChange](/class/intlgregoriancalendar.html#IntlGregorianCalendar::setGregorianChange)
        — Set the Gregorian Calendar the change date
-   [IntlTimeZone](/class/intltimezone.html) — The IntlTimeZone class
    -   [IntlTimeZone::countEquivalentIDs](/class/intltimezone.html#IntlTimeZone::countEquivalentIDs)
        — Get the number of IDs in the equivalency group that includes
        the given ID
    -   [IntlTimeZone::createDefault](/class/intltimezone.html#IntlTimeZone::createDefault)
        — Create a new copy of the default timezone for this host
    -   [IntlTimeZone::createEnumeration](/class/intltimezone.html#IntlTimeZone::createEnumeration)
        — Get an enumeration over time zone IDs associated with the
        given country or offset
    -   [IntlTimeZone::createTimeZone](/class/intltimezone.html#IntlTimeZone::createTimeZone)
        — Create a timezone object for the given ID
    -   [IntlTimeZone::createTimeZoneIDEnumeration](/class/intltimezone.html#IntlTimeZone::createTimeZoneIDEnumeration)
        — Get an enumeration over system time zone IDs with the given
        filter conditions
    -   [IntlTimeZone::fromDateTimeZone](/class/intltimezone.html#IntlTimeZone::fromDateTimeZone)
        — Create a timezone object from DateTimeZone
    -   [IntlTimeZone::getCanonicalID](/class/intltimezone.html#IntlTimeZone::getCanonicalID)
        — Get the canonical system timezone ID or the normalized custom
        time zone ID for the given time zone ID
    -   [IntlTimeZone::getDisplayName](/class/intltimezone.html#IntlTimeZone::getDisplayName)
        — Get a name of this time zone suitable for presentation to the
        user
    -   [IntlTimeZone::getDSTSavings](/class/intltimezone.html#IntlTimeZone::getDSTSavings)
        — Get the amount of time to be added to local standard time to
        get local wall clock time
    -   [IntlTimeZone::getEquivalentID](/class/intltimezone.html#IntlTimeZone::getEquivalentID)
        — Get an ID in the equivalency group that includes the given ID
    -   [IntlTimeZone::getErrorCode](/class/intltimezone.html#IntlTimeZone::getErrorCode)
        — Get last error code on the object
    -   [IntlTimeZone::getErrorMessage](/class/intltimezone.html#IntlTimeZone::getErrorMessage)
        — Get last error message on the object
    -   [IntlTimeZone::getGMT](/class/intltimezone.html#IntlTimeZone::getGMT)
        — Create GMT (UTC) timezone
    -   [IntlTimeZone::getID](/class/intltimezone.html#IntlTimeZone::getID)
        — Get timezone ID
    -   [IntlTimeZone::getIDForWindowsID](/class/intltimezone.html#IntlTimeZone::getIDForWindowsID)
        — Translate a Windows timezone into a system timezone
    -   [IntlTimeZone::getOffset](/class/intltimezone.html#IntlTimeZone::getOffset)
        — Get the time zone raw and GMT offset for the given moment in
        time
    -   [IntlTimeZone::getRawOffset](/class/intltimezone.html#IntlTimeZone::getRawOffset)
        — Get the raw GMT offset (before taking daylight savings time
        into account
    -   [IntlTimeZone::getRegion](/class/intltimezone.html#IntlTimeZone::getRegion)
        — Get the region code associated with the given system time zone
        ID
    -   [IntlTimeZone::getTZDataVersion](/class/intltimezone.html#IntlTimeZone::getTZDataVersion)
        — Get the timezone data version currently used by ICU
    -   [IntlTimeZone::getUnknown](/class/intltimezone.html#IntlTimeZone::getUnknown)
        — Get the "unknown" time zone
    -   [IntlTimeZone::getWindowsID](/class/intltimezone.html#IntlTimeZone::getWindowsID)
        — Translate a system timezone into a Windows timezone
    -   [IntlTimeZone::hasSameRules](/class/intltimezone.html#IntlTimeZone::hasSameRules)
        — Check if this zone has the same rules and offset as another
        zone
    -   [IntlTimeZone::toDateTimeZone](/class/intltimezone.html#IntlTimeZone::toDateTimeZone)
        — Convert to DateTimeZone object
    -   [IntlTimeZone::useDaylightTime](/class/intltimezone.html#IntlTimeZone::useDaylightTime)
        — Check if this time zone uses daylight savings time
-   [IntlDateFormatter](/class/intldateformatter.html) — The
    IntlDateFormatter class
    -   [IntlDateFormatter::create](/class/intldateformatter.html#IntlDateFormatter::create)
        — Create a date formatter
    -   [IntlDateFormatter::format](/class/intldateformatter.html#IntlDateFormatter::format)
        — Format the date/time value as a string
    -   [IntlDateFormatter::formatObject](/class/intldateformatter.html#IntlDateFormatter::formatObject)
        — Formats an object
    -   [IntlDateFormatter::getCalendar](/class/intldateformatter.html#IntlDateFormatter::getCalendar)
        — Get the calendar type used for the IntlDateFormatter
    -   [IntlDateFormatter::getDateType](/class/intldateformatter.html#IntlDateFormatter::getDateType)
        — Get the datetype used for the IntlDateFormatter
    -   [IntlDateFormatter::getErrorCode](/class/intldateformatter.html#IntlDateFormatter::getErrorCode)
        — Get the error code from last operation
    -   [IntlDateFormatter::getErrorMessage](/class/intldateformatter.html#IntlDateFormatter::getErrorMessage)
        — Get the error text from the last operation
    -   [IntlDateFormatter::getLocale](/class/intldateformatter.html#IntlDateFormatter::getLocale)
        — Get the locale used by formatter
    -   [IntlDateFormatter::getPattern](/class/intldateformatter.html#IntlDateFormatter::getPattern)
        — Get the pattern used for the IntlDateFormatter
    -   [IntlDateFormatter::getTimeType](/class/intldateformatter.html#IntlDateFormatter::getTimeType)
        — Get the timetype used for the IntlDateFormatter
    -   [IntlDateFormatter::getTimeZoneId](/class/intldateformatter.html#IntlDateFormatter::getTimeZoneId)
        — Get the timezone-id used for the IntlDateFormatter
    -   [IntlDateFormatter::getCalendarObject](/class/intldateformatter.html#IntlDateFormatter::getCalendarObject)
        — Get copy of formatterʼs calendar object
    -   [IntlDateFormatter::getTimeZone](/class/intldateformatter.html#IntlDateFormatter::getTimeZone)
        — Get formatterʼs timezone
    -   [IntlDateFormatter::isLenient](/class/intldateformatter.html#IntlDateFormatter::isLenient)
        — Get the lenient used for the IntlDateFormatter
    -   [IntlDateFormatter::localtime](/class/intldateformatter.html#IntlDateFormatter::localtime)
        — Parse string to a field-based time value
    -   [IntlDateFormatter::parse](/class/intldateformatter.html#IntlDateFormatter::parse)
        — Parse string to a timestamp value
    -   [IntlDateFormatter::setCalendar](/class/intldateformatter.html#IntlDateFormatter::setCalendar)
        — Sets the calendar type used by the formatter
    -   [IntlDateFormatter::setLenient](/class/intldateformatter.html#IntlDateFormatter::setLenient)
        — Set the leniency of the parser
    -   [IntlDateFormatter::setPattern](/class/intldateformatter.html#IntlDateFormatter::setPattern)
        — Set the pattern used for the IntlDateFormatter
    -   [IntlDateFormatter::setTimeZoneId](/class/intldateformatter.html#IntlDateFormatter::setTimeZoneId)
        — Sets the time zone to use
    -   [IntlDateFormatter::setTimeZone](/class/intldateformatter.html#IntlDateFormatter::setTimeZone)
        — Sets formatterʼs timezone
-   [ResourceBundle](/class/resourcebundle.html) — The ResourceBundle
    class
    -   [ResourceBundle::count](/class/resourcebundle.html#ResourceBundle::count)
        — Get number of elements in the bundle
    -   [ResourceBundle::create](/class/resourcebundle.html#ResourceBundle::create)
        — Create a resource bundle
    -   [ResourceBundle::getErrorCode](/class/resourcebundle.html#ResourceBundle::getErrorCode)
        — Get bundle's last error code
    -   [ResourceBundle::getErrorMessage](/class/resourcebundle.html#ResourceBundle::getErrorMessage)
        — Get bundle's last error message
    -   [ResourceBundle::get](/class/resourcebundle.html#ResourceBundle::get)
        — Get data from the bundle
    -   [ResourceBundle::getLocales](/class/resourcebundle.html#ResourceBundle::getLocales)
        — Get supported locales
-   [Spoofchecker](/class/spoofchecker.html) — The Spoofchecker class
    -   [Spoofchecker::areConfusable](/class/spoofchecker.html#Spoofchecker::areConfusable)
        — Checks if given strings can be confused
    -   [Spoofchecker::\_\_construct](/class/spoofchecker.html#Spoofchecker::__construct)
        — Constructor
    -   [Spoofchecker::isSuspicious](/class/spoofchecker.html#Spoofchecker::isSuspicious)
        — Checks if a given text contains any suspicious characters
    -   [Spoofchecker::setAllowedLocales](/class/spoofchecker.html#Spoofchecker::setAllowedLocales)
        — Locales to use when running checks
    -   [Spoofchecker::setChecks](/class/spoofchecker.html#Spoofchecker::setChecks)
        — Set the checks to run
-   [Transliterator](/class/transliterator.html) — The Transliterator
    class
    -   [Transliterator::\_\_construct](/class/transliterator.html#Transliterator::__construct)
        — Private constructor to deny instantiation
    -   [Transliterator::create](/class/transliterator.html#Transliterator::create)
        — Create a transliterator
    -   [Transliterator::createFromRules](/class/transliterator.html#Transliterator::createFromRules)
        — Create transliterator from rules
    -   [Transliterator::createInverse](/class/transliterator.html#Transliterator::createInverse)
        — Create an inverse transliterator
    -   [Transliterator::getErrorCode](/class/transliterator.html#Transliterator::getErrorCode)
        — Get last error code
    -   [Transliterator::getErrorMessage](/class/transliterator.html#Transliterator::getErrorMessage)
        — Get last error message
    -   [Transliterator::listIDs](/class/transliterator.html#Transliterator::listIDs)
        — Get transliterator IDs
    -   [Transliterator::transliterate](/class/transliterator.html#Transliterator::transliterate)
        — Transliterate a string
-   [IntlBreakIterator](/class/intlbreakiterator.html) — The
    IntlBreakIterator class
    -   [IntlBreakIterator::\_\_construct](/class/intlbreakiterator.html#IntlBreakIterator::__construct)
        — Private constructor for disallowing instantiation
    -   [IntlBreakIterator::createCharacterInstance](/class/intlbreakiterator.html#IntlBreakIterator::createCharacterInstance)
        — Create break iterator for boundaries of combining character
        sequences
    -   [IntlBreakIterator::createCodePointInstance](/class/intlbreakiterator.html#IntlBreakIterator::createCodePointInstance)
        — Create break iterator for boundaries of code points
    -   [IntlBreakIterator::createLineInstance](/class/intlbreakiterator.html#IntlBreakIterator::createLineInstance)
        — Create break iterator for logically possible line breaks
    -   [IntlBreakIterator::createSentenceInstance](/class/intlbreakiterator.html#IntlBreakIterator::createSentenceInstance)
        — Create break iterator for sentence breaks
    -   [IntlBreakIterator::createTitleInstance](/class/intlbreakiterator.html#IntlBreakIterator::createTitleInstance)
        — Create break iterator for title-casing breaks
    -   [IntlBreakIterator::createWordInstance](/class/intlbreakiterator.html#IntlBreakIterator::createWordInstance)
        — Create break iterator for word breaks
    -   [IntlBreakIterator::current](/class/intlbreakiterator.html#IntlBreakIterator::current)
        — Get index of current position
    -   [IntlBreakIterator::first](/class/intlbreakiterator.html#IntlBreakIterator::first)
        — Set position to the first character in the text
    -   [IntlBreakIterator::following](/class/intlbreakiterator.html#IntlBreakIterator::following)
        — Advance the iterator to the first boundary following specified
        offset
    -   [IntlBreakIterator::getErrorCode](/class/intlbreakiterator.html#IntlBreakIterator::getErrorCode)
        — Get last error code on the object
    -   [IntlBreakIterator::getErrorMessage](/class/intlbreakiterator.html#IntlBreakIterator::getErrorMessage)
        — Get last error message on the object
    -   [IntlBreakIterator::getLocale](/class/intlbreakiterator.html#IntlBreakIterator::getLocale)
        — Get the locale associated with the object
    -   [IntlBreakIterator::getPartsIterator](/class/intlbreakiterator.html#IntlBreakIterator::getPartsIterator)
        — Create iterator for navigating fragments between boundaries
    -   [IntlBreakIterator::getText](/class/intlbreakiterator.html#IntlBreakIterator::getText)
        — Get the text being scanned
    -   [IntlBreakIterator::isBoundary](/class/intlbreakiterator.html#IntlBreakIterator::isBoundary)
        — Tell whether an offset is a boundaryʼs offset
    -   [IntlBreakIterator::last](/class/intlbreakiterator.html#IntlBreakIterator::last)
        — Set the iterator position to index beyond the last character
    -   [IntlBreakIterator::next](/class/intlbreakiterator.html#IntlBreakIterator::next)
        — Advance the iterator the next boundary
    -   [IntlBreakIterator::preceding](/class/intlbreakiterator.html#IntlBreakIterator::preceding)
        — Set the iterator position to the first boundary before an
        offset
    -   [IntlBreakIterator::previous](/class/intlbreakiterator.html#IntlBreakIterator::previous)
        — Set the iterator position to the boundary immediately before
        the current
    -   [IntlBreakIterator::setText](/class/intlbreakiterator.html#IntlBreakIterator::setText)
        — Set the text being scanned
-   [IntlRuleBasedBreakIterator](/class/intlrulebasedbreakiterator.html)
    — The IntlRuleBasedBreakIterator class
    -   [IntlRuleBasedBreakIterator::\_\_construct](/class/intlrulebasedbreakiterator.html#IntlRuleBasedBreakIterator::__construct)
        — Create iterator from ruleset
    -   [IntlRuleBasedBreakIterator::getBinaryRules](/class/intlrulebasedbreakiterator.html#IntlRuleBasedBreakIterator::getBinaryRules)
        — Get the binary form of compiled rules
    -   [IntlRuleBasedBreakIterator::getRules](/class/intlrulebasedbreakiterator.html#IntlRuleBasedBreakIterator::getRules)
        — Get the rule set used to create this object
    -   [IntlRuleBasedBreakIterator::getRuleStatus](/class/intlrulebasedbreakiterator.html#IntlRuleBasedBreakIterator::getRuleStatus)
        — Get the largest status value from the break rules that
        determined the current break position
    -   [IntlRuleBasedBreakIterator::getRuleStatusVec](/class/intlrulebasedbreakiterator.html#IntlRuleBasedBreakIterator::getRuleStatusVec)
        — Get the status values from the break rules that determined the
        current break position
-   [IntlCodePointBreakIterator](/class/intlcodepointbreakiterator.html)
    — The IntlCodePointBreakIterator class
    -   [IntlCodePointBreakIterator::getLastCodePoint](/class/intlcodepointbreakiterator.html#IntlCodePointBreakIterator::getLastCodePoint)
        — Get last code point passed over after advancing or receding
        the iterator
-   [IntlPartsIterator](/class/intlpartsiterator.html) — The
    IntlPartsIterator class
    -   [IntlPartsIterator::getBreakIterator](/class/intlpartsiterator.html#IntlPartsIterator::getBreakIterator)
        — Get IntlBreakIterator backing this parts iterator
-   [UConverter](/class/uconverter.html) — The UConverter class
    -   [UConverter::\_\_construct](/class/uconverter.html#UConverter::__construct)
        — Create UConverter object
    -   [UConverter::convert](/class/uconverter.html#UConverter::convert)
        — Convert string from one charset to another
    -   [UConverter::fromUCallback](/class/uconverter.html#UConverter::fromUCallback)
        — Default "from" callback function
    -   [UConverter::getAliases](/class/uconverter.html#UConverter::getAliases)
        — Get the aliases of the given name
    -   [UConverter::getAvailable](/class/uconverter.html#UConverter::getAvailable)
        — Get the available canonical converter names
    -   [UConverter::getDestinationEncoding](/class/uconverter.html#UConverter::getDestinationEncoding)
        — Get the destination encoding
    -   [UConverter::getDestinationType](/class/uconverter.html#UConverter::getDestinationType)
        — Get the destination converter type
    -   [UConverter::getErrorCode](/class/uconverter.html#UConverter::getErrorCode)
        — Get last error code on the object
    -   [UConverter::getErrorMessage](/class/uconverter.html#UConverter::getErrorMessage)
        — Get last error message on the object
    -   [UConverter::getSourceEncoding](/class/uconverter.html#UConverter::getSourceEncoding)
        — Get the source encoding
    -   [UConverter::getSourceType](/class/uconverter.html#UConverter::getSourceType)
        — Get the source converter type
    -   [UConverter::getStandards](/class/uconverter.html#UConverter::getStandards)
        — Get standards associated to converter names
    -   [UConverter::getSubstChars](/class/uconverter.html#UConverter::getSubstChars)
        — Get substitution chars
    -   [UConverter::reasonText](/class/uconverter.html#UConverter::reasonText)
        — Get string representation of the callback reason
    -   [UConverter::setDestinationEncoding](/class/uconverter.html#UConverter::setDestinationEncoding)
        — Set the destination encoding
    -   [UConverter::setSourceEncoding](/class/uconverter.html#UConverter::setSourceEncoding)
        — Set the source encoding
    -   [UConverter::setSubstChars](/class/uconverter.html#UConverter::setSubstChars)
        — Set the substitution chars
    -   [UConverter::toUCallback](/class/uconverter.html#UConverter::toUCallback)
        — Default "to" callback function
    -   [UConverter::transcode](/class/uconverter.html#UConverter::transcode)
        — Convert string from one charset to another
-   [Grapheme 函数](/ref/intl/grapheme.html)
    -   [grapheme\_extract](/ref/intl/grapheme.html#grapheme_extract) —
        Function to extract a sequence of default grapheme clusters from
        a text buffer, which must be encoded in UTF-8
    -   [grapheme\_stripos](/ref/intl/grapheme.html#grapheme_stripos) —
        Find position (in grapheme units) of first occurrence of a
        case-insensitive string
    -   [grapheme\_stristr](/ref/intl/grapheme.html#grapheme_stristr) —
        Returns part of haystack string from the first occurrence of
        case-insensitive needle to the end of haystack
    -   [grapheme\_strlen](/ref/intl/grapheme.html#grapheme_strlen) —
        Get string length in grapheme units
    -   [grapheme\_strpos](/ref/intl/grapheme.html#grapheme_strpos) —
        Find position (in grapheme units) of first occurrence of a
        string
    -   [grapheme\_strripos](/ref/intl/grapheme.html#grapheme_strripos)
        — Find position (in grapheme units) of last occurrence of a
        case-insensitive string
    -   [grapheme\_strrpos](/ref/intl/grapheme.html#grapheme_strrpos) —
        Find position (in grapheme units) of last occurrence of a string
    -   [grapheme\_strstr](/ref/intl/grapheme.html#grapheme_strstr) —
        Returns part of haystack string from the first occurrence of
        needle to the end of haystack
    -   [grapheme\_substr](/ref/intl/grapheme.html#grapheme_substr) —
        Return part of a string
-   [IDN 函数](/ref/intl/idn.html)
    -   [idn\_to\_ascii](/ref/intl/idn.html#idn_to_ascii) — Convert
        domain name to IDNA ASCII form
    -   [idn\_to\_utf8](/ref/intl/idn.html#idn_to_utf8) — Convert domain
        name from IDNA ASCII to Unicode
-   [IntlChar](/class/intlchar.html) — IntlChar
    -   [IntlChar::charAge](/class/intlchar.html#IntlChar::charAge) —
        Get the "age" of the code point
    -   [IntlChar::charDigitValue](/class/intlchar.html#IntlChar::charDigitValue)
        — Get the decimal digit value of a decimal digit character
    -   [IntlChar::charDirection](/class/intlchar.html#IntlChar::charDirection)
        — Get bidirectional category value for a code point
    -   [IntlChar::charFromName](/class/intlchar.html#IntlChar::charFromName)
        — Find Unicode character by name and return its code point value
    -   [IntlChar::charMirror](/class/intlchar.html#IntlChar::charMirror)
        — Get the "mirror-image" character for a code point
    -   [IntlChar::charName](/class/intlchar.html#IntlChar::charName) —
        Retrieve the name of a Unicode character
    -   [IntlChar::charType](/class/intlchar.html#IntlChar::charType) —
        Get the general category value for a code point
    -   [IntlChar::chr](/class/intlchar.html#IntlChar::chr) — Return
        Unicode character by code point value
    -   [IntlChar::digit](/class/intlchar.html#IntlChar::digit) — Get
        the decimal digit value of a code point for a given radix
    -   [IntlChar::enumCharNames](/class/intlchar.html#IntlChar::enumCharNames)
        — Enumerate all assigned Unicode characters within a range
    -   [IntlChar::enumCharTypes](/class/intlchar.html#IntlChar::enumCharTypes)
        — Enumerate all code points with their Unicode general
        categories
    -   [IntlChar::foldCase](/class/intlchar.html#IntlChar::foldCase) —
        Perform case folding on a code point
    -   [IntlChar::forDigit](/class/intlchar.html#IntlChar::forDigit) —
        Get character representation for a given digit and radix
    -   [IntlChar::getBidiPairedBracket](/class/intlchar.html#IntlChar::getBidiPairedBracket)
        — Get the paired bracket character for a code point
    -   [IntlChar::getBlockCode](/class/intlchar.html#IntlChar::getBlockCode)
        — Get the Unicode allocation block containing a code point
    -   [IntlChar::getCombiningClass](/class/intlchar.html#IntlChar::getCombiningClass)
        — Get the combining class of a code point
    -   [IntlChar::getFC\_NFKC\_Closure](/class/intlchar.html#IntlChar::getFC_NFKC_Closure)
        — Get the FC\_NFKC\_Closure property for a code point
    -   [IntlChar::getIntPropertyMaxValue](/class/intlchar.html#IntlChar::getIntPropertyMaxValue)
        — Get the max value for a Unicode property
    -   [IntlChar::getIntPropertyMinValue](/class/intlchar.html#IntlChar::getIntPropertyMinValue)
        — Get the min value for a Unicode property
    -   [IntlChar::getIntPropertyValue](/class/intlchar.html#IntlChar::getIntPropertyValue)
        — Get the value for a Unicode property for a code point
    -   [IntlChar::getNumericValue](/class/intlchar.html#IntlChar::getNumericValue)
        — Get the numeric value for a Unicode code point
    -   [IntlChar::getPropertyEnum](/class/intlchar.html#IntlChar::getPropertyEnum)
        — Get the property constant value for a given property name
    -   [IntlChar::getPropertyName](/class/intlchar.html#IntlChar::getPropertyName)
        — Get the Unicode name for a property
    -   [IntlChar::getPropertyValueEnum](/class/intlchar.html#IntlChar::getPropertyValueEnum)
        — Get the property value for a given value name
    -   [IntlChar::getPropertyValueName](/class/intlchar.html#IntlChar::getPropertyValueName)
        — Get the Unicode name for a property value
    -   [IntlChar::getUnicodeVersion](/class/intlchar.html#IntlChar::getUnicodeVersion)
        — Get the Unicode version
    -   [IntlChar::hasBinaryProperty](/class/intlchar.html#IntlChar::hasBinaryProperty)
        — Check a binary Unicode property for a code point
    -   [IntlChar::isalnum](/class/intlchar.html#IntlChar::isalnum) —
        Check if code point is an alphanumeric character
    -   [IntlChar::isalpha](/class/intlchar.html#IntlChar::isalpha) —
        Check if code point is a letter character
    -   [IntlChar::isbase](/class/intlchar.html#IntlChar::isbase) —
        Check if code point is a base character
    -   [IntlChar::isblank](/class/intlchar.html#IntlChar::isblank) —
        Check if code point is a "blank" or "horizontal space" character
    -   [IntlChar::iscntrl](/class/intlchar.html#IntlChar::iscntrl) —
        Check if code point is a control character
    -   [IntlChar::isdefined](/class/intlchar.html#IntlChar::isdefined)
        — Check whether the code point is defined
    -   [IntlChar::isdigit](/class/intlchar.html#IntlChar::isdigit) —
        Check if code point is a digit character
    -   [IntlChar::isgraph](/class/intlchar.html#IntlChar::isgraph) —
        Check if code point is a graphic character
    -   [IntlChar::isIDIgnorable](/class/intlchar.html#IntlChar::isIDIgnorable)
        — Check if code point is an ignorable character
    -   [IntlChar::isIDPart](/class/intlchar.html#IntlChar::isIDPart) —
        Check if code point is permissible in an identifier
    -   [IntlChar::isIDStart](/class/intlchar.html#IntlChar::isIDStart)
        — Check if code point is permissible as the first character in
        an identifier
    -   [IntlChar::isISOControl](/class/intlchar.html#IntlChar::isISOControl)
        — Check if code point is an ISO control code
    -   [IntlChar::isJavaIDPart](/class/intlchar.html#IntlChar::isJavaIDPart)
        — Check if code point is permissible in a Java identifier
    -   [IntlChar::isJavaIDStart](/class/intlchar.html#IntlChar::isJavaIDStart)
        — Check if code point is permissible as the first character in a
        Java identifier
    -   [IntlChar::isJavaSpaceChar](/class/intlchar.html#IntlChar::isJavaSpaceChar)
        — Check if code point is a space character according to Java
    -   [IntlChar::islower](/class/intlchar.html#IntlChar::islower) —
        Check if code point is a lowercase letter
    -   [IntlChar::isMirrored](/class/intlchar.html#IntlChar::isMirrored)
        — Check if code point has the Bidi\_Mirrored property
    -   [IntlChar::isprint](/class/intlchar.html#IntlChar::isprint) —
        Check if code point is a printable character
    -   [IntlChar::ispunct](/class/intlchar.html#IntlChar::ispunct) —
        Check if code point is punctuation character
    -   [IntlChar::isspace](/class/intlchar.html#IntlChar::isspace) —
        Check if code point is a space character
    -   [IntlChar::istitle](/class/intlchar.html#IntlChar::istitle) —
        Check if code point is a titlecase letter
    -   [IntlChar::isUAlphabetic](/class/intlchar.html#IntlChar::isUAlphabetic)
        — Check if code point has the Alphabetic Unicode property
    -   [IntlChar::isULowercase](/class/intlchar.html#IntlChar::isULowercase)
        — Check if code point has the Lowercase Unicode property
    -   [IntlChar::isupper](/class/intlchar.html#IntlChar::isupper) —
        Check if code point has the general category "Lu" (uppercase
        letter)
    -   [IntlChar::isUUppercase](/class/intlchar.html#IntlChar::isUUppercase)
        — Check if code point has the Uppercase Unicode property
    -   [IntlChar::isUWhiteSpace](/class/intlchar.html#IntlChar::isUWhiteSpace)
        — Check if code point has the White\_Space Unicode property
    -   [IntlChar::isWhitespace](/class/intlchar.html#IntlChar::isWhitespace)
        — Check if code point is a whitespace character according to ICU
    -   [IntlChar::isxdigit](/class/intlchar.html#IntlChar::isxdigit) —
        Check if code point is a hexadecimal digit
    -   [IntlChar::ord](/class/intlchar.html#IntlChar::ord) — Return
        Unicode code point value of character
    -   [IntlChar::tolower](/class/intlchar.html#IntlChar::tolower) —
        Make Unicode character lowercase
    -   [IntlChar::totitle](/class/intlchar.html#IntlChar::totitle) —
        Make Unicode character titlecase
    -   [IntlChar::toupper](/class/intlchar.html#IntlChar::toupper) —
        Make Unicode character uppercase
-   [IntlException](/class/intlexception.html) — Exception class for
    intl errors
-   [IntlIterator](/class/intliterator.html) — The IntlIterator class
    -   [IntlIterator::current](/class/intliterator.html#IntlIterator::current)
        — Get the current element
    -   [IntlIterator::key](/class/intliterator.html#IntlIterator::key)
        — Get the current key
    -   [IntlIterator::next](/class/intliterator.html#IntlIterator::next)
        — Move forward to the next element
    -   [IntlIterator::rewind](/class/intliterator.html#IntlIterator::rewind)
        — Rewind the iterator to the first element
    -   [IntlIterator::valid](/class/intliterator.html#IntlIterator::valid)
        — Check if current position is valid
-   [intl 函数](/ref/intl.html)
    -   [intl\_error\_name](/ref/intl.html#intl_error_name) — Get
        symbolic name for a given error code
    -   [intl\_get\_error\_code](/ref/intl.html#intl_get_error_code) —
        Get the last error code
    -   [intl\_get\_error\_message](/ref/intl.html#intl_get_error_message)
        — Get description of the last error
    -   [intl\_is\_failure](/ref/intl.html#intl_is_failure) — Check
        whether the given error code indicates failure

简介
----

Provides string comparison capability with support for appropriate
locale-sensitive sort orderings.

类摘要
------

**Collator**

<span class="ooclass"> class **Collator** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">asort</span> ( <span class="methodparam"><span
class="type">array</span> `&$arr`</span> \[, <span
class="methodparam"><span class="type">int</span> `$sort_flag`</span> \]
)

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">compare</span> ( <span class="methodparam"><span
class="type">string</span> `$str1`</span> , <span
class="methodparam"><span class="type">string</span> `$str2`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">Collator</span> <span
class="methodname">create</span> ( <span class="methodparam"><span
class="type">string</span> `$locale`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getAttribute</span> ( <span class="methodparam"><span
class="type">int</span> `$attr`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getErrorCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getErrorMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getLocale</span> ( <span
class="methodparam"><span class="type">int</span> `$type`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getSortKey</span> ( <span
class="methodparam"><span class="type">string</span> `$str`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getStrength</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setAttribute</span> ( <span
class="methodparam"><span class="type">int</span> `$attr`</span> , <span
class="methodparam"><span class="type">int</span> `$val`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setStrength</span> ( <span
class="methodparam"><span class="type">int</span> `$strength`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">sortWithSortKeys</span> ( <span
class="methodparam"><span class="type">array</span> `&$arr`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">sort</span> ( <span class="methodparam"><span
class="type">array</span> `&$arr`</span> \[, <span
class="methodparam"><span class="type">int</span> `$sort_flag`</span> \]
)

}

预定义常量
----------

**`Collator::FRENCH_COLLATION`** (<span class="type">integer</span>)  
Sort strings with different accents from the back of the string. This
attribute is automatically set to *On* for the French locales and a few
others. Users normally would not need to explicitly set this attribute.
There is a string comparison performance cost when it is set *On*, but
sort key length is unaffected. Possible values are:

-   **`Collator::ON`**
-   **`Collator::OFF`**(default)
-   **`Collator::DEFAULT_VALUE`**

**示例 \#1 FRENCH\_COLLATION rules**

-   F=OFF cote \< coté \< côte \< côté
-   F=ON cote \< côte \< coté \< côté

**`Collator::ALTERNATE_HANDLING`** (<span class="type">integer</span>)  
The Alternate attribute is used to control the handling of the so called
variable characters in the UCA: whitespace, punctuation and symbols. If
Alternate is set to *NonIgnorable* (N), then differences among these
characters are of the same importance as differences among letters. If
Alternate is set to *Shifted* (S), then these characters are of only
minor importance. The *Shifted* value is often used in combination with
*Strength* set to Quaternary. In such a case, whitespace, punctuation,
and symbols are considered when comparing strings, but only if all other
aspects of the strings (base letters, accents, and case) are identical.
If Alternate is not set to Shifted, then there is no difference between
a Strength of 3 and a Strength of 4. For more information and examples,
see Variable\_Weighting in the
<a href="http://www.unicode.org/reports/tr10/" class="link external">» UCA</a>.
The reason the Alternate values are not simply *On* and *Off* is that
additional Alternate values may be added in the future. The UCA option
Blanked is expressed with Strength set to 3, and Alternate set to
Shifted. The default for most locales is NonIgnorable. If Shifted is
selected, it may be slower if there are many strings that are the same
except for punctuation; sort key length will not be affected unless the
strength level is also increased.

Possible values are:

-   **`Collator::NON_IGNORABLE`**(default)
-   **`Collator::SHIFTED`**
-   **`Collator::DEFAULT_VALUE`**

**示例 \#2 ALTERNATE\_HANDLING rules**

-   S=3, A=N di Silva \< Di Silva \< diSilva \< U.S.A. \< USA
-   S=3, A=S di Silva = diSilva \< Di Silva \< U.S.A. = USA
-   S=4, A=S di Silva \< diSilva \< Di Silva \< U.S.A. \< USA

**`Collator::CASE_FIRST`** (<span class="type">integer</span>)  
The Case\_First attribute is used to control whether uppercase letters
come before lowercase letters or vice versa, in the absence of other
differences in the strings. The possible values are
*Uppercase\_First* (U) and *Lowercase\_First* (L), plus the standard
*Default* and *Off*. There is almost no difference between the Off and
Lowercase\_First options in terms of results, so typically users will
not use Lowercase\_First: only Off or Uppercase\_First. (People
interested in the detailed differences between X and L should consult
the *Collation Customization*). Specifying either L or U won't affect
string comparison performance, but will affect the sort key length.

Possible values are:

-   **`Collator::OFF`**(default)
-   **`Collator::LOWER_FIRST`**
-   **`Collator::UPPER_FIRST`**
-   **`Collator:DEFAULT`**

**示例 \#3 CASE\_FIRST rules**

-   C=X or C=L "china" \< "China" \< "denmark" \< "Denmark"
-   C=U "China" \< "china" \< "Denmark" \< "denmark"

**`Collator::CASE_LEVEL`** (<span class="type">integer</span>)  
The Case\_Level attribute is used when ignoring accents but not case. In
such a situation, set Strength to be *Primary*, and Case\_Level to be
*On*. In most locales, this setting is Off by default. There is a small
string comparison performance and sort key impact if this attribute is
set to be *On*.

Possible values are:

-   **`Collator::OFF`**(default)
-   **`Collator::ON`**
-   **`Collator::DEFAULT_VALUE`**

**示例 \#4 CASE\_LEVEL rules**

-   S=1, E=X role = Role = rôle
-   S=1, E=O role = rôle \< Role

**`Collator::NORMALIZATION_MODE`** (<span class="type">integer</span>)  
The Normalization setting determines whether text is thoroughly
normalized or not in comparison. Even if the setting is off (which is
the default for many locales), text as represented in common usage will
compare correctly (for details, see UTN \#5). Only if the accent marks
are in noncanonical order will there be a problem. If the setting is
*On*, then the best results are guaranteed for all possible text input.
There is a medium string comparison performance cost if this attribute
is *On*, depending on the frequency of sequences that require
normalization. There is no significant effect on sort key length. If the
input text is known to be in NFD or NFKD normalization forms, there is
no need to enable this Normalization option.

Possible values are:

-   **`Collator::OFF`**(default)
-   **`Collator::ON`**
-   **`Collator::DEFAULT_VALUE`**

**`Collator::STRENGTH`** (<span class="type">integer</span>)  
The ICU Collation Service supports many levels of comparison (named
"Levels", but also known as "Strengths"). Having these categories
enables ICU to sort strings precisely according to local conventions.
However, by allowing the levels to be selectively employed, searching
for a string in text can be performed with various matching conditions.
For more detailed information, see <span
class="function">collator\_set\_strength</span> chapter.

Possible values are:

-   **`Collator::PRIMARY`**
-   **`Collator::SECONDARY`**
-   **`Collator::TERTIARY`**(default)
-   **`Collator::QUATERNARY`**
-   **`Collator::IDENTICAL`**
-   **`Collator::DEFAULT_VALUE`**

**`Collator::HIRAGANA_QUATERNARY_MODE`** (<span class="type">integer</span>)  
Compatibility with JIS x 4061 requires the introduction of an additional
level to distinguish Hiragana and Katakana characters. If compatibility
with that standard is required, then this attribute should be set *On*,
and the strength set to Quaternary. This will affect sort key length and
string comparison string comparison performance.

Possible values are:

-   **`Collator::OFF`**(default)
-   **`Collator::ON`**
-   **`Collator::DEFAULT_VALUE`**

**`Collator::NUMERIC_COLLATION`** (<span class="type">integer</span>)  
When turned on, this attribute generates a collation key for the numeric
value of substrings of digits. This is a way to get '100' to sort AFTER
'2'.

Possible values are:

-   **`Collator::OFF`**(default)
-   **`Collator::ON`**
-   **`Collator::DEFAULT_VALUE`**

**`Collator::DEFAULT_VALUE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Collator::PRIMARY`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Collator::SECONDARY`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Collator::TERTIARY`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Collator::DEFAULT_STRENGTH`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Collator::QUATERNARY`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Collator::IDENTICAL`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Collator::OFF`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Collator::ON`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Collator::SHIFTED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Collator::NON_IGNORABLE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Collator::LOWER_FIRST`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Collator::UPPER_FIRST`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

Collator::asort
===============

collator\_asort
===============

Sort array maintaining index association

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Collator::asort</span> ( <span
class="methodparam"><span class="type">array</span> `&$arr`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$sort_flag`</span> \] )

过程化风格

<span class="type">bool</span> <span
class="methodname">collator\_asort</span> ( <span
class="methodparam"><span class="type">Collator</span> `$coll`</span> ,
<span class="methodparam"><span class="type">array</span> `&$arr`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$sort_flag`</span> \] )

This function sorts an array such that array indices maintain their
correlation with the array elements they are associated with. This is
used mainly when sorting associative arrays where the actual element
order is significant. Array elements will have sort order according to
current locale rules.

Equivalent to standard PHP <span class="function">asort</span>.

### 参数

`coll`  
<span class="classname">Collator</span> object.

`arr`  
Array of strings to sort.

`sort_flag`  
Optional sorting type, one of the following:

-   **`Collator::SORT_REGULAR`** - compare items normally (don't change
    types)

-   **`Collator::SORT_NUMERIC`** - compare items numerically

-   **`Collator::SORT_STRING`** - compare items as strings

Default $sort\_flag value is **`Collator::SORT_REGULAR`**. It is also
used if an invalid $sort\_flag value has been specified.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">collator\_asort</span>example**

``` php
<?php
$coll = collator_create( 'en_US' );
$arr = array(
     'a' => '100',
     'b' => '50',
     'c' => '7'
);
collator_asort( $coll, $arr, Collator::SORT_NUMERIC );
var_export( $arr );

collator_asort( $coll, $arr, Collator::SORT_STRING );
var_export( $arr );
?>
```

以上例程会输出：

    array (
      'c' => '7',
      'b' => '50',
      'a' => '100',
    )array (
      'a' => '100',
      'b' => '50',
      'c' => '7',
    )

### 参见

-   <a href="/class/collator.html#预定义常量" class="link"><span class="classname">Collator</span> constants</a>
-   <span class="function">collator\_sort</span>
-   <span class="function">collator\_sort\_with\_sort\_keys</span>

Collator::compare
=================

collator\_compare
=================

Compare two Unicode strings

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Collator::compare</span> ( <span
class="methodparam"><span class="type">string</span> `$str1`</span> ,
<span class="methodparam"><span class="type">string</span>
`$str2`</span> )

过程化风格

<span class="type">int</span> <span
class="methodname">collator\_compare</span> ( <span
class="methodparam"><span class="type">Collator</span> `$coll`</span> ,
<span class="methodparam"><span class="type">string</span>
`$str1`</span> , <span class="methodparam"><span
class="type">string</span> `$str2`</span> )

Compare two Unicode strings according to collation rules.

### 参数

`coll`  
<span class="classname">Collator</span> object.

`str1`  
The first string to compare.

`str2`  
The second string to compare.

### 返回值

Return comparison result:

-   1 if `str1` is *greater* than `str2` ;

-   0 if `str1` is *equal* to `str2`;

-   -1 if `str1` is *less* than `str2` .

On error <span class="type">boolean</span> **`FALSE`** is returned.

**Warning**

此函数可能返回布尔值 **`FALSE`**，但也可能返回等同于 **`FALSE`**
的非布尔值。请阅读
<a href="/language/types/boolean.html" class="link">布尔类型</a>章节以获取更多信息。应使用
<a href="/language/operators/comparison.html" class="link">=== 运算符</a>来测试此函数的返回值。

### 范例

**示例 \#1 <span class="function">collator\_compare</span>example**

``` php
<?php
$s1 = 'Hello';
$s2 = 'hello';

$coll = collator_create( 'en_US' );
$res  = collator_compare( $coll, $s1, $s2 );

if ($res === false) {
    echo collator_get_error_message( $coll );
} else if( $res > 0 ) {
    echo "s1 is greater than s2\n";
} else if( $res < 0 ) {
    echo "s1 is less than s2\n";
} else {
    echo "s1 is equal to s2\n";
}
?>
```

以上例程会输出：

  
s1 is greater than s2  

### 参见

-   <span class="function">collator\_sort</span>

Collator::\_\_construct
=======================

Create a collator

### 说明

<span class="modifier">public</span> <span
class="methodname">Collator::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> )

Creates a new instance of Collator.

### 参数

`locale`  
The locale whose collation rules should be used. Special values for
locales can be passed in - if null is passed for the locale, the default
locale's collation rules will be used. If "root" is passed, UCA rules
will be used.

The Locale attribute is typically the most important attribute for
correct sorting and matching, according to the user expectations in
different countries and regions. The default
<a href="http://www.unicode.org/reports/tr10/" class="link external">» UCA</a>
ordering will only sort a few languages such as Dutch and Portuguese
correctly ("correctly" meaning according to the normal expectations for
users of the languages). Otherwise, you need to supply the locale to UCA
in order to properly collate text for a given language. Thus a locale
needs to be supplied so as to choose a collator that is correctly
tailored for that locale. The choice of a locale will automatically
preset the values for all of the attributes to something that is
reasonable for that locale. Thus most of the time the other attributes
do not need to be explicitly set. In some cases, the choice of locale
will make a difference in string comparison performance and/or sort key
length.

### 返回值

Returns Collator instance.

### 错误／异常

Returns an "empty" object on error. You can use <span
class="function">intl\_get\_error\_code</span> and/or <span
class="function">intl\_get\_error\_message</span> to know what happened.

### 范例

**示例 \#1 <span class="function">Collator::\_\_construct</span>
example**

``` php
<?php
$coll = new Collator( 'en_CA' );
?>
```

### 参见

-   <span class="function">Collator::create</span>
-   <span class="function">collator\_create</span>

Collator::create
================

collator\_create
================

Create a collator

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">Collator</span> <span
class="methodname">Collator::create</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> )

过程化风格

<span class="type">Collator</span> <span
class="methodname">collator\_create</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> )

The strings will be compared using the options already specified.

### 参数

`locale`  
The locale containing the required collation rules. Special values for
locales can be passed in - if null is passed for the locale, the default
locale collation rules will be used. If empty string ("") or "root" are
passed,
<a href="http://www.unicode.org/reports/tr10/" class="link external">» UCA</a>
rules will be used.

### 返回值

Return new instance of <span class="classname">Collator</span> object,
or **`NULL`** on error.

### 范例

**示例 \#1 <span class="function">collator\_create</span> example**

``` php
<?php
$coll = collator_create( 'en_US' );

if( !isset( $coll ) ) {
    printf( "Collator creation failed: %s\n", intl_get_error_message() );
    exit( 1 );
}
?>
```

### 参见

-   <span class="function">Collator::\_\_construct</span>

Collator::getAttribute
======================

collator\_get\_attribute
========================

Get collation attribute value

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Collator::getAttribute</span> ( <span
class="methodparam"><span class="type">int</span> `$attr`</span> )

过程化风格

<span class="type">int</span> <span
class="methodname">collator\_get\_attribute</span> ( <span
class="methodparam"><span class="type">Collator</span> `$coll`</span> ,
<span class="methodparam"><span class="type">int</span> `$attr`</span> )

Get a value of an integer collator attribute.

### 参数

`coll`  
<span class="classname">Collator</span> object.

`attr`  
Attribute to get value for.

### 返回值

Attribute value, or <span class="type">boolean</span> **`FALSE`** on
error.

### 范例

**示例 \#1 <span class="function">collator\_get\_attribute</span>
example**

``` php
<?php
$coll = collator_create( 'en_CA' );
$val = collator_get_attribute( $coll, Collator::NUMERIC_COLLATION );
if( $val === false )
{
    // Handle error.
}
?>
```

### 参见

-   <a href="/class/collator.html#预定义常量" class="link"><span class="classname">Collator</span> constants</a>
-   <span class="function">collator\_set\_attribute</span>
-   <span class="function">collator\_get\_strength</span>

Collator::getErrorCode
======================

collator\_get\_error\_code
==========================

Get collator's last error code

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Collator::getErrorCode</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">int</span> <span
class="methodname">collator\_get\_error\_code</span> ( <span
class="methodparam"><span class="type">Collator</span> `$coll`</span> )

### 参数

`coll`  
<span class="classname">Collator</span> object.

### 返回值

Error code returned by the last Collator API function call.

### 范例

**示例 \#1 <span class="function">collator\_get\_error\_code</span>
example**

``` php
<?php
$coll = collator_create( 'en_US' );
if( collator_get_attribute( $coll, Collator::FRENCH_COLLATION ) === false )
        handle_error( collator_get_error_code() );
?>
```

### 参见

-   <span class="function">collator\_get\_error\_message</span>

Collator::getErrorMessage
=========================

collator\_get\_error\_message
=============================

Get text for collator's last error code

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Collator::getErrorMessage</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">string</span> <span
class="methodname">collator\_get\_error\_message</span> ( <span
class="methodparam"><span class="type">Collator</span> `$coll`</span> )

Retrieves the message for the last error.

### 参数

`coll`  
<span class="classname">Collator</span> object.

### 返回值

Description of an error occurred in the last Collator API function call.

### 范例

**示例 \#1 <span class="function">collator\_get\_error\_message</span>
example**

``` php
<?php
$coll = collator_create( 'lt' );
if( collator_compare( $coll, 'y', 'k' ) === false ) {
    echo collator_get_error_message( $coll );
}
?>
```

### 参见

-   <span class="function">collator\_get\_error\_code</span>

Collator::getLocale
===================

collator\_get\_locale
=====================

Get the locale name of the collator

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Collator::getLocale</span> ( <span
class="methodparam"><span class="type">int</span> `$type`</span> )

过程化风格

<span class="type">string</span> <span
class="methodname">collator\_get\_locale</span> ( <span
class="methodparam"><span class="type">Collator</span> `$coll`</span> ,
<span class="methodparam"><span class="type">int</span> `$type`</span> )

Get collector locale name.

### 参数

`coll`  
<span class="classname">Collator</span> object.

`type`  
You can choose between valid and actual locale (
**`Locale::VALID_LOCALE`** and **`Locale::ACTUAL_LOCALE`**,
respectively).

### 返回值

Real locale name from which the collation data comes. If the collator
was instantiated from rules or an error occurred, returns <span
class="type">boolean</span> **`FALSE`**.

### 范例

**示例 \#1 <span class="function">collator\_get\_locale</span> example**

``` php
<?php
$coll    = collator_create( 'en_US_California' );
$res_val = collator_get_locale( $coll, Locale::VALID_LOCALE );
$res_act = collator_get_locale( $coll, Locale::ACTUAL_LOCALE );
printf( "Valid locale name: %s\nActual locale name: %s\n",
         $res_val, $res_act );
?>
```

以上例程会输出：

    Requested locale name: en_US_California
    Valid locale name: en_US
    Actual locale name: en

### 参见

-   <span class="function">collator\_create</span>

Collator::getSortKey
====================

collator\_get\_sort\_key
========================

Get sorting key for a string

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Collator::getSortKey</span> ( <span
class="methodparam"><span class="type">string</span> `$str`</span> )

过程化风格

<span class="type">string</span> <span
class="methodname">collator\_get\_sort\_key</span> ( <span
class="methodparam"><span class="type">Collator</span> `$coll`</span> ,
<span class="methodparam"><span class="type">string</span> `$str`</span>
)

Return collation key for a string. Collation keys can be compared
directly instead of strings, though are implementation specific and may
change between ICU library versions. Sort keys are generally only useful
in databases or other circumstances where function calls are extremely
expensive.

### 参数

`coll`  
<span class="classname">Collator</span> object.

`str`  
The string to produce the key from.

### 返回值

Returns the collation key for the string, 或者在失败时返回 **`FALSE`**.

**Warning**

此函数可能返回布尔值 **`FALSE`**，但也可能返回等同于 **`FALSE`**
的非布尔值。请阅读
<a href="/language/types/boolean.html" class="link">布尔类型</a>章节以获取更多信息。应使用
<a href="/language/operators/comparison.html" class="link">=== 运算符</a>来测试此函数的返回值。

### 更新日志

| 版本          | 说明                                            |
|---------------|-------------------------------------------------|
| 5.3.15, 5.4.5 | Sort keys do no longer contain any *NUL* bytes. |

### 范例

**示例 \#1 <span
class="function">collator\_get\_sort\_key</span>example**

``` php
<?php
$s1 = 'Hello';

$coll = collator_create('en_US');
$res  = collator_get_sort_key($coll, $s1);

echo bin2hex($res);
?>
```

以上例程的输出类似于：

  
3832404046010901dc08  

### 参见

-   <span class="function">collator\_sort</span>
-   <span class="function">collator\_sort\_with\_sort\_keys</span>

Collator::getStrength
=====================

collator\_get\_strength
=======================

Get current collation strength

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Collator::getStrength</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">int</span> <span
class="methodname">collator\_get\_strength</span> ( <span
class="methodparam"><span class="type">Collator</span> `$coll`</span> )

### 参数

`coll`  
<span class="classname">Collator</span> object.

### 返回值

Returns current collation strength, or <span class="type">boolean</span>
**`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">collator\_get\_strength</span>
example**

``` php
<?php
$coll     = collator_create( 'en_US' );
$strength = collator_get_strength( $coll );
?>
```

### 参见

-   <a href="/class/collator.html#预定义常量" class="link"><span class="classname">Collator</span> constants</a>
-   <span class="function">collator\_set\_strength</span>
-   <span class="function">collator\_get\_attribute</span>

Collator::setAttribute
======================

collator\_set\_attribute
========================

Set collation attribute

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Collator::setAttribute</span> ( <span
class="methodparam"><span class="type">int</span> `$attr`</span> , <span
class="methodparam"><span class="type">int</span> `$val`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">collator\_set\_attribute</span> ( <span
class="methodparam"><span class="type">Collator</span> `$coll`</span> ,
<span class="methodparam"><span class="type">int</span> `$attr`</span> ,
<span class="methodparam"><span class="type">int</span> `$val`</span> )

### 参数

`coll`  
<span class="classname">Collator</span> <span
class="type">object</span>.

`attr`  
Attribute.

`val`  
Attribute value.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">collator\_set\_attribute</span>
example**

``` php
<?php
$coll = collator_create( 'en_CA' );
$val  = collator_get_attribute( $coll, Collator::NUMERIC_COLLATION );
if ($val === false) {
    // Handle error.
} elseif ($val === Collator::ON) {
    // Do something useful.
}
?>
```

### 参见

-   <a href="/class/collator.html#预定义常量" class="link"><span class="classname">Collator</span> constants</a>
-   <span class="function">collator\_get\_attribute</span>
-   <span class="function">collator\_set\_strength</span>

Collator::setStrength
=====================

collator\_set\_strength
=======================

Set collation strength

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Collator::setStrength</span> ( <span
class="methodparam"><span class="type">int</span> `$strength`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">collator\_set\_strength</span> ( <span
class="methodparam"><span class="type">Collator</span> `$coll`</span> ,
<span class="methodparam"><span class="type">int</span>
`$strength`</span> )

The
<a href="http://www.icu-project.org/" class="link external">» ICU</a>
Collation Service supports many levels of comparison (named "Levels",
but also known as "Strengths"). Having these categories enables ICU to
sort strings precisely according to local conventions. However, by
allowing the levels to be selectively employed, searching for a string
in text can be performed with various matching conditions.

1.  *Primary Level*: Typically, this is used to denote differences
    between base characters (for example, "a" \< "b"). It is the
    strongest difference. For example, dictionaries are divided into
    different sections by base character. This is also called the level1
    strength.

2.  *Secondary Level*: Accents in the characters are considered
    secondary differences (for example, "as" \< "às" \< "at"). Other
    differences between letters can also be considered secondary
    differences, depending on the language. A secondary difference is
    ignored when there is a primary difference anywhere in the strings.
    This is also called the level2 strength.

    > **Note**:
    >
    > Note: In some languages (such as Danish), certain accented letters
    > are considered to be separate base characters. In most languages,
    > however, an accented letter only has a secondary difference from
    > the unaccented version of that letter.

3.  *Tertiary Level*: Upper and lower case differences in characters are
    distinguished at the tertiary level (for example, "ao" \< "Ao" \<
    "aò"). In addition, a variant of a letter differs from the base form
    on the tertiary level (such as "A" and " "). Another example is the
    difference between large and small Kana. A tertiary difference is
    ignored when there is a primary or secondary difference anywhere in
    the strings. This is also called the level3 strength.

4.  *Quaternary Level*: When punctuation is ignored (see Ignoring
    Punctuations ) at level 13, an additional level can be used to
    distinguish words with and without punctuation (for example, "ab" \<
    "a-b" \< "aB"). This difference is ignored when there is a primary,
    secondary or tertiary difference. This is also known as the level4
    strength. The quaternary level should only be used if ignoring
    punctuation is required or when processing Japanese text (see
    Hiragana processing).

5.  *Identical Level*: When all other levels are equal, the identical
    level is used as a tiebreaker. The Unicode code point values of the
    NFD form of each string are compared at this level, just in case
    there is no difference at levels 14. For example, Hebrew
    cantillation marks are only distinguished at this level. This level
    should be used sparingly, as only code point values differences
    between two strings is an extremely rare occurrence. Using this
    level substantially decreases the performance for both incremental
    comparison and sort key generation (as well as increasing the sort
    key length). It is also known as level 5 strength.

For example, people may choose to ignore accents or ignore accents and
case when searching for text. Almost all characters are distinguished by
the first three levels, and in most locales the default value is thus
Tertiary. However, if Alternate is set to be Shifted, then the
Quaternary strength can be used to break ties among whitespace,
punctuation, and symbols that would otherwise be ignored. If very fine
distinctions among characters are required, then the Identical strength
can be used (for example, Identical Strength distinguishes between the
Mathematical Bold Small A and the Mathematical Italic Small A.).
However, using levels higher than Tertiary the Identical strength result
in significantly longer sort keys, and slower string comparison
performance for equal strings.

### 参数

`coll`  
<span class="classname">Collator</span> object.

`strength`  
Strength to set.

Possible values are:

-   **`Collator::PRIMARY`**

-   **`Collator::SECONDARY`**

-   **`Collator::TERTIARY`**

-   **`Collator::QUATERNARY`**

-   **`Collator::IDENTICAL`**

-   **`Collator::DEFAULT_STRENGTH`**

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">collator\_set\_strength</span>
example**

``` php
<?php
$arr  = array( 'aò', 'Ao', 'ao' );
$coll = collator_create( 'en_US' );

// Sort array using default strength.
collator_sort( $coll, $arr ); 
var_export( $arr );

// Sort array using primary strength.
collator_set_strength( $coll, Collator::PRIMARY );
collator_sort( $coll, $arr );
var_export( $arr );
?>
```

以上例程会输出：

    array (
      0 => 'ao',
      1 => 'Ao',
      2 => 'aò',
    )
    array (
      0 => 'aò',
      1 => 'Ao',
      2 => 'ao',
    )

### 参见

-   <a href="/class/collator.html#预定义常量" class="link"><span class="classname">Collator</span> constants</a>
-   <span class="function">collator\_get\_strength</span>

Collator::sortWithSortKeys
==========================

collator\_sort\_with\_sort\_keys
================================

Sort array using specified collator and sort keys

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Collator::sortWithSortKeys</span> ( <span
class="methodparam"><span class="type">array</span> `&$arr`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">collator\_sort\_with\_sort\_keys</span> ( <span
class="methodparam"><span class="type">Collator</span> `$coll`</span> ,
<span class="methodparam"><span class="type">array</span> `&$arr`</span>
)

Similar to <span class="function">collator\_sort</span> but uses ICU
sorting keys produced by ucol\_getSortKey() to gain more speed on large
arrays.

### 参数

`coll`  
<span class="classname">Collator</span> object.

`arr`  
Array of strings to sort

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span
class="function">collator\_sort\_with\_sort\_keys</span> example**

``` php
<?php
$arr  = array( 'Köpfe', 'Kypper', 'Kopfe' );
$coll = collator_create( 'sv' );

collator_sort_with_sort_keys( $coll, $arr );
var_export( $arr );
?>
```

以上例程会输出：

    array (
      0 => 'Kopfe',
      1 => 'Kypper',
      2 => 'Köpfe',
    )

### 参见

-   <a href="/class/collator.html#预定义常量" class="link"><span class="classname">Collator</span> constants</a>
-   <span class="function">collator\_sort</span>
-   <span class="function">collator\_asort</span>

Collator::sort
==============

collator\_sort
==============

Sort array using specified collator

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Collator::sort</span> ( <span
class="methodparam"><span class="type">array</span> `&$arr`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$sort_flag`</span> \] )

过程化风格

<span class="type">bool</span> <span
class="methodname">collator\_sort</span> ( <span
class="methodparam"><span class="type">Collator</span> `$coll`</span> ,
<span class="methodparam"><span class="type">array</span> `&$arr`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$sort_flag`</span> \] )

This function sorts an array according to current locale rules.

Equivalent to standard PHP <span class="function">sort</span> .

### 参数

`coll`  
<span class="classname">Collator</span> object.

`arr`  
Array of strings to sort.

`sort_flag`  
Optional sorting type, one of the following:

-   **`Collator::SORT_REGULAR`** - compare items normally (don't change
    types)

-   **`Collator::SORT_NUMERIC`** - compare items numerically

-   **`Collator::SORT_STRING`** - compare items as strings

Default sorting type is **`Collator::SORT_REGULAR`**. It is also used if
an invalid `sort_flag` value has been specified.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">collator\_sort</span> example**

``` php
<?php
$coll = collator_create( 'en_US' );
$arr  = array( 'at', 'às', 'as' );

var_export( $arr );
collator_sort( $coll, $arr );
var_export( $arr );
?>
```

以上例程会输出：

    array (
      0 => 'at',
      1 => 'às',
      2 => 'as',
    )array (
      0 => 'as',
      1 => 'às',
      2 => 'at',
    )

### 参见

-   <a href="/class/collator.html#预定义常量" class="link"><span class="classname">Collator</span> constants</a>
-   <span class="function">collator\_asort</span>
-   <span class="function">collator\_sort\_with\_sort\_keys</span>

简介
----

Programs store and operate on numbers using a locale-independent binary
representation. When displaying or printing a number it is converted to
a locale-specific string. For example, the number 12345.67 is
"12,345.67" in the US, "12 345,67" in France and "12.345,67" in Germany.

By invoking the methods provided by the NumberFormatter class, you can
format numbers, currencies, and percentages according to the specified
or default locale. NumberFormatter is locale-sensitive so you need to
create a new NumberFormatter for each locale. NumberFormatter methods
format primitive-type numbers, such as double and output the number as a
locale-specific string.

For currencies you can use currency format type to create a formatter
that returns a string with the formatted number and the appropriate
currency sign. Of course, the NumberFormatter class is unaware of
exchange rates so, the number output is the same regardless of the
specified currency. This means that the same number has different
monetary values depending on the currency locale. If the number is
9988776.65 the results will be:

-   9 988 776,65 € in France
-   9.988.776,65 € in Germany
-   $9,988,776.65 in the United States

In order to format percentages, create a locale-specific formatter with
percentage format type. With this formatter, a decimal fraction such as
0.75 is displayed as 75%.

For more complex formatting, like spelled-out numbers, the rule-based
number formatters are used.

类摘要
------

**NumberFormatter**

<span class="ooclass"> class **NumberFormatter** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> ,
<span class="methodparam"><span class="type">int</span> `$style`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$pattern`</span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">NumberFormatter</span>
<span class="methodname">create</span> ( <span class="methodparam"><span
class="type">string</span> `$locale`</span> , <span
class="methodparam"><span class="type">int</span> `$style`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$pattern`</span> \] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">formatCurrency</span> ( <span
class="methodparam"><span class="type">float</span> `$value`</span> ,
<span class="methodparam"><span class="type">string</span>
`$currency`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">format</span> ( <span class="methodparam"><span
class="type">number</span> `$value`</span> \[, <span
class="methodparam"><span class="type">int</span> `$type`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getAttribute</span> ( <span class="methodparam"><span
class="type">int</span> `$attr`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getErrorCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getErrorMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getLocale</span> (\[ <span
class="methodparam"><span class="type">int</span> `$type`</span> \] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getPattern</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getSymbol</span> ( <span
class="methodparam"><span class="type">int</span> `$attr`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getTextAttribute</span> ( <span
class="methodparam"><span class="type">int</span> `$attr`</span> )

<span class="modifier">public</span> <span class="type">float</span>
<span class="methodname">parseCurrency</span> ( <span
class="methodparam"><span class="type">string</span> `$value`</span> ,
<span class="methodparam"><span class="type">string</span>
`&$currency`</span> \[, <span class="methodparam"><span
class="type">int</span> `&$position`</span> \] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">parse</span> ( <span class="methodparam"><span
class="type">string</span> `$value`</span> \[, <span
class="methodparam"><span class="type">int</span> `$type`</span> \[,
<span class="methodparam"><span class="type">int</span>
`&$position`</span> \]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setAttribute</span> ( <span
class="methodparam"><span class="type">int</span> `$attr`</span> , <span
class="methodparam"><span class="type">int</span> `$value`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setPattern</span> ( <span
class="methodparam"><span class="type">string</span> `$pattern`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setSymbol</span> ( <span
class="methodparam"><span class="type">int</span> `$attr`</span> , <span
class="methodparam"><span class="type">string</span> `$value`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setTextAttribute</span> ( <span
class="methodparam"><span class="type">int</span> `$attr`</span> , <span
class="methodparam"><span class="type">string</span> `$value`</span> )

}

预定义常量
----------

These styles are used by the <span
class="function">numfmt\_create</span> to define the type of the
formatter.

**`NumberFormatter::PATTERN_DECIMAL`** (<span class="type">integer</span>)  
<span class="simpara">Decimal format defined by pattern</span>

**`NumberFormatter::DECIMAL`** (<span class="type">integer</span>)  
<span class="simpara">Decimal format</span>

**`NumberFormatter::CURRENCY`** (<span class="type">integer</span>)  
<span class="simpara">Currency format</span>

**`NumberFormatter::PERCENT`** (<span class="type">integer</span>)  
<span class="simpara">Percent format</span>

**`NumberFormatter::SCIENTIFIC`** (<span class="type">integer</span>)  
<span class="simpara">Scientific format</span>

**`NumberFormatter::SPELLOUT`** (<span class="type">integer</span>)  
<span class="simpara">Spellout rule-based format</span>

**`NumberFormatter::ORDINAL`** (<span class="type">integer</span>)  
<span class="simpara">Ordinal rule-based format</span>

**`NumberFormatter::DURATION`** (<span class="type">integer</span>)  
<span class="simpara">Duration rule-based format</span>

**`NumberFormatter::PATTERN_RULEBASED`** (<span class="type">integer</span>)  
<span class="simpara">Rule-based format defined by pattern</span>

**`NumberFormatter::CURRENCY_ACCOUNTING`** (<span class="type">integer</span>)  
<span class="simpara"> Currency format for accounting, e.g., *($3.00)*
for negative currency amount instead of *-$3.00*. Available as of PHP
7.4.1 and ICU 53. </span>

**`NumberFormatter::DEFAULT_STYLE`** (<span class="type">integer</span>)  
<span class="simpara">Default format for the locale</span>

**`NumberFormatter::IGNORE`** (<span class="type">integer</span>)  
<span class="simpara">Alias for PATTERN\_DECIMAL</span>

These constants define how the numbers are parsed or formatted. They
should be used as arguments to <span
class="function">numfmt\_format</span> and <span
class="function">numfmt\_parse</span>.

**`NumberFormatter::TYPE_DEFAULT`** (<span class="type">integer</span>)  
<span class="simpara">Derive the type from variable type</span>

**`NumberFormatter::TYPE_INT32`** (<span class="type">integer</span>)  
<span class="simpara">Format/parse as 32-bit integer</span>

**`NumberFormatter::TYPE_INT64`** (<span class="type">integer</span>)  
<span class="simpara">Format/parse as 64-bit integer</span>

**`NumberFormatter::TYPE_DOUBLE`** (<span class="type">integer</span>)  
<span class="simpara">Format/parse as floating point value</span>

**`NumberFormatter::TYPE_CURRENCY`** (<span class="type">integer</span>)  
<span class="simpara">Format/parse as currency value</span>

Number format attribute used by <span
class="function">numfmt\_get\_attribute</span> and <span
class="function">numfmt\_set\_attribute</span>.

**`NumberFormatter::PARSE_INT_ONLY`** (<span class="type">integer</span>)  
<span class="simpara">Parse integers only.</span>

**`NumberFormatter::GROUPING_USED`** (<span class="type">integer</span>)  
<span class="simpara">Use grouping separator.</span>

**`NumberFormatter::DECIMAL_ALWAYS_SHOWN`** (<span class="type">integer</span>)  
<span class="simpara">Always show decimal point.</span>

**`NumberFormatter::MAX_INTEGER_DIGITS`** (<span class="type">integer</span>)  
<span class="simpara">Maximum integer digits.</span>

**`NumberFormatter::MIN_INTEGER_DIGITS`** (<span class="type">integer</span>)  
<span class="simpara">Minimum integer digits.</span>

**`NumberFormatter::INTEGER_DIGITS`** (<span class="type">integer</span>)  
<span class="simpara">Integer digits.</span>

**`NumberFormatter::MAX_FRACTION_DIGITS`** (<span class="type">integer</span>)  
<span class="simpara">Maximum fraction digits.</span>

**`NumberFormatter::MIN_FRACTION_DIGITS`** (<span class="type">integer</span>)  
<span class="simpara">Minimum fraction digits.</span>

**`NumberFormatter::FRACTION_DIGITS`** (<span class="type">integer</span>)  
<span class="simpara">Fraction digits.</span>

**`NumberFormatter::MULTIPLIER`** (<span class="type">integer</span>)  
<span class="simpara">Multiplier.</span>

**`NumberFormatter::GROUPING_SIZE`** (<span class="type">integer</span>)  
<span class="simpara">Grouping size.</span>

**`NumberFormatter::ROUNDING_MODE`** (<span class="type">integer</span>)  
<span class="simpara">Rounding Mode.</span>

**`NumberFormatter::ROUNDING_INCREMENT`** (<span class="type">integer</span>)  
<span class="simpara">Rounding increment.</span>

**`NumberFormatter::FORMAT_WIDTH`** (<span class="type">integer</span>)  
<span class="simpara">The width to which the output of format() is
padded.</span>

**`NumberFormatter::PADDING_POSITION`** (<span class="type">integer</span>)  
<span class="simpara"> The position at which padding will take place.
See pad position constants for possible argument values. </span>

**`NumberFormatter::SECONDARY_GROUPING_SIZE`** (<span class="type">integer</span>)  
<span class="simpara">Secondary grouping size.</span>

**`NumberFormatter::SIGNIFICANT_DIGITS_USED`** (<span class="type">integer</span>)  
<span class="simpara">Use significant digits.</span>

**`NumberFormatter::MIN_SIGNIFICANT_DIGITS`** (<span class="type">integer</span>)  
<span class="simpara">Minimum significant digits.</span>

**`NumberFormatter::MAX_SIGNIFICANT_DIGITS`** (<span class="type">integer</span>)  
<span class="simpara">Maximum significant digits.</span>

**`NumberFormatter::LENIENT_PARSE`** (<span class="type">integer</span>)  
<span class="simpara">Lenient parse mode used by rule-based
formats.</span>

Number format text attribute used by <span
class="function">numfmt\_get\_text\_attribute</span> and <span
class="function">numfmt\_set\_text\_attribute</span>.

**`NumberFormatter::POSITIVE_PREFIX`** (<span class="type">integer</span>)  
<span class="simpara">Positive prefix.</span>

**`NumberFormatter::POSITIVE_SUFFIX`** (<span class="type">integer</span>)  
<span class="simpara">Positive suffix.</span>

**`NumberFormatter::NEGATIVE_PREFIX`** (<span class="type">integer</span>)  
<span class="simpara">Negative prefix.</span>

**`NumberFormatter::NEGATIVE_SUFFIX`** (<span class="type">integer</span>)  
<span class="simpara">Negative suffix.</span>

**`NumberFormatter::PADDING_CHARACTER`** (<span class="type">integer</span>)  
<span class="simpara">The character used to pad to the format
width.</span>

**`NumberFormatter::CURRENCY_CODE`** (<span class="type">integer</span>)  
<span class="simpara">The ISO currency code.</span>

**`NumberFormatter::DEFAULT_RULESET`** (<span class="type">integer</span>)  
<span class="simpara"> The default rule set. This is only available with
rule-based formatters. </span>

**`NumberFormatter::PUBLIC_RULESETS`** (<span class="type">integer</span>)  
<span class="simpara"> The public rule sets. This is only available with
rule-based formatters. This is a read-only attribute. The public
rulesets are returned as a single string, with each ruleset name
delimited by ';' (semicolon). </span>

Number format symbols used by <span
class="function">numfmt\_get\_symbol</span> and <span
class="function">numfmt\_set\_symbol</span>.

**`NumberFormatter::DECIMAL_SEPARATOR_SYMBOL`** (<span class="type">integer</span>)  
<span class="simpara">The decimal separator.</span>

**`NumberFormatter::GROUPING_SEPARATOR_SYMBOL`** (<span class="type">integer</span>)  
<span class="simpara">The grouping separator.</span>

**`NumberFormatter::PATTERN_SEPARATOR_SYMBOL`** (<span class="type">integer</span>)  
<span class="simpara">The pattern separator.</span>

**`NumberFormatter::PERCENT_SYMBOL`** (<span class="type">integer</span>)  
<span class="simpara">The percent sign.</span>

**`NumberFormatter::ZERO_DIGIT_SYMBOL`** (<span class="type">integer</span>)  
<span class="simpara">Zero.</span>

**`NumberFormatter::DIGIT_SYMBOL`** (<span class="type">integer</span>)  
<span class="simpara">Character representing a digit in the
pattern.</span>

**`NumberFormatter::MINUS_SIGN_SYMBOL`** (<span class="type">integer</span>)  
<span class="simpara">The minus sign.</span>

**`NumberFormatter::PLUS_SIGN_SYMBOL`** (<span class="type">integer</span>)  
<span class="simpara">The plus sign.</span>

**`NumberFormatter::CURRENCY_SYMBOL`** (<span class="type">integer</span>)  
<span class="simpara">The currency symbol.</span>

**`NumberFormatter::INTL_CURRENCY_SYMBOL`** (<span class="type">integer</span>)  
<span class="simpara">The international currency symbol.</span>

**`NumberFormatter::MONETARY_SEPARATOR_SYMBOL`** (<span class="type">integer</span>)  
<span class="simpara">The monetary separator.</span>

**`NumberFormatter::EXPONENTIAL_SYMBOL`** (<span class="type">integer</span>)  
<span class="simpara">The exponential symbol.</span>

**`NumberFormatter::PERMILL_SYMBOL`** (<span class="type">integer</span>)  
<span class="simpara">Per mill symbol.</span>

**`NumberFormatter::PAD_ESCAPE_SYMBOL`** (<span class="type">integer</span>)  
<span class="simpara">Escape padding character.</span>

**`NumberFormatter::INFINITY_SYMBOL`** (<span class="type">integer</span>)  
<span class="simpara">Infinity symbol.</span>

**`NumberFormatter::NAN_SYMBOL`** (<span class="type">integer</span>)  
<span class="simpara">Not-a-number symbol.</span>

**`NumberFormatter::SIGNIFICANT_DIGIT_SYMBOL`** (<span class="type">integer</span>)  
<span class="simpara">Significant digit symbol.</span>

**`NumberFormatter::MONETARY_GROUPING_SEPARATOR_SYMBOL`** (<span class="type">integer</span>)  
<span class="simpara">The monetary grouping separator.</span>

Rounding mode values used by <span
class="function">numfmt\_get\_attribute</span> and <span
class="function">numfmt\_set\_attribute</span> with
**`NumberFormatter::ROUNDING_MODE`** attribute.

**`NumberFormatter::ROUND_CEILING`** (<span class="type">integer</span>)  
<span class="simpara">Rounding mode to round towards positive
infinity.</span>

**`NumberFormatter::ROUND_DOWN`** (<span class="type">integer</span>)  
<span class="simpara">Rounding mode to round towards zero.</span>

**`NumberFormatter::ROUND_FLOOR`** (<span class="type">integer</span>)  
<span class="simpara">Rounding mode to round towards negative
infinity.</span>

**`NumberFormatter::ROUND_HALFDOWN`** (<span class="type">integer</span>)  
<span class="simpara"> Rounding mode to round towards "nearest neighbor"
unless both neighbors are equidistant, in which case round down. </span>

**`NumberFormatter::ROUND_HALFEVEN`** (<span class="type">integer</span>)  
<span class="simpara"> Rounding mode to round towards the "nearest
neighbor" unless both neighbors are equidistant, in which case, round
towards the even neighbor. </span>

**`NumberFormatter::ROUND_HALFUP`** (<span class="type">integer</span>)  
<span class="simpara"> Rounding mode to round towards "nearest neighbor"
unless both neighbors are equidistant, in which case round up. </span>

**`NumberFormatter::ROUND_UP`** (<span class="type">integer</span>)  
<span class="simpara">Rounding mode to round away from zero.</span>

Pad position values used by <span
class="function">numfmt\_get\_attribute</span> and <span
class="function">numfmt\_set\_attribute</span> with
**`NumberFormatter::PADDING_POSITION`** attribute.

**`NumberFormatter::PAD_AFTER_PREFIX`** (<span class="type">integer</span>)  
<span class="simpara">Pad characters inserted after the prefix.</span>

**`NumberFormatter::PAD_AFTER_SUFFIX`** (<span class="type">integer</span>)  
<span class="simpara">Pad characters inserted after the suffix.</span>

**`NumberFormatter::PAD_BEFORE_PREFIX`** (<span class="type">integer</span>)  
<span class="simpara">Pad characters inserted before the prefix.</span>

**`NumberFormatter::PAD_BEFORE_SUFFIX`** (<span class="type">integer</span>)  
<span class="simpara">Pad characters inserted before the suffix.</span>

参见
----

-   <a href="http://icu-project.org/userguide/formatParse.html" class="link external">»  ICU formatting documentation</a>
-   <a href="http://icu-project.org/userguide/formatNumbers.html" class="link external">» ICU number formatters</a>
-   <a href="http://www.icu-project.org/apiref/icu4c/classDecimalFormat.html#details" class="link external">» ICU decimal formatters</a>
-   <a href="http://www.icu-project.org/apiref/icu4c/classRuleBasedNumberFormat.html#details" class="link external">»  ICU rule-based number formatters</a>

NumberFormatter::create
=======================

numfmt\_create
==============

NumberFormatter::\_\_construct
==============================

Create a number formatter

### 说明

面向对象风格 (method)

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">NumberFormatter</span>
<span class="methodname">NumberFormatter::create</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> ,
<span class="methodparam"><span class="type">int</span> `$style`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$pattern`</span> \] )

过程化风格

<span class="type">NumberFormatter</span> <span
class="methodname">numfmt\_create</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> ,
<span class="methodparam"><span class="type">int</span> `$style`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$pattern`</span> \] )

面向对象风格 (constructor):

<span class="modifier">public</span> <span
class="methodname">NumberFormatter::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> ,
<span class="methodparam"><span class="type">int</span> `$style`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$pattern`</span> \] )

Creates a number formatter.

### 参数

`locale`  
Locale in which the number would be formatted (locale name, e.g.
en\_CA).

`style`  
Style of the formatting, one of the
<a href="/class/numberformatter.html#" class="link">format style</a>
constants. If **`NumberFormatter::PATTERN_DECIMAL`** or
**`NumberFormatter::PATTERN_RULEBASED`** is passed then the number
format is opened using the given pattern, which must conform to the
syntax described in
<a href="http://www.icu-project.org/apiref/icu4c/classDecimalFormat.html#details" class="link external">» ICU DecimalFormat documentation</a>
or
<a href="http://www.icu-project.org/apiref/icu4c/classRuleBasedNumberFormat.html#details" class="link external">» ICU RuleBasedNumberFormat documentation</a>,
respectively.

`pattern`  
Pattern string if the chosen style requires a pattern.

### 返回值

Returns <span class="classname">NumberFormatter</span> object or
**`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">numfmt\_create</span> example**

``` php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::DECIMAL );
echo numfmt_format($fmt, 1234567.891234567890000)."\n";
$fmt = numfmt_create( 'it', NumberFormatter::SPELLOUT );
echo numfmt_format($fmt, 1142)."\n";
?>
```

**示例 \#2 <span class="function">NumberFormatter::create</span>
example**

``` php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::DECIMAL );
echo $fmt->format(1234567.891234567890000)."\n";
$fmt = new NumberFormatter( 'it', NumberFormatter::SPELLOUT );
echo $fmt->format(1142)."\n";
?>
```

以上例程会输出：

    1.234.567,891
    millicentoquarantadue

### 参见

-   <span class="function">numfmt\_format</span>
-   <span class="function">numfmt\_parse</span>

NumberFormatter::formatCurrency
===============================

numfmt\_format\_currency
========================

Format a currency value

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">NumberFormatter::formatCurrency</span> ( <span
class="methodparam"><span class="type">float</span> `$value`</span> ,
<span class="methodparam"><span class="type">string</span>
`$currency`</span> )

过程化风格

<span class="type">string</span> <span
class="methodname">numfmt\_format\_currency</span> ( <span
class="methodparam"><span class="type">NumberFormatter</span>
`$fmt`</span> , <span class="methodparam"><span
class="type">float</span> `$value`</span> , <span
class="methodparam"><span class="type">string</span> `$currency`</span>
)

Format the currency value according to the formatter rules.

### 参数

`fmt`  
<span class="classname">NumberFormatter</span> object.

`value`  
The numeric currency value.

`currency`  
The 3-letter ISO 4217 currency code indicating the currency to use.

### 返回值

String representing the formatted currency value, 或者在失败时返回
**`FALSE`**.

### 范例

**示例 \#1 <span class="function">numfmt\_format\_currency</span>
example**

``` php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::CURRENCY );
echo numfmt_format_currency($fmt, 1234567.891234567890000, "EUR")."\n";
echo numfmt_format_currency($fmt, 1234567.891234567890000, "RUR")."\n";
$fmt = numfmt_create( 'ru_RU', NumberFormatter::CURRENCY );
echo numfmt_format_currency($fmt, 1234567.891234567890000, "EUR")."\n";
echo numfmt_format_currency($fmt, 1234567.891234567890000, "RUR")."\n";
?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::CURRENCY );
echo $fmt->formatCurrency(1234567.891234567890000, "EUR")."\n";
echo $fmt->formatCurrency(1234567.891234567890000, "RUR")."\n";
$fmt = new NumberFormatter( 'ru_RU', NumberFormatter::CURRENCY );
echo $fmt->formatCurrency(1234567.891234567890000, "EUR")."\n";
echo $fmt->formatCurrency(1234567.891234567890000, "RUR")."\n";
?>
```

以上例程会输出：

    1.234.567,89 €
    1.234.567,89 RUR
    1 234 567,89€
    1 234 567,89р.

### 参见

-   <span class="function">numfmt\_get\_error\_code</span>
-   <span class="function">numfmt\_format</span>
-   <span class="function">numfmt\_parse\_currency</span>

NumberFormatter::format
=======================

numfmt\_format
==============

Format a number

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">NumberFormatter::format</span> ( <span
class="methodparam"><span class="type">number</span> `$value`</span> \[,
<span class="methodparam"><span class="type">int</span> `$type`</span>
\] )

过程化风格

<span class="type">string</span> <span
class="methodname">numfmt\_format</span> ( <span
class="methodparam"><span class="type">NumberFormatter</span>
`$fmt`</span> , <span class="methodparam"><span
class="type">number</span> `$value`</span> \[, <span
class="methodparam"><span class="type">int</span> `$type`</span> \] )

Format a numeric value according to the formatter rules.

### 参数

`fmt`  
<span class="classname">NumberFormatter</span> object.

`value`  
The value to format. Can be <span class="type">integer</span> or <span
class="type">float</span>, other values will be converted to a numeric
value.

`type`  
The
<a href="/class/numberformatter.html#" class="link">formatting type</a>
to use.

### 返回值

Returns the string containing formatted value, or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">numfmt\_format</span> example**

``` php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::DECIMAL );
$data = numfmt_format($fmt, 1234567.891234567890000);
if(intl_is_failure(numfmt_format($fmt))) {
    report_error("Formatter error");
}
?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::DECIMAL );
$fmt->format(1234567.891234567890000);
if(intl_is_failure($fmt->getErrorCode())) {
    report_error("Formatter error");
}
?>
```

以上例程会输出：

    1.234.567,891

### 参见

-   <span class="function">numfmt\_get\_error\_code</span>
-   <span class="function">numfmt\_format\_currency</span>
-   <span class="function">numfmt\_parse</span>

NumberFormatter::getAttribute
=============================

numfmt\_get\_attribute
======================

Get an attribute

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">NumberFormatter::getAttribute</span> ( <span
class="methodparam"><span class="type">int</span> `$attr`</span> )

过程化风格

<span class="type">int</span> <span
class="methodname">numfmt\_get\_attribute</span> ( <span
class="methodparam"><span class="type">NumberFormatter</span>
`$fmt`</span> , <span class="methodparam"><span class="type">int</span>
`$attr`</span> )

Get a numeric attribute associated with the formatter. An example of a
numeric attribute is the number of integer digits the formatter will
produce.

### 参数

`fmt`  
<span class="classname">NumberFormatter</span> object.

`attr`  
Attribute specifier - one of the
<a href="/class/numberformatter.html#" class="link">numeric attribute</a>
constants.

### 返回值

Return attribute value on success, or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">numfmt\_get\_attribute</span>
example**

``` php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::DECIMAL );
echo "Digits: ".numfmt_get_attribute($fmt, NumberFormatter::MAX_FRACTION_DIGITS)."\n";
echo numfmt_format($fmt, 1234567.891234567890000)."\n";
numfmt_set_attribute($fmt, NumberFormatter::MAX_FRACTION_DIGITS, 2);
echo "Digits: ".numfmt_get_attribute($fmt, NumberFormatter::MAX_FRACTION_DIGITS)."\n";
echo numfmt_format($fmt, 1234567.891234567890000)."\n";
?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::DECIMAL );
echo "Digits: ".$fmt->getAttribute(NumberFormatter::MAX_FRACTION_DIGITS)."\n";
echo $fmt->format(1234567.891234567890000)."\n";
$fmt->setAttribute(NumberFormatter::MAX_FRACTION_DIGITS, 2);
echo "Digits: ".$fmt->getAttribute(NumberFormatter::MAX_FRACTION_DIGITS)."\n";
echo $fmt->format(1234567.891234567890000)."\n";
?>
```

以上例程会输出：

    Digits: 3
    1.234.567,891
    Digits: 2
    1.234.567,89

### 参见

-   <span class="function">numfmt\_get\_error\_code</span>
-   <span class="function">numfmt\_get\_text\_attribute</span>
-   <span class="function">numfmt\_set\_attribute</span>

NumberFormatter::getErrorCode
=============================

numfmt\_get\_error\_code
========================

Get formatter's last error code

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">NumberFormatter::getErrorCode</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">int</span> <span
class="methodname">numfmt\_get\_error\_code</span> ( <span
class="methodparam"><span class="type">NumberFormatter</span>
`$fmt`</span> )

Get error code from the last function performed by the formatter.

### 参数

`fmt`  
<span class="classname">NumberFormatter</span> object.

### 返回值

Returns error code from last formatter call.

### 范例

**示例 \#1 <span class="function">numfmt\_get\_error\_code</span>
example**

``` php
<?php
$fmt  = numfmt_create( 'de_DE', NumberFormatter::DECIMAL );
$data = numfmt_format($fmt, 1234567.891234567890000);
if(intl_is_failure(numfmt_get_error_code($fmt))) {
    report_error("Formatter error");
}
?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::DECIMAL );
$fmt->format(1234567.891234567890000);
if(intl_is_failure($fmt->getErrorCode())) {
    report_error("Formatter error");
}
?>
```

### 参见

-   <span class="function">numfmt\_get\_error\_message</span>
-   <span class="function">intl\_get\_error\_code</span>
-   <span class="function">intl\_is\_failure</span>

NumberFormatter::getErrorMessage
================================

numfmt\_get\_error\_message
===========================

Get formatter's last error message

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">NumberFormatter::getErrorMessage</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">string</span> <span
class="methodname">numfmt\_get\_error\_message</span> ( <span
class="methodparam"><span class="type">NumberFormatter</span>
`$fmt`</span> )

Get error message from the last function performed by the formatter.

### 参数

`fmt`  
<span class="classname">NumberFormatter</span> object.

### 返回值

Returns error message from last formatter call.

### 范例

**示例 \#1 <span class="function">numfmt\_get\_error\_message</span>
example**

``` php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::DECIMAL );
$data = numfmt_format($fmt, 1234567.891234567890000);
var_dump(numfmt_get_error_message($fmt));
?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::DECIMAL );
$fmt->format(1234567.891234567890000);
var_dump(numfmt_get_error_message($fmt));
?>
```

### 参见

-   <span class="function">numfmt\_get\_error\_code</span>
-   <span class="function">intl\_get\_error\_code</span>
-   <span class="function">intl\_is\_failure</span>

NumberFormatter::getLocale
==========================

numfmt\_get\_locale
===================

Get formatter locale

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">NumberFormatter::getLocale</span> (\[ <span
class="methodparam"><span class="type">int</span> `$type`</span> \] )

过程化风格

<span class="type">string</span> <span
class="methodname">numfmt\_get\_locale</span> ( <span
class="methodparam"><span class="type">NumberFormatter</span>
`$fmt`</span> \[, <span class="methodparam"><span
class="type">int</span> `$type`</span> \] )

Get formatter locale name.

### 参数

`fmt`  
<span class="classname">NumberFormatter</span> object.

`type`  
You can choose between valid and actual locale (
**`Locale::VALID_LOCALE`**, **`Locale::ACTUAL_LOCALE`**, respectively).
The default is the actual locale.

### 返回值

The locale name used to create the formatter.

### 范例

**示例 \#1 <span class="function">numfmt\_get\_locale</span> example**

``` php
<?php
$req     = 'fr_FR_PARIS';
$fmt     = numfmt_create( $req,  NumberFormatter::DECIMAL);
$res_val = numfmt_get_locale( $fmt, Locale::VALID_LOCALE );
$res_act = numfmt_get_locale( $fmt, Locale::ACTUAL_LOCALE );
printf( "Requested locale name: %s\nValid locale name: %s\nActual locale name: %s\n",
         $req, $res_val, $res_act );
?>
```

以上例程会输出：

    Requested locale name: fr_FR_PARIS
    Valid locale name: fr_FR
    Actual locale name: fr

### 参见

-   <span class="function">numfmt\_create</span>
-   <span class="function">numfmt\_get\_error\_code</span>

NumberFormatter::getPattern
===========================

numfmt\_get\_pattern
====================

Get formatter pattern

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">NumberFormatter::getPattern</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">string</span> <span
class="methodname">numfmt\_get\_pattern</span> ( <span
class="methodparam"><span class="type">NumberFormatter</span>
`$fmt`</span> )

Extract pattern used by the formatter.

### 参数

`fmt`  
<span class="classname">NumberFormatter</span> object.

### 返回值

Pattern <span class="type">string</span> that is used by the formatter,
or **`FALSE`** if an error happens.

### 范例

**示例 \#1 <span class="function">numfmt\_get\_pattern</span> example**

``` php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::DECIMAL );
echo "Pattern: ".numfmt_get_pattern($fmt)."\n";
echo numfmt_format($fmt, 1234567.891234567890000)."\n";
numfmt_set_pattern($fmt, "#0.# kg");
echo "Pattern: ".numfmt_get_pattern($fmt)."\n";
echo numfmt_format($fmt, 1234567.891234567890000)."\n";
?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::DECIMAL );
echo "Pattern: ".$fmt->getPattern()."\n";
echo $fmt->format(1234567.891234567890000)."\n";
$fmt->setPattern("#0.# kg");
echo "Pattern: ".$fmt->getPattern()."\n";
echo $fmt->format(1234567.891234567890000)."\n";
?>
```

以上例程会输出：

    Pattern: #,##0.###
    1.234.567,891
    Pattern: #0.# kg
    1234567,9 kg

### 参见

-   <span class="function">numfmt\_get\_error\_code</span>
-   <span class="function">numfmt\_set\_pattern</span>
-   <span class="function">numfmt\_create</span>

NumberFormatter::getSymbol
==========================

numfmt\_get\_symbol
===================

Get a symbol value

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">NumberFormatter::getSymbol</span> ( <span
class="methodparam"><span class="type">int</span> `$attr`</span> )

过程化风格

<span class="type">string</span> <span
class="methodname">numfmt\_get\_symbol</span> ( <span
class="methodparam"><span class="type">NumberFormatter</span>
`$fmt`</span> , <span class="methodparam"><span class="type">int</span>
`$attr`</span> )

Get a symbol associated with the formatter. The formatter uses symbols
to represent the special locale-dependent characters in a number, for
example the percent sign. This API is not supported for rule-based
formatters.

### 参数

`fmt`  
<span class="classname">NumberFormatter</span> object.

`attr`  
Symbol specifier, one of the
<a href="/class/numberformatter.html#" class="link">format symbol</a>
constants.

### 返回值

The symbol string or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">numfmt\_get\_symbol</span> example**

``` php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::DECIMAL );
echo "Sep: ".numfmt_get_symbol($fmt, NumberFormatter::GROUPING_SEPARATOR_SYMBOL)."\n";
echo numfmt_format($fmt, 1234567.891234567890000)."\n";
numfmt_set_symbol($fmt, NumberFormatter::GROUPING_SEPARATOR_SYMBOL, "*");
echo "Sep: ".numfmt_get_symbol($fmt, NumberFormatter::GROUPING_SEPARATOR_SYMBOL)."\n";
echo numfmt_format($fmt, 1234567.891234567890000)."\n";
?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::DECIMAL );
echo "Sep: ".$fmt->getSymbol(NumberFormatter::GROUPING_SEPARATOR_SYMBOL)."\n";
echo $fmt->format(1234567.891234567890000)."\n";
$fmt->setSymbol(NumberFormatter::GROUPING_SEPARATOR_SYMBOL, "*");
echo "Sep: ".$fmt->getSymbol(NumberFormatter::GROUPING_SEPARATOR_SYMBOL)."\n";
echo $fmt->format(1234567.891234567890000)."\n";
?>
```

以上例程会输出：

    Sep: .
    1.234.567,891
    Sep: *
    1*234*567,891

### 参见

-   <span class="function">numfmt\_get\_error\_code</span>
-   <span class="function">numfmt\_set\_symbol</span>

NumberFormatter::getTextAttribute
=================================

numfmt\_get\_text\_attribute
============================

Get a text attribute

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">NumberFormatter::getTextAttribute</span> (
<span class="methodparam"><span class="type">int</span> `$attr`</span> )

过程化风格

<span class="type">string</span> <span
class="methodname">numfmt\_get\_text\_attribute</span> ( <span
class="methodparam"><span class="type">NumberFormatter</span>
`$fmt`</span> , <span class="methodparam"><span class="type">int</span>
`$attr`</span> )

Get a text attribute associated with the formatter. An example of a text
attribute is the suffix for positive numbers. If the formatter does not
understand the attribute, **`U_UNSUPPORTED_ERROR`** error is produced.
Rule-based formatters only understand
**`NumberFormatter::DEFAULT_RULESET`** and
**`NumberFormatter::PUBLIC_RULESETS`**.

### 参数

`fmt`  
<span class="classname">NumberFormatter</span> object.

`attr`  
Attribute specifier - one of the
<a href="/class/numberformatter.html#" class="link">text attribute</a>
constants.

### 返回值

Return attribute value on success, or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">numfmt\_get\_text\_attribute</span>
example**

``` php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::DECIMAL );
echo "Prefix: ".numfmt_get_text_attribute($fmt, NumberFormatter::NEGATIVE_PREFIX)."\n";
echo numfmt_format($fmt, -1234567.891234567890000)."\n";
numfmt_set_text_attribute($fmt, NumberFormatter::NEGATIVE_PREFIX, "MINUS");
echo "Prefix: ".numfmt_get_text_attribute($fmt, NumberFormatter::NEGATIVE_PREFIX)."\n";
echo numfmt_format($fmt, -1234567.891234567890000)."\n";
?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::DECIMAL );
echo "Prefix: ".$fmt->getTextAttribute(NumberFormatter::NEGATIVE_PREFIX)."\n";
echo $fmt->format(-1234567.891234567890000)."\n";
$fmt->setTextAttribute(NumberFormatter::NEGATIVE_PREFIX, "MINUS");
echo "Prefix: ".$fmt->getTextAttribute(NumberFormatter::NEGATIVE_PREFIX)."\n";
echo $fmt->format(-1234567.891234567890000)."\n";
?>
```

以上例程会输出：

    Prefix: -
    -1.234.567,891
    Prefix: MINUS
    MINUS1.234.567,891

### 参见

-   <span class="function">numfmt\_get\_error\_code</span>
-   <span class="function">numfmt\_get\_attribute</span>
-   <span class="function">numfmt\_set\_text\_attribute</span>

NumberFormatter::parseCurrency
==============================

numfmt\_parse\_currency
=======================

Parse a currency number

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">float</span>
<span class="methodname">NumberFormatter::parseCurrency</span> ( <span
class="methodparam"><span class="type">string</span> `$value`</span> ,
<span class="methodparam"><span class="type">string</span>
`&$currency`</span> \[, <span class="methodparam"><span
class="type">int</span> `&$position`</span> \] )

过程化风格

<span class="type">float</span> <span
class="methodname">numfmt\_parse\_currency</span> ( <span
class="methodparam"><span class="type">NumberFormatter</span>
`$fmt`</span> , <span class="methodparam"><span
class="type">string</span> `$value`</span> , <span
class="methodparam"><span class="type">string</span> `&$currency`</span>
\[, <span class="methodparam"><span class="type">int</span>
`&$position`</span> \] )

Parse a string into a double and a currency using the current formatter.

### 参数

`fmt`  
<span class="classname">NumberFormatter</span> object.

`currency`  
Parameter to receive the currency name (3-letter ISO 4217 currency
code).

`position`  
Offset in the string at which to begin parsing. On return, this value
will hold the offset at which parsing ended.

### 返回值

The parsed numeric value or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">numfmt\_parse\_currency</span>
example**

``` php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::CURRENCY );
$num = "1.234.567,89\xc2\xa0$";
echo "We have ".numfmt_parse_currency($fmt, $num, $curr)." in $curr\n";
?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::CURRENCY );
$num = "1.234.567,89\xc2\xa0$";
echo "We have ".$fmt->parseCurrency($num, $curr)." in $curr\n";
?>
```

以上例程会输出：

    We have 1234567.89 in USD

### 参见

-   <span class="function">numfmt\_get\_error\_code</span>
-   <span class="function">numfmt\_parse</span>
-   <span class="function">numfmt\_format\_currency</span>

NumberFormatter::parse
======================

numfmt\_parse
=============

Parse a number

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">NumberFormatter::parse</span> ( <span
class="methodparam"><span class="type">string</span> `$value`</span> \[,
<span class="methodparam"><span class="type">int</span> `$type`</span>
\[, <span class="methodparam"><span class="type">int</span>
`&$position`</span> \]\] )

过程化风格

<span class="type">mixed</span> <span
class="methodname">numfmt\_parse</span> ( <span
class="methodparam"><span class="type">NumberFormatter</span>
`$fmt`</span> , <span class="methodparam"><span
class="type">string</span> `$value`</span> \[, <span
class="methodparam"><span class="type">int</span> `$type`</span> \[,
<span class="methodparam"><span class="type">int</span>
`&$position`</span> \]\] )

Parse a string into a number using the current formatter rules.

### 参数

`fmt`  
<span class="classname">NumberFormatter</span> object.

`type`  
The
<a href="/class/numberformatter.html#" class="link">formatting type</a>
to use. By default, **`NumberFormatter::TYPE_DOUBLE`** is used.

`position`  
Offset in the string at which to begin parsing. On return, this value
will hold the offset at which parsing ended.

### 返回值

The value of the parsed number or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">numfmt\_parse</span> example**

``` php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::DECIMAL );
$num = "1.234.567,891";
echo numfmt_parse($fmt, $num)."\n";
echo numfmt_parse($fmt, $num, NumberFormatter::TYPE_INT32)."\n";
?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::DECIMAL );
$num = "1.234.567,891";
echo $fmt->parse($num)."\n";
echo $fmt->parse($num, NumberFormatter::TYPE_INT32)."\n";
?>
```

以上例程会输出：

    1234567.891
    1234567

### 参见

-   <span class="function">numfmt\_get\_error\_code</span>
-   <span class="function">numfmt\_format</span>
-   <span class="function">numfmt\_parse\_currency</span>

NumberFormatter::setAttribute
=============================

numfmt\_set\_attribute
======================

Set an attribute

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">NumberFormatter::setAttribute</span> ( <span
class="methodparam"><span class="type">int</span> `$attr`</span> , <span
class="methodparam"><span class="type">int</span> `$value`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">numfmt\_set\_attribute</span> ( <span
class="methodparam"><span class="type">NumberFormatter</span>
`$fmt`</span> , <span class="methodparam"><span class="type">int</span>
`$attr`</span> , <span class="methodparam"><span class="type">int</span>
`$value`</span> )

Set a numeric attribute associated with the formatter. An example of a
numeric attribute is the number of integer digits the formatter will
produce.

### 参数

`fmt`  
<span class="classname">NumberFormatter</span> object.

`attr`  
Attribute specifier - one of the
<a href="/class/numberformatter.html#" class="link">numeric attribute</a>
constants.

`value`  
The attribute value.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">numfmt\_set\_attribute</span>
example**

``` php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::DECIMAL );
echo "Digits: ".numfmt_get_attribute($fmt, NumberFormatter::MAX_FRACTION_DIGITS)."\n";
echo numfmt_format($fmt, 1234567.891234567890000)."\n";
numfmt_set_attribute($fmt, NumberFormatter::MAX_FRACTION_DIGITS, 2);
echo "Digits: ".numfmt_get_attribute($fmt, NumberFormatter::MAX_FRACTION_DIGITS)."\n";
echo numfmt_format($fmt, 1234567.891234567890000)."\n";
?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::DECIMAL );
echo "Digits: ".$fmt->getAttribute(NumberFormatter::MAX_FRACTION_DIGITS)."\n";
echo $fmt->format(1234567.891234567890000)."\n";
$fmt->setAttribute(NumberFormatter::MAX_FRACTION_DIGITS, 2);
echo "Digits: ".$fmt->getAttribute(NumberFormatter::MAX_FRACTION_DIGITS)."\n";
echo $fmt->format(1234567.891234567890000)."\n";
?>
```

以上例程会输出：

    Digits: 3
    1.234.567,891
    Digits: 2
    1.234.567,89

### 参见

-   <span class="function">numfmt\_get\_error\_code</span>
-   <span class="function">numfmt\_get\_attribute</span>
-   <span class="function">numfmt\_set\_text\_attribute</span>

NumberFormatter::setPattern
===========================

numfmt\_set\_pattern
====================

Set formatter pattern

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">NumberFormatter::setPattern</span> ( <span
class="methodparam"><span class="type">string</span> `$pattern`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">numfmt\_set\_pattern</span> ( <span
class="methodparam"><span class="type">NumberFormatter</span>
`$fmt`</span> , <span class="methodparam"><span
class="type">string</span> `$pattern`</span> )

Set the pattern used by the formatter. Can not be used on a rule-based
formatter.

### 参数

`fmt`  
<span class="classname">NumberFormatter</span> object.

`pattern`  
Pattern in syntax described in
<a href="http://www.icu-project.org/apiref/icu4c/classDecimalFormat.html#details" class="link external">» ICU DecimalFormat documentation</a>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">numfmt\_set\_pattern</span> example**

``` php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::DECIMAL );
echo "Pattern: ".numfmt_get_pattern($fmt)."\n";
echo numfmt_format($fmt, 1234567.891234567890000)."\n";
numfmt_set_pattern($fmt, "#0.# kg");
echo "Pattern: ".numfmt_get_pattern($fmt)."\n";
echo numfmt_format($fmt, 1234567.891234567890000)."\n";
?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::DECIMAL );
echo "Pattern: ".$fmt->getPattern()."\n";
echo $fmt->format(1234567.891234567890000)."\n";
$fmt->setPattern("#0.# kg");
echo "Pattern: ".$fmt->getPattern()."\n";
echo $fmt->format(1234567.891234567890000)."\n";
?>
```

以上例程会输出：

    Pattern: #,##0.###
    1.234.567,891
    Pattern: #0.# kg
    1234567,9 kg

### 参见

-   <span class="function">numfmt\_get\_error\_code</span>
-   <span class="function">numfmt\_create</span>
-   <span class="function">numfmt\_get\_pattern</span>

NumberFormatter::setSymbol
==========================

numfmt\_set\_symbol
===================

Set a symbol value

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">NumberFormatter::setSymbol</span> ( <span
class="methodparam"><span class="type">int</span> `$attr`</span> , <span
class="methodparam"><span class="type">string</span> `$value`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">numfmt\_set\_symbol</span> ( <span
class="methodparam"><span class="type">NumberFormatter</span>
`$fmt`</span> , <span class="methodparam"><span class="type">int</span>
`$attr`</span> , <span class="methodparam"><span
class="type">string</span> `$value`</span> )

Set a symbol associated with the formatter. The formatter uses symbols
to represent the special locale-dependent characters in a number, for
example the percent sign. This API is not supported for rule-based
formatters.

### 参数

`fmt`  
<span class="classname">NumberFormatter</span> object.

`attr`  
Symbol specifier, one of the
<a href="/class/numberformatter.html#" class="link">format symbol</a>
constants.

`value`  
Text for the symbol.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">numfmt\_set\_symbol</span> example**

``` php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::DECIMAL );
echo "Sep: ".numfmt_get_symbol($fmt, NumberFormatter::GROUPING_SEPARATOR_SYMBOL)."\n";
echo numfmt_format($fmt, 1234567.891234567890000)."\n";
numfmt_set_symbol($fmt, NumberFormatter::GROUPING_SEPARATOR_SYMBOL, "*");
echo "Sep: ".numfmt_get_symbol($fmt, NumberFormatter::GROUPING_SEPARATOR_SYMBOL)."\n";
echo numfmt_format($fmt, 1234567.891234567890000)."\n";
?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::DECIMAL );
echo "Sep: ".$fmt->getSymbol(NumberFormatter::GROUPING_SEPARATOR_SYMBOL)."\n";
echo $fmt->format(1234567.891234567890000)."\n";
$fmt->setSymbol(NumberFormatter::GROUPING_SEPARATOR_SYMBOL, "*");
echo "Sep: ".$fmt->getSymbol(NumberFormatter::GROUPING_SEPARATOR_SYMBOL)."\n";
echo $fmt->format(1234567.891234567890000)."\n";
?>
```

以上例程会输出：

    Sep: .
    1.234.567,891
    Sep: *
    1*234*567,891

### 参见

-   <span class="function">numfmt\_get\_error\_code</span>
-   <span class="function">numfmt\_get\_symbol</span>

NumberFormatter::setTextAttribute
=================================

numfmt\_set\_text\_attribute
============================

Set a text attribute

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">NumberFormatter::setTextAttribute</span> (
<span class="methodparam"><span class="type">int</span> `$attr`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">numfmt\_set\_text\_attribute</span> ( <span
class="methodparam"><span class="type">NumberFormatter</span>
`$fmt`</span> , <span class="methodparam"><span class="type">int</span>
`$attr`</span> , <span class="methodparam"><span
class="type">string</span> `$value`</span> )

Set a text attribute associated with the formatter. An example of a text
attribute is the suffix for positive numbers. If the formatter does not
understand the attribute, **`U_UNSUPPORTED_ERROR`** error is produced.
Rule-based formatters only understand
**`NumberFormatter::DEFAULT_RULESET`** and
**`NumberFormatter::PUBLIC_RULESETS`**.

### 参数

`fmt`  
<span class="classname">NumberFormatter</span> object.

`attr`  
Attribute specifier - one of the
<a href="/class/numberformatter.html#" class="link">text attribute</a>
constants.

`value`  
Text for the attribute value.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">numfmt\_set\_text\_attribute</span>
example**

``` php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::DECIMAL );
echo "Prefix: ".numfmt_get_text_attribute($fmt, NumberFormatter::NEGATIVE_PREFIX)."\n";
echo numfmt_format($fmt, -1234567.891234567890000)."\n";
numfmt_set_text_attribute($fmt, NumberFormatter::NEGATIVE_PREFIX, "MINUS");
echo "Prefix: ".numfmt_get_text_attribute($fmt, NumberFormatter::NEGATIVE_PREFIX)."\n";
echo numfmt_format($fmt, -1234567.891234567890000)."\n";
?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::DECIMAL );
echo "Prefix: ".$fmt->getTextAttribute(NumberFormatter::NEGATIVE_PREFIX)."\n";
echo $fmt->format(-1234567.891234567890000)."\n";
$fmt->setTextAttribute(NumberFormatter::NEGATIVE_PREFIX, "MINUS");
echo "Prefix: ".$fmt->getTextAttribute(NumberFormatter::NEGATIVE_PREFIX)."\n";
echo $fmt->format(-1234567.891234567890000)."\n";
?>
```

以上例程会输出：

    Prefix: -
    -1.234.567,891
    Prefix: MINUS
    MINUS1.234.567,891

### 参见

-   <span class="function">numfmt\_get\_error\_code</span>
-   <span class="function">numfmt\_get\_text\_attribute</span>
-   <span class="function">numfmt\_set\_attribute</span>

简介
----

A "Locale" is an identifier used to get language, culture, or
regionally-specific behavior from an API. PHP locales are organized and
identified the same way that the CLDR locales used by ICU (and many
vendors of Unix-like operating systems, the Mac, Java, and so forth)
use. Locales are identified using RFC 4646 language tags (which use
hyphen, not underscore) in addition to the more traditional
underscore-using identifiers. Unless otherwise noted the functions in
this class are tolerant of both formats.

Examples of identifiers include:

-   en-US (English, United States)
-   zh-Hant-TW (Chinese, Traditional Script, Taiwan)
-   fr-CA, fr-FR (French for Canada and France respectively)

The Locale class (and related procedural functions) are used to interact
with locale identifiers--to verify that an ID is well-formed, valid,
etc. The extensions used by CLDR in UAX \#35 (and inherited by ICU) are
valid and used wherever they would be in ICU normally.

Locales cannot be instantiated as objects. All of the functions/methods
provided are static.

The null or empty string obtains the "root" locale. The "root" locale is
equivalent to "en\_US\_POSIX" in CLDR. Language tags (and thus locale
identifiers) are case insensitive. There exists a canonicalization
function to make case match the specification.

类摘要
------

**Locale**

<span class="ooclass"> class **Locale** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">acceptFromHttp</span> ( <span
class="methodparam"><span class="type">string</span> `$header`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">canonicalize</span> ( <span class="methodparam"><span
class="type">string</span> `$locale`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">composeLocale</span> ( <span
class="methodparam"><span class="type">array</span> `$subtags`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">filterMatches</span> ( <span
class="methodparam"><span class="type">string</span> `$langtag`</span> ,
<span class="methodparam"><span class="type">string</span>
`$locale`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$canonicalize`<span class="initializer"> =
**`FALSE`**</span></span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">getAllVariants</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">getDefault</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">getDisplayLanguage</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$in_locale`</span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">getDisplayName</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$in_locale`</span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">getDisplayRegion</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$in_locale`</span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">getDisplayScript</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$in_locale`</span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">getDisplayVariant</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$in_locale`</span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">getKeywords</span> ( <span class="methodparam"><span
class="type">string</span> `$locale`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">getPrimaryLanguage</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">getRegion</span> ( <span class="methodparam"><span
class="type">string</span> `$locale`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">getScript</span> ( <span class="methodparam"><span
class="type">string</span> `$locale`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">lookup</span> ( <span class="methodparam"><span
class="type">array</span> `$langtag`</span> , <span
class="methodparam"><span class="type">string</span> `$locale`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$canonicalize`<span class="initializer"> = **`FALSE`**</span></span>
\[, <span class="methodparam"><span class="type">string</span>
`$default`</span> \]\] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">parseLocale</span> ( <span class="methodparam"><span
class="type">string</span> `$locale`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">setDefault</span> ( <span class="methodparam"><span
class="type">string</span> `$locale`</span> )

}

预定义常量
----------

**`Locale::DEFAULT_LOCALE`** (<span class="type">null</span>)  
<span class="simpara"> Used as locale parameter with the methods of the
various locale affected classes, such as NumberFormatter. This constant
would make the methods to use default locale. </span>

These constants describe the choice of the locale for the getLocale
method of different classes.

**`Locale::ACTUAL_LOCALE`** (<span class="type">string</span>)  
<span class="simpara">This is locale the data actually comes
from.</span>

**`Locale::VALID_LOCALE`** (<span class="type">string</span>)  
<span class="simpara">This is the most specific locale supported by
ICU.</span>

These constants define how the Locales are parsed or composed. They
should be used as keys in the argument array to <span
class="function">locale\_compose</span> and are returned from <span
class="function">locale\_parse</span> as keys of the returned
associative <span class="type">array</span>.

**`Locale::LANG_TAG`** (<span class="type">string</span>)  
<span class="simpara">Language subtag</span>

**`Locale::EXTLANG_TAG`** (<span class="type">string</span>)  
<span class="simpara">Extended language subtag</span>

**`Locale::SCRIPT_TAG`** (<span class="type">string</span>)  
<span class="simpara">Script subtag</span>

**`Locale::REGION_TAG`** (<span class="type">string</span>)  
<span class="simpara">Region subtag</span>

**`Locale::VARIANT_TAG`** (<span class="type">string</span>)  
<span class="simpara">Variant subtag</span>

**`Locale::GRANDFATHERED_LANG_TAG`** (<span class="type">string</span>)  
<span class="simpara">Grandfathered Language subtag</span>

**`Locale::PRIVATE_TAG`** (<span class="type">string</span>)  
<span class="simpara">Private subtag</span>

参见
----

-   <a href="http://www.faqs.org/rfcs/rfc4646" class="link external">» RFC 4646 - Tags for Identifying Languages</a>
-   <a href="http://www.faqs.org/rfcs/rfc4647" class="link external">» RFC 4647 - Matching of Language Tags</a>
-   <a href="http://www.unicode.org/cldr/" class="link external">» Unicode CLDR Project:Common Locale Data Repository</a>
-   <a href="http://www.iana.org/assignments/language-subtag-registry" class="link external">» IANA Language Subtags Registry</a>
-   <a href="http://www.icu-project.org/userguide/locale.html" class="link external">» ICU User Guide - Locale</a>
-   <a href="http://www.icu-project.org/apiref/icu4c/uloc_8h.html#details" class="link external">» ICU Locale api</a>

Locale::acceptFromHttp
======================

locale\_accept\_from\_http
==========================

Tries to find out best available locale based on HTTP "Accept-Language"
header

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">Locale::acceptFromHttp</span> ( <span
class="methodparam"><span class="type">string</span> `$header`</span> )

过程化风格

<span class="type">string</span> <span
class="methodname">locale\_accept\_from\_http</span> ( <span
class="methodparam"><span class="type">string</span> `$header`</span> )

Tries to find locale that can satisfy the language list that is
requested by the HTTP "Accept-Language" header.

### 参数

`header`  
The string containing the "Accept-Language" header according to format
in RFC 2616.

### 返回值

The corresponding locale identifier.

### 范例

**示例 \#1 <span class="function">locale\_accept\_from\_http</span>
example**

``` php
<?php
$locale = locale_accept_from_http($_SERVER['HTTP_ACCEPT_LANGUAGE']);
echo $locale;
?>
```

**示例 \#2 OO example**

``` php
<?php
$locale = Locale::acceptFromHttp($_SERVER['HTTP_ACCEPT_LANGUAGE']);
echo $locale;
?>
```

以上例程会输出：

    en_US

### 参见

-   <span class="function">locale\_lookup</span>

Locale::canonicalize
====================

locale\_canonicalize
====================

Canonicalize the locale string

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">Locale::canonicalize</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`locale`  

### 返回值

Locale::composeLocale
=====================

locale\_compose
===============

Returns a correctly ordered and delimited locale ID

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">Locale::composeLocale</span> ( <span
class="methodparam"><span class="type">array</span> `$subtags`</span> )

过程化风格

<span class="type">string</span> <span
class="methodname">locale\_compose</span> ( <span
class="methodparam"><span class="type">array</span> `$subtags`</span> )

Returns a correctly ordered and delimited locale ID the keys identify
the particular locale ID subtags, and the values are the associated
subtag values.

### 参数

`subtags`  
an array containing a list of key-value pairs, where the keys identify
the particular locale ID subtags, and the values are the associated
subtag values.

> **Note**:
>
> The 'variant' and 'private' subtags can take maximum 15 values whereas
> 'extlang' can take maximum 3 values.e.g. Variants are allowed with the
> suffix ranging from 0-14. Hence the keys for the input array can be
> variant0, variant1, ...,variant14. In the returned locale id, the
> subtag is ordered by suffix resulting in variant0 followed by variant1
> followed by variant2 and so on.
>
> The 'variant', 'private' and 'extlang' multiple values can be
> specified both as array under specific key (e.g. 'variant') and as
> multiple numbered keys (e.g. 'variant0', 'variant1', etc.).

### 返回值

The corresponding locale identifier.

### 范例

**示例 \#1 <span class="function">locale\_compose</span> example**

``` php
<?php
$arr = array(
    'language'=>'en' ,
    'script'  =>'Hans' ,
    'region'  =>'CN',
    'variant2'=>'rozaj' ,
    'variant1'=>'nedis' ,
    'private1'=>'prv1' ,
    'private2'=>'prv2'
);
echo locale_compose( $arr );
?>
```

**示例 \#2 OO example**

``` php
<?php
$arr = array(
    'language'=>'en' ,
    'script'  =>'Hans' ,
    'region'  =>'CN',
    'variant2'=>'rozaj' ,
    'variant1'=>'nedis' ,
    'private1'=>'prv1' ,
    'private2'=>'prv2'
);
echo Locale::composeLocale( $arr );
?>
```

以上例程会输出：

    Locale: en_Hans_CN_nedis_rozaj_x_prv1_prv2

### 参见

-   <span class="function">locale\_parse</span>

Locale::filterMatches
=====================

locale\_filter\_matches
=======================

Checks if a language tag filter matches with locale

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">Locale::filterMatches</span> ( <span
class="methodparam"><span class="type">string</span> `$langtag`</span> ,
<span class="methodparam"><span class="type">string</span>
`$locale`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$canonicalize`<span class="initializer"> =
**`FALSE`**</span></span> \] )

过程化风格

<span class="type">bool</span> <span
class="methodname">locale\_filter\_matches</span> ( <span
class="methodparam"><span class="type">string</span> `$langtag`</span> ,
<span class="methodparam"><span class="type">string</span>
`$locale`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$canonicalize`<span class="initializer"> =
**`FALSE`**</span></span> \] )

Checks if a $langtag filter matches with $locale according to RFC 4647's
basic filtering algorithm

### 参数

`langtag`  
The language tag to check

`locale`  
The language range to check against

`canonicalize`  
If true, the arguments will be converted to canonical form before
matching.

### 返回值

**`TRUE`** if $locale matches $langtag **`FALSE`** otherwise.

### 范例

**示例 \#1 <span class="function">locale\_filter\_matches</span>
example**

``` php
<?php
echo (locale_filter_matches('de-DEVA','de-DE', false)) ? "Matches" : "Does not match"; 
echo '; ';
echo (locale_filter_matches('de-DE_1996','de-DE', false)) ? "Matches" : "Does not match"; 
?>
```

**示例 \#2 OO example**

``` php
<?php
echo (Locale::filterMatches('de-DEVA','de-DE', false)) ? "Matches" : "Does not match"; 
echo '; ';
echo (Locale::filterMatches('de-DE-1996','de-DE', false)) ? "Matches" : "Does not match"; 
?>
```

以上例程会输出：

    Does not match; Matches

### 参见

-   <span class="function">locale\_lookup</span>

Locale::getAllVariants
======================

locale\_get\_all\_variants
==========================

Gets the variants for the input locale

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">Locale::getAllVariants</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> )

过程化风格

<span class="type">array</span> <span
class="methodname">locale\_get\_all\_variants</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> )

Gets the variants for the input locale

### 参数

`locale`  
The locale to extract the variants from

### 返回值

The <span class="type">array</span> containing the list of all variants
subtag for the locale or **`NULL`** if not present

### 范例

**示例 \#1 <span class="function">locale\_get\_all\_variants</span>
example**

``` php
<?php
$arr = locale_get_all_variants('sl_IT_NEDIS_ROJAZ_1901');
var_export( $arr );
?>
```

**示例 \#2 OO example**

``` php
<?php
 $arr = Locale::getAllVariants('sl_IT_NEDIS_ROJAZ_1901');
 var_export( $arr );
?>
```

以上例程会输出：

    array (
        0 => 'NEDIS',
        1 => 'ROJAZ',
        2 => '1901',
    )

### 参见

-   <span class="function">locale\_get\_primary\_language</span>
-   <span class="function">locale\_get\_script</span>
-   <span class="function">locale\_get\_region</span>

Locale::getDefault
==================

locale\_get\_default
====================

Gets the default locale value from the INTL global 'default\_locale'

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">Locale::getDefault</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">string</span> <span
class="methodname">locale\_get\_default</span> ( <span
class="methodparam">void</span> )

Gets the default locale value. At the PHP initialization this value is
set to 'intl.default\_locale' value from `php.ini` if that value exists
or from ICU's function uloc\_getDefault().

### 参数

### 返回值

The current runtime locale

### 范例

**示例 \#1 <span class="function">locale\_get\_default</span> example**

``` php
<?php
ini_set('intl.default_locale', 'de-DE');
echo locale_get_default();
echo '; ';
locale_set_default('fr');
echo locale_get_default();
?>
```

**示例 \#2 OO example**

``` php
<?php
ini_set('intl.default_locale', 'de-DE');
echo Locale::getDefault();
echo '; ';
Locale::setDefault('fr');
echo Locale::getDefault();
?>
```

以上例程会输出：

    de-DE; fr

### 参见

-   <span class="function">locale\_set\_default</span>

Locale::getDisplayLanguage
==========================

locale\_get\_display\_language
==============================

Returns an appropriately localized display name for language of the
inputlocale

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">Locale::getDisplayLanguage</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$in_locale`</span> \] )

过程化风格

<span class="type">string</span> <span
class="methodname">locale\_get\_display\_language</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$in_locale`</span> \] )

Returns an appropriately localized display name for language of the
input locale. If is **`NULL`** then the default locale is used.

### 参数

`locale`  
The locale to return a display language for

`in_locale`  
Optional format locale to use to display the language name

### 返回值

display name of the language for the $locale in the format appropriate
for $in\_locale.

### 范例

**示例 \#1 <span class="function">locale\_get\_display\_language</span>
example**

``` php
<?php
echo locale_get_display_language('sl-Latn-IT-nedis', 'en');
echo ";\n";
echo locale_get_display_language('sl-Latn-IT-nedis', 'fr');
echo ";\n";
echo locale_get_display_language('sl-Latn-IT-nedis', 'de');
?>
```

**示例 \#2 OO example**

``` php
<?php
echo Locale::getDisplayLanguage('sl-Latn-IT-nedis', 'en');
echo ";\n";
echo Locale::getDisplayLanguage('sl-Latn-IT-nedis', 'fr');
echo ";\n";
echo Locale::getDisplayLanguage('sl-Latn-IT-nedis', 'de');
?>
```

以上例程会输出：

    Slovenian;
    slov\xc3\xa8ne;
    Slowenisch

### 参见

-   <span class="function">locale\_get\_display\_name</span>
-   <span class="function">locale\_get\_display\_script</span>
-   <span class="function">locale\_get\_display\_region</span>
-   <span class="function">locale\_get\_display\_variant</span>

Locale::getDisplayName
======================

locale\_get\_display\_name
==========================

Returns an appropriately localized display name for the input locale

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">Locale::getDisplayName</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$in_locale`</span> \] )

过程化风格

<span class="type">string</span> <span
class="methodname">locale\_get\_display\_name</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$in_locale`</span> \] )

Returns an appropriately localized display name for the input locale. If
$locale is **`NULL`** then the default locale is used.

### 参数

`locale`  
The locale to return a display name for.

`in_locale`  
optional format locale

### 返回值

Display name of the locale in the format appropriate for $in\_locale.

### 范例

**示例 \#1 <span class="function">locale\_get\_display\_name</span>
example**

``` php
<?php
echo locale_get_display_name('sl-Latn-IT-nedis', 'en');
echo ";\n";
echo locale_get_display_name('sl-Latn-IT-nedis', 'fr');
echo ";\n";
echo locale_get_display_name('sl-Latn-IT-nedis', 'de');
?>
```

**示例 \#2 OO example**

``` php
<?php
echo Locale::getDisplayName('sl-Latn-IT-nedis', 'en');
echo ";\n";
echo Locale::getDisplayName('sl-Latn-IT-nedis', 'fr');
echo ";\n";
echo Locale::getDisplayName('sl-Latn-IT-nedis', 'de');
?>
```

以上例程会输出：

    Slovenian (Latin, Italy, Natisone dialect);
    slov\xc3\xa8ne (latin, Italie, dialecte de Natisone;
    Slowenisch (Lateinisch, Italien, NEDIS)
      

### 参见

-   <span class="function">locale\_get\_display\_language</span>
-   <span class="function">locale\_get\_display\_script</span>
-   <span class="function">locale\_get\_display\_region</span>
-   <span class="function">locale\_get\_display\_variant</span>

Locale::getDisplayRegion
========================

locale\_get\_display\_region
============================

Returns an appropriately localized display name for region of the input
locale

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">Locale::getDisplayRegion</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$in_locale`</span> \] )

过程化风格

<span class="type">string</span> <span
class="methodname">locale\_get\_display\_region</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$in_locale`</span> \] )

Returns an appropriately localized display name for region of the input
locale. If is **`NULL`** then the default locale is used.

### 参数

`locale`  
The locale to return a display region for.

`in_locale`  
Optional format locale to use to display the region name

### 返回值

display name of the region for the $locale in the format appropriate for
$in\_locale.

### 范例

**示例 \#1 <span class="function">locale\_get\_display\_region</span>
example**

``` php
<?php
echo locale_get_display_region('sl-Latn-IT-nedis', 'en');
echo ";\n";
echo locale_get_display_region('sl-Latn-IT-nedis', 'fr');
echo ";\n";
echo locale_get_display_region('sl-Latn-IT-nedis', 'de');
?>
```

**示例 \#2 OO example**

``` php
<?php
echo Locale::getDisplayRegion('sl-Latn-IT-nedis', 'en');
echo ";\n";
echo Locale::getDisplayRegion('sl-Latn-IT-nedis', 'fr');
echo ";\n";
echo Locale::getDisplayRegion('sl-Latn-IT-nedis', 'de');
?>
```

以上例程会输出：

    Italy;
    Italie;
    Italien

### 参见

-   <span class="function">locale\_get\_display\_name</span>
-   <span class="function">locale\_get\_display\_language</span>
-   <span class="function">locale\_get\_display\_script</span>
-   <span class="function">locale\_get\_display\_variant</span>

Locale::getDisplayScript
========================

locale\_get\_display\_script
============================

Returns an appropriately localized display name for script of the input
locale

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">Locale::getDisplayScript</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$in_locale`</span> \] )

过程化风格

<span class="type">string</span> <span
class="methodname">locale\_get\_display\_script</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$in_locale`</span> \] )

Returns an appropriately localized display name for script of the input
locale. If is **`NULL`** then the default locale is used.

### 参数

`locale`  
The locale to return a display script for

`in_locale`  
Optional format locale to use to display the script name

### 返回值

Display name of the script for the $locale in the format appropriate for
$in\_locale.

### 范例

**示例 \#1 <span class="function">locale\_get\_display\_script</span>
example**

``` php
<?php
echo locale_get_display_script('sl-Latn-IT-nedis', 'en');
echo ";\n";
echo locale_get_display_script('sl-Latn-IT-nedis', 'fr');
echo ";\n";
echo locale_get_display_script('sl-Latn-IT-nedis', 'de');
?>
```

**示例 \#2 OO example**

``` php
<?php
echo Locale::getDisplayScript('sl-Latn-IT-nedis', 'en');
echo ";\n";
echo Locale::getDisplayScript('sl-Latn-IT-nedis', 'fr');
echo ";\n";
echo Locale::getDisplayScript('sl-Latn-IT-nedis', 'de');
?>
```

以上例程会输出：

    Latin;
    latin;
    Lateinisch

### 参见

-   <span class="function">locale\_get\_display\_name</span>
-   <span class="function">locale\_get\_display\_language</span>
-   <span class="function">locale\_get\_display\_region</span>
-   <span class="function">locale\_get\_display\_variant</span>

Locale::getDisplayVariant
=========================

locale\_get\_display\_variant
=============================

Returns an appropriately localized display name for variants of the
input locale

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">Locale::getDisplayVariant</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$in_locale`</span> \] )

过程化风格

<span class="type">string</span> <span
class="methodname">locale\_get\_display\_variant</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$in_locale`</span> \] )

Returns an appropriately localized display name for variants of the
input locale. If is **`NULL`** then the default locale is used.

### 参数

`locale`  
The locale to return a display variant for

`in_locale`  
Optional format locale to use to display the variant name

### 返回值

Display name of the variant for the $locale in the format appropriate
for $in\_locale.

### 范例

**示例 \#1 <span class="function">locale\_get\_display\_variant</span>
example**

``` php
<?php
echo locale_get_display_variant('sl-Latn-IT-nedis', 'en');
echo ";\n";
echo locale_get_display_variant('sl-Latn-IT-nedis', 'fr');
echo ";\n";
echo locale_get_display_variant('sl-Latn-IT-nedis', 'de');
?>
```

**示例 \#2 OO example**

``` php
<?php
echo Locale::getDisplayVariant('sl-Latn-IT-nedis', 'en');
echo ";\n";
echo Locale::getDisplayVariant('sl-Latn-IT-nedis', 'fr');
echo ";\n";
echo Locale::getDisplayVariant('sl-Latn-IT-nedis', 'de');
?>
```

以上例程会输出：

    Natisone dialect;
    dialecte de Natisone;
    NEDIS
      

### 参见

-   <span class="function">locale\_get\_display\_name</span>
-   <span class="function">locale\_get\_display\_language</span>
-   <span class="function">locale\_get\_display\_script</span>
-   <span class="function">locale\_get\_display\_region</span>

Locale::getKeywords
===================

locale\_get\_keywords
=====================

Gets the keywords for the input locale

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">Locale::getKeywords</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> )

过程化风格

<span class="type">array</span> <span
class="methodname">locale\_get\_keywords</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> )

Gets the keywords for the input locale.

### 参数

`locale`  
The locale to extract the keywords from

### 返回值

Associative <span class="type">array</span> containing the keyword-value
pairs for this locale

### 范例

**示例 \#1 <span class="function">locale\_get\_keywords</span> example**

``` php
<?php
$keywords_arr = locale_get_keywords( 'de_DE@currency=EUR;collation=PHONEBOOK' );
if ($keywords_arr) {
    foreach ($keywords_arr as $key => $value) {
        echo "$key = $value\n"; 
    }
}
?>
```

**示例 \#2 OO example**

``` php
<?php
$keywords_arr = Locale::getKeywords( 'de_DE@currency=EUR;collation=PHONEBOOK' );
if ($keywords_arr) {
    foreach( $keywords_arr as $key => $value){
        echo "$key = $value\n"; 
    }
}
?>
```

以上例程会输出：

    collation = PHONEBOOK
    currency = EUR

### 参见

-   <span class="function">locale\_get\_all\_variants</span>

Locale::getPrimaryLanguage
==========================

locale\_get\_primary\_language
==============================

Gets the primary language for the input locale

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">Locale::getPrimaryLanguage</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> )

过程化风格

<span class="type">string</span> <span
class="methodname">locale\_get\_primary\_language</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> )

Gets the primary language for the input locale

### 参数

`locale`  
The locale to extract the primary language code from

### 返回值

The language code associated with the language or **`NULL`** in case of
error.

### 范例

**示例 \#1 <span class="function">locale\_get\_primary\_language</span>
example**

``` php
<?php
echo locale_get_primary_language('zh-Hant');
?>
```

**示例 \#2 OO example**

``` php
<?php
echo Locale::getPrimaryLanguage('zh-Hant');
?>
```

以上例程会输出：

    zh

### 参见

-   <span class="function">locale\_get\_script</span>
-   <span class="function">locale\_get\_region</span>
-   <span class="function">locale\_get\_all\_variants</span>

Locale::getRegion
=================

locale\_get\_region
===================

Gets the region for the input locale

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">Locale::getRegion</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> )

过程化风格

<span class="type">string</span> <span
class="methodname">locale\_get\_region</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> )

Gets the region for the input locale.

### 参数

`locale`  
The locale to extract the region code from

### 返回值

The region subtag for the locale or **`NULL`** if not present

### 范例

**示例 \#1 <span class="function">locale\_get\_region</span> example**

``` php
<?php
echo locale_get_region('de-CH-1901');
?>
```

**示例 \#2 OO example**

``` php
<?php
echo Locale::getRegion('de-CH-1901');
?>
```

以上例程会输出：

    CH

### 参见

-   <span class="function">locale\_get\_primary\_language</span>
-   <span class="function">locale\_get\_script</span>
-   <span class="function">locale\_get\_all\_variants</span>

Locale::getScript
=================

locale\_get\_script
===================

Gets the script for the input locale

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">Locale::getScript</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> )

过程化风格

<span class="type">string</span> <span
class="methodname">locale\_get\_script</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> )

Gets the script for the input locale.

### 参数

`locale`  
The locale to extract the script code from

### 返回值

The script subtag for the locale or **`NULL`** if not present

### 范例

**示例 \#1 <span class="function">locale\_get\_script</span> example**

``` php
<?php
echo locale_get_script('sr-Cyrl');
?>
```

**示例 \#2 OO example**

``` php
<?php
echo Locale::getScript('sr-Cyrl');
?>
```

以上例程会输出：

    Cyrl

### 参见

-   <span class="function">locale\_get\_primary\_language</span>
-   <span class="function">locale\_get\_region</span>
-   <span class="function">locale\_get\_all\_variants</span>

Locale::lookup
==============

locale\_lookup
==============

Searches the language tag list for the best match to the language

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">Locale::lookup</span> ( <span
class="methodparam"><span class="type">array</span> `$langtag`</span> ,
<span class="methodparam"><span class="type">string</span>
`$locale`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$canonicalize`<span class="initializer"> =
**`FALSE`**</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$default`</span> \]\] )

过程化风格

<span class="type">string</span> <span
class="methodname">locale\_lookup</span> ( <span
class="methodparam"><span class="type">array</span> `$langtag`</span> ,
<span class="methodparam"><span class="type">string</span>
`$locale`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$canonicalize`<span class="initializer"> =
**`FALSE`**</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$default`</span> \]\] )

Searches the items in `langtag` for the best match to the language range
specified in `locale` according to RFC 4647's lookup algorithm.

### 参数

`langtag`  
An <span class="type">array</span> containing a list of language tags to
compare to `locale`. Maximum 100 items allowed.

`locale`  
The locale to use as the language range when matching.

`canonicalize`  
If true, the arguments will be converted to canonical form before
matching.

`default`  
The locale to use if no match is found.

### 返回值

The closest matching language tag or default value.

### 范例

**示例 \#1 <span class="function">locale\_lookup</span> example**

``` php
<?php
$arr = array(
    'de-DEVA',
    'de-DE-1996',
    'de',
    'de-De'
);
echo locale_lookup($arr, 'de-DE-1996-x-prv1-prv2', true, 'en_US');
?>
```

**示例 \#2 OO example**

``` php
<?php
$arr = array(
    'de-DEVA',
    'de-DE-1996',
    'de',
    'de-De'
);
echo Locale::lookup($arr, 'de-DE-1996-x-prv1-prv2', true, 'en_US');
?>
```

以上例程会输出：

    de_de_1996

### 参见

-   <span class="function">locale\_filter\_matches</span>

Locale::parseLocale
===================

locale\_parse
=============

Returns a key-value array of locale ID subtag elements

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">Locale::parseLocale</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> )

过程化风格

<span class="type">array</span> <span
class="methodname">locale\_parse</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> )

Returns a key-value array of locale ID subtag elements.

### 参数

`locale`  
The locale to extract the subtag array from. Note: The 'variant' and
'private' subtags can take maximum 15 values whereas 'extlang' can take
maximum 3 values.

### 返回值

Returns an array containing a list of key-value pairs, where the keys
identify the particular locale ID subtags, and the values are the
associated subtag values. The array will be ordered as the locale id
subtags e.g. in the locale id if variants are '-varX-varY-varZ' then the
returned array will have variant0=\>varX , variant1=\>varY ,
variant2=\>varZ

Returns **`NULL`** when the length of `locale` exceeds
**`INTL_MAX_LOCALE_LEN`**.

### 范例

**示例 \#1 <span class="function">locale\_parse</span> example**

``` php
<?php
$arr = locale_parse('sl-Latn-IT-nedis');
if ($arr) {
    foreach ($arr as $key => $value) {
        echo "$key : $value , ";
    }
}
?>
```

**示例 \#2 OO example**

``` php
<?php
$arr = Locale::parseLocale('sl-Latn-IT-nedis');
if ($arr) {
    foreach ($arr as $key => $value) {
        echo "$key : $value , ";
    }
}
?>
```

以上例程会输出：

    language : sl , script : Latn , region : IT , variant0 : NEDIS ,

### 参见

-   <span class="function">locale\_compose</span>

Locale::setDefault
==================

locale\_set\_default
====================

Sets the default runtime locale

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">Locale::setDefault</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">locale\_set\_default</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> )

Sets the default runtime locale to $locale. This changes the value of
INTL global 'default\_locale' locale identifier. UAX \#35 extensions are
accepted.

### 参数

`locale`  
Is a BCP 47 compliant language tag.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">locale\_set\_default</span> example**

``` php
<?php
locale_set_default('de-DE');
echo locale_get_default();
?>
```

**示例 \#2 OO example**

``` php
<?php
Locale::setDefault('de-DE');
echo Locale::getDefault();
?>
```

以上例程会输出：

    de-DE

### 参见

-   <span class="function">locale\_get\_default</span>

简介
----

Normalization is a process that involves transforming characters and
sequences of characters into a formally-defined underlying
representation. This process is most important when text needs to be
compared for sorting and searching, but it is also used when storing
text to ensure that the text is stored in a consistent representation.

The Unicode Consortium has defined a number of normalization forms
reflecting the various needs of applications:

-   Normalization Form D (NFD) - Canonical Decomposition
-   Normalization Form C (NFC) - Canonical Decomposition followed by
    Canonical Composition
-   Normalization Form KD (NFKD) - Compatibility Decomposition
-   Normalization Form KC (NFKC) - Compatibility Decomposition followed
    by Canonical Composition

The different forms are defined in terms of a set of transformations on
the text, transformations that are expressed by both an algorithm and a
set of data files.

类摘要
------

**Normalizer**

<span class="ooclass"> class **Normalizer** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">getRawDecomposition</span> ( <span
class="methodparam"><span class="type">string</span> `$input`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">isNormalized</span> ( <span class="methodparam"><span
class="type">string</span> `$input`</span> \[, <span
class="methodparam"><span class="type">int</span> `$form`<span
class="initializer"> = Normalizer::FORM\_C</span></span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">normalize</span> ( <span class="methodparam"><span
class="type">string</span> `$input`</span> \[, <span
class="methodparam"><span class="type">int</span> `$form`<span
class="initializer"> = Normalizer::FORM\_C</span></span> \] )

}

预定义常量
----------

The following constants define the normalization form used by the
normalizer:

**`Normalizer::FORM_C`** (<span class="type">integer</span>)  
<span class="simpara"> Normalization Form C (NFC) - Canonical
Decomposition followed by Canonical Composition </span>

**`Normalizer::FORM_D`** (<span class="type">integer</span>)  
<span class="simpara">Normalization Form D (NFD) - Canonical
Decomposition</span>

**`Normalizer::FORM_KC`** (<span class="type">integer</span>)  
<span class="simpara"> Normalization Form KC (NFKC) - Compatibility
Decomposition, followed by Canonical Composition </span>

**`Normalizer::FORM_KD`** (<span class="type">integer</span>)  
<span class="simpara"> Normalization Form KD (NFKD) - Compatibility
Decomposition </span>

**`Normalizer::NONE`** (<span class="type">integer</span>)  
<span class="simpara">No decomposition/composition</span>

**`Normalizer::OPTION_DEFAULT`** (<span class="type">integer</span>)  
<span class="simpara">Default normalization options</span>

参见
----

-   <a href="http://unicode.org/reports/tr15/" class="link external">»  Unicode Normalization</a>
-   <a href="http://unicode.org/faq/normalization.html" class="link external">»  Unicode Normalization FAQ</a>
-   <a href="http://www.icu-project.org/userguide/normalization.html" class="link external">»  ICU User Guide - Normalization</a>
-   <a href="http://www.icu-project.org/apiref/icu4c/unorm_8h.html" class="link external">»  ICU API Reference - Normalization</a>

Normalizer::getRawDecomposition
===============================

normalizer\_get\_raw\_decomposition
===================================

Gets the Decomposition\_Mapping property for the given UTF-8 encoded
code point

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">Normalizer::getRawDecomposition</span> ( <span
class="methodparam"><span class="type">string</span> `$input`</span> )

过程化风格

<span class="type">string</span> <span
class="methodname">normalizer\_get\_raw\_decomposition</span> ( <span
class="methodparam"><span class="type">string</span> `$input`</span> )

Gets the Decomposition\_Mapping property, as specified in the Unicode
Character Database (UCD), for the given UTF-8 encoded code point.

### 参数

`input`  
The input string, which should be a single, UTF-8 encoded, code point.

### 返回值

Returns a <span class="type">string</span> containing the
Decomposition\_Mapping property, if present in the UCD.

Returns **`NULL`** if there is no Decomposition\_Mapping property for
the character.

### 范例

**示例 \#1 <span
class="methodname">Normalizer::getRawDecomposition</span> example**

``` php
<?php

$result = "";
$strings = [
    "a",
    "\u{FFDA}",
    "\u{FDFA}",
    "",
    "aa",
    "\xF5",
];

foreach ($strings as $string) {
    $decomposition = Normalizer::getRawDecomposition($string);
    // $decomposition = normalizer_get_raw_decomposition($string); Procedural way

    $error_code = intl_get_error_code();
    $error_message = intl_get_error_message();

    $string_hex = bin2hex($string);
    $result .= "---------------------\n";

    if ($decomposition === null) {
        $result .= "'$string_hex' has no decomposition mapping\n" ;
    } else {
        $result .= "'$string_hex' has the decomposition mapping '" . bin2hex($decomposition) . "'\n" ;
    }

    $result .= "error info: '$error_message' ($error_code)\n";
}

echo $result;
?>
```

以上例程会输出：

    ---------------------
    '61' has no decomposition mapping
    error info: 'U_ZERO_ERROR' (0)
    ---------------------
    'efbf9a' has the decomposition mapping 'e385a1'
    error info: 'U_ZERO_ERROR' (0)
    ---------------------
    'efb7ba' has the decomposition mapping 'd8b5d984d98920d8a7d984d984d98720d8b9d984d98ad98720d988d8b3d984d985'
    error info: 'U_ZERO_ERROR' (0)
    ---------------------
    '' has no decomposition mapping
    error info: 'Input string must be exactly one UTF-8 encoded code point long.: U_ILLEGAL_ARGUMENT_ERROR' (1)
    ---------------------
    '6161' has no decomposition mapping
    error info: 'Input string must be exactly one UTF-8 encoded code point long.: U_ILLEGAL_ARGUMENT_ERROR' (1)
    ---------------------
    'f5' has no decomposition mapping
    error info: 'Code point out of range: U_ILLEGAL_ARGUMENT_ERROR' (1)

### 参见

-   <span class="methodname">Normalizer::normalize</span>
-   <span class="methodname">Normalizer::isNormalized</span>

Normalizer::isNormalized
========================

normalizer\_is\_normalized
==========================

Checks if the provided string is already in the specified normalization
form

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">Normalizer::isNormalized</span> ( <span
class="methodparam"><span class="type">string</span> `$input`</span> \[,
<span class="methodparam"><span class="type">int</span> `$form`<span
class="initializer"> = Normalizer::FORM\_C</span></span> \] )

过程化风格

<span class="type">bool</span> <span
class="methodname">normalizer\_is\_normalized</span> ( <span
class="methodparam"><span class="type">string</span> `$input`</span> \[,
<span class="methodparam"><span class="type">int</span> `$form`<span
class="initializer"> = Normalizer::FORM\_C</span></span> \] )

Checks if the provided string is already in the specified normalization
form.

### 参数

`input`  
The input string to normalize

`form`  
One of the normalization forms.

### 返回值

**`TRUE`** if normalized, **`FALSE`** otherwise or if there an error

### 范例

**示例 \#1 <span class="function">normalizer\_is\_normalized</span>
example**

``` php
<?php
$char_A_ring = "\xC3\x85"; // 'LATIN CAPITAL LETTER A WITH RING ABOVE' (U+00C5)
$char_combining_ring_above = "\xCC\x8A";  // 'COMBINING RING ABOVE' (U+030A)
 
$char_orig = 'A' . $char_combining_ring_above;
$char_norm = normalizer_normalize( 'A' . $char_combining_ring_above, Normalizer::FORM_C );
 
echo ( normalizer_is_normalized($char_orig, Normalizer::FORM_C) ) ? "normalized" : "not normalized";
echo '; ';
echo ( normalizer_is_normalized($char_norm, Normalizer::FORM_C) ) ? "normalized" : "not normalized";
?>
```

**示例 \#2 OO example**

``` php
<?php
$char_A_ring = "\xC3\x85"; // 'LATIN CAPITAL LETTER A WITH RING ABOVE' (U+00C5)
$char_combining_ring_above = "\xCC\x8A";  // 'COMBINING RING ABOVE' (U+030A)
 
$char_orig = 'A' . $char_combining_ring_above;
$char_norm = Normalizer::normalize( 'A' . $char_combining_ring_above, Normalizer::FORM_C );
 
echo ( Normalizer::isNormalized($char_orig, Normalizer::FORM_C) ) ? "normalized" : "not normalized";
echo '; ';
echo ( Normalizer::isNormalized($char_norm, Normalizer::FORM_C) ) ? "normalized" : "not normalized";
?>
```

以上例程会输出：

    not normalized; normalized

### 参见

-   <span class="function">normalizer\_normalize</span>

Normalizer::normalize
=====================

normalizer\_normalize
=====================

Normalizes the input provided and returns the normalized string

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">Normalizer::normalize</span> ( <span
class="methodparam"><span class="type">string</span> `$input`</span> \[,
<span class="methodparam"><span class="type">int</span> `$form`<span
class="initializer"> = Normalizer::FORM\_C</span></span> \] )

过程化风格

<span class="type">string</span> <span
class="methodname">normalizer\_normalize</span> ( <span
class="methodparam"><span class="type">string</span> `$input`</span> \[,
<span class="methodparam"><span class="type">int</span> `$form`<span
class="initializer"> = Normalizer::FORM\_C</span></span> \] )

Normalizes the input provided and returns the normalized string

### 参数

`input`  
The input string to normalize

`form`  
One of the normalization forms.

### 返回值

The normalized string or **`FALSE`** if an error occurred.

### 范例

**示例 \#1 <span class="function">normalizer\_normalize</span> example**

``` php
<?php
$char_A_ring = "\xC3\x85"; // 'LATIN CAPITAL LETTER A WITH RING ABOVE' (U+00C5)
$char_combining_ring_above = "\xCC\x8A";  // 'COMBINING RING ABOVE' (U+030A)
 
$char_1 = normalizer_normalize( $char_A_ring, Normalizer::FORM_C );
$char_2 = normalizer_normalize( 'A' . $char_combining_ring_above, Normalizer::FORM_C );
 
echo urlencode($char_1);
echo ' ';
echo urlencode($char_2);
?>
```

**示例 \#2 OO example**

``` php
<?php
$char_A_ring = "\xC3\x85"; // 'LATIN CAPITAL LETTER A WITH RING ABOVE' (U+00C5)
$char_combining_ring_above = "\xCC\x8A";  // 'COMBINING RING ABOVE' (U+030A)
 
$char_1 = Normalizer::normalize( $char_A_ring, Normalizer::FORM_C );
$char_2 = Normalizer::normalize( 'A' . $char_combining_ring_above, Normalizer::FORM_C );
 
echo urlencode($char_1);
echo ' ';
echo urlencode($char_2);
?>
```

以上例程会输出：

    %C3%85 %C3%85

### 参见

-   <span class="function">normalizer\_is\_normalized</span>

简介
----

MessageFormatter is a concrete class that enables users to produce
concatenated, language-neutral messages. The methods supplied in this
class are used to build all the messages that are seen by end users.

The MessageFormatter class assembles messages from various fragments
(such as text fragments, numbers, and dates) supplied by the program.
Because of the MessageFormatter class, the program does not need to know
the order of the fragments. The class uses the formatting specifications
for the fragments to assemble them into a message that is contained in a
single string within a resource bundle. For example, MessageFormatter
enables you to print the phrase "Finished printing x out of y files..."
in a manner that still allows for flexibility in translation.

Previously, an end user message was created as a sentence and handled as
a string. This procedure created problems for localizers because the
sentence structure, word order, number format and so on are very
different from language to language. The language-neutral way to create
messages keeps each part of the message separate and provides keys to
the data. Using these keys, the MessageFormatter class can concatenate
the parts of the message, localize them, and display a well-formed
string to the end user.

MessageFormatter takes a set of objects, formats them, and then inserts
the formatted strings into the pattern at the appropriate places. Choice
formats can be used in conjunction with MessageFormatter to handle
plurals, match numbers, and select from an array of items. Typically,
the message format will come from resources and the arguments will be
dynamically set at runtime.

类摘要
------

**MessageFormatter**

<span class="ooclass"> class **MessageFormatter** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> ,
<span class="methodparam"><span class="type">string</span>
`$pattern`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">MessageFormatter</span> <span
class="methodname">create</span> ( <span class="methodparam"><span
class="type">string</span> `$locale`</span> , <span
class="methodparam"><span class="type">string</span> `$pattern`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">formatMessage</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> ,
<span class="methodparam"><span class="type">string</span>
`$pattern`</span> , <span class="methodparam"><span
class="type">array</span> `$args`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">format</span> ( <span class="methodparam"><span
class="type">array</span> `$args`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getErrorCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getErrorMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getLocale</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getPattern</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">parseMessage</span> ( <span class="methodparam"><span
class="type">string</span> `$locale`</span> , <span
class="methodparam"><span class="type">string</span> `$pattern`</span> ,
<span class="methodparam"><span class="type">string</span>
`$source`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">parse</span> ( <span class="methodparam"><span
class="type">string</span> `$value`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setPattern</span> ( <span
class="methodparam"><span class="type">string</span> `$pattern`</span> )

}

参见
----

-   <a href="http://icu-project.org/userguide/formatParse.html" class="link external">»  ICU formatting documentation</a>
-   <a href="http://icu-project.org/userguide/formatMessages.html" class="link external">»  ICU message formatting description</a>
-   <a href="http://icu-project.org/apiref/icu4c/classMessageFormat.html#details" class="link external">» ICU message formatters</a>
-   <a href="http://icu-project.org/apiref/icu4c/classChoiceFormat.html#details" class="link external">» ICU choice formatters</a>

MessageFormatter::create
========================

MessageFormatter::\_\_construct
===============================

msgfmt\_create
==============

Constructs a new Message Formatter

### 说明

面向对象风格 (method)

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">MessageFormatter</span> <span
class="methodname">MessageFormatter::create</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> ,
<span class="methodparam"><span class="type">string</span>
`$pattern`</span> )

面向对象风格 (constructor):

<span class="modifier">public</span> <span
class="methodname">MessageFormatter::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> ,
<span class="methodparam"><span class="type">string</span>
`$pattern`</span> )

过程化风格

<span class="type">MessageFormatter</span> <span
class="methodname">msgfmt\_create</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> ,
<span class="methodparam"><span class="type">string</span>
`$pattern`</span> )

Constructs a new Message Formatter

### 参数

`locale`  
The locale to use when formatting arguments

`pattern`  
The pattern string to stick arguments into. The pattern uses an
'apostrophe-friendly' syntax; it is run through
<a href="http://www.icu-project.org/apiref/icu4c/umsg_8h.html#9da796210146ff51d395affe4928f0b7" class="link external">» umsg_autoQuoteApostrophe</a>
before being interpreted.

### 返回值

The formatter <span class="type">object</span>

### 错误／异常

When invoked as constructor, on failure an <span
class="classname">IntlException</span> is thrown.

### 范例

**示例 \#1 <span class="function">msgfmt\_create</span> example**

``` php
<?php
$fmt = msgfmt_create("en_US", "{0,number,integer} monkeys on {1,number,integer} trees make {2,number} monkeys per tree");
echo msgfmt_format($fmt, array(4560, 123, 4560/123));
$fmt = msgfmt_create("de", "{0,number,integer} Affen auf {1,number,integer} Bäumen sind {2,number} Affen pro Baum");
echo msgfmt_format($fmt, array(4560, 123, 4560/123));
?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new MessageFormatter("en_US", "{0,number,integer} monkeys on {1,number,integer} trees make {2,number} monkeys per tree");
echo $fmt->format(array(4560, 123, 4560/123));
$fmt = new MessageFormatter("de", "{0,number,integer} Affen auf {1,number,integer} Bäumen sind {2,number} Affen pro Baum");
echo $fmt->format(array(4560, 123, 4560/123));
?>
```

以上例程会输出：

    4,560 monkeys on 123 trees make 37.073 monkeys per tree
    4.560 Affen auf 123 Bäumen sind 37,073 Affen pro Baum

### 参见

-   <span class="function">msgfmt\_format</span>
-   <span class="function">msgfmt\_parse</span>
-   <span class="function">msgfmt\_get\_error\_code</span>
-   <span class="function">msgfmt\_get\_error\_message</span>

MessageFormatter::formatMessage
===============================

msgfmt\_format\_message
=======================

Quick format message

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">MessageFormatter::formatMessage</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> ,
<span class="methodparam"><span class="type">string</span>
`$pattern`</span> , <span class="methodparam"><span
class="type">array</span> `$args`</span> )

过程化风格

<span class="type">string</span> <span
class="methodname">msgfmt\_format\_message</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> ,
<span class="methodparam"><span class="type">string</span>
`$pattern`</span> , <span class="methodparam"><span
class="type">array</span> `$args`</span> )

Quick formatting function that formats the string without having to
explicitly create the formatter object. Use this function when the
format operation is done only once and does not need and parameters or
state to be kept.

### 参数

`locale`  
The locale to use for formatting locale-dependent parts

`pattern`  
The pattern <span class="type">string</span> to insert things into. The
pattern uses an 'apostrophe-friendly' syntax; it is run through
<a href="http://www.icu-project.org/apiref/icu4c/umsg_8h.html#9da796210146ff51d395affe4928f0b7" class="link external">» umsg_autoQuoteApostrophe</a>
before being interpreted.

`args`  
The <span class="type">array</span> of values to insert into the format
<span class="type">string</span>

### 返回值

The formatted pattern string or **`FALSE`** if an error occurred

### 范例

**示例 \#1 <span class="function">msgfmt\_format\_message</span>
example**

``` php
<?php
echo msgfmt_format_message("en_US", "{0,number,integer} monkeys on {1,number,integer} trees make {2,number} monkeys per tree\n", array(4560, 123, 4560/123));
echo msgfmt_format_message("de", "{0,number,integer} Affen auf {1,number,integer} Bäumen sind {2,number} Affen pro Baum\n", array(4560, 123, 4560/123));
?>
```

**示例 \#2 OO example**

``` php
<?php
echo MessageFormatter::formatMessage("en_US", "{0,number,integer} monkeys on {1,number,integer} trees make {2,number} monkeys per tree\n", array(4560, 123, 4560/123));
echo MessageFormatter::formatMessage("de", "{0,number,integer} Affen auf {1,number,integer} Bäumen sind {2,number} Affen pro Baum\n", array(4560, 123, 4560/123));
?>
```

以上例程会输出：

    4,560 monkeys on 123 trees make 37.073 monkeys per tree
    4.560 Affen auf 123 Bäumen sind 37,073 Affen pro Baum

### 参见

-   <span class="function">msgfmt\_create</span>
-   <span class="function">msgfmt\_parse</span>
-   <span class="function">msgfmt\_get\_error\_code</span>
-   <span class="function">msgfmt\_get\_error\_message</span>

MessageFormatter::format
========================

msgfmt\_format
==============

Format the message

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">MessageFormatter::format</span> ( <span
class="methodparam"><span class="type">array</span> `$args`</span> )

过程化风格

<span class="type">string</span> <span
class="methodname">msgfmt\_format</span> ( <span
class="methodparam"><span class="type">MessageFormatter</span>
`$fmt`</span> , <span class="methodparam"><span
class="type">array</span> `$args`</span> )

Format the message by substituting the data into the format string
according to the locale rules

### 参数

`fmt`  
The message formatter

`args`  
Arguments to insert into the format string

### 返回值

The formatted string, or **`FALSE`** if an error occurred

### 范例

**示例 \#1 <span class="function">msgfmt\_format</span> example**

``` php
<?php
$fmt = msgfmt_create("en_US", "{0,number,integer} monkeys on {1,number,integer} trees make {2,number} monkeys per tree");
echo msgfmt_format($fmt, array(4560, 123, 4560/123));
$fmt = msgfmt_create("de", "{0,number,integer} Affen auf {1,number,integer} Bäumen sind {2,number} Affen pro Baum");
echo msgfmt_format($fmt, array(4560, 123, 4560/123));
?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new MessageFormatter("en_US", "{0,number,integer} monkeys on {1,number,integer} trees make {2,number} monkeys per tree");
echo $fmt->format(array(4560, 123, 4560/123));
$fmt = new MessageFormatter("de", "{0,number,integer} Affen auf {1,number,integer} Bäumen sind {2,number} Affen pro Baum");
echo $fmt->format(array(4560, 123, 4560/123));
?>
```

以上例程会输出：

    4,560 monkeys on 123 trees make 37.073 monkeys per tree
    4.560 Affen auf 123 Bäumen sind 37,073 Affen pro Baum

### 参见

-   <span class="function">msgfmt\_create</span>
-   <span class="function">msgfmt\_parse</span>
-   <span class="function">msgfmt\_format\_message</span>
-   <span class="function">msgfmt\_get\_error\_code</span>
-   <span class="function">msgfmt\_get\_error\_message</span>

MessageFormatter::getErrorCode
==============================

msgfmt\_get\_error\_code
========================

Get the error code from last operation

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">MessageFormatter::getErrorCode</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">int</span> <span
class="methodname">msgfmt\_get\_error\_code</span> ( <span
class="methodparam"><span class="type">MessageFormatter</span>
`$fmt`</span> )

Get the error code from last operation.

### 参数

`fmt`  
The message formatter

### 返回值

The error code, one of UErrorCode values. Initial value is
U\_ZERO\_ERROR.

### 参见

-   <span class="function">msgfmt\_get\_error\_message</span>
-   <span class="function">intl\_get\_error\_code</span>
-   <span class="function">intl\_is\_failure</span>

MessageFormatter::getErrorMessage
=================================

msgfmt\_get\_error\_message
===========================

Get the error text from the last operation

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">MessageFormatter::getErrorMessage</span> (
<span class="methodparam">void</span> )

过程化风格

<span class="type">string</span> <span
class="methodname">msgfmt\_get\_error\_message</span> ( <span
class="methodparam"><span class="type">MessageFormatter</span>
`$fmt`</span> )

Get the error text from the last operation.

### 参数

`fmt`  
The message formatter

### 返回值

Description of the last error.

### 范例

**示例 \#1 <span class="function">msgfmt\_get\_error\_message</span>
example**

``` php
<?php
$fmt = msgfmt_create("en_US", "{0, number} monkeys on {1, number} trees");
$str = msgfmt_format($fmt, array());
if(!$str) {
    echo "ERROR: ".msgfmt_get_error_message($fmt) . " (" . msgfmt_get_error_code($fmt) . ")\n";
}
?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new MessageFormatter("en_US", "{0, number} monkeys on {1, number} trees");
$str = $fmt->format(array());
if(!$str) {
    echo "ERROR: ".$fmt->getErrorMessage() . " (" . $fmt->getErrorCode() . ")\n";
}
?>
```

以上例程会输出：

    ERROR: msgfmt_format: not enough parameters: U_ILLEGAL_ARGUMENT_ERROR (1)

### 参见

-   <span class="function">msgfmt\_get\_error\_code</span>
-   <span class="function">intl\_get\_error\_code</span>
-   <span class="function">intl\_is\_failure</span>

MessageFormatter::getLocale
===========================

msgfmt\_get\_locale
===================

Get the locale for which the formatter was created

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">MessageFormatter::getLocale</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">string</span> <span
class="methodname">msgfmt\_get\_locale</span> ( <span
class="methodparam"><span class="type">NumberFormatter</span>
`$formatter`</span> )

Get the locale for which the formatter was created.

### 参数

`formatter`  
The formatter resource

### 返回值

The locale name

### 范例

**示例 \#1 <span class="function">msgfmt\_get\_locale</span> example**

``` php
<?php
$fmt = msgfmt_create('en_US', "Number {0,number}");
echo msgfmt_get_locale($fmt);
?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new MessageFormatter('en_US', "Number {0,number}");
echo $fmt->getLocale();
?>
```

以上例程会输出：

    en_US

### 参见

-   <span class="function">msgfmt\_create</span>

MessageFormatter::getPattern
============================

msgfmt\_get\_pattern
====================

Get the pattern used by the formatter

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">MessageFormatter::getPattern</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">string</span> <span
class="methodname">msgfmt\_get\_pattern</span> ( <span
class="methodparam"><span class="type">MessageFormatter</span>
`$fmt`</span> )

Get the pattern used by the formatter

### 参数

`fmt`  
The message formatter

### 返回值

The pattern <span class="type">string</span> for this message formatter

### 范例

**示例 \#1 <span class="function">msgfmt\_get\_pattern</span> example**

``` php
<?php
$fmt = msgfmt_create( "en_US", "{0, number} monkeys on {1, number} trees" );
echo "Default pattern: '" . msgfmt_get_pattern( $fmt ) . "'\n";
echo "Formatting result: " . msgfmt_format( $fmt, array(123, 456) ) . "\n";

msgfmt_set_pattern( $fmt, "{0, number} trees hosting {1, number} monkeys" );
echo "New pattern: '" . msgfmt_get_pattern( $fmt ) . "'\n";
echo "Formatted number: " . msgfmt_format( $fmt, array(123, 456) ) . "\n";
?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new MessageFormatter( "en_US", "{0, number} monkeys on {1, number} trees" );
echo "Default pattern: '" . $fmt->getPattern() . "'\n";
echo "Formatting result: " . $fmt->format(array(123, 456)) . "\n";

$fmt->setPattern("{0, number} trees hosting {1, number} monkeys" );
echo "New pattern: '" . $fmt->getPattern() . "'\n";
echo "Formatted number: " . $fmt->format(array(123, 456)) . "\n";
?>
```

以上例程会输出：

    Default pattern: '{0,number} monkeys on {1,number} trees'
    Formatting result: 123 monkeys on 456 trees
    New pattern: '{0,number} trees hosting {1,number} monkeys'
    Formatted number: 123 trees hosting 456 monkeys

### 参见

-   <span class="function">msgfmt\_create</span>
-   <span class="function">msgfmt\_set\_pattern</span>

MessageFormatter::parseMessage
==============================

msgfmt\_parse\_message
======================

Quick parse input string

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">MessageFormatter::parseMessage</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> ,
<span class="methodparam"><span class="type">string</span>
`$pattern`</span> , <span class="methodparam"><span
class="type">string</span> `$source`</span> )

过程化风格

<span class="type">array</span> <span
class="methodname">msgfmt\_parse\_message</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> ,
<span class="methodparam"><span class="type">string</span>
`$pattern`</span> , <span class="methodparam"><span
class="type">string</span> `$value`</span> )

Parses input string without explicitly creating the formatter object.
Use this function when the format operation is done only once and does
not need and parameters or state to be kept.

### 参数

`locale`  
The locale to use for parsing locale-dependent parts

`pattern`  
The pattern with which to parse the `value`.

`source`  
The <span class="type">string</span> to parse, conforming to the
`pattern`.

### 返回值

An <span class="type">array</span> containing items extracted, or
**`FALSE`** on error

### 范例

**示例 \#1 <span class="function">msgfmt\_parse\_message</span>
example**

``` php
<?php
$fmt = msgfmt_parse_message('en_US', "{0,number,integer} monkeys on {1,number,integer} trees make {2,number} monkeys per tree",
                            "4,560 monkeys on 123 trees make 37.073 monkeys per tree");
var_export($fmt);

$fmt = msgfmt_parse_message('de', "{0,number,integer} Affen auf {1,number,integer} Bäumen sind {2,number} Affen pro Baum", 
                            "4.560 Affen auf 123 Bäumen sind 37,073 Affen pro Baum");
var_export($fmt);
?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = MessageFormatter::parseMessage('en_US', "{0,number,integer} monkeys on {1,number,integer} trees make {2,number} monkeys per tree",
                            "4,560 monkeys on 123 trees make 37.073 monkeys per tree");
var_export($fmt);

$fmt = MessageFormatter::parseMessage('de', "{0,number,integer} Affen auf {1,number,integer} Bäumen sind {2,number} Affen pro Baum", 
                            "4.560 Affen auf 123 Bäumen sind 37,073 Affen pro Baum");
var_export($fmt);
?>
```

以上例程会输出：

    array (
      0 => 4560,
      1 => 123,
      2 => 37.073,
    )
    array (
      0 => 4560,
      1 => 123,
      2 => 37.073,
    )

### 参见

-   <span class="function">msgfmt\_create</span>
-   <span class="function">msgfmt\_format\_message</span>
-   <span class="function">msgfmt\_parse</span>

MessageFormatter::parse
=======================

msgfmt\_parse
=============

Parse input string according to pattern

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MessageFormatter::parse</span> ( <span
class="methodparam"><span class="type">string</span> `$value`</span> )

过程化风格

<span class="type">array</span> <span
class="methodname">msgfmt\_parse</span> ( <span
class="methodparam"><span class="type">MessageFormatter</span>
`$fmt`</span> , <span class="methodparam"><span
class="type">string</span> `$value`</span> )

Parses input <span class="type">string</span> and return any extracted
items as an <span class="type">array</span>.

### 参数

`fmt`  
The message formatter

`value`  
The <span class="type">string</span> to parse

### 返回值

An <span class="type">array</span> containing the items extracted, or
**`FALSE`** on error

### 范例

**示例 \#1 <span class="function">msgfmt\_parse</span> example**

``` php
<?php
$fmt = msgfmt_create('en_US', "{0,number,integer} monkeys on {1,number,integer} trees make {2,number} monkeys per tree");
$res = msgfmt_parse($fmt, "4,560 monkeys on 123 trees make 37.073 monkeys per tree");
var_export($res);

$fmt = msgfmt_create('de', "{0,number,integer} Affen auf {1,number,integer} Bäumen sind {2,number} Affen pro Baum");
$res = msgfmt_parse($fmt, "4.560 Affen auf 123 Bäumen sind 37,073 Affen pro Baum");
var_export($res);
?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new MessageFormatter('en_US', "{0,number,integer} monkeys on {1,number,integer} trees make {2,number} monkeys per tree");
$res = $fmt->parse("4,560 monkeys on 123 trees make 37.073 monkeys per tree");
var_export($res);

$fmt = new MessageFormatter('de', "{0,number,integer} Affen auf {1,number,integer} Bäumen sind {2,number} Affen pro Baum");
$res = $fmt->parse("4.560 Affen auf 123 Bäumen sind 37,073 Affen pro Baum");
var_export($res);
?>
```

以上例程会输出：

    array (
      0 => 4560,
      1 => 123,
      2 => 37.073,
    )
    array (
      0 => 4560,
      1 => 123,
      2 => 37.073,
    )

### 参见

-   <span class="function">msgfmt\_create</span>
-   <span class="function">msgfmt\_format</span>
-   <span class="function">msgfmt\_parse\_message</span>

MessageFormatter::setPattern
============================

msgfmt\_set\_pattern
====================

Set the pattern used by the formatter

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">MessageFormatter::setPattern</span> ( <span
class="methodparam"><span class="type">string</span> `$pattern`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">msgfmt\_set\_pattern</span> ( <span
class="methodparam"><span class="type">MessageFormatter</span>
`$fmt`</span> , <span class="methodparam"><span
class="type">string</span> `$pattern`</span> )

Set the pattern used by the formatter

### 参数

`fmt`  
The message formatter

`pattern`  
The pattern <span class="type">string</span> to use in this message
formatter. The pattern uses an 'apostrophe-friendly' syntax; it is run
through
<a href="http://www.icu-project.org/apiref/icu4c/umsg_8h.html#9da796210146ff51d395affe4928f0b7" class="link external">» umsg_autoQuoteApostrophe</a>
before being interpreted.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">msgfmt\_set\_pattern</span> example**

``` php
<?php
$fmt = msgfmt_create( "en_US", "{0, number} monkeys on {1, number} trees" );
echo "Default pattern: '" . msgfmt_get_pattern( $fmt ) . "'\n";
echo "Formatting result: " . msgfmt_format( $fmt, array(123, 456) ) . "\n";

msgfmt_set_pattern( $fmt, "{0, number} trees hosting {1, number} monkeys" );
echo "New pattern: '" . msgfmt_get_pattern( $fmt ) . "'\n";
echo "Formatted number: " . msgfmt_format( $fmt, array(123, 456) ) . "\n";
?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new MessageFormatter( "en_US", "{0, number} monkeys on {1, number} trees" );
echo "Default pattern: '" . $fmt->getPattern() . "'\n";
echo "Formatting result: " . $fmt->format(array(123, 456)) . "\n";

$fmt->setPattern("{0, number} trees hosting {1, number} monkeys" );
echo "New pattern: '" . $fmt->getPattern() . "'\n";
echo "Formatted number: " . $fmt->format(array(123, 456)) . "\n";
?>
```

以上例程会输出：

    Default pattern: '{0,number} monkeys on {1,number} trees'
    Formatting result: 123 monkeys on 456 trees
    New pattern: '{0,number} trees hosting {1,number} monkeys'
    Formatted number: 123 trees hosting 456 monkeys

### 参见

-   <span class="function">msgfmt\_create</span>
-   <span class="function">msgfmt\_get\_pattern</span>

简介
----

类摘要
------

**IntlCalendar**

<span class="ooclass"> class **IntlCalendar** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_ERA` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_YEAR` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_MONTH` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_WEEK_OF_YEAR` <span class="initializer"> = 3</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_WEEK_OF_MONTH` <span class="initializer"> =
4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_DATE` <span class="initializer"> = 5</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_DAY_OF_YEAR` <span class="initializer"> = 6</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_DAY_OF_WEEK` <span class="initializer"> = 7</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_DAY_OF_WEEK_IN_MONTH` <span class="initializer"> =
8</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_AM_PM` <span class="initializer"> = 9</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_HOUR` <span class="initializer"> = 10</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_HOUR_OF_DAY` <span class="initializer"> = 11</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_MINUTE` <span class="initializer"> = 12</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_SECOND` <span class="initializer"> = 13</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_MILLISECOND` <span class="initializer"> = 14</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_ZONE_OFFSET` <span class="initializer"> = 15</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_DST_OFFSET` <span class="initializer"> = 16</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_YEAR_WOY` <span class="initializer"> = 17</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_DOW_LOCAL` <span class="initializer"> = 18</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_EXTENDED_YEAR` <span class="initializer"> =
19</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_JULIAN_DAY` <span class="initializer"> = 20</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_MILLISECONDS_IN_DAY` <span class="initializer"> =
21</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_IS_LEAP_MONTH` <span class="initializer"> =
22</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_FIELD_COUNT ` <span class="initializer"> =
23</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_DAY_OF_MONTH` <span class="initializer"> = 5</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::DOW_SUNDAY` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::DOW_MONDAY` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::DOW_TUESDAY` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::DOW_WEDNESDAY` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::DOW_THURSDAY` <span class="initializer"> = 5</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::DOW_FRIDAY` <span class="initializer"> = 6</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::DOW_SATURDAY` <span class="initializer"> = 7</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::DOW_TYPE_WEEKDAY` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::DOW_TYPE_WEEKEND` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::DOW_TYPE_WEEKEND_OFFSET` <span class="initializer"> =
2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::DOW_TYPE_WEEKEND_CEASE` <span class="initializer"> =
3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::WALLTIME_FIRST` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::WALLTIME_LAST` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::WALLTIME_NEXT_VALID` <span class="initializer"> =
2</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">add</span> ( <span class="methodparam"><span
class="type">int</span> `$field`</span> , <span
class="methodparam"><span class="type">int</span> `$amount`</span> )

<span class="type">bool</span> <span
class="methodname">intlcal\_add</span> ( <span class="methodparam"><span
class="type">IntlCalendar</span> `$cal`</span> , <span
class="methodparam"><span class="type">int</span> `$field`</span> ,
<span class="methodparam"><span class="type">int</span> `$amount`</span>
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">after</span> ( <span class="methodparam"><span
class="type">IntlCalendar</span> `$other`</span> )

<span class="type">bool</span> <span
class="methodname">intlcal\_after</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">IntlCalendar</span>
`$other`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">before</span> ( <span class="methodparam"><span
class="type">IntlCalendar</span> `$other`</span> )

<span class="type">bool</span> <span
class="methodname">intlcal\_before</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">IntlCalendar</span>
`$other`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">clear</span> (\[ <span
class="methodparam"><span class="type">int</span> `$field`<span
class="initializer"> = NULL</span></span> \] )

<span class="type">bool</span> <span
class="methodname">intlcal\_clear</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$field`<span class="initializer"> = NULL</span></span> \] )

<span class="modifier">private</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">IntlCalendar</span>
<span class="methodname">createInstance</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$timeZone`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$locale`<span
class="initializer"> = ""</span></span> \]\] )

<span class="type">IntlCalendar</span> <span
class="methodname">intlcal\_create\_instance</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$timeZone`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$locale`<span
class="initializer"> = ""</span></span> \]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">equals</span> ( <span class="methodparam"><span
class="type">IntlCalendar</span> `$other`</span> )

<span class="type">bool</span> <span
class="methodname">intlcal\_equals</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">IntlCalendar</span>
`$other`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">fieldDifference</span> ( <span
class="methodparam"><span class="type">float</span> `$when`</span> ,
<span class="methodparam"><span class="type">int</span> `$field`</span>
)

<span class="type">int</span> <span
class="methodname">intlcal\_field\_difference</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">float</span>
`$when`</span> , <span class="methodparam"><span class="type">int</span>
`$field`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">IntlCalendar</span>
<span class="methodname">fromDateTime</span> ( <span
class="methodparam"><span class="type">mixed</span> `$dateTime`</span> )

<span class="type">IntlCalendar</span> <span
class="methodname">intlcal\_from\_date\_time</span> ( <span
class="methodparam"><span class="type">mixed</span> `$dateTime`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">get</span> ( <span class="methodparam"><span
class="type">int</span> `$field`</span> )

<span class="type">int</span> <span
class="methodname">intlcal\_get</span> ( <span class="methodparam"><span
class="type">IntlCalendar</span> `$cal`</span> , <span
class="methodparam"><span class="type">int</span> `$field`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getActualMaximum</span> ( <span
class="methodparam"><span class="type">int</span> `$field`</span> )

<span class="type">int</span> <span
class="methodname">intlcal\_get\_actual\_maximum</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$field`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getActualMinimum</span> ( <span
class="methodparam"><span class="type">int</span> `$field`</span> )

<span class="type">int</span> <span
class="methodname">intlcal\_get\_actual\_minimum</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$field`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">getAvailableLocales</span> ( <span
class="methodparam">void</span> )

<span class="type">array</span> <span
class="methodname">intlcal\_get\_available\_locales</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getDayOfWeekType</span> ( <span
class="methodparam"><span class="type">int</span> `$dayOfWeek`</span> )

<span class="type">int</span> <span
class="methodname">intlcal\_get\_day\_of\_week\_type</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$dayOfWeek`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getErrorCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getErrorMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getFirstDayOfWeek</span> ( <span
class="methodparam">void</span> )

<span class="type">int</span> <span
class="methodname">intlcal\_get\_first\_day\_of\_week</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
)

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getGreatestMinimum</span> ( <span
class="methodparam"><span class="type">int</span> `$field`</span> )

<span class="type">int</span> <span
class="methodname">intlcal\_get\_greatest\_minimum</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$field`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">Iterator</span> <span
class="methodname">getKeywordValuesForLocale</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> ,
<span class="methodparam"><span class="type">string</span>
`$locale`</span> , <span class="methodparam"><span
class="type">bool</span> `$commonlyUsed`</span> )

<span class="type">Iterator</span> <span
class="methodname">intlcal\_get\_keyword\_values\_for\_locale</span> (
<span class="methodparam"><span class="type">string</span> `$key`</span>
, <span class="methodparam"><span class="type">string</span>
`$locale`</span> , <span class="methodparam"><span
class="type">bool</span> `$commonlyUsed`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getLeastMaximum</span> ( <span
class="methodparam"><span class="type">int</span> `$field`</span> )

<span class="type">int</span> <span
class="methodname">intlcal\_get\_least\_maximum</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$field`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getLocale</span> ( <span
class="methodparam"><span class="type">int</span> `$localeType`</span> )

<span class="type">string</span> <span
class="methodname">intlcal\_get\_locale</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$localeType`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getMaximum</span> ( <span class="methodparam"><span
class="type">int</span> `$field`</span> )

<span class="type">int</span> <span
class="methodname">intlcal\_get\_maximum</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$field`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getMinimalDaysInFirstWeek</span> ( <span
class="methodparam">void</span> )

<span class="type">int</span> <span
class="methodname">intlcal\_get\_minimal\_days\_in\_first\_week</span> (
<span class="methodparam"><span class="type">IntlCalendar</span>
`$cal`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getMinimum</span> ( <span class="methodparam"><span
class="type">int</span> `$field`</span> )

<span class="type">int</span> <span
class="methodname">intlcal\_get\_minimum</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$field`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">float</span> <span
class="methodname">getNow</span> ( <span class="methodparam">void</span>
)

<span class="type">float</span> <span
class="methodname">intlcal\_get\_now</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getRepeatedWallTimeOption</span> ( <span
class="methodparam">void</span> )

<span class="type">int</span> <span
class="methodname">intlcal\_get\_repeated\_wall\_time\_option</span> (
<span class="methodparam"><span class="type">IntlCalendar</span>
`$cal`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getSkippedWallTimeOption</span> ( <span
class="methodparam">void</span> )

<span class="type">int</span> <span
class="methodname">intlcal\_get\_skipped\_wall\_time\_option</span> (
<span class="methodparam"><span class="type">IntlCalendar</span>
`$cal`</span> )

<span class="modifier">public</span> <span class="type">float</span>
<span class="methodname">getTime</span> ( <span
class="methodparam">void</span> )

<span class="type">float</span> <span
class="methodname">intlcal\_get\_time</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
)

<span class="modifier">public</span> <span
class="type">IntlTimeZone</span> <span
class="methodname">getTimeZone</span> ( <span
class="methodparam">void</span> )

<span class="type">IntlTimeZone</span> <span
class="methodname">intlcal\_get\_time\_zone</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
)

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getType</span> ( <span
class="methodparam">void</span> )

<span class="type">string</span> <span
class="methodname">intlcal\_get\_type</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
)

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getWeekendTransition</span> ( <span
class="methodparam"><span class="type">string</span> `$dayOfWeek`</span>
)

<span class="type">int</span> <span
class="methodname">intlcal\_get\_weekend\_transition</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">string</span>
`$dayOfWeek`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">inDaylightTime</span> ( <span
class="methodparam">void</span> )

<span class="type">bool</span> <span
class="methodname">intlcal\_in\_daylight\_time</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isEquivalentTo</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span>
`$other`</span> )

<span class="type">bool</span> <span
class="methodname">intlcal\_is\_equivalent\_to</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">IntlCalendar</span>
`$other`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isLenient</span> ( <span
class="methodparam">void</span> )

<span class="type">bool</span> <span
class="methodname">intlcal\_is\_lenient</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isSet</span> ( <span class="methodparam"><span
class="type">int</span> `$field`</span> )

<span class="type">bool</span> <span
class="methodname">intlcal\_is\_set</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$field`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isWeekend</span> (\[ <span
class="methodparam"><span class="type">float</span> `$date`<span
class="initializer"> = NULL</span></span> \] )

<span class="type">bool</span> <span
class="methodname">intlcal\_is\_weekend</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
\[, <span class="methodparam"><span class="type">float</span>
`$date`<span class="initializer"> = NULL</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">roll</span> ( <span class="methodparam"><span
class="type">int</span> `$field`</span> , <span
class="methodparam"><span class="type">mixed</span>
`$amountOrUpOrDown`</span> )

<span class="type">bool</span> <span
class="methodname">intlcal\_roll</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$field`</span> , <span class="methodparam"><span
class="type">mixed</span> `$amountOrUpOrDown`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">set</span> ( <span class="methodparam"><span
class="type">int</span> `$field`</span> , <span
class="methodparam"><span class="type">int</span> `$value`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">set</span> ( <span class="methodparam"><span
class="type">int</span> `$year`</span> , <span class="methodparam"><span
class="type">int</span> `$month`</span> \[, <span
class="methodparam"><span class="type">int</span> `$dayOfMonth`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$hour`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$minute`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$second`<span
class="initializer"> = NULL</span></span> \]\]\]\] )

<span class="type">bool</span> <span
class="methodname">intlcal\_set</span> ( <span class="methodparam"><span
class="type">IntlCalendar</span> `$cal`</span> , <span
class="methodparam"><span class="type">int</span> `$field`</span> ,
<span class="methodparam"><span class="type">int</span> `$value`</span>
)

<span class="type">bool</span> <span
class="methodname">intlcal\_set</span> ( <span class="methodparam"><span
class="type">IntlCalendar</span> `$cal`</span> , <span
class="methodparam"><span class="type">int</span> `$year`</span> , <span
class="methodparam"><span class="type">int</span> `$month`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$dayOfMonth`<span class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$hour`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$minute`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$second`<span
class="initializer"> = NULL</span></span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setFirstDayOfWeek</span> ( <span
class="methodparam"><span class="type">int</span> `$dayOfWeek`</span> )

<span class="type">bool</span> <span
class="methodname">intlcal\_set\_first\_day\_of\_week</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$dayOfWeek`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setLenient</span> ( <span
class="methodparam"><span class="type">bool</span> `$isLenient`</span> )

<span class="type">bool</span> <span
class="methodname">intlcal\_set\_lenient</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">bool</span>
`$isLenient`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setMinimalDaysInFirstWeek</span> ( <span
class="methodparam"><span class="type">int</span> `$minimalDays`</span>
)

<span class="type">bool</span> <span
class="methodname">intlcal\_set\_minimal\_days\_in\_first\_week</span> (
<span class="methodparam"><span class="type">IntlCalendar</span>
`$cal`</span> , <span class="methodparam"><span class="type">int</span>
`$minimalDays`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setRepeatedWallTimeOption</span> ( <span
class="methodparam"><span class="type">int</span>
`$wallTimeOption`</span> )

<span class="type">bool</span> <span
class="methodname">intlcal\_set\_repeated\_wall\_time\_option</span> (
<span class="methodparam"><span class="type">IntlCalendar</span>
`$cal`</span> , <span class="methodparam"><span class="type">int</span>
`$wallTimeOption`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setSkippedWallTimeOption</span> ( <span
class="methodparam"><span class="type">int</span>
`$wallTimeOption`</span> )

<span class="type">bool</span> <span
class="methodname">intlcal\_set\_skipped\_wall\_time\_option</span> (
<span class="methodparam"><span class="type">IntlCalendar</span>
`$cal`</span> , <span class="methodparam"><span class="type">int</span>
`$wallTimeOption`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setTime</span> ( <span
class="methodparam"><span class="type">float</span> `$date`</span> )

<span class="type">bool</span> <span
class="methodname">intlcal\_set\_time</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">float</span>
`$date`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setTimeZone</span> ( <span
class="methodparam"><span class="type">mixed</span> `$timeZone`</span> )

<span class="type">bool</span> <span
class="methodname">intlcal\_set\_time\_zone</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">mixed</span>
`$timeZone`</span> )

<span class="modifier">public</span> <span class="type">DateTime</span>
<span class="methodname">toDateTime</span> ( <span
class="methodparam">void</span> )

<span class="type">DateTime</span> <span
class="methodname">intlcal\_to\_date\_time</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
)

}

预定义常量
----------

**`IntlCalendar::FIELD_ERA`**  
Calendar field numerically representing an era, for instance *1* for AD
and *0* for BC in the Gregorian/Julian calendars and *235* for the
Heisei (平成) era in the Japanese calendar. Not all calendars have more
than one era.

**`IntlCalendar::FIELD_YEAR`**  
Calendar field for the year. This is not unique across eras. If the
calendar type has more than one era, generally the minimum value for
this field will be *1*.

**`IntlCalendar::FIELD_MONTH`**  
Calendar field for the month. The month sequence is zero-based, so
January (here used to signify the first month of the calendar; this may
be called another name, such as Muharram in the Islamic calendar) is
represented by *0*, February by *1*, …, December by *11* and, for
calendars that have it, the 13th or leap month by *12*.

**`IntlCalendar::FIELD_WEEK_OF_YEAR`**  
Calendar field for the number of the week of the year. This depends on
which day of the week is
<a href="/class/intlcalendar.html#IntlCalendar::getFirstDayOfWeek" class="link">deemed to start the week</a>
and the
<a href="/class/intlcalendar.html#IntlCalendar::getMinimalDaysInFirstWeek" class="link">minimal number of days in a week</a>.

**`IntlCalendar::FIELD_WEEK_OF_MONTH`**  
Calendar field for the number of the week of the month. This depends on
which day of the week is
<a href="/class/intlcalendar.html#IntlCalendar::getFirstDayOfWeek" class="link">deemed to start the week</a>
and the
<a href="/class/intlcalendar.html#IntlCalendar::getMinimalDaysInFirstWeek" class="link">minimal number of days in a week</a>.

**`IntlCalendar::FIELD_DATE`**  
Calendar field for the day of the month. The same as
**`IntlCalendar::FIELD_DAY_OF_MONTH`**, which has a clearer name.

**`IntlCalendar::FIELD_DAY_OF_YEAR`**  
Calendar field for the day of the year. For the Gregorian calendar,
starts with **`1`** and ends with **`365`** or **`366`**.

**`IntlCalendar::FIELD_DAY_OF_WEEK`**  
Calendar field for the day of the week. Its values start with *1*
(Sunday, see
<a href="/class/intlcalendar.html#" class="link"><strong><code>IntlCalendar::DOW_SUNDAY</code></strong></a>
and subsequent constants) and the last valid value is 7 (Saturday).

**`IntlCalendar::FIELD_DAY_OF_WEEK_IN_MONTH`**  
Given a day of the week (Sunday, Monday, …), this calendar field assigns
an ordinal to such a day of the week in a specific month. Thus, if the
value of this field is *1* and the value of the day of the week is *2*
(Monday), then the set day of the month is the 1st Monday of the month;
the maximum value is *5*.

Additionally, the value *0* and negative values are also allowed. The
value *0* encompasses the seven days that occur immediately before the
first seven days of a month (which therefore have a ‘day of week in
month’ with value *1*). Negative values starts counting from the end of
the month – *-1* points to the last occurrence of a day of the week in a
month, *-2* to the second last, and so on.

Unlike
<a href="/class/intlcalendar.html#" class="link"><strong><code>IntlCalendar::FIELD_WEEK_OF_MONTH</code></strong></a>
and
<a href="/class/intlcalendar.html#" class="link"><strong><code>IntlCalendar::FIELD_WEEK_OF_YEAR</code></strong></a>,
this value does not depend on <span
class="function">IntlCalendar::getFirstDayOfWeek</span> or on <span
class="function">IntlCalendar::getMinimalDaysInFirstWeek</span>. The
first Monday is the first Monday, even if it occurs in a week that
belongs to the previous month.

**`IntlCalendar::FIELD_AM_PM`**  
Calendar field indicating whether a time is before noon (value *0*, AM)
or after (*1*). Midnight is AM, noon is PM.

**`IntlCalendar::FIELD_HOUR`**  
Calendar field for the hour, without specifying whether itʼs in the
morning or in the afternoon. Valid values are *0* to *11*.

**`IntlCalendar::FIELD_HOUR_OF_DAY`**  
Calendar field for the full (24h) hour of the day. Valid values are *0*
to *23*.

**`IntlCalendar::FIELD_MINUTE`**  
Calendar field for the minutes component of the time.

**`IntlCalendar::FIELD_SECOND`**  
Calendar field for the seconds component of the time.

**`IntlCalendar::FIELD_MILLISECOND`**  
Calendar field the milliseconds component of the time.

**`IntlCalendar::FIELD_ZONE_OFFSET`**  
Calendar field indicating the raw offset of the timezone, in
milliseconds. The raw offset is the timezone offset, excluding any
offset due to daylight saving time.

**`IntlCalendar::FIELD_DST_OFFSET`**  
Calendar field for the daylight saving time offset of the calendarʼs
timezone, in milliseconds, if active for calendarʼs time.

**`IntlCalendar::FIELD_YEAR_WOY`**  
Calendar field representing the year for
<a href="/class/intlcalendar.html#" class="link">week of year</a>
purposes.

**`IntlCalendar::FIELD_DOW_LOCAL`**  
Calendar field for the localized day of the week. This is a value
between *1* and *7*, *1* being used for the day of the week that matches
the value returned by <span
class="function">IntlCalendar::getFirstDayOfWeek</span>.

**`IntlCalendar::FIELD_EXTENDED_YEAR`**  
Calendar field for a year number representation that is continuous
across eras. For the Gregorian calendar, the value of this field matches
that of **`IntlCalendar::FIELD_YEAR`** for AD years; a BC year *y* is
represented by *-y + 1*.

**`IntlCalendar::FIELD_JULIAN_DAY`**  
Calendar field for a modified Julian day number. It is different from a
conventional Julian day number in that its transitions occur at local
zone midnight rather than at noon UTC. It uniquely identifies a date.

**`IntlCalendar::FIELD_MILLISECONDS_IN_DAY`**  
Calendar field encompassing the information in
**`IntlCalendar::FIELD_HOUR_OF_DAY`**, **`IntlCalendar::FIELD_MINUTE`**,
**`IntlCalendar::FIELD_SECOND`** and
**`IntlCalendar::FIELD_MILLISECOND`**. Range is from the *0* to *24 \*
3600 \* 1000 - 1*. It is not the amount of milliseconds elapsed in the
day since on DST transitions it will have discontinuities analog to
those of the wall time.

**`IntlCalendar::FIELD_IS_LEAP_MONTH`**  
Calendar field whose value is *1* for indicating a leap month and *0*
otherwise.

**`IntlCalendar::FIELD_FIELD_COUNT`**  
The total number of fields.

**`IntlCalendar::FIELD_DAY_OF_MONTH`**  
Alias for
<a href="/class/intlcalendar.html#" class="link"><strong><code>IntlCalendar::FIELD_DATE</code></strong></a>.

**`IntlCalendar::DOW_SUNDAY`**  
Sunday.

**`IntlCalendar::DOW_MONDAY`**  
Monday.

**`IntlCalendar::DOW_TUESDAY`**  
Tuesday.

**`IntlCalendar::DOW_WEDNESDAY`**  
Wednesday.

**`IntlCalendar::DOW_THURSDAY`**  
Thursday.

**`IntlCalendar::DOW_FRIDAY`**  
Friday.

**`IntlCalendar::DOW_SATURDAY`**  
Saturday.

**`IntlCalendar::DOW_TYPE_WEEKDAY`**  
Output of <span class="function">IntlCalendar::getDayOfWeekType</span>
indicating a day of week is a weekday.

**`IntlCalendar::DOW_TYPE_WEEKEND`**  
Output of <span class="function">IntlCalendar::getDayOfWeekType</span>
indicating a day of week belongs to the weekend.

**`IntlCalendar::DOW_TYPE_WEEKEND_OFFSET`**  
Output of <span class="function">IntlCalendar::getDayOfWeekType</span>
indicating the weekend begins during the given day of week.

**`IntlCalendar::DOW_TYPE_WEEKEND_CEASE`**  
Output of <span class="function">IntlCalendar::getDayOfWeekType</span>
indicating the weekend ends during the given day of week.

**`IntlCalendar::WALLTIME_FIRST`**  
Output of <span
class="function">IntlCalendar::getSkippedWallTimeOption</span>
indicating that wall times in the skipped range should refer to the same
instant as wall times with one hour less and of <span
class="function">IntlCalendar::getRepeatedWallTimeOption</span>
indicating the wall times in the repeated range should refer to the
instant of the first occurrence of such wall time.

**`IntlCalendar::WALLTIME_LAST`**  
Output of <span
class="function">IntlCalendar::getSkippedWallTimeOption</span>
indicating that wall times in the skipped range should refer to the same
instant as wall times with one hour after and of <span
class="function">IntlCalendar::getRepeatedWallTimeOption</span>
indicating the wall times in the repeated range should refer to the
instant of the second occurrence of such wall time.

**`IntlCalendar::WALLTIME_NEXT_VALID`**  
Output of <span
class="function">IntlCalendar::getSkippedWallTimeOption</span>
indicating that wall times in the skipped range should refer to the
instant when the daylight saving time transition occurs (begins).

IntlCalendar::add
=================

Add a (signed) amount of time to a field

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::add</span> ( <span
class="methodparam"><span class="type">int</span> `$field`</span> ,
<span class="methodparam"><span class="type">int</span> `$amount`</span>
)

过程化风格

<span class="type">bool</span> <span
class="methodname">intlcal\_add</span> ( <span class="methodparam"><span
class="type">IntlCalendar</span> `$cal`</span> , <span
class="methodparam"><span class="type">int</span> `$field`</span> ,
<span class="methodparam"><span class="type">int</span> `$amount`</span>
)

Add a signed amount to a field. Adding a positive amount allows advances
in time, even if the numeric value of the field decreases (e.g. when
working with years in BC dates).

Other fields may need to adjusted – for instance, adding a month to the
31st of January will result in the 28th (or 29th) of February. Contrary
to <span class="function">IntlCalendar::roll</span>, when a value wraps
around, more significant fields may change. For instance, adding a day
to the 31st of January will result in the 1st of February, not the 1st
of January.

### 参数

`cal`  
The IntlCalendar resource.

`field`  
One of the <span class="classname">IntlCalendar</span> date/time
<a href="/class/intlcalendar.html#预定义常量" class="link">field constants</a>.
These are integer values between *0* and
**`IntlCalendar::FIELD_COUNT`**.

`amount`  
The signed amount to add to the current field. If the amount is
positive, the instant will be moved forward; if it is negative, the
instant will be moved into the past. The unit is implicit to the field
type. For instance, hours for **`IntlCalendar::FIELD_HOUR_OF_DAY`**.

### 返回值

Returns **`TRUE`** on success 或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 <span class="function">IntlCalendar::add</span>**

``` php
<?php
ini_set('intl.default_locale', 'fr_FR');
ini_set('date.timezone', 'UTC');

$cal = new IntlGregorianCalendar(2012, 0 /* January */, 31);
echo IntlDateFormatter::formatObject($cal), "\n";

$cal->add(IntlCalendar::FIELD_MONTH, 1);
echo IntlDateFormatter::formatObject($cal), "\n";

$cal->add(IntlCalendar::FIELD_DAY_OF_MONTH, 1);
echo IntlDateFormatter::formatObject($cal), "\n";
```

以上例程会输出：

    31 janv. 2012 00:00:00
    29 févr. 2012 00:00:00
    1 mars 2012 00:00:00

IntlCalendar::after
===================

Whether this objectʼs time is after that of the passed object

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::after</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span>
`$other`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">intlcal\_after</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">IntlCalendar</span>
`$other`</span> )

Returns whether this objectʼs time succeeds the argumentʼs time.

### 参数

`cal`  
The IntlCalendar resource.

`other`  
The calendar whose time will be checked against the primary objectʼs
time.

### 返回值

Returns **`TRUE`** if this objectʼs current time is after that of the
`calendar` argumentʼs time. Returns **`FALSE`** otherwise. Also returns
**`FALSE`** on failure. You can use
<a href="/intl/setup.html#" class="link">exceptions</a> or <span
class="function">intl\_get\_error\_code</span> to detect error
conditions.

### 范例

**示例 \#1 <span class="function">IntlCalendar::after</span>**

``` php
<?php
$cal1 = IntlCalendar::createInstance();
$cal2 = clone $cal1;

var_dump($cal1->after($cal2), //false
        $cal2->after($cal1)); //false

$cal1->roll(IntlCalendar::FIELD_MILLISECOND, true);

var_dump($cal1->after($cal2), //true
        $cal2->after($cal1)); //false
```

IntlCalendar::before
====================

Whether this objectʼs time is before that of the passed object

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::before</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span>
`$other`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">intlcal\_before</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">IntlCalendar</span>
`$other`</span> )

Returns whether this objectʼs time precedes the argumentʼs time.

### 参数

`cal`  
The IntlCalendar resource.

`other`  
The calendar whose time will be checked against the primary objectʼs
time.

### 返回值

Returns **`TRUE`** if this objectʼs current time is before that of the
`calendar` argumentʼs time. Returns **`FALSE`** otherwise. Also returns
**`FALSE`** on failure. You can use
<a href="/intl/setup.html#" class="link">exceptions</a> or <span
class="function">intl\_get\_error\_code</span> to detect error
conditions.

IntlCalendar::clear
===================

Clear a field or all fields

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::clear</span> (\[ <span
class="methodparam"><span class="type">int</span> `$field`<span
class="initializer"> = NULL</span></span> \] )

过程化风格

<span class="type">bool</span> <span
class="methodname">intlcal\_clear</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$field`<span class="initializer"> = NULL</span></span> \] )

Clears either all of the fields or a specific field. A cleared field is
marked as unset, giving it the lowest priority against overlapping
fields or even default values when calculating the time. Additionally,
its value is set to *0*, though given the fieldʼs low priority, its
value may have been internally set to another value by the time the
field has finished been queried.

### 参数

`cal`  
The IntlCalendar resource.

`field`  
One of the <span class="classname">IntlCalendar</span> date/time
<a href="/class/intlcalendar.html#预定义常量" class="link">field constants</a>.
These are integer values between *0* and
**`IntlCalendar::FIELD_COUNT`**.

### 返回值

Returns **`TRUE`** on success 或者在失败时返回 **`FALSE`**. Failure can
only occur is invalid arguments are provided.

### 范例

**示例 \#1 <span class="function">IntlCalendar::clear</span> examples**

``` php
<?php
ini_set('intl.default_locale', 'es_ES');
ini_set('date.timezone', 'UTC');

$fields = array(
    'FIELD_ERA'                  => 0,
    'FIELD_YEAR'                 => 1,
    'FIELD_MONTH'                => 2,
    'FIELD_WEEK_OF_YEAR'         => 3,
    'FIELD_WEEK_OF_MONTH'        => 4,
    'FIELD_DATE'                 => 5,
    'FIELD_DAY_OF_YEAR'          => 6,
    'FIELD_DAY_OF_WEEK'          => 7,
    'FIELD_DAY_OF_WEEK_IN_MONTH' => 8,
    'FIELD_AM_PM'                => 9,
    'FIELD_HOUR'                 => 10,
    'FIELD_HOUR_OF_DAY'          => 11,
    'FIELD_MINUTE'               => 12,
    'FIELD_SECOND'               => 13,
    'FIELD_MILLISECOND'          => 14,
    'FIELD_ZONE_OFFSET'          => 15,
    'FIELD_DST_OFFSET'           => 16,
    'FIELD_YEAR_WOY'             => 17,
    'FIELD_DOW_LOCAL'            => 18,
    'FIELD_EXTENDED_YEAR'        => 19,
    'FIELD_JULIAN_DAY'           => 20,
    'FIELD_MILLISECONDS_IN_DAY'  => 21,
    'FIELD_IS_LEAP_MONTH'        => 22,
    'FIELD_FIELD_COUNT'          => 23,
);
function getSetFields(IntlCalendar $cal) {
    global $fields;
    $ret = array();
    foreach ($fields as $name => $value) {
        if ($cal->isSet($value)) {
            $ret[] = $name;
        }
    }
    return $ret;
}

$cal = new IntlGregorianCalendar(2013, 2 /* March */, 15);
echo "After GregorianCalendar creation\n";
print_r(getSetFields($cal));
echo "\n";

echo IntlDateFormatter::formatObject($cal), "\n";
echo "After the formatter requested the extended year\n";
print_r(getSetFields($cal));
echo "\n";

$cal->clear(IntlCalendar::FIELD_YEAR);
echo "After the year has been cleared, the date stays the same\n";
echo IntlDateFormatter::formatObject($cal), "\n";
echo "because FIELD_EXTENDED_YEAR is still set\n";
print_r(getSetFields($cal));
echo "\n";

var_dump($cal->clear(IntlCalendar::FIELD_EXTENDED_YEAR));
echo "After the extended year has been cleared\n";
print_r(getSetFields($cal));
echo IntlDateFormatter::formatObject($cal), "\n";
echo "\n";

echo "After the fields are recalculated,\n"
        . " extended year is set again (to 1970)\n";
print_r(getSetFields($cal));
echo "\n";

$cal->clear();
echo "After calling variant with no arguments\n";
print_r(getSetFields($cal));
echo IntlDateFormatter::formatObject($cal), "\n";
```

以上例程会输出：

    After GregorianCalendar creation
    Array
    (
        [0] => FIELD_ERA
        [1] => FIELD_YEAR
        [2] => FIELD_MONTH
        [3] => FIELD_DATE
    )

    15/03/2013 00:00:00
    After the formatter requested the extended year
    Array
    (
        [0] => FIELD_ERA
        [1] => FIELD_YEAR
        [2] => FIELD_MONTH
        [3] => FIELD_DATE
        [4] => FIELD_EXTENDED_YEAR
    )

    After the year has been cleared, the date stays the same
    15/03/2013 00:00:00
    because FIELD_EXTENDED_YEAR is still set
    Array
    (
        [0] => FIELD_ERA
        [1] => FIELD_MONTH
        [2] => FIELD_DATE
        [3] => FIELD_EXTENDED_YEAR
    )

    bool(true)
    After the extended year has been cleared
    Array
    (
        [0] => FIELD_ERA
        [1] => FIELD_MONTH
        [2] => FIELD_DATE
    )
    15/03/1970 00:00:00

    After the fields are recalculated,
     extended year is set again (to 1970)
    Array
    (
        [0] => FIELD_ERA
        [1] => FIELD_MONTH
        [2] => FIELD_DATE
        [3] => FIELD_EXTENDED_YEAR
    )

    After calling variant with no arguments
    Array
    (
    )
    01/01/1970 00:00:00

IntlCalendar::\_\_construct
===========================

Private constructor for disallowing instantiation

### 说明

<span class="modifier">private</span> <span
class="methodname">IntlCalendar::\_\_construct</span> ( <span
class="methodparam">void</span> )

A private constructor for disallowing instantiation with the
<a href="/language/oop5/basic.html#language.oop5.basic.new" class="link">new</a>
operator.

Call <span class="function">IntlCalendar::createInstance</span> instead.

### 参数

此函数没有参数。

### 返回值

没有返回值。

IntlCalendar::createInstance
============================

Create a new IntlCalendar

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">IntlCalendar</span>
<span class="methodname">IntlCalendar::createInstance</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$timeZone`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$locale`<span
class="initializer"> = ""</span></span> \]\] )

过程化风格

<span class="type">IntlCalendar</span> <span
class="methodname">intlcal\_create\_instance</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$timeZone`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$locale`<span
class="initializer"> = ""</span></span> \]\] )

Given a timezone and locale, this method creates an <span
class="classname">IntlCalendar</span> object. This factory method may
return a subclass of <span class="classname">IntlCalendar</span>.

The calendar created will represent the time instance at which it was
created, based on the system time. The fields can all be cleared by
calling <span class="function">IntCalendar::clear</span> with no
arguments. See also <span
class="function">IntlGregorianCalendar::\_\_construct</span>.

### 参数

`timeZone`  
The timezone to use.

-   **`NULL`**, in which case the default timezone will be used, as
    specified in the ini setting
    <a href="/datetime/setup.html#" class="link">date.timezone</a> or
    through the function <span
    class="function">date\_default\_timezone\_set</span> and as returned
    by <span class="function">date\_default\_timezone\_get</span>.

-   An <span class="classname">IntlTimeZone</span>, which will be used
    directly.

-   A <span class="classname">DateTimeZone</span>. Its identifier will
    be extracted and an ICU timezone object will be created; the
    timezone will be backed by ICUʼs database, not PHPʼs.

-   A <span class="type">string</span>, which should be a valid ICU
    timezone identifier. See <span
    class="function">IntlTimeZone::createTimeZoneIDEnumeration</span>.
    Raw offsets such as *"GMT+08:30"* are also accepted.

`locale`  
A locale to use or **`NULL`** to use
<a href="/intl/setup.html#" class="link">the default locale</a>.

### 返回值

The created <span class="classname">IntlCalendar</span> instance or
**`NULL`** on failure.

### 范例

**示例 \#1 <span class="function">IntlCalendar::createInstance</span>**

``` php
<?php
ini_set('intl.default_locale', 'es_ES');
ini_set('date.timezone', 'Europe/Madrid');

$cal = IntlCalendar::createInstance();
echo "No arguments\n";
var_dump(get_class($cal),
        IntlDateFormatter::formatObject($cal, IntlDateFormatter::FULL));
echo "\n";

echo "Explicit timezone\n";
$cal = IntlCalendar::createInstance(IntlTimeZone::getGMT());
var_dump(get_class($cal),
        IntlDateFormatter::formatObject($cal, IntlDateFormatter::FULL));
echo "\n";

echo "Explicit locale (with calendar)\n";
$cal = IntlCalendar::createInstance(NULL, 'es_ES@calendar=persian');
var_dump(get_class($cal),
        IntlDateFormatter::formatObject($cal, IntlDateFormatter::FULL));
```

以上例程会输出：

    No arguments
    string(21) "IntlGregorianCalendar"
    string(68) "martes 18 de junio de 2013 14:11:02 Hora de verano de Europa Central"

    Explicit timezone
    string(21) "IntlGregorianCalendar"
    string(45) "martes 18 de junio de 2013 12:11:02 GMT+00:00"

    Explicit locale (with calendar)
    string(12) "IntlCalendar"
    string(70) "martes 28 de Khordad de 1392 14:11:02 Hora de verano de Europa Central"

### 参见

-   <span class="methodname">IntlGregorianCalendar::\_\_construct</span>

IntlCalendar::equals
====================

Compare time of two IntlCalendar objects for equality

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::equals</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span>
`$other`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">intlcal\_equals</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">IntlCalendar</span>
`$other`</span> )

Returns true if this calendar and the given calendar have the same time.
The settings, calendar types and field states do not have to be the
same.

### 参数

`cal`  
The IntlCalendar resource.

`other`  
The calendar to compare with the primary object.

### 返回值

Returns **`TRUE`** if the current time of both this and the passed in
<span class="classname">IntlCalendar</span> object are the same, or
**`FALSE`** otherwise. The value **`FALSE`** can also be returned on
failure. This can only happen if bad arguments are passed in. In any
case, the two cases can be distinguished by calling <span
class="function">intl\_get\_error\_code</span>.

### 范例

**示例 \#1 <span class="function">IntlCalendar::equals</span>**

``` php
<?php
ini_set('date.timezone', 'UTC');

$cal1 = IntlCalendar::createInstance(NULL, 'es_ES');
$cal2 = clone $cal1;

var_dump($cal1->equals($cal2)); //TRUE

//The locale is not included in the comparison
$cal2 = IntlCalendar::createInstance(NULL, 'pt_PT');
$cal2->setTime($cal1->getTime());
var_dump($cal1->equals($cal2)); //TRUE

//And set fields state is not included as well
$cal2->clear(IntlCalendar::FIELD_YEAR);
var_dump($cal1->isSet(IntlCalendar::FIELD_YEAR) ==
        $cal2->isSet(IntlCalendar::FIELD_YEAR)); //FALSE
var_dump($cal1->equals($cal2)); //TRUE

//Neither is the calendar type
$cal2 = IntlCalendar::createInstance(NULL, 'es_ES@calendar=islamic');
$cal2->setTime($cal1->getTime());
var_dump($cal1->equals($cal2)); //TRUE

//Only the time is
$cal2 = clone $cal1;
$cal2->setTime($cal1->getTime() + 1.);
var_dump($cal1->equals($cal2)); //FALSE
```

IntlCalendar::fieldDifference
=============================

Calculate difference between given time and this objectʼs time

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlCalendar::fieldDifference</span> ( <span
class="methodparam"><span class="type">float</span> `$when`</span> ,
<span class="methodparam"><span class="type">int</span> `$field`</span>
)

过程化风格

<span class="type">int</span> <span
class="methodname">intlcal\_field\_difference</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">float</span>
`$when`</span> , <span class="methodparam"><span class="type">int</span>
`$field`</span> )

Return the difference between the given time and the time this object is
set to, with respect to the quantity specified the `field` parameter.

This method is meant to be called successively, first with the most
significant field of interest down to the least significant field. To
this end, as a side effect, this calendarʼs value for the field
specified is advanced by the amount returned.

### 参数

`cal`  
The IntlCalendar resource.

`when`  
The time against which to compare the quantity represented by the
`field`. For the result to be positive, the time given for this
parameter must be ahead of the time of the object the method is being
invoked on.

`field`  
The field that represents the quantity being compared.

One of the <span class="classname">IntlCalendar</span> date/time
<a href="/class/intlcalendar.html#预定义常量" class="link">field constants</a>.
These are integer values between *0* and
**`IntlCalendar::FIELD_COUNT`**.

### 返回值

Returns a (signed) difference of time in the unit associated with the
specified field 或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 <span class="function">IntlCalendar::fieldDifference</span>**

``` php
<?php
ini_set('date.timezone', 'Europe/Lisbon');
ini_set('intl.default_locale', 'fr_FR');

$cal1 = IntlCalendar::fromDateTime('2012-02-29 09:00:11');
$cal2 = IntlCalendar::fromDateTime('2013-03-01 09:19:29');
$time = $cal2->getTime();

echo "Time before: ", IntlDateFormatter::formatObject($cal1), "\n";

printf(
    "The difference in time is %d year(s), %d month(s), "
  . "%d day(s), %d hour(s) and %d minute(s)\n",
    $cal1->fieldDifference($time, IntlCalendar::FIELD_YEAR),
    $cal1->fieldDifference($time, IntlCalendar::FIELD_MONTH),
    $cal1->fieldDifference($time, IntlCalendar::FIELD_DAY_OF_MONTH),
    $cal1->fieldDifference($time, IntlCalendar::FIELD_HOUR_OF_DAY),
    $cal1->fieldDifference($time, IntlCalendar::FIELD_MINUTE)
);

//now it was advanced to the target time, exception for the seconds,
//for which we did not measure the difference
echo "Time after: ", IntlDateFormatter::formatObject($cal1), "\n";
```

以上例程会输出：

    Time before: 29 févr. 2012 09:00:11
    The difference in time is 1 year(s), 0 month(s), 1 day(s), 0 hour(s) and 19 minute(s)
    Time after: 1 mars 2013 09:19:11

IntlCalendar::fromDateTime
==========================

Create an IntlCalendar from a DateTime object or string

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">IntlCalendar</span>
<span class="methodname">IntlCalendar::fromDateTime</span> ( <span
class="methodparam"><span class="type">mixed</span> `$dateTime`</span> )

过程化风格

<span class="type">IntlCalendar</span> <span
class="methodname">intlcal\_from\_date\_time</span> ( <span
class="methodparam"><span class="type">mixed</span> `$dateTime`</span> )

Creates an <span class="classname">IntlCalendar</span> object either
from a <span class="classname">DateTime</span> object or from a string
from which a <span class="classname">DateTime</span> object can be
built.

The new calendar will represent not only the same instant as the given
<span class="classname">DateTime</span> (subject to precision loss for
dates very far into the past or future), but also the same timezone
(subject to the caveat that different timezone databases will be used,
and therefore the results may differ).

### 参数

`dateTime`  
A <span class="classname">DateTime</span> object or a <span
class="type">string</span> that can be passed to <span
class="function">DateTime::\_\_construct</span>.

### 返回值

The created <span class="classname">IntlCalendar</span> object or
**`NULL`** in case of failure. If a <span class="type">string</span> is
passed, any exception that occurs inside the <span
class="classname">DateTime</span> constructor is propagated.

### 范例

**示例 \#1 <span class="function">IntlCalendar::fromDateTime</span>**

``` php
<?php
ini_set('date.timezone', 'Europe/Lisbon');

//same as IntlCalendar::fromDateTime(new DateTime(...))
$cal1 = IntlCalendar::fromDateTime('2013-02-28 00:01:02 Europe/Berlin');

//Note the timezone is Europe/Berlin, not the default Europe/Lisbon
echo IntlDateFormatter::formatObject($cal1, 'yyyy MMMM d HH:mm:ss VVVV', 'de_DE'), "\n";
```

以上例程会输出：

    2013 Februar 28 00:01:02 Deutschland Zeit

IntlCalendar::get
=================

Get the value for a field

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlCalendar::get</span> ( <span
class="methodparam"><span class="type">int</span> `$field`</span> )

过程化风格

<span class="type">int</span> <span
class="methodname">intlcal\_get</span> ( <span class="methodparam"><span
class="type">IntlCalendar</span> `$cal`</span> , <span
class="methodparam"><span class="type">int</span> `$field`</span> )

Gets the value for a specific field.

### 参数

`cal`  
The IntlCalendar resource.

`field`  
One of the <span class="classname">IntlCalendar</span> date/time
<a href="/class/intlcalendar.html#预定义常量" class="link">field constants</a>.
These are integer values between *0* and
**`IntlCalendar::FIELD_COUNT`**.

### 返回值

An integer with the value of the time field.

### 范例

**示例 \#1 <span class="function">IntlCalendar::get</span>**

``` php
<?php
ini_set('date.timezone', 'Europe/Lisbon');
ini_set('intl.default_locale', 'en_US');

$class = new ReflectionClass('IntlCalendar');
$fields = array();
foreach ($class->getConstants() as $name => $val) {
    if (strpos($name, 'FIELD_') !== 0 || $val > 22)
        continue;
    $fields[$val] = $name;
}

$cal = IntlCalendar::createInstance(); // current time
var_dump(IntlDateFormatter::formatObject($cal));
foreach ($fields as $val => $name) {
    echo "$val ($name)", "\n    ", $cal->get($val), "\n";
}
```

以上例程会输出：

    string(23) "Jul 1, 2013, 4:44:44 AM"
    0 (FIELD_ERA)
        1
    1 (FIELD_YEAR)
        2013
    2 (FIELD_MONTH)
        6
    3 (FIELD_WEEK_OF_YEAR)
        27
    4 (FIELD_WEEK_OF_MONTH)
        1
    5 (FIELD_DAY_OF_MONTH)
        1
    6 (FIELD_DAY_OF_YEAR)
        182
    7 (FIELD_DAY_OF_WEEK)
        2
    8 (FIELD_DAY_OF_WEEK_IN_MONTH)
        1
    9 (FIELD_AM_PM)
        0
    10 (FIELD_HOUR)
        4
    11 (FIELD_HOUR_OF_DAY)
        4
    12 (FIELD_MINUTE)
        44
    13 (FIELD_SECOND)
        44
    14 (FIELD_MILLISECOND)
        551
    15 (FIELD_ZONE_OFFSET)
        0
    16 (FIELD_DST_OFFSET)
        3600000
    17 (FIELD_YEAR_WOY)
        2013
    18 (FIELD_DOW_LOCAL)
        2
    19 (FIELD_EXTENDED_YEAR)
        2013
    20 (FIELD_JULIAN_DAY)
        2456475
    21 (FIELD_MILLISECONDS_IN_DAY)
        17084551
    22 (FIELD_IS_LEAP_MONTH)
        0

IntlCalendar::getActualMaximum
==============================

The maximum value for a field, considering the objectʼs current time

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlCalendar::getActualMaximum</span> ( <span
class="methodparam"><span class="type">int</span> `$field`</span> )

过程化风格

<span class="type">int</span> <span
class="methodname">intlcal\_get\_actual\_maximum</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$field`</span> )

Returns a fieldʼs relative maximum value around the current time. The
exact semantics vary by field, but in the general case this is the value
that would be obtained if one would set the field value into the
<a href="/class/intlcalendar.html#IntlCalendar::getLeastMaximum" class="link">smallest relative maximum</a>
for the field and would increment it until reaching the
<a href="/class/intlcalendar.html#IntlCalendar::getMaximum" class="link">global maximum</a>
or the field value wraps around, in which the value returned would be
the global maximum or the value before the wrapping, respectively.

For instance, in the gregorian calendar, the actual maximum value for
the <a href="/class/intlcalendar.html#" class="link">day of month</a>
would vary between *28* and *31*, depending on the month and year of the
current time.

### 参数

`cal`  
The IntlCalendar resource.

`field`  
One of the <span class="classname">IntlCalendar</span> date/time
<a href="/class/intlcalendar.html#预定义常量" class="link">field constants</a>.
These are integer values between *0* and
**`IntlCalendar::FIELD_COUNT`**.

### 返回值

An <span class="type">int</span> representing the maximum value in the
units associated with the given `field` 或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 <span
class="function">IntlCalendar::getActualMaximum</span>**

``` php
<?php
ini_set('date.timezone', 'Europe/Lisbon');

$cal = IntlCalendar::fromDateTime('2013-02-15');
var_dump($cal->getActualMaximum(IntlCalendar::FIELD_DAY_OF_MONTH)); //28

$cal->add(IntlCalendar::FIELD_EXTENDED_YEAR, -1);
var_dump($cal->getActualMaximum(IntlCalendar::FIELD_DAY_OF_MONTH)); //29
```

以上例程会输出：

    int(28)
    int(29)

### 参见

-   <span class="methodname">IntlCalendar::getMaximum</span>
-   <span class="methodname">IntlCalendar::getLeastMaximum</span>
-   <span class="methodname">IntlCalendar::getActualMinimum</span>

IntlCalendar::getActualMinimum
==============================

The minimum value for a field, considering the objectʼs current time

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlCalendar::getActualMinimum</span> ( <span
class="methodparam"><span class="type">int</span> `$field`</span> )

过程化风格

<span class="type">int</span> <span
class="methodname">intlcal\_get\_actual\_minimum</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$field`</span> )

Returns a fieldʼs relative minimum value around the current time. The
exact semantics vary by field, but in the general case this is the value
that would be obtained if one would set the field value into the
<a href="/class/intlcalendar.html#IntlCalendar::getGreatestMinimum" class="link">greatest relative minimum</a>
for the field and would decrement it until reaching the
<a href="/class/intlcalendar.html#IntlCalendar::getMinimum" class="link">global minimum</a>
or the field value wraps around, in which the value returned would be
the global minimum or the value before the wrapping, respectively.

For the Gregorian calendar, this is always the same as <span
class="function">IntlCalendar::getMinimum</span>.

### 参数

`cal`  
The IntlCalendar resource.

`field`  
One of the <span class="classname">IntlCalendar</span> date/time
<a href="/class/intlcalendar.html#预定义常量" class="link">field constants</a>.
These are integer values between *0* and
**`IntlCalendar::FIELD_COUNT`**.

### 返回值

An <span class="type">int</span> representing the minimum value in the
fieldʼs unit 或者在失败时返回 **`FALSE`**.

### 参见

-   <span class="methodname">IntlCalendar::getMinimum</span>
-   <span class="methodname">IntlCalendar::getGreatestMinimum</span>
-   <span class="methodname">IntlCalendar::getActualMaximum</span>

IntlCalendar::getAvailableLocales
=================================

Get array of locales for which there is data

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">IntlCalendar::getAvailableLocales</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">array</span> <span
class="methodname">intlcal\_get\_available\_locales</span> ( <span
class="methodparam">void</span> )

Gives the list of locales for which calendars are installed. As of ICU
51, this is the list of all installed ICU locales.

### 参数

此函数没有参数。

### 返回值

An <span class="type">array</span> of <span class="type">string</span>s,
one for which locale.

### 范例

**示例 \#1 <span
class="function">IntlCalendar::getAvailableLocales</span>**

``` php
<?php
print_r(IntlCalendar::getAvailableLocales());
```

以上例程会输出：

    Array
    (
        [0] => af
        [1] => af_NA
        [2] => af_ZA
        [3] => agq
        [4] => agq_CM
        [5] => ak
        [6] => ak_GH
        [7] => am
        [8] => am_ET
        [9] => ar
        [10] => ar_001
        [11] => ar_AE
        [12] => ar_BH
        [13] => ar_DJ
        … output abbreviated …
        [595] => zh_Hant_HK
        [596] => zh_Hant_MO
        [597] => zh_Hant_TW
        [598] => zu
        [599] => zu_ZA
    )

IntlCalendar::getDayOfWeekType
==============================

Tell whether a day is a weekday, weekend or a day that has a transition
between the two

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlCalendar::getDayOfWeekType</span> ( <span
class="methodparam"><span class="type">int</span> `$dayOfWeek`</span> )

过程化风格

<span class="type">int</span> <span
class="methodname">intlcal\_get\_day\_of\_week\_type</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$dayOfWeek`</span> )

Returns whether the passed day is a weekday
(**`IntlCalendar::DOW_TYPE_WEEKDAY`**), a weekend day
(**`IntlCalendar::DOW_TYPE_WEEKEND`**), a day during which a transition
occurs into the weekend (**`IntlCalendar::DOW_TYPE_WEEKEND_OFFSET`**) or
a day during which the weekend ceases
(**`IntlCalendar::DOW_TYPE_WEEKEND_CEASE`**).

If the return is either **`IntlCalendar::DOW_TYPE_WEEKEND_OFFSET`** or
**`IntlCalendar::DOW_TYPE_WEEKEND_CEASE`**, then <span
class="function">IntlCalendar::getWeekendTransition</span> can be called
to obtain the time of the transition.

This function requires ICU 4.4 or later.

### 参数

`cal`  
The IntlCalendar resource.

`dayOfWeek`  
One of the constants **`IntlCalendar::DOW_SUNDAY`**,
**`IntlCalendar::DOW_MONDAY`**, …, **`IntlCalendar::DOW_SATURDAY`**.

### 返回值

Returns one of the constants **`IntlCalendar::DOW_TYPE_WEEKDAY`**,
**`IntlCalendar::DOW_TYPE_WEEKEND`**,
**`IntlCalendar::DOW_TYPE_WEEKEND_OFFSET`** or
**`IntlCalendar::DOW_TYPE_WEEKEND_CEASE`** 或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 <span
class="function">IntlCalendar::getDayOfWeekType</span>**

``` php
<?php

foreach (array('en_US', 'ar_SA') as $locale) {
    echo "Locale: ", Locale::getDisplayName($locale, "en_US"), "\n";

    $cal = IntlCalendar::createInstance('UTC', $locale);

    for ($i = IntlCalendar::DOW_SUNDAY; $i <= IntlCalendar::DOW_SATURDAY; $i++) {
        echo $i, " ", $cal->getDayOfWeekType($i), " ",
                $cal->getDayOfWeekType($i) >= IntlCalendar::DOW_TYPE_WEEKEND_OFFSET
                        ? $cal->getWeekendTransition($i)
                        : '',
                "\n";
    }
    echo "\n";
}
```

以上例程会输出：

    Locale: English (United States)
    1 3 86400000
    2 0 
    3 0 
    4 0 
    5 0 
    6 0 
    7 1 

    Locale: Arabic (Saudi Arabia)
    1 0 
    2 0 
    3 0 
    4 0 
    5 1 
    6 3 86400000
    7 0 

IntlCalendar::getErrorCode
==========================

intlcal\_get\_error\_code
=========================

Get last error code on the object

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlCalendar::getErrorCode</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">int</span> <span
class="methodname">intlcal\_get\_error\_code</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span>
`$calendar`</span> )

Returns the numeric ICU error code for the last call on this object
(including cloning) or the <span class="classname">IntlCalendar</span>
given for the `calendar` parameter (in the procedural‒style version).
This may indicate only a warning (negative error code) or no error at
all (**`U_ZERO_ERROR`**). The actual presence of an error can be tested
with <span class="function">intl\_is\_failure</span>.

Invalid arguments detected on the PHP side (before invoking functions of
the ICU library) are not recorded for the purposes of this function.

The last error that occurred in any call to a function of the intl
extension, including early argument errors, can be obtained with <span
class="function">intl\_get\_error\_code</span>. This function resets the
global error code, but not the objectʼs error code.

### 参数

`calendar`  
The calendar object, on the procedural style interface.

### 返回值

An ICU error code indicating either success, failure or a warning.

### 范例

**示例 \#1 <span class="function">IntlCalendar::getErrorCode</span> and
<span class="function">IntlCalendar::getErrorMessage</span>**

``` php
<?php
ini_set("intl.error_level", E_WARNING);
ini_set("intl.default_locale", "nl");

$intlcal = new IntlGregorianCalendar(2012, 1, 29);
var_dump(
    $intlcal->getErrorCode(),
    $intlcal->getErrorMessage()
);
$intlcal->fieldDifference(-1e100, IntlCalendar::FIELD_SECOND);

var_dump(
    $intlcal->getErrorCode(),
    $intlcal->getErrorMessage()
);
```

以上例程会输出：

    int(0)
    string(12) "U_ZERO_ERROR"

    Warning: IntlCalendar::fieldDifference(): intlcal_field_difference: Call to ICU method has failed in /home/glopes/php/ws/example.php on line 10
    int(1)
    string(81) "intlcal_field_difference: Call to ICU method has failed: U_ILLEGAL_ARGUMENT_ERROR"

### 参见

-   <span class="methodname">IntlCalendar::getErrorMessage</span>
-   <span class="methodname">intl\_is\_failure</span>
-   <span class="methodname">intl\_error\_name</span>
-   <span class="methodname">intl\_get\_error\_code</span>
-   <span class="methodname">intl\_get\_error\_message</span>

IntlCalendar::getErrorMessage
=============================

intlcal\_get\_error\_message
============================

Get last error message on the object

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">IntlCalendar::getErrorMessage</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">string</span> <span
class="methodname">intlcal\_get\_error\_message</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span>
`$calendar`</span> )

Returns the error message (if any) associated with the error reported by
<span class="function">IntlCalendar::getErrorCode</span> or <span
class="function">intlcal\_get\_error\_code</span>. If there is no
associated error message, only the string representation of the name of
the error constant will be returned. Otherwise, the message also
includes a message set on the side of the PHP binding.

### 参数

`calendar`  
The calendar object, on the procedural style interface.

### 返回值

The error message associated with last error that occurred in a function
call on this object, or a string indicating the non-existance of an
error.

### 范例

**示例 \#1 <span class="function">IntlCalendar::getErrorMessage</span>**

``` php
<?php
$cal = IntlCalendar::createInstance('UTC', 'en_US');
var_dump($cal->getErrorMessage());

$cal->getWeekendTransition(IntlCalendar::DOW_WEDNESDAY);
var_dump($cal->getErrorMessage());
```

以上例程会输出：

    string(12) "U_ZERO_ERROR"
    string(82) "intlcal_get_weekend_transition: Error calling ICU method: U_ILLEGAL_ARGUMENT_ERROR"

IntlCalendar::getFirstDayOfWeek
===============================

Get the first day of the week for the calendarʼs locale

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlCalendar::getFirstDayOfWeek</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">int</span> <span
class="methodname">intlcal\_get\_first\_day\_of\_week</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
)

The week day deemed to start a week, either the default value for this
locale or the value set with <span
class="function">IntlCalendar::setFirstDayOfWeek</span>.

### 参数

`cal`  
The IntlCalendar resource.

### 返回值

One of the constants **`IntlCalendar::DOW_SUNDAY`**,
**`IntlCalendar::DOW_MONDAY`**, …, **`IntlCalendar::DOW_SATURDAY`**
或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 <span
class="function">IntlCalendar::getFirstDayOfWeek</span>**

``` php
<?php
ini_set('date.timezone', 'UTC');

$cal1 = IntlCalendar::createInstance(NULL, 'es_ES');
var_dump($cal1->getFirstDayOfWeek()); // Monday
$cal1->set(2013, 1 /* February */, 3); // a Sunday
var_dump($cal1->get(IntlCalendar::FIELD_WEEK_OF_YEAR)); // 5

$cal2 = IntlCalendar::createInstance(NULL, 'en_US');
var_dump($cal2->getFirstDayOfWeek()); // Sunday
$cal2->set(2013, 1 /* February */, 3); // a Sunday
var_dump($cal2->get(IntlCalendar::FIELD_WEEK_OF_YEAR)); // 6
```

以上例程会输出：

    int(2)
    int(5)
    int(1)
    int(6)

### 参见

-   <span class="methodname">IntlCalendar::setFirstDayOfWeek</span>

IntlCalendar::getGreatestMinimum
================================

Get the largest local minimum value for a field

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlCalendar::getGreatestMinimum</span> ( <span
class="methodparam"><span class="type">int</span> `$field`</span> )

过程化风格

<span class="type">int</span> <span
class="methodname">intlcal\_get\_greatest\_minimum</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$field`</span> )

Returns the largest local minimum for a field. This should be a value
larger or equal to that returned by <span
class="function">IntlCalendar::getActualMinimum</span>, which is in its
turn larger or equal to that returned by <span
class="function">IntlCalendar::getMinimum</span>. All these three
functions return the same value for the Gregorian calendar.

### 参数

`cal`  
The IntlCalendar resource.

`field`  
One of the <span class="classname">IntlCalendar</span> date/time
<a href="/class/intlcalendar.html#预定义常量" class="link">field constants</a>.
These are integer values between *0* and
**`IntlCalendar::FIELD_COUNT`**.

### 返回值

An <span class="type">int</span> representing a field value, in the
fieldʼs unit, 或者在失败时返回 **`FALSE`**.

IntlCalendar::getKeywordValuesForLocale
=======================================

Get set of locale keyword values

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">Iterator</span> <span
class="methodname">IntlCalendar::getKeywordValuesForLocale</span> (
<span class="methodparam"><span class="type">string</span> `$key`</span>
, <span class="methodparam"><span class="type">string</span>
`$locale`</span> , <span class="methodparam"><span
class="type">bool</span> `$commonlyUsed`</span> )

过程化风格

<span class="type">Iterator</span> <span
class="methodname">intlcal\_get\_keyword\_values\_for\_locale</span> (
<span class="methodparam"><span class="type">string</span> `$key`</span>
, <span class="methodparam"><span class="type">string</span>
`$locale`</span> , <span class="methodparam"><span
class="type">bool</span> `$commonlyUsed`</span> )

For a given locale key, get the set of values for that key that would
result in a different behavior. For now, only the *'calendar'* keyword
is supported.

This function requires ICU 4.2 or later.

### 参数

`key`  
The locale keyword for which relevant values are to be queried. Only
*'calendar'* is supported.

`locale`  
The locale onto which the keyword/value pair are to be appended.

`commonlyUsed`  
Whether to show only the values commonly used for the specified locale.

### 返回值

An iterator that yields strings with the locale keyword values
或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 <span
class="function">IntlCalendar::getKeyworkValuesForLocale</span>**

``` php
<?php
print_r(
        iterator_to_array(
                IntlCalendar::getKeywordValuesForLocale(
                        'calendar', 'fa_IR', true)));
print_r(
        iterator_to_array(
                IntlCalendar::getKeywordValuesForLocale(
                        'calendar', 'fa_IR', false)));
```

以上例程会输出：

    Array
    (
        [0] => persian
        [1] => gregorian
        [2] => islamic
        [3] => islamic-civil
    )
    Array
    (
        [0] => persian
        [1] => gregorian
        [2] => islamic
        [3] => islamic-civil
        [4] => japanese
        [5] => buddhist
        [6] => roc
        [7] => hebrew
        [8] => chinese
        [9] => indian
        [10] => coptic
        [11] => ethiopic
        [12] => ethiopic-amete-alem
    )

IntlCalendar::getLeastMaximum
=============================

Get the smallest local maximum for a field

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlCalendar::getLeastMaximum</span> ( <span
class="methodparam"><span class="type">int</span> `$field`</span> )

过程化风格

<span class="type">int</span> <span
class="methodname">intlcal\_get\_least\_maximum</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$field`</span> )

Returns the smallest local maximumw for a field. This should be a value
smaller or equal to that returned by <span
class="function">IntlCalendar::getActualMaxmimum</span>, which is in its
turn smaller or equal to that returned by <span
class="function">IntlCalendar::getMaximum</span>.

### 参数

`cal`  
The IntlCalendar resource.

`field`  
One of the <span class="classname">IntlCalendar</span> date/time
<a href="/class/intlcalendar.html#预定义常量" class="link">field constants</a>.
These are integer values between *0* and
**`IntlCalendar::FIELD_COUNT`**.

### 返回值

An <span class="type">int</span> representing a field value in the
fieldʼs unit 或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 Maxima examples**

``` php
<?php
ini_set('date.timezone', 'UTC');
ini_set('intl.default_locale', 'it_IT');

$cal = new IntlGregorianCalendar(2013, 3 /* April */, 6);
var_dump(
    $cal->getLeastMaximum(IntlCalendar::FIELD_DAY_OF_MONTH),  // 28
    $cal->getActualMaximum(IntlCalendar::FIELD_DAY_OF_MONTH), // 30
    $cal->getMaximum(IntlCalendar::FIELD_DAY_OF_MONTH)        // 31
);
```

以上例程会输出：

    int(28)
    int(30)
    int(31)

### 参见

-   <span class="methodname">IntlCalendar::getActualMaximum</span>
-   <span class="methodname">IntlCalendar::getMaximum</span>
-   <span class="methodname">IntlCalendar::getGreatestMinimum</span>

IntlCalendar::getLocale
=======================

Get the locale associated with the object

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">IntlCalendar::getLocale</span> ( <span
class="methodparam"><span class="type">int</span> `$localeType`</span> )

过程化风格

<span class="type">string</span> <span
class="methodname">intlcal\_get\_locale</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$localeType`</span> )

Returns the locale used by this calendar object.

### 参数

`cal`  
The IntlCalendar resource.

`localeType`  
Whether to fetch the actual locale (the locale from which the calendar
data originates, with **`Locale::ACTUAL_LOCALE`**) or the valid locale,
i.e., the most specific locale supported by ICU relatively to the
requested locale – see **`Locale::VALID_LOCALE`**. From the most general
to the most specific, the locales are ordered in this fashion – actual
locale, valid locale, requested locale.

### 返回值

A locale string 或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 <span class="function">IntlCalendar::getLocale</span>**

``` php
<?php
$cal = IntlCalendar::createInstance(IntlTimeZone::getGMT(), 'en_US_CALIFORNIA');
var_dump(
    $cal->getLocale(Locale::ACTUAL_LOCALE),
    $cal->getLocale(Locale::VALID_LOCALE)
);
```

以上例程会输出：

    string(2) "en"
    string(5) "en_US"

IntlCalendar::getMaximum
========================

Get the global maximum value for a field

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlCalendar::getMaximum</span> ( <span
class="methodparam"><span class="type">int</span> `$field`</span> )

过程化风格

<span class="type">int</span> <span
class="methodname">intlcal\_get\_maximum</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$field`</span> )

Gets the global maximum for a field, in this specific calendar. This
value is larger or equal to that returned by <span
class="function">IntlCalendar::getActualMaximum</span>, which is in its
turn larger or equal to that returned by <span
class="function">IntlCalendar::getLeastMaximum</span>.

### 参数

`cal`  
The IntlCalendar resource.

`field`  
One of the <span class="classname">IntlCalendar</span> date/time
<a href="/class/intlcalendar.html#预定义常量" class="link">field constants</a>.
These are integer values between *0* and
**`IntlCalendar::FIELD_COUNT`**.

### 返回值

An <span class="type">int</span> representing a field value in the
fieldʼs unit 或者在失败时返回 **`FALSE`**.

### 参见

-   <span class="methodname">IntlCalendar::getActualMaximum</span>
-   <span class="methodname">IntlCalendar::getLeastMaximum</span>
-   <span class="methodname">IntlCalendar::getMinimum</span>

IntlCalendar::getMinimalDaysInFirstWeek
=======================================

Get minimal number of days the first week in a year or month can have

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlCalendar::getMinimalDaysInFirstWeek</span> (
<span class="methodparam">void</span> )

过程化风格

<span class="type">int</span> <span
class="methodname">intlcal\_get\_minimal\_days\_in\_first\_week</span> (
<span class="methodparam"><span class="type">IntlCalendar</span>
`$cal`</span> )

Returns the smallest number of days the first week of a year or month
must have in the new year or month. For instance, in the Gregorian
calendar, if this value is 1, then the first week of the year will
necessarily include January 1st, while if this value is 7, then the week
with January 1st will be the first week of the year only if the day of
the week for January 1st matches the day of the week returned by <span
class="function">IntlCalendar::getFirstDayOfWeek</span>; otherwise it
will be the previous yearʼs last week.

### 参数

`cal`  
The IntlCalendar resource.

### 返回值

An <span class="type">int</span> representing a number of days
或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 <span
class="function">IntlCalendar::getMinimalDaysInFirstWeek</span>**

``` php
<?php
ini_set('date.timezone', 'UTC');
ini_set('intl.default_locale', 'en_US');

$cal = new IntlGregorianCalendar(2013, 0 /* January */, 2);
var_dump(IntlDateFormatter::formatObject($cal, 'cccc')); // Wednesday

var_dump($cal->getMinimalDaysInFirstWeek(), // 1
$cal->getFirstDayofWeek()); // 1 (Sunday)

// Week 1 of 2013
var_dump(IntlDateFormatter::formatObject($cal, "'Week 'w' of 'Y"));

$cal->setMinimalDaysInFirstWeek(4);
// Still Week 1 of 2013 (1st week has 5 days in the new year)
var_dump(IntlDateFormatter::formatObject($cal, "'Week 'w' of 'Y"));

$cal->setMinimalDaysInFirstWeek(6);
// Week 53 of 2012
var_dump(IntlDateFormatter::formatObject($cal, "'Week 'w' of 'Y"));
```

以上例程会输出：

    string(9) "Wednesday"
    int(1)
    int(1)
    string(14) "Week 1 of 2013"
    string(14) "Week 1 of 2013"
    string(15) "Week 53 of 2012"

IntlCalendar::getMinimum
========================

Get the global minimum value for a field

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlCalendar::getMinimum</span> ( <span
class="methodparam"><span class="type">int</span> `$field`</span> )

过程化风格

<span class="type">int</span> <span
class="methodname">intlcal\_get\_minimum</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$field`</span> )

Gets the global minimum for a field, in this specific calendar. This
value is smaller or equal to that returned by <span
class="function">IntlCalendar::getActualMinimum</span>, which is in its
turn smaller or equal to that returned by <span
class="function">IntlCalendar::getGreatestMinimum</span>. For the
Gregorian calendar, these three functions always return the same value
(for each field).

### 参数

`cal`  
The IntlCalendar resource.

`field`  
One of the <span class="classname">IntlCalendar</span> date/time
<a href="/class/intlcalendar.html#预定义常量" class="link">field constants</a>.
These are integer values between *0* and
**`IntlCalendar::FIELD_COUNT`**.

### 返回值

An <span class="type">int</span> representing a value for the given
field in the fieldʼs unit 或者在失败时返回 **`FALSE`**.

IntlCalendar::getNow
====================

Get number representing the current time

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">float</span> <span
class="methodname">IntlCalendar::getNow</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">float</span> <span
class="methodname">intlcal\_get\_now</span> ( <span
class="methodparam">void</span> )

The number of milliseconds that have passed since the reference date.
This number is derived from the system time.

### 参数

此函数没有参数。

### 返回值

A <span class="type">float</span> representing a number of milliseconds
since the epoch, not counting leap seconds.

### 范例

**示例 \#1 <span class="function">IntlCalendar::getNow</span>**

``` php
<?php
$formatter = IntlDateFormatter::create('es_ES',
        IntlDateFormatter::FULL,
        IntlDateFormatter::FULL,
        'Europe/Madrid');

$val = IntlCalendar::getNow();

var_dump($val);
echo $formatter->format(IntlCalendar::getNow() / 1000.), "\n";
```

以上例程会输出：

    float(1371425814666)
    lunes, 17 de junio de 2013 01:36:54 Hora de verano de Europa central

IntlCalendar::getRepeatedWallTimeOption
=======================================

Get behavior for handling repeating wall time

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlCalendar::getRepeatedWallTimeOption</span> (
<span class="methodparam">void</span> )

过程化风格

<span class="type">int</span> <span
class="methodname">intlcal\_get\_repeated\_wall\_time\_option</span> (
<span class="methodparam"><span class="type">IntlCalendar</span>
`$cal`</span> )

Gets the current strategy for dealing with wall times that are repeated
whenever the clock is set back during dailight saving time end
transitions. The default value is **`IntlCalendar::WALLTIME_LAST`**.

This function requires ICU 4.9 or later.

### 参数

`cal`  
The IntlCalendar resource.

### 返回值

One of the constants **`IntlCalendar::WALLTIME_FIRST`** or
**`IntlCalendar::WALLTIME_LAST`**.

### 范例

**示例 \#1 <span
class="function">IntlCalendar::getRepeatedWallTimeOption</span>**

``` php
<?php
ini_set('date.timezone', 'Europe/Lisbon');
ini_set('intl.default_locale', 'en_US');
ini_set('intl.error_level', E_WARNING);

//On October 27th at 0200, the clock goes back 1 hour and from GMT+01 to GMT+00
$cal = new IntlGregorianCalendar(2013, 9 /* October */, 27, 1, 30);

var_dump($cal->getRepeatedWalltimeOption()); // 0 WALLTIME_LAST

$formatter = IntlDateFormatter::create(
    NULL,
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'UTC'
);
var_dump($formatter->format($cal->getTime() / 1000.));

$cal->setRepeatedWalltimeOption(IntlCalendar::WALLTIME_FIRST);
var_dump($cal->getRepeatedWalltimeOption()); // 1 WALLTIME_FIRST
$cal->set(IntlCalendar::FIELD_HOUR_OF_DAY, 1);

var_dump($formatter->format($cal->getTime() / 1000.));
```

以上例程会输出：

    int(0)
    string(42) "Sunday, October 27, 2013 at 1:30:00 AM GMT"
    int(1)
    string(43) "Sunday, October 27, 2013 at 12:30:00 AM GMT"

### 参见

-   <span
    class="methodname">IntlCalendar::getSkippedWallTimeOption</span>
-   <span
    class="methodname">IntlCalendar::setSkippedWallTimeOption</span>
-   <span
    class="methodname">IntlCalendar::setRepeatedWallTimeOption</span>

IntlCalendar::getSkippedWallTimeOption
======================================

Get behavior for handling skipped wall time

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlCalendar::getSkippedWallTimeOption</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">int</span> <span
class="methodname">intlcal\_get\_skipped\_wall\_time\_option</span> (
<span class="methodparam"><span class="type">IntlCalendar</span>
`$cal`</span> )

Gets the current strategy for dealing with wall times that are skipped
whenever the clock is forwarded during dailight saving time start
transitions. The default value is **`IntlCalendar::WALLTIME_LAST`**.

The calendar must be
<a href="/class/intlcalendar.html#IntlCalendar::setLenient" class="link">lenient</a>
for this option to have any effect, otherwise attempting to set a
non-existing time will cause an error.

This function requires ICU 4.9 or later.

### 参数

`cal`  
The IntlCalendar resource.

### 返回值

One of the constants **`IntlCalendar::WALLTIME_FIRST`**,
**`IntlCalendar::WALLTIME_LAST`** or
**`IntlCalendar::WALLTIME_NEXT_VALID`**.

### 范例

**示例 \#1 <span
class="function">IntlCalendar::getSkippedWallTimeOption</span>**

``` php
<?php
ini_set('date.timezone', 'Europe/Lisbon');
ini_set('intl.default_locale', 'en_US');
ini_set('intl.error_level', E_WARNING);

//On March 31st at 0100, the clock goes forward 1 hour and from GMT+00 to GMT+01
$cal = new IntlGregorianCalendar(2013, 2 /* March */, 31, 1, 30);

var_dump(
    $cal->isLenient(),               // true
    $cal->getSkippedWalltimeOption() // 0 WALLTIME_LAST
);

$formatter = IntlDateFormatter::create(
    NULL,
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'UTC'
);
var_dump($formatter->format($cal->getTime() / 1000));

$cal->setSkippedWallTimeOption(IntlCalendar::WALLTIME_FIRST);
var_dump($cal->getSkippedWalltimeOption()); // 1 WALLTIME_FIRST
$cal->set(IntlCalendar::FIELD_HOUR_OF_DAY, 1);

var_dump($formatter->format($cal->getTime() / 1000));

$cal->setSkippedWallTimeOption(IntlCalendar::WALLTIME_NEXT_VALID);
var_dump($cal->getSkippedWalltimeOption()); // 2 WALLTIME_NEXT_VALID
$cal->set(IntlCalendar::FIELD_HOUR_OF_DAY, 1);

var_dump($formatter->format($cal->getTime() / 1000));
```

以上例程会输出：

    bool(true)
    int(0)
    string(40) "Sunday, March 31, 2013 at 1:30:00 AM GMT"
    int(1)
    string(41) "Sunday, March 31, 2013 at 12:30:00 AM GMT"
    int(2)
    string(40) "Sunday, March 31, 2013 at 1:00:00 AM GMT"

### 参见

-   <span
    class="methodname">IntlCalendar::getRepeatedWallTimeOption</span>
-   <span
    class="methodname">IntlCalendar::setSkippedWallTimeOption</span>
-   <span
    class="methodname">IntlCalendar::setRepeatedWallTimeOption</span>

IntlCalendar::getTime
=====================

Get time currently represented by the object

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">float</span>
<span class="methodname">IntlCalendar::getTime</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">float</span> <span
class="methodname">intlcal\_get\_time</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
)

Returns the time associated with this object, expressed as the number of
milliseconds since the epoch.

### 参数

`cal`  
The IntlCalendar resource.

### 返回值

A <span class="type">float</span> representing the number of
milliseconds elapsed since the reference time (1 Jan 1970 00:00:00 UTC).

### 范例

**示例 \#1 <span class="function">IntlCalendar::getTime</span>**

``` php
<?php
ini_set('date.timezone', 'Europe/Lisbon');
ini_set('intl.default_locale', 'en_US');

$cal = new IntlGregorianCalendar(2013, 4 /* May */, 1, 0, 0, 0);
$time = $cal->getTime();
var_dump($time, $time / 1000 == strtotime('2013-05-01 00:00:00')); //true
```

以上例程会输出：

    float(1367362800000)
    bool(true)

### 参见

-   <span class="methodname">IntlCalendar::getNow</span>

IntlCalendar::getTimeZone
=========================

Get the objectʼs timezone

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="type">IntlTimeZone</span> <span
class="methodname">IntlCalendar::getTimeZone</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">IntlTimeZone</span> <span
class="methodname">intlcal\_get\_time\_zone</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
)

Returns the <span class="classname">IntlTimeZone</span> object
associated with this calendar.

### 参数

`cal`  
The IntlCalendar resource.

### 返回值

An <span class="classname">IntlTimeZone</span> object corresponding to
the one used internally in this object.

### 范例

**示例 \#1 <span class="function">IntlCalendar::getTimeZone</span>**

``` php
<?php
ini_set('date.timezone', 'Europe/Lisbon');
ini_set('intl.default_locale', 'en_US');

$cal = IntlCalendar::createInstance();
print_r($cal->getTimeZone());

$cal->setTimeZone('UTC');
print_r($cal->getTimeZone());

$cal = IntlCalendar::fromDateTime('2012-01-01 00:00:00 GMT+03:33');
print_r($cal->getTimeZone());
```

以上例程会输出：

    IntlTimeZone Object
    (
        [valid] => 1
        [id] => Europe/Lisbon
        [rawOffset] => 0
        [currentOffset] => 3600000
    )
    IntlTimeZone Object
    (
        [valid] => 1
        [id] => UTC
        [rawOffset] => 0
        [currentOffset] => 0
    )
    IntlTimeZone Object
    (
        [valid] => 1
        [id] => GMT+03:33
        [rawOffset] => 12780000
        [currentOffset] => 12780000
    )

### 参见

-   <span class="methodname">IntlCalendar::setTimeZone</span>
-   <span class="methodname">IntlCalendar::createInstance</span>
-   <span class="methodname">IntlGregorianCalendar::\_\_construct</span>

IntlCalendar::getType
=====================

Get the calendar type

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">IntlCalendar::getType</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">string</span> <span
class="methodname">intlcal\_get\_type</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
)

A string describing the type of this calendar. This is one of the
<a href="/class/intlcalendar.html#IntlCalendar::getKeywordValuesForLocale" class="link">valid values</a>
for the calendar keyword value *'calendar'*.

### 参数

`cal`  
The IntlCalendar resource.

### 返回值

A <span class="type">string</span> representing the calendar type, such
as *'gregorian'*, *'islamic'*, etc.

### 范例

**示例 \#1 <span class="function">IntlCalendar::getType</span>**

``` php
<?php
ini_set('date.timezone', 'Europe/Lisbon');
ini_set('intl.default_locale', 'en_US');

$cal = IntlCalendar::createInstance(NULL, '@calendar=ethiopic-amete-alem');
var_dump($cal->getType());

$cal = new IntlGregorianCalendar();
var_dump($cal->getType());
```

以上例程会输出：

    string(19) "ethiopic-amete-alem"
    string(9) "gregorian"

IntlCalendar::getWeekendTransition
==================================

Get time of the day at which weekend begins or ends

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlCalendar::getWeekendTransition</span> ( <span
class="methodparam"><span class="type">string</span> `$dayOfWeek`</span>
)

过程化风格

<span class="type">int</span> <span
class="methodname">intlcal\_get\_weekend\_transition</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">string</span>
`$dayOfWeek`</span> )

Returns the number of milliseconds after midnight at which the weekend
begins or ends.

This is only applicable for days of the week for which <span
class="function">IntlCalendar::getDayOfWeekType</span> returns either
**`IntlCalendar::DOW_TYPE_WEEKEND_OFFSET`** or
**`IntlCalendar::DOW_TYPE_WEEKEND_CEASE`**. Calling this function for
other days of the week is an error condition.

This function requires ICU 4.4 or later.

### 参数

`cal`  
The IntlCalendar resource.

`dayOfWeek`  
One of the constants **`IntlCalendar::DOW_SUNDAY`**,
**`IntlCalendar::DOW_MONDAY`**, …, **`IntlCalendar::DOW_SATURDAY`**.

### 返回值

The number of milliseconds into the day at which the weekend begins or
ends 或者在失败时返回 **`FALSE`**.

### 范例

See example on <span
class="function">IntlCalendar::getDayOfWeekType</span>.

IntlCalendar::inDaylightTime
============================

Whether the objectʼs time is in Daylight Savings Time

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::inDaylightTime</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">intlcal\_in\_daylight\_time</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
)

Whether, for the instant represented by this object and for this
objectʼs timezone, daylight saving time is in place.

### 参数

`cal`  
The IntlCalendar resource.

### 返回值

Returns **`TRUE`** if the date is in Daylight Savings Time, **`FALSE`**
otherwise. The value **`FALSE`** may also be returned on failure, for
instance after specifying invalid field values on non-lenient mode; use
<a href="/intl/setup.html#" class="link">exceptions</a> or query <span
class="function">intl\_get\_error\_code</span> to disambiguate.

### 范例

**示例 \#1 <span class="function">IntlCalendar::inDaylightTime</span>**

``` php
<?php
ini_set('date.timezone', 'Europe/Lisbon');
ini_set('intl.default_locale', 'pt_PT');

$cal = new IntlGregorianCalendar(2013, 6 /* July */, 1, 4, 56, 31);
var_dump($cal->inDaylightTime()); // true
$cal->set(IntlCalendar::FIELD_MONTH, 11 /* December */);
var_dump($cal->inDaylightTime()); // false

//DST end transition on 2013-10-27 at 0200 (wall time back 1 hour)
$cal = new IntlGregorianCalendar(2013, 9 /* October */, 27, 1, 30, 0);

var_dump($cal->inDaylightTime()); // false (default WALLTIME_LAST)

$cal->setRepeatedWallTimeOption(IntlCalendar::WALLTIME_FIRST);
$cal->set(IntlCalendar::FIELD_HOUR_OF_DAY, 1); // force time recalculation
var_dump($cal->inDaylightTime()); // true
```

IntlCalendar::isEquivalentTo
============================

Whether another calendar is equal but for a different time

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::isEquivalentTo</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span>
`$other`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">intlcal\_is\_equivalent\_to</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">IntlCalendar</span>
`$other`</span> )

Returns whether this and the given object are equivalent for all
purposes except as to the time they have set. The locales do not have to
match, as long as no change in behavior results from such mismatch. This
includes the
<a href="/class/intlcalendar.html#IntlCalendar::getTimeZone" class="link">timezone</a>,
whether the
<a href="/class/intlcalendar.html#IntlCalendar::isLenient" class="link">lenient mode</a>
is set, the
<a href="/class/intlcalendar.html#IntlCalendar::getRepeatedWallTimeOption" class="link">repeated</a>
and
<a href="/class/intlcalendar.html#IntlCalendar::getSkippedWallTimeOption" class="link">skipped</a>
wall time settings, the
<a href="/class/intlcalendar.html#IntlCalendar::getDayOfWeekType" class="link">days of the week when the weekend starts and ceases</a>
and the
<a href="/class/intlcalendar.html#IntlCalendar::getWeekendTransition" class="link">times where such transitions occur</a>.
It may also include other calendar specific settings, such as the
Gregorian/Julian transition instant.

### 参数

`cal`  
The IntlCalendar resource.

`other`  
The other calendar against which the comparison is to be made.

### 返回值

Assuming there are no argument errors, returns **`TRUE`** if the
calendars are equivalent except possibly for their set time.

### 范例

**示例 \#1 <span class="function">IntlCalendar::isEquivalentTo</span>**

``` php
<?php
$cal1 = IntlCalendar::createInstance('Europe/Lisbon', 'pt_PT');
$cal2 = IntlCalendar::createInstance('Europe/Lisbon', 'es_ES');
$cal2->clear();

var_dump($cal1->isEquivalentTo($cal2)); // true

$cal3 = IntlCalendar::createInstance('Europe/Lisbon', 'en_US');
var_dump($cal1->isEquivalentTo($cal3)); // false
var_dump($cal1->getFirstDayOfWeek(),    // 2 (Monday)
$cal3->getFirstDayOfWeek());            // 1 (Sunday)
```

以上例程会输出：

    bool(true)
    bool(false)
    int(2)
    int(1)

### 参见

-   <span class="methodname">IntlCalendar::equals</span>

IntlCalendar::isLenient
=======================

Whether date/time interpretation is in lenient mode

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::isLenient</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">intlcal\_is\_lenient</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
)

Returns whether the current date/time interpretations is lenient (the
default). If that is case, some out of range values for fields will be
accepted instead of raising an error.

### 参数

`cal`  
The IntlCalendar resource.

### 返回值

A <span class="type">bool</span> representing whether the calendar is
set to lenient mode.

### 范例

**示例 \#1 <span class="function">IntlCalendar::isLenient</span>**

``` php
<?php
ini_set('date.timezone', 'Europe/Lisbon');
ini_set('intl.default_locale', 'pt_PT');
ini_set('intl.use_exceptions', '1');

$cal = new IntlGregorianCalendar(2013, 6 /* July */, 1);
var_dump(IntlDateFormatter::formatObject($cal), // 01/07/2013, 00:00:00
$cal->isLenient()); // true

$cal->set(IntlCalendar::FIELD_DAY_OF_MONTH, 33);
var_dump(IntlDateFormatter::formatObject($cal)); // 02/08/2013, 00:00:00

$cal->setLenient(false);
var_dump($cal->isLenient()); // false
$cal->set(IntlCalendar::FIELD_DAY_OF_MONTH, 33);
var_dump(IntlDateFormatter::formatObject($cal)); // error
```

以上例程会输出：

    string(20) "01/07/2013, 00:00:00"
    bool(true)
    string(20) "02/08/2013, 00:00:00"
    bool(false)

    Fatal error: Uncaught exception 'IntlException' with message 'datefmt_format_object: error obtaining instant from IntlCalendar' in /home/foobar/example.php:16
    Stack trace:
    #0 /home/foobar/example.php(16): IntlDateFormatter::formatObject(Object(IntlGregorianCalendar))
    #1 {main}
      thrown in /home/foobar/example.php on line 16

IntlCalendar::isSet
===================

Whether a field is set

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::isSet</span> ( <span
class="methodparam"><span class="type">int</span> `$field`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">intlcal\_is\_set</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$field`</span> )

Returns whether a field is set (as opposed to
<a href="/class/intlcalendar.html#IntlCalendar::clear" class="link">clear</a>).
Set fields take priority over unset fields and their default values when
the date/time is being calculated. Fields set later take priority over
fields set earlier.

### 参数

`cal`  
The IntlCalendar resource.

`field`  
One of the <span class="classname">IntlCalendar</span> date/time
<a href="/class/intlcalendar.html#预定义常量" class="link">field constants</a>.
These are integer values between *0* and
**`IntlCalendar::FIELD_COUNT`**.

### 返回值

Assuming there are no argument errors, returns **`TRUE`** if the field
is set.

### 范例

See the example on <span class="function">IntlCalendar::clear</span>.

### 参见

-   <span class="methodname">IntlCalendar::clear</span>
-   <span class="methodname">IntlCalendar::set</span>

IntlCalendar::isWeekend
=======================

Whether a certain date/time is in the weekend

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::isWeekend</span> (\[ <span
class="methodparam"><span class="type">float</span> `$date`<span
class="initializer"> = NULL</span></span> \] )

过程化风格

<span class="type">bool</span> <span
class="methodname">intlcal\_is\_weekend</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
\[, <span class="methodparam"><span class="type">float</span>
`$date`<span class="initializer"> = NULL</span></span> \] )

Returns whether either the obejctʼs current time or the provided
timestamp occur during a weekend in this objectʼs calendar system.

This function requires ICU 4.4 or later.

### 参数

`cal`  
The IntlCalendar resource.

`date`  
An optional timestamp representing the number of milliseconds since the
epoch, excluding leap seconds. If **`NULL`**, this objectʼs current time
is used instead.

### 返回值

A <span class="type">bool</span> indicating whether the given or this
objectʼs time occurs in a weekend.

The value **`FALSE`** may also be returned on failure, for instance
after giving a date out of bounds on non-lenient mode; use
<a href="/intl/setup.html#" class="link">exceptions</a> or query <span
class="function">intl\_get\_error\_code</span> to disambiguate.

### 范例

**示例 \#1 <span class="function">IntlCalendar::isWeekend</span>**

``` php
<?php
ini_set('date.timezone', 'Europe/Lisbon');

$cal = new IntlGregorianCalendar(NULL, 'en_US');
$cal->set(2013, 6 /* July */, 7); // a Sunday 

var_dump($cal->isWeekend()); // true
var_dump($cal->isWeekend(strtotime('2013-07-01 00:00:00'))); // false, Monday

$cal = new IntlGregorianCalendar(NULL, 'ar_SA');
$cal->set(2013, 6 /* July */, 7); // a Sunday 
var_dump($cal->isWeekend()); // false, Sunday not in weekend in this calendar
```

### 参见

-   <span class="methodname">IntlCalendar::getDayOfWeekType</span>
-   <span class="methodname">IntlCalendar::getWeekendTransition</span>

IntlCalendar::roll
==================

Add value to field without carrying into more significant fields

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::roll</span> ( <span
class="methodparam"><span class="type">int</span> `$field`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$amountOrUpOrDown`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">intlcal\_roll</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$field`</span> , <span class="methodparam"><span
class="type">mixed</span> `$amountOrUpOrDown`</span> )

Adds a (signed) amount to a field. The difference with respect to <span
class="function">IntlCalendar::add</span> is that when the field value
overflows, it does not carry into more significant fields.

### 参数

`cal`  
The IntlCalendar resource.

`field`  
One of the <span class="classname">IntlCalendar</span> date/time
<a href="/class/intlcalendar.html#预定义常量" class="link">field constants</a>.
These are integer values between *0* and
**`IntlCalendar::FIELD_COUNT`**.

`amountOrUpOrDown`  
The (signed) amount to add to the field, **`TRUE`** for rolling up
(adding *1*), or **`FALSE`** for rolling down (subtracting *1*).

### 返回值

Returns **`TRUE`** on success or **`FALSE`** on failure.

### 范例

**示例 \#1 <span class="function">IntlCalendar::roll</span>**

``` php
<?php
ini_set('date.timezone', 'Europe/Lisbon');
ini_set('intl.default_locale', 'pt_PT');

$cal = new IntlGregorianCalendar(2013, 5 /* June */, 30);

$cal->add(IntlCalendar::FIELD_DAY_OF_MONTH, 1);
var_dump(IntlDateFormatter::formatObject($cal)); // "01/07/2013, 00:00:00"

$cal->set(2013, 5 /* June */, 30);
$cal->roll(IntlCalendar::FIELD_DAY_OF_MONTH, true); // roll up, same as rolling +1
var_dump(IntlDateFormatter::formatObject($cal)); // "01/06/2013, 00:00:00"
```

以上例程会输出：

    string(20) "01/07/2013, 00:00:00"
    string(20) "01/06/2013, 00:00:00"

### 参见

-   <span class="methodname">IntlCalendar::add</span>
-   <span class="methodname">IntlCalendar::set</span>

IntlCalendar::set
=================

Set a time field or several common fields at once

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::set</span> ( <span
class="methodparam"><span class="type">int</span> `$field`</span> ,
<span class="methodparam"><span class="type">int</span> `$value`</span>
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::set</span> ( <span
class="methodparam"><span class="type">int</span> `$year`</span> , <span
class="methodparam"><span class="type">int</span> `$month`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$dayOfMonth`<span class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$hour`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$minute`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$second`<span
class="initializer"> = NULL</span></span> \]\]\]\] )

过程化风格

<span class="type">bool</span> <span
class="methodname">intlcal\_set</span> ( <span class="methodparam"><span
class="type">IntlCalendar</span> `$cal`</span> , <span
class="methodparam"><span class="type">int</span> `$field`</span> ,
<span class="methodparam"><span class="type">int</span> `$value`</span>
)

<span class="type">bool</span> <span
class="methodname">intlcal\_set</span> ( <span class="methodparam"><span
class="type">IntlCalendar</span> `$cal`</span> , <span
class="methodparam"><span class="type">int</span> `$year`</span> , <span
class="methodparam"><span class="type">int</span> `$month`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$dayOfMonth`<span class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$hour`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$minute`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$second`<span
class="initializer"> = NULL</span></span> \]\]\]\] )

Sets either a specific field to the given value, or sets at once several
common fields. The range of values that are accepted depend on whether
the calendar is using the
<a href="/class/intlcalendar.html#IntlCalendar::setLenient" class="link">lenient mode</a>.

For fields that conflict, the fields that are set later have priority.

This method cannot be called with exactly four arguments.

### 参数

`cal`  
The IntlCalendar resource.

`field`  
One of the <span class="classname">IntlCalendar</span> date/time
<a href="/class/intlcalendar.html#预定义常量" class="link">field constants</a>.
These are integer values between *0* and
**`IntlCalendar::FIELD_COUNT`**.

`value`  
The new value of the given field.

`year`  
The new value for **`IntlCalendar::FIELD_YEAR`**.

`month`  
The new value for **`IntlCalendar::FIELD_MONTH`**.

`dayOfMonth`  
The new value for **`IntlCalendar::FIELD_DAY_OF_MONTH`**. The month
sequence is zero-based, i.e., January is represented by 0, February by
1, …, December is 11 and Undecember (if the calendar has it) is 12.

`hour`  
The new value for **`IntlCalendar::FIELD_HOUR_OF_DAY`**.

`minute`  
The new value for **`IntlCalendar::FIELD_MINUTE`**.

`second`  
The new value for **`IntlCalendar::FIELD_SECOND`**.

### 返回值

Returns **`TRUE`** on success and **`FALSE`** on failure.

### 范例

**示例 \#1 <span class="function">IntlCalendar::set</span>**

``` php
<?php
ini_set('date.timezone', 'Europe/Lisbon');
ini_set('intl.default_locale', 'pt_PT');

//Calls made later have priority
$cal = new IntlGregorianCalendar(2013, 6 /* July */, 1);
$cal->set(IntlCalendar::FIELD_YEAR, 2012);
$cal->set(IntlCalendar::FIELD_EXTENDED_YEAR, 2011);
var_dump(IntlDateFormatter::formatObject($cal));


$cal = new IntlGregorianCalendar(2013, 6 /* July */, 1);
$cal->set(IntlCalendar::FIELD_YEAR, 2012);
$cal->set(IntlCalendar::FIELD_EXTENDED_YEAR, 2011);
//the time has not been recalculated yet. If we clear the extended year,
//the year set before will be used
$cal->clear(IntlCalendar::FIELD_EXTENDED_YEAR);
var_dump(IntlDateFormatter::formatObject($cal));
```

以上例程会输出：

    string(20) "01/07/2011, 00:00:00"
    string(20) "01/07/2012, 00:00:00"

### 参见

-   <span class="methodname">IntlCalendar::get</span>
-   <span class="methodname">IntlCalendar::add</span>
-   <span class="methodname">IntlCalendar::roll</span>

IntlCalendar::setFirstDayOfWeek
===============================

Set the day on which the week is deemed to start

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::setFirstDayOfWeek</span> ( <span
class="methodparam"><span class="type">int</span> `$dayOfWeek`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">intlcal\_set\_first\_day\_of\_week</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$dayOfWeek`</span> )

Defines the day of week deemed to start the week. This affects the
behavior of fields that depend on the concept of week start and end such
as **`IntlCalendar::FIELD_WEEK_OF_YEAR`** and
**`IntlCalendar::FIELD_YEAR_WOY`**.

### 参数

`cal`  
The IntlCalendar resource.

`dayOfWeek`  
One of the constants **`IntlCalendar::DOW_SUNDAY`**,
**`IntlCalendar::DOW_MONDAY`**, …, **`IntlCalendar::DOW_SATURDAY`**.

### 返回值

Returns **`TRUE`** on success. Failure can only happen due to invalid
parameters.

### 范例

**示例 \#1 <span
class="function">IntlCalendar::setFirstDayOfWeek</span>**

``` php
<?php
ini_set('date.timezone', 'Europe/Lisbon');
ini_set('intl.default_locale', 'es_ES');

$cal = IntlCalendar::createInstance();
$cal->set(2013, 5 /* June */, 30); // A Sunday

var_dump($cal->getFirstDayOfWeek()); // 2 (Monday)

echo IntlDateFormatter::formatObject($cal, <<<EOD
'local day of week: 'cc'
week of month    : 'W'
week of year     : 'ww
EOD
), "\n";

$cal->setFirstDayOfWeek(IntlCalendar::DOW_SUNDAY);

echo IntlDateFormatter::formatObject($cal, <<<EOD
'local day of week: 'cc'
week of month    : 'W'
week of year     : 'ww
EOD
), "\n";
```

以上例程会输出：

    int(2)
    local day of week: 7
    week of month    : 4
    week of year     : 26
    local day of week: 1
    week of month    : 5
    week of year     : 27

IntlCalendar::setLenient
========================

Set whether date/time interpretation is to be lenient

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::setLenient</span> ( <span
class="methodparam"><span class="type">bool</span> `$isLenient`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">intlcal\_set\_lenient</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">bool</span>
`$isLenient`</span> )

Defines whether the calendar is ‘lenient mode’. In such a mode, some of
out-of-bounds values for some fields are accepted, the behavior being
similar to that of <span class="function">IntlCalendar::add</span>
(i.e., the value wraps around, carrying into more significant fields
each time). If the lenient mode is off, then such values will generate
an error.

### 参数

`cal`  
The IntlCalendar resource.

`isLenient`  
Use **`TRUE`** to activate the lenient mode; **`FALSE`** otherwise.

### 返回值

Returns **`TRUE`** on success. Failure can only happen due to invalid
parameters.

### 范例

See the example in <span
class="function">IntlCalendar::isLenient</span>.

IntlCalendar::setMinimalDaysInFirstWeek
=======================================

Set minimal number of days the first week in a year or month can have

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::setMinimalDaysInFirstWeek</span>
( <span class="methodparam"><span class="type">int</span>
`$minimalDays`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">intlcal\_set\_minimal\_days\_in\_first\_week</span> (
<span class="methodparam"><span class="type">IntlCalendar</span>
`$cal`</span> , <span class="methodparam"><span class="type">int</span>
`$minimalDays`</span> )

Sets the smallest number of days the first week of a year or month must
have in the new year or month. For instance, in the Gregorian calendar,
if this value is 1, then the first week of the year will necessarily
include January 1st, while if this value is 7, then the week with
January 1st will be the first week of the year only if the day of the
week for January 1st matches the day of the week returned by <span
class="function">IntlCalendar::getFirstDayOfWeek</span>; otherwise it
will be the previous yearʼs last week.

### 参数

`cal`  
The IntlCalendar resource.

`minimalDays`  
The number of minimal days to set.

### 返回值

**`TRUE`** on success, **`FALSE`** on failure.

IntlCalendar::setRepeatedWallTimeOption
=======================================

Set behavior for handling repeating wall times at negative timezone
offset transitions

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::setRepeatedWallTimeOption</span>
( <span class="methodparam"><span class="type">int</span>
`$wallTimeOption`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">intlcal\_set\_repeated\_wall\_time\_option</span> (
<span class="methodparam"><span class="type">IntlCalendar</span>
`$cal`</span> , <span class="methodparam"><span class="type">int</span>
`$wallTimeOption`</span> )

Sets the current strategy for dealing with wall times that are repeated
whenever the clock is set back during dailight saving time end
transitions. The default value is **`IntlCalendar::WALLTIME_LAST`**
(take the post-DST instant). The other possible value is
**`IntlCalendar::WALLTIME_FIRST`** (take the instant that occurs during
DST).

This function requires ICU 4.9 or later.

### 参数

`cal`  
The IntlCalendar resource.

`wallTimeOption`  
One of the constants **`IntlCalendar::WALLTIME_FIRST`** or
**`IntlCalendar::WALLTIME_LAST`**.

### 返回值

Returns **`TRUE`** on success. Failure can only happen due to invalid
parameters.

### 范例

See the example on <span
class="function">IntlCalendar::getRepeatedWallTimeOption</span>.

### 参见

-   <span
    class="methodname">intlCalendar::getRepeatedWallTimeOption</span>
-   <span
    class="methodname">intlCalendar::setSkippedWallTimeOption</span>
-   <span
    class="methodname">intlCalendar::getSkippedWallTimeOption</span>

IntlCalendar::setSkippedWallTimeOption
======================================

Set behavior for handling skipped wall times at positive timezone offset
transitions

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::setSkippedWallTimeOption</span> (
<span class="methodparam"><span class="type">int</span>
`$wallTimeOption`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">intlcal\_set\_skipped\_wall\_time\_option</span> (
<span class="methodparam"><span class="type">IntlCalendar</span>
`$cal`</span> , <span class="methodparam"><span class="type">int</span>
`$wallTimeOption`</span> )

Sets the current strategy for dealing with wall times that are skipped
whenever the clock is forwarded during dailight saving time start
transitions. The default value is **`IntlCalendar::WALLTIME_LAST`**
(take it as being the same instant as the one when the wall time is one
hour more). Alternative values are **`IntlCalendar::WALLTIME_FIRST`**
(same instant as the one with a wall time of one hour less) and
**`IntlCalendar::WALLTIME_NEXT_VALID`** (same instant as when DST
begins).

This affects only the instant represented by the calendar (as reported
by <span class="function">IntlCalendar::getTime</span>), the field
values will not be rewritten accordingly.

The calendar must be
<a href="/class/intlcalendar.html#IntlCalendar::setLenient" class="link">lenient</a>
for this option to have any effect, otherwise attempting to set a
non-existing time will cause an error.

This function requires ICU 4.9 or later.

### 参数

`cal`  
The IntlCalendar resource.

`wallTimeOption`  
One of the constants **`IntlCalendar::WALLTIME_FIRST`**,
**`IntlCalendar::WALLTIME_LAST`** or
**`IntlCalendar::WALLTIME_NEXT_VALID`**.

### 返回值

Returns **`TRUE`** on success. Failure can only happen due to invalid
parameters.

### 范例

See the example on <span
class="function">IntlCalendar::getSkippedWallTimeOption</span>.

### 参见

-   <span
    class="methodname">intlCalendar::getSkippedWallTimeOption</span>
-   <span
    class="methodname">intlCalendar::setRepeatedWallTimeOption</span>
-   <span
    class="methodname">intlCalendar::getRepeatedWallTimeOption</span>

IntlCalendar::setTime
=====================

Set the calendar time in milliseconds since the epoch

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::setTime</span> ( <span
class="methodparam"><span class="type">float</span> `$date`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">intlcal\_set\_time</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">float</span>
`$date`</span> )

Sets the instant represented by this object. The instant is represented
by a <span class="type">float</span> whose value should be an integer
number of milliseconds since the epoch (1 Jan 1970 00:00:00.000 UTC),
ignoring leap seconds. All the field values will be recalculated
accordingly.

### 参数

`cal`  
The IntlCalendar resource.

`date`  
An instant represented by the number of number of milliseconds between
such instant and the epoch, ignoring leap seconds.

### 返回值

Returns **`TRUE`** on success and **`FALSE`** on failure.

### 范例

**示例 \#1 <span class="function">IntlCalendar::setTime</span>**

``` php
<?php
ini_set('date.timezone', 'Europe/Lisbon');
ini_set('intl.default_locale', 'fr_FR');

$cal = new IntlGregorianCalendar(2013, 5 /* May */, 1, 12, 0, 0);

echo IntlDateFormatter::formatObject($cal, IntlDateFormatter::FULL), "\n";

/* In Europe/Lisbon, on 2013-10-27 at 0200, the clock goes back one hour and
   the timezone from UTC+01 to UTC+00 */

$cal->setTime(strtotime('2013-10-27 00:30:00 UTC') * 1000.);

echo IntlDateFormatter::formatObject($cal, IntlDateFormatter::FULL), "\n";

$cal->setTime(strtotime('2013-10-27 01:30:00 UTC') * 1000.);

echo IntlDateFormatter::formatObject($cal, IntlDateFormatter::FULL), "\n";
```

以上例程会输出：

    samedi 1 juin 2013 12:00:00 heure avancée d’Europe de l’Ouest
    dimanche 27 octobre 2013 01:30:00 heure avancée d’Europe de l’Ouest
    dimanche 27 octobre 2013 01:30:00 heure normale d’Europe de l’Ouest

IntlCalendar::setTimeZone
=========================

Set the timezone used by this calendar

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::setTimeZone</span> ( <span
class="methodparam"><span class="type">mixed</span> `$timeZone`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">intlcal\_set\_time\_zone</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">mixed</span>
`$timeZone`</span> )

Defines a new timezone for this calendar. The time represented by the
object is preserved to the detriment of the field values.

### 参数

`cal`  
The IntlCalendar resource.

`timeZone`  
The new timezone to be used by this calendar. It can be specified in the
following ways:

-   **`NULL`**, in which case the default timezone will be used, as
    specified in the ini setting
    <a href="/datetime/setup.html#" class="link">date.timezone</a> or
    through the function <span
    class="function">date\_default\_timezone\_set</span> and as returned
    by <span class="function">date\_default\_timezone\_get</span>.

-   An <span class="classname">IntlTimeZone</span>, which will be used
    directly.

-   A <span class="classname">DateTimeZone</span>. Its identifier will
    be extracted and an ICU timezone object will be created; the
    timezone will be backed by ICUʼs database, not PHPʼs.

-   A <span class="type">string</span>, which should be a valid ICU
    timezone identifier. See <span
    class="function">IntlTimeZone::createTimeZoneIDEnumeration</span>.
    Raw offsets such as *"GMT+08:30"* are also accepted.

### 返回值

Returns **`TRUE`** on success and **`FALSE`** on failure.

### 范例

**示例 \#1 <span class="function">IntlCalendar::setTimeZone</span>**

``` php
<?php
ini_set('date.timezone', 'Europe/Lisbon');
ini_set('intl.default_locale', 'es_ES');

$cal = new IntlGregorianCalendar(2013, 5 /* May */, 1, 12, 0, 0);

echo IntlDateFormatter::formatObject($cal, IntlDateFormatter::FULL), "\n";
echo "(instant {$cal->getTime()})\n";

$cal->setTimeZone(IntlTimeZone::getGMT());
echo IntlDateFormatter::formatObject($cal, IntlDateFormatter::FULL), "\n";
echo "(instant {$cal->getTime()})\n";

$cal->setTimeZone('GMT+03:33');
echo IntlDateFormatter::formatObject($cal, IntlDateFormatter::FULL), "\n";
echo "(instant {$cal->getTime()})\n";
```

以上例程会输出：

    sábado, 1 de junio de 2013 12:00:00 Hora de verano de Europa occidental
    (instant 1370084400000)
    sábado, 1 de junio de 2013 11:00:00 GMT
    (instant 1370084400000)
    sábado, 1 de junio de 2013 14:33:00 GMT+03:33
    (instant 1370084400000)

IntlCalendar::toDateTime
========================

Convert an IntlCalendar into a DateTime object

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">DateTime</span>
<span class="methodname">IntlCalendar::toDateTime</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">DateTime</span> <span
class="methodname">intlcal\_to\_date\_time</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
)

Create a <span class="classname">DateTime</span> object that represents
the same instant (up to second precision, with a rounding error of less
than 1 second) and has an analog timezone to this object (the difference
being <span class="classname">DateTime</span>ʼs timezone will be backed
by PHPʼs timezone while <span class="classname">IntlCalendar</span>ʼs
timezone is backed by ICUʼs).

### 参数

`cal`  
The IntlCalendar resource.

### 返回值

A <span class="classname">DateTime</span> object with the same timezone
as this object (though using PHPʼs database instead of ICUʼs) and the
same time, except for the smaller precision (second precision instead of
millisecond). Returns **`FALSE`** on failure.

### 范例

**示例 \#1 <span class="function">IntlCalendar::toDateTime</span>**

``` php
<?php
ini_set('date.timezone', 'UTC');
ini_set('intl.default_locale', 'pt_PT');

$cal = IntlCalendar::createInstance('Europe/Lisbon'); //current time

$dt = $cal->toDateTime();
print_r($dt);
```

以上例程会输出：

    DateTime Object
    (
        [date] => 2013-07-02 00:29:13
        [timezone_type] => 3
        [timezone] => Europe/Lisbon
    )

### 参见

-   <span class="methodname">IntlCalendar::fromDateTime</span>
-   <span class="methodname">IntlCalendar::getTime</span>
-   <span class="methodname">IntlCalendar::createInstance</span>
-   <span class="methodname">DateTime:\_\_construct</span>

简介
----

类摘要
------

**IntlGregorianCalendar**

<span class="ooclass"> class **IntlGregorianCalendar** </span> <span
class="ooclass"> <span class="modifier">extends</span> **IntlCalendar**
</span> {

/\* 继承的常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_ERA` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_YEAR` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_MONTH` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_WEEK_OF_YEAR` <span class="initializer"> = 3</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_WEEK_OF_MONTH` <span class="initializer"> =
4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_DATE` <span class="initializer"> = 5</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_DAY_OF_YEAR` <span class="initializer"> = 6</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_DAY_OF_WEEK` <span class="initializer"> = 7</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_DAY_OF_WEEK_IN_MONTH` <span class="initializer"> =
8</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_AM_PM` <span class="initializer"> = 9</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_HOUR` <span class="initializer"> = 10</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_HOUR_OF_DAY` <span class="initializer"> = 11</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_MINUTE` <span class="initializer"> = 12</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_SECOND` <span class="initializer"> = 13</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_MILLISECOND` <span class="initializer"> = 14</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_ZONE_OFFSET` <span class="initializer"> = 15</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_DST_OFFSET` <span class="initializer"> = 16</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_YEAR_WOY` <span class="initializer"> = 17</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_DOW_LOCAL` <span class="initializer"> = 18</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_EXTENDED_YEAR` <span class="initializer"> =
19</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_JULIAN_DAY` <span class="initializer"> = 20</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_MILLISECONDS_IN_DAY` <span class="initializer"> =
21</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_IS_LEAP_MONTH` <span class="initializer"> =
22</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_FIELD_COUNT ` <span class="initializer"> =
23</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::FIELD_DAY_OF_MONTH` <span class="initializer"> = 5</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::DOW_SUNDAY` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::DOW_MONDAY` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::DOW_TUESDAY` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::DOW_WEDNESDAY` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::DOW_THURSDAY` <span class="initializer"> = 5</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::DOW_FRIDAY` <span class="initializer"> = 6</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::DOW_SATURDAY` <span class="initializer"> = 7</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::DOW_TYPE_WEEKDAY` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::DOW_TYPE_WEEKEND` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::DOW_TYPE_WEEKEND_OFFSET` <span class="initializer"> =
2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::DOW_TYPE_WEEKEND_CEASE` <span class="initializer"> =
3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::WALLTIME_FIRST` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::WALLTIME_LAST` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlCalendar::WALLTIME_NEXT_VALID` <span class="initializer"> =
2</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">IntlTimeZone</span> `$tz`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$locale`</span> \]\] )

<span class="modifier">public</span> <span class="type">float</span>
<span class="methodname">getGregorianChange</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isLeapYear</span> ( <span
class="methodparam"><span class="type">int</span> `$year`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setGregorianChange</span> ( <span
class="methodparam"><span class="type">float</span> `$date`</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::add</span> ( <span
class="methodparam"><span class="type">int</span> `$field`</span> ,
<span class="methodparam"><span class="type">int</span> `$amount`</span>
)

<span class="type">bool</span> <span
class="methodname">intlcal\_add</span> ( <span class="methodparam"><span
class="type">IntlCalendar</span> `$cal`</span> , <span
class="methodparam"><span class="type">int</span> `$field`</span> ,
<span class="methodparam"><span class="type">int</span> `$amount`</span>
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::after</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span>
`$other`</span> )

<span class="type">bool</span> <span
class="methodname">intlcal\_after</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">IntlCalendar</span>
`$other`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::before</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span>
`$other`</span> )

<span class="type">bool</span> <span
class="methodname">intlcal\_before</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">IntlCalendar</span>
`$other`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::clear</span> (\[ <span
class="methodparam"><span class="type">int</span> `$field`<span
class="initializer"> = NULL</span></span> \] )

<span class="type">bool</span> <span
class="methodname">intlcal\_clear</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$field`<span class="initializer"> = NULL</span></span> \] )

<span class="modifier">private</span> <span
class="methodname">IntlCalendar::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">IntlCalendar</span>
<span class="methodname">IntlCalendar::createInstance</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$timeZone`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$locale`<span
class="initializer"> = ""</span></span> \]\] )

<span class="type">IntlCalendar</span> <span
class="methodname">intlcal\_create\_instance</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$timeZone`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$locale`<span
class="initializer"> = ""</span></span> \]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::equals</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span>
`$other`</span> )

<span class="type">bool</span> <span
class="methodname">intlcal\_equals</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">IntlCalendar</span>
`$other`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlCalendar::fieldDifference</span> ( <span
class="methodparam"><span class="type">float</span> `$when`</span> ,
<span class="methodparam"><span class="type">int</span> `$field`</span>
)

<span class="type">int</span> <span
class="methodname">intlcal\_field\_difference</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">float</span>
`$when`</span> , <span class="methodparam"><span class="type">int</span>
`$field`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">IntlCalendar</span>
<span class="methodname">IntlCalendar::fromDateTime</span> ( <span
class="methodparam"><span class="type">mixed</span> `$dateTime`</span> )

<span class="type">IntlCalendar</span> <span
class="methodname">intlcal\_from\_date\_time</span> ( <span
class="methodparam"><span class="type">mixed</span> `$dateTime`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlCalendar::get</span> ( <span
class="methodparam"><span class="type">int</span> `$field`</span> )

<span class="type">int</span> <span
class="methodname">intlcal\_get</span> ( <span class="methodparam"><span
class="type">IntlCalendar</span> `$cal`</span> , <span
class="methodparam"><span class="type">int</span> `$field`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlCalendar::getActualMaximum</span> ( <span
class="methodparam"><span class="type">int</span> `$field`</span> )

<span class="type">int</span> <span
class="methodname">intlcal\_get\_actual\_maximum</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$field`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlCalendar::getActualMinimum</span> ( <span
class="methodparam"><span class="type">int</span> `$field`</span> )

<span class="type">int</span> <span
class="methodname">intlcal\_get\_actual\_minimum</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$field`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">IntlCalendar::getAvailableLocales</span> ( <span
class="methodparam">void</span> )

<span class="type">array</span> <span
class="methodname">intlcal\_get\_available\_locales</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlCalendar::getDayOfWeekType</span> ( <span
class="methodparam"><span class="type">int</span> `$dayOfWeek`</span> )

<span class="type">int</span> <span
class="methodname">intlcal\_get\_day\_of\_week\_type</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$dayOfWeek`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlCalendar::getErrorCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">IntlCalendar::getErrorMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlCalendar::getFirstDayOfWeek</span> ( <span
class="methodparam">void</span> )

<span class="type">int</span> <span
class="methodname">intlcal\_get\_first\_day\_of\_week</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
)

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlCalendar::getGreatestMinimum</span> ( <span
class="methodparam"><span class="type">int</span> `$field`</span> )

<span class="type">int</span> <span
class="methodname">intlcal\_get\_greatest\_minimum</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$field`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">Iterator</span> <span
class="methodname">IntlCalendar::getKeywordValuesForLocale</span> (
<span class="methodparam"><span class="type">string</span> `$key`</span>
, <span class="methodparam"><span class="type">string</span>
`$locale`</span> , <span class="methodparam"><span
class="type">bool</span> `$commonlyUsed`</span> )

<span class="type">Iterator</span> <span
class="methodname">intlcal\_get\_keyword\_values\_for\_locale</span> (
<span class="methodparam"><span class="type">string</span> `$key`</span>
, <span class="methodparam"><span class="type">string</span>
`$locale`</span> , <span class="methodparam"><span
class="type">bool</span> `$commonlyUsed`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlCalendar::getLeastMaximum</span> ( <span
class="methodparam"><span class="type">int</span> `$field`</span> )

<span class="type">int</span> <span
class="methodname">intlcal\_get\_least\_maximum</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$field`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">IntlCalendar::getLocale</span> ( <span
class="methodparam"><span class="type">int</span> `$localeType`</span> )

<span class="type">string</span> <span
class="methodname">intlcal\_get\_locale</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$localeType`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlCalendar::getMaximum</span> ( <span
class="methodparam"><span class="type">int</span> `$field`</span> )

<span class="type">int</span> <span
class="methodname">intlcal\_get\_maximum</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$field`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlCalendar::getMinimalDaysInFirstWeek</span> (
<span class="methodparam">void</span> )

<span class="type">int</span> <span
class="methodname">intlcal\_get\_minimal\_days\_in\_first\_week</span> (
<span class="methodparam"><span class="type">IntlCalendar</span>
`$cal`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlCalendar::getMinimum</span> ( <span
class="methodparam"><span class="type">int</span> `$field`</span> )

<span class="type">int</span> <span
class="methodname">intlcal\_get\_minimum</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$field`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">float</span> <span
class="methodname">IntlCalendar::getNow</span> ( <span
class="methodparam">void</span> )

<span class="type">float</span> <span
class="methodname">intlcal\_get\_now</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlCalendar::getRepeatedWallTimeOption</span> (
<span class="methodparam">void</span> )

<span class="type">int</span> <span
class="methodname">intlcal\_get\_repeated\_wall\_time\_option</span> (
<span class="methodparam"><span class="type">IntlCalendar</span>
`$cal`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlCalendar::getSkippedWallTimeOption</span> ( <span
class="methodparam">void</span> )

<span class="type">int</span> <span
class="methodname">intlcal\_get\_skipped\_wall\_time\_option</span> (
<span class="methodparam"><span class="type">IntlCalendar</span>
`$cal`</span> )

<span class="modifier">public</span> <span class="type">float</span>
<span class="methodname">IntlCalendar::getTime</span> ( <span
class="methodparam">void</span> )

<span class="type">float</span> <span
class="methodname">intlcal\_get\_time</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
)

<span class="modifier">public</span> <span
class="type">IntlTimeZone</span> <span
class="methodname">IntlCalendar::getTimeZone</span> ( <span
class="methodparam">void</span> )

<span class="type">IntlTimeZone</span> <span
class="methodname">intlcal\_get\_time\_zone</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
)

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">IntlCalendar::getType</span> ( <span
class="methodparam">void</span> )

<span class="type">string</span> <span
class="methodname">intlcal\_get\_type</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
)

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlCalendar::getWeekendTransition</span> ( <span
class="methodparam"><span class="type">string</span> `$dayOfWeek`</span>
)

<span class="type">int</span> <span
class="methodname">intlcal\_get\_weekend\_transition</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">string</span>
`$dayOfWeek`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::inDaylightTime</span> ( <span
class="methodparam">void</span> )

<span class="type">bool</span> <span
class="methodname">intlcal\_in\_daylight\_time</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::isEquivalentTo</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span>
`$other`</span> )

<span class="type">bool</span> <span
class="methodname">intlcal\_is\_equivalent\_to</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">IntlCalendar</span>
`$other`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::isLenient</span> ( <span
class="methodparam">void</span> )

<span class="type">bool</span> <span
class="methodname">intlcal\_is\_lenient</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::isSet</span> ( <span
class="methodparam"><span class="type">int</span> `$field`</span> )

<span class="type">bool</span> <span
class="methodname">intlcal\_is\_set</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$field`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::isWeekend</span> (\[ <span
class="methodparam"><span class="type">float</span> `$date`<span
class="initializer"> = NULL</span></span> \] )

<span class="type">bool</span> <span
class="methodname">intlcal\_is\_weekend</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
\[, <span class="methodparam"><span class="type">float</span>
`$date`<span class="initializer"> = NULL</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::roll</span> ( <span
class="methodparam"><span class="type">int</span> `$field`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$amountOrUpOrDown`</span> )

<span class="type">bool</span> <span
class="methodname">intlcal\_roll</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$field`</span> , <span class="methodparam"><span
class="type">mixed</span> `$amountOrUpOrDown`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::set</span> ( <span
class="methodparam"><span class="type">int</span> `$field`</span> ,
<span class="methodparam"><span class="type">int</span> `$value`</span>
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::set</span> ( <span
class="methodparam"><span class="type">int</span> `$year`</span> , <span
class="methodparam"><span class="type">int</span> `$month`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$dayOfMonth`<span class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$hour`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$minute`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$second`<span
class="initializer"> = NULL</span></span> \]\]\]\] )

<span class="type">bool</span> <span
class="methodname">intlcal\_set</span> ( <span class="methodparam"><span
class="type">IntlCalendar</span> `$cal`</span> , <span
class="methodparam"><span class="type">int</span> `$field`</span> ,
<span class="methodparam"><span class="type">int</span> `$value`</span>
)

<span class="type">bool</span> <span
class="methodname">intlcal\_set</span> ( <span class="methodparam"><span
class="type">IntlCalendar</span> `$cal`</span> , <span
class="methodparam"><span class="type">int</span> `$year`</span> , <span
class="methodparam"><span class="type">int</span> `$month`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$dayOfMonth`<span class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$hour`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$minute`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$second`<span
class="initializer"> = NULL</span></span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::setFirstDayOfWeek</span> ( <span
class="methodparam"><span class="type">int</span> `$dayOfWeek`</span> )

<span class="type">bool</span> <span
class="methodname">intlcal\_set\_first\_day\_of\_week</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">int</span>
`$dayOfWeek`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::setLenient</span> ( <span
class="methodparam"><span class="type">bool</span> `$isLenient`</span> )

<span class="type">bool</span> <span
class="methodname">intlcal\_set\_lenient</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">bool</span>
`$isLenient`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::setMinimalDaysInFirstWeek</span>
( <span class="methodparam"><span class="type">int</span>
`$minimalDays`</span> )

<span class="type">bool</span> <span
class="methodname">intlcal\_set\_minimal\_days\_in\_first\_week</span> (
<span class="methodparam"><span class="type">IntlCalendar</span>
`$cal`</span> , <span class="methodparam"><span class="type">int</span>
`$minimalDays`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::setRepeatedWallTimeOption</span>
( <span class="methodparam"><span class="type">int</span>
`$wallTimeOption`</span> )

<span class="type">bool</span> <span
class="methodname">intlcal\_set\_repeated\_wall\_time\_option</span> (
<span class="methodparam"><span class="type">IntlCalendar</span>
`$cal`</span> , <span class="methodparam"><span class="type">int</span>
`$wallTimeOption`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::setSkippedWallTimeOption</span> (
<span class="methodparam"><span class="type">int</span>
`$wallTimeOption`</span> )

<span class="type">bool</span> <span
class="methodname">intlcal\_set\_skipped\_wall\_time\_option</span> (
<span class="methodparam"><span class="type">IntlCalendar</span>
`$cal`</span> , <span class="methodparam"><span class="type">int</span>
`$wallTimeOption`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::setTime</span> ( <span
class="methodparam"><span class="type">float</span> `$date`</span> )

<span class="type">bool</span> <span
class="methodname">intlcal\_set\_time</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">float</span>
`$date`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlCalendar::setTimeZone</span> ( <span
class="methodparam"><span class="type">mixed</span> `$timeZone`</span> )

<span class="type">bool</span> <span
class="methodname">intlcal\_set\_time\_zone</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
, <span class="methodparam"><span class="type">mixed</span>
`$timeZone`</span> )

<span class="modifier">public</span> <span class="type">DateTime</span>
<span class="methodname">IntlCalendar::toDateTime</span> ( <span
class="methodparam">void</span> )

<span class="type">DateTime</span> <span
class="methodname">intlcal\_to\_date\_time</span> ( <span
class="methodparam"><span class="type">IntlCalendar</span> `$cal`</span>
)

}

IntlGregorianCalendar::\_\_construct
====================================

Create the Gregorian Calendar class

### 说明

<span class="modifier">public</span> <span
class="methodname">IntlGregorianCalendar::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">IntlTimeZone</span> `$tz`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$locale`</span> \]\] )

<span class="modifier">public</span> <span
class="methodname">IntlGregorianCalendar::\_\_construct</span> ( <span
class="methodparam"><span class="type">int</span>
`$timeZoneOrYear`</span> , <span class="methodparam"><span
class="type">int</span> `$localeOrMonth`</span> , <span
class="methodparam"><span class="type">int</span> `$dayOfMonth`</span> )

<span class="modifier">public</span> <span
class="methodname">IntlGregorianCalendar::\_\_construct</span> ( <span
class="methodparam"><span class="type">int</span>
`$timeZoneOrYear`</span> , <span class="methodparam"><span
class="type">int</span> `$localeOrMonth`</span> , <span
class="methodparam"><span class="type">int</span> `$dayOfMonth`</span> ,
<span class="methodparam"><span class="type">int</span> `$hour`</span> ,
<span class="methodparam"><span class="type">int</span> `$minute`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$second`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`tz`  

`locale`  

`timeZoneOrYear`  

`localeOrMonth`  

`dayOfMonth`  

`hour`  

`minute`  

`second`  

IntlGregorianCalendar::getGregorianChange
=========================================

Get the Gregorian Calendar change date

### 说明

<span class="modifier">public</span> <span class="type">float</span>
<span
class="methodname">IntlGregorianCalendar::getGregorianChange</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Returns the change date 或者在失败时返回 **`FALSE`**.

IntlGregorianCalendar::isLeapYear
=================================

Determine if the given year is a leap year

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlGregorianCalendar::isLeapYear</span> (
<span class="methodparam"><span class="type">int</span> `$year`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`year`  

### 返回值

Returns **`TRUE`** for leap years, **`FALSE`** otherwise and on failure.

IntlGregorianCalendar::setGregorianChange
=========================================

Set the Gregorian Calendar the change date

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span
class="methodname">IntlGregorianCalendar::setGregorianChange</span> (
<span class="methodparam"><span class="type">float</span> `$date`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`date`  

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

简介
----

类摘要
------

**IntlTimeZone**

<span class="ooclass"> class **IntlTimeZone** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">integer</span>
`IntlTimeZone::DISPLAY_SHORT` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlTimeZone::DISPLAY_LONG` <span class="initializer"> = 2</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">countEquivalentIDs</span> ( <span
class="methodparam"><span class="type">string</span> `$zoneId`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">IntlTimeZone</span>
<span class="methodname">createDefault</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">IntlIterator</span>
<span class="methodname">createEnumeration</span> (\[ <span
class="methodparam"><span class="type">mixed</span>
`$countryOrRawOffset`</span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">IntlTimeZone</span>
<span class="methodname">createTimeZone</span> ( <span
class="methodparam"><span class="type">string</span> `$zoneId`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">IntlIterator</span>
<span class="methodname">createTimeZoneIDEnumeration</span> ( <span
class="methodparam"><span class="type">int</span> `$zoneType`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$region`</span> \[, <span class="methodparam"><span
class="type">int</span> `$rawOffset`</span> \]\] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">IntlTimeZone</span>
<span class="methodname">fromDateTimeZone</span> ( <span
class="methodparam"><span class="type">DateTimeZone</span>
`$zoneId`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">getCanonicalID</span> ( <span
class="methodparam"><span class="type">string</span> `$zoneId`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`&$isSystemID`</span> \] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getDisplayName</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$isDaylight`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$style`</span> \[, <span class="methodparam"><span
class="type">string</span> `$locale`</span> \]\]\] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getDSTSavings</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">getEquivalentID</span> ( <span
class="methodparam"><span class="type">string</span> `$zoneId`</span> ,
<span class="methodparam"><span class="type">int</span> `$index`</span>
)

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getErrorCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getErrorMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">IntlTimeZone</span>
<span class="methodname">getGMT</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getID</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">getIDForWindowsID</span> ( <span
class="methodparam"><span class="type">string</span> `$timezone`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$region`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getOffset</span> ( <span class="methodparam"><span
class="type">float</span> `$date`</span> , <span
class="methodparam"><span class="type">bool</span> `$local`</span> ,
<span class="methodparam"><span class="type">int</span>
`&$rawOffset`</span> , <span class="methodparam"><span
class="type">int</span> `&$dstOffset`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getRawOffset</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">getRegion</span> ( <span class="methodparam"><span
class="type">string</span> `$zoneId`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">getTZDataVersion</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">IntlTimeZone</span>
<span class="methodname">getUnknown</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">getWindowsID</span> ( <span class="methodparam"><span
class="type">string</span> `$timezone`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">hasSameRules</span> ( <span
class="methodparam"><span class="type">IntlTimeZone</span>
`$otherTimeZone`</span> )

<span class="modifier">public</span> <span
class="type">DateTimeZone</span> <span
class="methodname">toDateTimeZone</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">useDaylightTime</span> ( <span
class="methodparam">void</span> )

}

预定义常量
----------

**`IntlTimeZone::DISPLAY_SHORT`**  

**`IntlTimeZone::DISPLAY_LONG`**  

IntlTimeZone::countEquivalentIDs
================================

Get the number of IDs in the equivalency group that includes the given
ID

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">IntlTimeZone::countEquivalentIDs</span> ( <span
class="methodparam"><span class="type">string</span> `$zoneId`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`zoneId`  

### 返回值

IntlTimeZone::createDefault
===========================

Create a new copy of the default timezone for this host

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">IntlTimeZone</span>
<span class="methodname">IntlTimeZone::createDefault</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

IntlTimeZone::createEnumeration
===============================

Get an enumeration over time zone IDs associated with the given country
or offset

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">IntlIterator</span>
<span class="methodname">IntlTimeZone::createEnumeration</span> (\[
<span class="methodparam"><span class="type">mixed</span>
`$countryOrRawOffset`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`countryOrRawOffset`  

### 返回值

IntlTimeZone::createTimeZone
============================

Create a timezone object for the given ID

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">IntlTimeZone</span>
<span class="methodname">IntlTimeZone::createTimeZone</span> ( <span
class="methodparam"><span class="type">string</span> `$zoneId`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`zoneId`  

### 返回值

IntlTimeZone::createTimeZoneIDEnumeration
=========================================

Get an enumeration over system time zone IDs with the given filter
conditions

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">IntlIterator</span>
<span
class="methodname">IntlTimeZone::createTimeZoneIDEnumeration</span> (
<span class="methodparam"><span class="type">int</span>
`$zoneType`</span> \[, <span class="methodparam"><span
class="type">string</span> `$region`</span> \[, <span
class="methodparam"><span class="type">int</span> `$rawOffset`</span>
\]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`zoneType`  

`region`  

`rawOffset`  

### 返回值

Returns <span class="classname">IntlIterator</span> 或者在失败时返回
**`FALSE`**.

IntlTimeZone::fromDateTimeZone
==============================

Create a timezone object from <span class="type">DateTimeZone</span>

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">IntlTimeZone</span>
<span class="methodname">IntlTimeZone::fromDateTimeZone</span> ( <span
class="methodparam"><span class="type">DateTimeZone</span>
`$zoneId`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`zoneId`  

### 返回值

IntlTimeZone::getCanonicalID
============================

Get the canonical system timezone ID or the normalized custom time zone
ID for the given time zone ID

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">IntlTimeZone::getCanonicalID</span> ( <span
class="methodparam"><span class="type">string</span> `$zoneId`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`&$isSystemID`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`zoneId`  

`isSystemID`  

### 返回值

IntlTimeZone::getDisplayName
============================

Get a name of this time zone suitable for presentation to the user

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">IntlTimeZone::getDisplayName</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$isDaylight`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$style`</span> \[, <span class="methodparam"><span
class="type">string</span> `$locale`</span> \]\]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`isDaylight`  

`style`  

`locale`  

### 返回值

IntlTimeZone::getDSTSavings
===========================

Get the amount of time to be added to local standard time to get local
wall clock time

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlTimeZone::getDSTSavings</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

IntlTimeZone::getEquivalentID
=============================

Get an ID in the equivalency group that includes the given ID

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">IntlTimeZone::getEquivalentID</span> ( <span
class="methodparam"><span class="type">string</span> `$zoneId`</span> ,
<span class="methodparam"><span class="type">int</span> `$index`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`zoneId`  

`index`  

### 返回值

IntlTimeZone::getErrorCode
==========================

intltz\_get\_error\_code
========================

Get last error code on the object

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlTimeZone::getErrorCode</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">int</span> <span
class="methodname">intltz\_get\_error\_code</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

IntlTimeZone::getErrorMessage
=============================

intltz\_get\_error\_message
===========================

Get last error message on the object

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">IntlTimeZone::getErrorMessage</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">string</span> <span
class="methodname">intltz\_get\_error\_message</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

IntlTimeZone::getGMT
====================

Create GMT (UTC) timezone

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">IntlTimeZone</span>
<span class="methodname">IntlTimeZone::getGMT</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

IntlTimeZone::getID
===================

Get timezone ID

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">IntlTimeZone::getID</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

IntlTimeZone::getIDForWindowsID
===============================

Translate a Windows timezone into a system timezone

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">IntlTimeZone::getIDForWindowsID</span> ( <span
class="methodparam"><span class="type">string</span> `$timezone`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$region`</span> \] )

Translates a Windows timezone (e.g. "Pacific Standard Time") into a
system timezone (e.g. "America/Los\_Angeles").

> **Note**: <span class="simpara"> This function requires ICU version ≥
> 52. </span>

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`timezone`  

`region`  

### 返回值

Returns the system timezone 或者在失败时返回 **`FALSE`**.

### 参见

-   <span class="methodname">IntlTimeZone::getWindowsID</span>

IntlTimeZone::getOffset
=======================

Get the time zone raw and GMT offset for the given moment in time

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlTimeZone::getOffset</span> ( <span
class="methodparam"><span class="type">float</span> `$date`</span> ,
<span class="methodparam"><span class="type">bool</span> `$local`</span>
, <span class="methodparam"><span class="type">int</span>
`&$rawOffset`</span> , <span class="methodparam"><span
class="type">int</span> `&$dstOffset`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`date`  

`local`  

`rawOffset`  

`dstOffset`  

### 返回值

IntlTimeZone::getRawOffset
==========================

Get the raw GMT offset (before taking daylight savings time into account

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlTimeZone::getRawOffset</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

IntlTimeZone::getRegion
=======================

Get the region code associated with the given system time zone ID

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">IntlTimeZone::getRegion</span> ( <span
class="methodparam"><span class="type">string</span> `$zoneId`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`zoneId`  

### 返回值

Return region 或者在失败时返回 **`FALSE`**.

IntlTimeZone::getTZDataVersion
==============================

Get the timezone data version currently used by ICU

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">IntlTimeZone::getTZDataVersion</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

IntlTimeZone::getUnknown
========================

Get the "unknown" time zone

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">IntlTimeZone</span>
<span class="methodname">IntlTimeZone::getUnknown</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Returns <span class="classname">IntlTimeZone</span> or **`NULL`** on
failure.

IntlTimeZone::getWindowsID
==========================

Translate a system timezone into a Windows timezone

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">IntlTimeZone::getWindowsID</span> ( <span
class="methodparam"><span class="type">string</span> `$timezone`</span>
)

Translates a system timezone (e.g. "America/Los\_Angeles") into a
Windows timezone (e.g. "Pacific Standard Time").

> **Note**: <span class="simpara"> This function requires ICU version ≥
> 52. </span>

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`timezone`  

### 返回值

Returns the Windows timezone 或者在失败时返回 **`FALSE`**.

### 参见

-   <span class="methodname">IntlTimeZone::getIDForWindowsID</span>

IntlTimeZone::hasSameRules
==========================

Check if this zone has the same rules and offset as another zone

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlTimeZone::hasSameRules</span> ( <span
class="methodparam"><span class="type">IntlTimeZone</span>
`$otherTimeZone`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`otherTimeZone`  

### 返回值

IntlTimeZone::toDateTimeZone
============================

Convert to <span class="type">DateTimeZone</span> object

### 说明

<span class="modifier">public</span> <span
class="type">DateTimeZone</span> <span
class="methodname">IntlTimeZone::toDateTimeZone</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

IntlTimeZone::useDaylightTime
=============================

Check if this time zone uses daylight savings time

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlTimeZone::useDaylightTime</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

简介
----

Date Formatter is a concrete class that enables locale-dependent
formatting/parsing of dates using pattern strings and/or canned
patterns.

This class represents the ICU date formatting functionality. It allows
users to display dates in a localized format or to parse strings into
PHP date values using pattern strings and/or canned patterns.

Class synopsis
--------------

**IntlDateFormatter**

<span class="ooclass"> class **IntlDateFormatter** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> ,
<span class="methodparam"><span class="type">int</span>
`$datetype`</span> , <span class="methodparam"><span
class="type">int</span> `$timetype`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$timezone`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$calendar`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$pattern`<span
class="initializer"> = ""</span></span> \]\]\] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">IntlDateFormatter</span> <span
class="methodname">create</span> ( <span class="methodparam"><span
class="type">string</span> `$locale`</span> , <span
class="methodparam"><span class="type">int</span> `$datetype`</span> ,
<span class="methodparam"><span class="type">int</span>
`$timetype`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$timezone`<span class="initializer"> =
NULL</span></span> \[, <span class="methodparam"><span
class="type">mixed</span> `$calendar`<span class="initializer"> =
NULL</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$pattern`<span class="initializer"> =
""</span></span> \]\]\] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">format</span> ( <span class="methodparam"><span
class="type">mixed</span> `$value`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">formatObject</span> ( <span class="methodparam"><span
class="type">object</span> `$object`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$format`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$locale`<span
class="initializer"> = NULL</span></span> \]\] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getCalendar</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getDateType</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getErrorCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getErrorMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getLocale</span> (\[ <span
class="methodparam"><span class="type">int</span> `$which`</span> \] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getPattern</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getTimeType</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getTimeZoneId</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">IntlCalendar</span> <span
class="methodname">getCalendarObject</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">IntlTimeZone</span> <span
class="methodname">getTimeZone</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isLenient</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">localtime</span> ( <span
class="methodparam"><span class="type">string</span> `$value`</span> \[,
<span class="methodparam"><span class="type">int</span>
`&$position`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">parse</span> ( <span class="methodparam"><span
class="type">string</span> `$value`</span> \[, <span
class="methodparam"><span class="type">int</span> `&$position`</span> \]
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setCalendar</span> ( <span
class="methodparam"><span class="type">mixed</span> `$which`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setLenient</span> ( <span
class="methodparam"><span class="type">bool</span> `$lenient`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setPattern</span> ( <span
class="methodparam"><span class="type">string</span> `$pattern`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setTimeZoneId</span> ( <span
class="methodparam"><span class="type">string</span> `$zone`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setTimeZone</span> ( <span
class="methodparam"><span class="type">mixed</span> `$zone`</span> )

}

参见
----

-   <a href="http://www.icu-project.org/apiref/icu4c/udat_8h.html#details" class="link external">» ICU Date formatter</a>

<!-- -->

-   <a href="http://www.icu-project.org/apiref/icu4c/classSimpleDateFormat.html#details" class="link external">» ICU Date formats</a>

预定义常量
----------

These constants are used to specify different formats in the constructor
for DateType and TimeType.

**`IntlDateFormatter::NONE`** (<span class="type">integer</span>)  
<span class="simpara">Do not include this element</span>

**`IntlDateFormatter::FULL`** (<span class="type">integer</span>)  
<span class="simpara">Completely specified style (Tuesday, April 12,
1952 AD or 3:30:42pm PST)</span>

**`IntlDateFormatter::LONG`** (<span class="type">integer</span>)  
<span class="simpara">Long style (January 12, 1952 or 3:30:32pm)</span>

**`IntlDateFormatter::MEDIUM`** (<span class="type">integer</span>)  
<span class="simpara">Medium style (Jan 12, 1952)</span>

**`IntlDateFormatter::SHORT`** (<span class="type">integer</span>)  
<span class="simpara">Most abbreviated style, only essential data
(12/13/52 or 3:30pm)</span>

The following int constants are used to specify the calendar. These
calendars are all based directly on the Gregorian calendar.
Non-Gregorian calendars need to be specified in locale. Examples might
include locale="hi@calendar=BUDDHIST".

**`IntlDateFormatter::TRADITIONAL`** (<span class="type">integer</span>)  
<span class="simpara">Non-Gregorian Calendar</span>

**`IntlDateFormatter::GREGORIAN`** (<span class="type">integer</span>)  
<span class="simpara">Gregorian Calendar</span>

IntlDateFormatter::create
=========================

datefmt\_create
===============

IntlDateFormatter::\_\_construct
================================

Create a date formatter

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">IntlDateFormatter</span> <span
class="methodname">IntlDateFormatter::create</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> ,
<span class="methodparam"><span class="type">int</span>
`$datetype`</span> , <span class="methodparam"><span
class="type">int</span> `$timetype`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$timezone`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$calendar`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$pattern`<span
class="initializer"> = ""</span></span> \]\]\] )

面向对象风格 (constructor)

<span class="modifier">public</span> <span
class="methodname">IntlDateFormatter::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> ,
<span class="methodparam"><span class="type">int</span>
`$datetype`</span> , <span class="methodparam"><span
class="type">int</span> `$timetype`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$timezone`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$calendar`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$pattern`<span
class="initializer"> = ""</span></span> \]\]\] )

过程化风格

<span class="type">IntlDateFormatter</span> <span
class="methodname">datefmt\_create</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> ,
<span class="methodparam"><span class="type">int</span>
`$datetype`</span> , <span class="methodparam"><span
class="type">int</span> `$timetype`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$timezone`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$calendar`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$pattern`<span
class="initializer"> = ""</span></span> \]\]\] )

Create a date formatter.

### 参数

`locale`  
Locale to use when formatting or parsing or **`NULL`** to use the value
specified in the ini setting
<a href="/intl/setup.html#" class="link">intl.default_locale</a>.

`datetype`  
Date type to use (**`none`**, **`short`**, **`medium`**, **`long`**,
**`full`**). This is one of the
<a href="/class/intldateformatter.html#预定义常量" class="link">IntlDateFormatter constants</a>.
It can also be **`NULL`**, in which case ICUʼs default date type will be
used.

`timetype`  
Time type to use (**`none`**, **`short`**, **`medium`**, **`long`**,
**`full`**). This is one of the
<a href="/class/intldateformatter.html#预定义常量" class="link">IntlDateFormatter constants</a>.
It can also be **`NULL`**, in which case ICUʼs default time type will be
used.

`timezone`  
Time zone ID. The default (and the one used if **`NULL`** is given) is
the one returned by <span
class="function">date\_default\_timezone\_get</span> or, if applicable,
that of the <span class="classname">IntlCalendar</span> object passed
for the `calendar` parameter. This ID must be a valid identifier on
ICUʼs database or an ID representing an explicit offset, such as
*GMT-05:30*.

This can also be an <span class="classname">IntlTimeZone</span> or a
<span class="classname">DateTimeZone</span> object.

`calendar`  
Calendar to use for formatting or parsing. The default value is
**`NULL`**, which corresponds to **`IntlDateFormatter::GREGORIAN`**.
This can either be one of the
<a href="/class/intldateformatter.html#" class="link">IntlDateFormatter calendar constants</a>
or an <span class="classname">IntlCalendar</span>. Any <span
class="classname">IntlCalendar</span> object passed will be clone; it
will not be changed by the <span
class="classname">IntlDateFormatter</span>. This will determine the
calendar type used (gregorian, islamic, persian, etc.) and, if
**`NULL`** is given for the `timezone` parameter, also the timezone
used.

`pattern`  
Optional pattern to use when formatting or parsing. Possible patterns
are documented at
<a href="http://userguide.icu-project.org/formatparse/datetime" class="link external">» http://userguide.icu-project.org/formatparse/datetime</a>.

### 返回值

The created <span class="classname">IntlDateFormatter</span> or
**`FALSE`** in case of failure.

### 更新日志

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>版本</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>5.5.0/PECL 3.0.0</td>
<td><p>An <span class="classname">IntlCalendar</span> object is allowed for <code class="parameter">calendar</code>.</p>
<p>Objects of type <span class="classname">IntlTimeZone</span> and <span class="classname">DateTimeZone</span> are allowed for <code class="parameter">timezone</code>.</p>
<p>Invalid timezone identifiers (including empty strings) are no longer allowed for <code class="parameter">timezone</code>.</p>
<p>If <strong><code>NULL</code></strong> is given for <code class="parameter">timezone</code>, the timezone identifier given by <span class="function">date_default_timezone_get</span> will be used instead of ICUʼs default.</p></td>
</tr>
</tbody>
</table>

### 范例

**示例 \#1 <span class="function">datefmt\_create</span> example**

``` php
<?php
$fmt = datefmt_create( "en_US" ,IntlDateFormatter::FULL, IntlDateFormatter::FULL,
    'America/Los_Angeles', IntlDateFormatter::GREGORIAN  );
echo "First Formatted output is ".datefmt_format( $fmt , 0);
$fmt = datefmt_create( "de-DE" ,IntlDateFormatter::FULL, IntlDateFormatter::FULL,
    'America/Los_Angeles',IntlDateFormatter::GREGORIAN  );
echo "Second Formatted output is ".datefmt_format( $fmt , 0);

$fmt = datefmt_create( "en_US" ,IntlDateFormatter::FULL, IntlDateFormatter::FULL,
     'America/Los_Angeles',IntlDateFormatter::GREGORIAN  ,"MM/dd/yyyy");
echo "First Formatted output with pattern is ".datefmt_format( $fmt , 0);
$fmt = datefmt_create( "de-DE" ,IntlDateFormatter::FULL, IntlDateFormatter::FULL,
     'America/Los_Angeles',IntlDateFormatter::GREGORIAN  ,"MM/dd/yyyy");
echo "Second Formatted output with pattern is ".datefmt_format( $fmt , 0);
?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new IntlDateFormatter( "en_US" ,IntlDateFormatter::FULL, IntlDateFormatter::FULL,
    'America/Los_Angeles',IntlDateFormatter::GREGORIAN  );
echo "First Formatted output is ".$fmt->format(0);
$fmt = new IntlDateFormatter( "de-DE" ,IntlDateFormatter::FULL, IntlDateFormatter::FULL, 
    'America/Los_Angeles',IntlDateFormatter::GREGORIAN  );
echo "Second Formatted output is ".$fmt->format(0);

$fmt = new IntlDateFormatter( "en_US" ,IntlDateFormatter::FULL, IntlDateFormatter::FULL, 
     'America/Los_Angeles',IntlDateFormatter::GREGORIAN  ,"MM/dd/yyyy");
echo "First Formatted output with pattern is ".$fmt->format(0);
$fmt = new IntlDateFormatter( "de-DE" ,IntlDateFormatter::FULL, IntlDateFormatter::FULL,
      'America/Los_Angeles',IntlDateFormatter::GREGORIAN , "MM/dd/yyyy");
echo "Second Formatted output with pattern is ".$fmt->format(0);
?>
```

以上例程会输出：

    First Formatted output is Wednesday, December 31, 1969 4:00:00 PM PT
    Second Formatted output is Mittwoch, 31. Dezember 1969 16:00 Uhr GMT-08:00
    First Formatted output with pattern is 12/31/1969
    Second Formatted output with pattern is 12/31/1969
             

### 参见

-   <span class="function">datefmt\_format</span>
-   <span class="function">datefmt\_parse</span>
-   <span class="function">datefmt\_get\_error\_code</span>
-   <span class="function">datefmt\_get\_error\_message</span>

IntlDateFormatter::format
=========================

datefmt\_format
===============

Format the date/time value as a string

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">IntlDateFormatter::format</span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

过程化风格

<span class="type">string</span> <span
class="methodname">datefmt\_format</span> ( <span
class="methodparam"><span class="type">IntlDateFormatter</span>
`$fmt`</span> , <span class="methodparam"><span
class="type">mixed</span> `$value`</span> )

Formats the time value as a string.

### 参数

`fmt`  
The date formatter resource.

`value`  
Value to format. This may be a <span
class="classname">DateTimeInterface</span> object, an <span
class="classname">IntlCalendar</span> object, a <span
class="type">numeric</span> type representing a (possibly fractional)
number of seconds since epoch or an <span class="type">array</span> in
the format output by <span class="function">localtime</span>.

If a <span class="classname">DateTime</span> or an <span
class="classname">IntlCalendar</span> object is passed, its timezone is
not considered. The object will be formatted using the formaterʼs
configured timezone. If one wants to use the timezone of the object to
be formatted, <span
class="function">IntlDateFormatter::setTimeZone</span> must be called
before with the objectʼs timezone. Alternatively, the static function
<span class="function">IntlDateFormatter::formatObject</span> may be
used instead.

### 返回值

The formatted string or, if an error occurred, **`FALSE`**.

### 更新日志

| 版本             | 说明                                                                                                                                                                                                             |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 7.1.5            | Support for providing general <span class="classname">DateTimeInterface</span> objects to the `value` parameter was added. Formerly, only proper <span class="classname">DateTime</span> objects were supported. |
| 5.5.0/PECL 3.0.0 | Support for providing <span class="classname">IntlCalendar</span> objects to the `value` parameter was added.                                                                                                    |
| 5.3.4            | Support for providing <span class="classname">DateTime</span> objects to the `value` parameter was added.                                                                                                        |

### 范例

**示例 \#1 <span class="function">datefmt\_format</span> example**

``` php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'First Formatted output is ' . datefmt_format($fmt, 0);

$fmt = datefmt_create(
    'de-DE',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Second Formatted output is ' . datefmt_format($fmt, 0);

$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN,
    'MM/dd/yyyy'
);
echo 'First Formatted output with pattern is ' . datefmt_format($fmt, 0);

$fmt = datefmt_create(
    'de-DE',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN,
    'MM/dd/yyyy'
);
echo "Second Formatted output with pattern is " . datefmt_format($fmt, 0);
?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'First Formatted output is ' . $fmt->format(0);

$fmt = new IntlDateFormatter(
    'de-DE',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Second Formatted output is ' . $fmt->format(0);

$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN,
    'MM/dd/yyyy'
);
echo 'First Formatted output with pattern is ' . $fmt->format(0);

$fmt = new IntlDateFormatter(
    'de-DE',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN,
    'MM/dd/yyyy'
);
echo 'Second Formatted output with pattern is ' . $fmt->format(0);
?>
```

以上例程会输出：

    First Formatted output is Wednesday, December 31, 1969 4:00:00 PM PT
    Second Formatted output is Mittwoch, 31. Dezember 1969 16:00 Uhr GMT-08:00
    First Formatted output with pattern is 12/31/1969
    Second Formatted output with pattern is 12/31/1969

**示例 \#3 With <span class="classname">IntlCalendar</span> object**

``` php
<?php
$tz = reset(iterator_to_array(IntlTimeZone::createEnumeration('FR')));
$formatter = IntlDateFormatter::create(
    'fr_FR',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    $tz,
    IntlDateFormatter::GREGORIAN
);

$cal = IntlCalendar::createInstance($tz, '@calendar=islamic-civil');
$cal->set(IntlCalendar::FIELD_MONTH, 8); //9th month, Ramadan
$cal->set(IntlCalendar::FIELD_DAY_OF_MONTH, 1); //1st day
$cal->clear(IntlCalendar::FIELD_HOUR_OF_DAY);
$cal->clear(IntlCalendar::FIELD_MINUTE);
$cal->clear(IntlCalendar::FIELD_SECOND);
$cal->clear(IntlCalendar::FIELD_MILLISECOND);

echo "In this islamic year, Ramadan started/will start on:\n\t",
        $formatter->format($cal), "\n";

//Itʼs the formatterʼs timezone that is used:
$formatter->setTimeZone('Asia/Tokyo');
echo "After changing timezone:\n\t",
        $formatter->format($cal), "\n";
```

以上例程会输出：

    In this islamic year, Ramadan started/will start on:
        mardi 9 juillet 2013 19:00:00 heure avancée d’Europe centrale
    After changing timezone:
        mercredi 10 juillet 2013 02:00:00 heure normale du Japon

### 参见

-   <span class="function">datefmt\_create</span>
-   <span class="function">datefmt\_parse</span>
-   <span class="function">datefmt\_get\_error\_code</span>
-   <span class="function">datefmt\_get\_error\_message</span>
-   <span class="function">datefmt\_format\_object</span>

IntlDateFormatter::formatObject
===============================

datefmt\_format\_object
=======================

Formats an object

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">IntlDateFormatter::formatObject</span> ( <span
class="methodparam"><span class="type">object</span> `$object`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$format`<span class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$locale`<span
class="initializer"> = NULL</span></span> \]\] )

过程化风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">datefmt\_format\_object</span> ( <span
class="methodparam"><span class="type">object</span> `$object`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$format`<span class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$locale`<span
class="initializer"> = NULL</span></span> \]\] )

This function allows formatting an <span
class="classname">IntlCalendar</span> or <span
class="classname">DateTime</span> object without first explicitly
creating a <span class="classname">IntlDateFormatter</span> object.

The temporary <span class="classname">IntlDateFormatter</span> that will
be created will take the timezone from the passed in object. The
timezone database bundled with PHP will not be used – ICU's will be used
instead. The timezone identifier used in <span
class="classname">DateTime</span> objects must therefore also exist in
ICU's database.

### 参数

`object`  
An object of type <span class="classname">IntlCalendar</span> or <span
class="classname">DateTime</span>. The timezone information in the
object will be used.

`format`  
How to format the date/time. This can either be an <span
class="type">array</span> with two elements (first the date style, then
the time style, these being one of the constants
**`IntlDateFormatter::NONE`**, **`IntlDateFormatter::SHORT`**,
**`IntlDateFormatter::MEDIUM`**, **`IntlDateFormatter::LONG`**,
**`IntlDateFormatter::FULL`**), an <span class="type">integer</span>
with the value of one of these constants (in which case it will be used
both for the time and the date) or a <span class="type">string</span>
with the format described in
<a href="http://www.icu-project.org/apiref/icu4c/classSimpleDateFormat.html#details" class="link external">» the ICU documentation</a>.
If **`NULL`**, the default style will be used.

`locale`  
The locale to use, or **`NULL`** to use the
<a href="/intl/setup.html#" class="link">default one</a>.

### 返回值

A string with result 或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 <span class="function">IntlDateFormatter::formatObject</span>
examples**

``` php
<?php
/* default timezone is irrelevant; timezone taken from the object */
ini_set('date.timezone', 'UTC');
/* default locale is taken from this ini setting */
ini_set('intl.default_locale', 'fr_FR');

$cal = IntlCalendar::fromDateTime("2013-06-06 17:05:06 Europe/Dublin");
echo "default:\n\t",
        IntlDateFormatter::formatObject($cal),
        "\n";

echo "long \$format (full):\n\t",
        IntlDateFormatter::formatObject($cal, IntlDateFormatter::FULL),
        "\n";

echo "array \$format (none, full):\n\t",
        IntlDateFormatter::formatObject($cal, array(
                IntlDateFormatter::NONE,
                IntlDateFormatter::FULL)),
        "\n";

echo "string \$format (d 'of' MMMM y):\n\t",
        IntlDateFormatter::formatObject($cal, "d 'of' MMMM y", 'en_US'),
        "\n";

echo "with DateTime:\n\t",
        IntlDateFormatter::formatObject(
                new DateTime("2013-09-09 09:09:09 Europe/Madrid"),
                IntlDateFormatter::FULL,
                'es_ES'),
        "\n";
```

以上例程会输出：

    default:
        6 juin 2013 17:05:06
    long $format (full):
        jeudi 6 juin 2013 17:05:06 heure d’été irlandaise
    array $format (none, full):
        17:05:06 heure d’été irlandaise
    string $format (d 'of' MMMM y):
        6 of June 2013
    with DateTime:
        lunes, 9 de septiembre de 2013 09:09:09 Hora de verano de Europa central

IntlDateFormatter::getCalendar
==============================

datefmt\_get\_calendar
======================

Get the calendar type used for the IntlDateFormatter

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlDateFormatter::getCalendar</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">int</span> <span
class="methodname">datefmt\_get\_calendar</span> ( <span
class="methodparam"><span class="type">IntlDateFormatter</span>
`$fmt`</span> )

### 参数

`fmt`  
The formatter resource

### 返回值

The
<a href="/class/intldateformatter.html#" class="link">calendar type</a>
being used by the formatter. Either **`IntlDateFormatter::TRADITIONAL`**
or **`IntlDateFormatter::GREGORIAN`**.

### 范例

**示例 \#1 <span class="function">datefmt\_get\_calendar</span>
example**

``` php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'calendar of the formatter is : ' . datefmt_get_calendar($fmt);
datefmt_set_calendar($fmt, IntlDateFormatter::TRADITIONAL);
echo 'Now calendar of the formatter is : ' . datefmt_get_calendar($fmt);
?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'calendar of the formatter is : ' . $fmt->getCalendar();
$fmt->setCalendar(IntlDateFormatter::TRADITIONAL);
echo 'Now calendar of the formatter is : ' . $fmt->getCalendar();

?>
```

以上例程会输出：

    calendar of the formatter is : 1
    Now calendar of the formatter is : 0

### 参见

-   <span class="function">datefmt\_get\_calendar\_object</span>
-   <span class="function">datefmt\_set\_calendar</span>
-   <span class="function">datefmt\_create</span>

IntlDateFormatter::getDateType
==============================

datefmt\_get\_datetype
======================

Get the datetype used for the IntlDateFormatter

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlDateFormatter::getDateType</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">int</span> <span
class="methodname">datefmt\_get\_datetype</span> ( <span
class="methodparam"><span class="type">IntlDateFormatter</span>
`$fmt`</span> )

Returns date type used by the formatter.

### 参数

`fmt`  
The formatter resource.

### 返回值

The current
<a href="/class/intldateformatter.html#预定义常量" class="link">date type</a>
value of the formatter.

### 范例

**示例 \#1 <span class="function">datefmt\_get\_datetype</span>
example**

``` php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'datetype of the formatter is : ' . datefmt_get_datetype($fmt);
echo 'First Formatted output with datetype is ' . datefmt_format($fmt, 0);

$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::SHORT,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Now datetype of the formatter is : ' . datefmt_get_datetype($fmt);
echo 'Second Formatted output with datetype is ' . datefmt_format($fmt, 0);

?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'datetype of the formatter is : ' . $fmt->getDateType();
echo 'First Formatted output is ' . $fmt->format(0);
$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::SHORT,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Now datetype of the formatter is : ' . $fmt->getDateType();
echo 'Second Formatted output is ' . $fmt->format(0);

?>
```

以上例程会输出：

    datetype of the formatter is : 0
    First Formatted output is Wednesday, December 31, 1969 4:00:00 PM PT
    Now datetype of the formatter is : 2
    Second Formatted output is 12/31/69 4:00:00 PM PT

### 参见

-   <span class="function">datefmt\_get\_timetype</span>
-   <span class="function">datefmt\_create</span>

IntlDateFormatter::getErrorCode
===============================

datefmt\_get\_error\_code
=========================

Get the error code from last operation

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlDateFormatter::getErrorCode</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">int</span> <span
class="methodname">datefmt\_get\_error\_code</span> ( <span
class="methodparam"><span class="type">IntlDateFormatter</span>
`$fmt`</span> )

Get the error code from last operation. Returns error code from the last
number formatting operation.

### 参数

`fmt`  
The formatter resource.

### 返回值

The error code, one of UErrorCode values. Initial value is
U\_ZERO\_ERROR.

### 范例

**示例 \#1 <span class="function">datefmt\_get\_error\_code</span>
example**

``` php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
$str = datefmt_format($fmt);
if (!$str) {
    printf(
        "ERROR: %s (%d)\n",
        datefmt_get_error_message($fmt),
        datefmt_get_error_code($fmt)
    );
}
?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
$str = $fmt->format();
if (!$str) {
    printf(
        "ERROR: %s (%d)\n",
        $fmt->getErrorMessage(),
        $fmt->getErrorCode()
    );
}
?>
```

以上例程会输出：

    ERROR: U_ZERO_ERROR (0)

### 参见

-   <span class="function">datefmt\_get\_error\_message</span>
-   <span class="function">intl\_get\_error\_code</span>
-   <span class="function">intl\_is\_failure</span>

IntlDateFormatter::getErrorMessage
==================================

datefmt\_get\_error\_message
============================

Get the error text from the last operation

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">IntlDateFormatter::getErrorMessage</span> (
<span class="methodparam">void</span> )

过程化风格

<span class="type">string</span> <span
class="methodname">datefmt\_get\_error\_message</span> ( <span
class="methodparam"><span class="type">IntlDateFormatter</span>
`$fmt`</span> )

Get the error text from the last operation.

### 参数

`fmt`  
The formatter resource.

### 返回值

Description of the last error.

### 范例

**示例 \#1 <span class="function">datefmt\_get\_error\_message</span>
example**

``` php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
$str = datefmt_format($fmt);
if (!$str) {
    printf(
        "ERROR: %s (%d)\n",
        datefmt_get_error_message($fmt),
        datefmt_get_error_code($fmt)
    );
}
?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
$str = $fmt->format();
if(!$str) {
    printf(
        "ERROR: %s (%d)\n",
        $fmt->getErrorMessage(),
        $fmt->getErrorCode()
    );
}

?>
```

以上例程会输出：

    ERROR: U_ZERO_ERROR (0)

### 参见

-   <span class="function">datefmt\_get\_error\_code</span>
-   <span class="function">intl\_get\_error\_code</span>
-   <span class="function">intl\_is\_failure</span>

IntlDateFormatter::getLocale
============================

datefmt\_get\_locale
====================

Get the locale used by formatter

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">IntlDateFormatter::getLocale</span> (\[ <span
class="methodparam"><span class="type">int</span> `$which`</span> \] )

过程化风格

<span class="type">string</span> <span
class="methodname">datefmt\_get\_locale</span> ( <span
class="methodparam"><span class="type">IntlDateFormatter</span>
`$fmt`</span> \[, <span class="methodparam"><span
class="type">int</span> `$which`</span> \] )

Get locale used by the formatter.

### 参数

`fmt`  
The formatter resource

`hich`  
You can choose between valid and actual locale (
**`Locale::VALID_LOCALE`**, **`Locale::ACTUAL_LOCALE`**, respectively).
The default is the actual locale.

### 返回值

the locale of this formatter or 'false' if error

### 范例

**示例 \#1 <span class="function">datefmt\_get\_locale</span> example**

``` php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'locale of the formatter is : " . datefmt_get_locale($fmt);
echo 'First Formatted output is " . datefmt_format($fmt, 0);

$fmt = datefmt_create(
    'de-DE',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'locale of the formatter is : ' . datefmt_get_locale($fmt);
echo 'Second Formatted output is ' . datefmt_format($fmt, 0);

?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'locale of the formatter is : ' . $fmt->getLocale();
echo 'First Formatted output is ' . $fmt->format(0);

$fmt = new IntlDateFormatter(
    'de-DE',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'locale of the formatter is : ' . $fmt->getLocale();
echo 'Second Formatted output is ' . $fmt->format(0);

?>
```

以上例程会输出：

    locale of the formatter is : en
    First Formatted output is Wednesday, December 31, 1969 4:00:00 PM PT
    locale of the formatter is : de
    Second Formatted output is Mittwoch, 31. Dezember 1969 16:00 Uhr GMT-08:00

### 参见

-   <span class="function">datefmt\_create</span>

IntlDateFormatter::getPattern
=============================

datefmt\_get\_pattern
=====================

Get the pattern used for the IntlDateFormatter

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">IntlDateFormatter::getPattern</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">string</span> <span
class="methodname">datefmt\_get\_pattern</span> ( <span
class="methodparam"><span class="type">IntlDateFormatter</span>
`$fmt`</span> )

Get pattern used by the formatter.

### 参数

`fmt`  
The formatter resource.

### 返回值

The pattern string being used to format/parse.

### 范例

**示例 \#1 <span class="function">datefmt\_get\_pattern</span> example**

``` php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN,
    'MM/dd/yyyy'
);
echo 'pattern of the formatter is : ' . datefmt_get_pattern($fmt);
echo 'First Formatted output with pattern is ' . datefmt_format($fmt, 0);
datefmt_set_pattern($fmt,'yyyymmdd hh:mm:ss z');
echo 'Now pattern of the formatter is : ' . datefmt_get_pattern($fmt);
echo 'Second Formatted output with pattern is ' . datefmt_format($fmt, 0);

?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN,
    'MM/dd/yyyy'
);
echo 'pattern of the formatter is : ' . $fmt->getPattern();
echo 'First Formatted output is ' . $fmt->format(0);
$fmt->setPattern('yyyymmdd hh:mm:ss z');
echo 'Now pattern of the formatter is : ' . $fmt->getPattern();
echo 'Second Formatted output is ' . $fmt->format(0);
?>
```

以上例程会输出：

    pattern of the formatter is : MM/dd/yyyy
    First Formatted output is 12/31/1969
    Now pattern of the formatter is : yyyymmdd hh:mm:ss z
    Second Formatted output is 19690031 04:00:00 PST

### 参见

-   <span class="function">datefmt\_set\_pattern</span>
-   <span class="function">datefmt\_create</span>

IntlDateFormatter::getTimeType
==============================

datefmt\_get\_timetype
======================

Get the timetype used for the IntlDateFormatter

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlDateFormatter::getTimeType</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">int</span> <span
class="methodname">datefmt\_get\_timetype</span> ( <span
class="methodparam"><span class="type">IntlDateFormatter</span>
`$fmt`</span> )

Return time type used by the formatter.

### 参数

`fmt`  
The formatter resource.

### 返回值

The current
<a href="/class/intldateformatter.html#预定义常量" class="link">date type</a>
value of the formatter.

### 范例

**示例 \#1 <span class="function">datefmt\_get\_timetype</span>
example**

``` php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'timetype of the formatter is : ' . datefmt_get_timetype($fmt);
echo 'First Formatted output with timetype is ' . datefmt_format($fmt, 0);

$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::SHORT,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Now timetype of the formatter is : ' . datefmt_get_timetype($fmt);
echo 'Second Formatted output with timetype is ' . datefmt_format($fmt, 0);

?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'timetype of the formatter is : ' . $fmt->getTimeType();
echo 'First Formatted output is ' . $fmt->format(0);

$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::SHORT,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Now timetype of the formatter is : ' . $fmt->getTimeType();
echo 'Second Formatted output is ' . $fmt->format(0);

?>
```

以上例程会输出：

    timetype of the formatter is : 0
    First Formatted output is Wednesday, December 31, 1969 4:00:00 PM PT
    Now timetype of the formatter is : 3
    Second Formatted output is Wednesday, December 31, 1969 4:00 PM

### 参见

-   <span class="function">datefmt\_get\_datetype</span>
-   <span class="function">datefmt\_create</span>

IntlDateFormatter::getTimeZoneId
================================

datefmt\_get\_timezone\_id
==========================

Get the timezone-id used for the IntlDateFormatter

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">IntlDateFormatter::getTimeZoneId</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">string</span> <span
class="methodname">datefmt\_get\_timezone\_id</span> ( <span
class="methodparam"><span class="type">IntlDateFormatter</span>
`$fmt`</span> )

Get the timezone-id used for the IntlDateFormatter.

### 参数

`fmt`  
The formatter resource.

### 返回值

ID string for the time zone used by this formatter.

### 范例

**示例 \#1 <span class="function">datefmt\_get\_timezone\_id</span>
example**

``` php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'timezone_id of the formatter is : ' . datefmt_get_timezone_id($fmt);
datefmt_set_timezone_id($fmt, 'CN');
echo 'Now timezone_id of the formatter is : ' . datefmt_get_timezone_id($fmt);

?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'timezone_id of the formatter is : ' . $fmt->getTimezoneId();
$fmt->setTimezoneId('CN');
echo 'Now timezone_id of the formatter is : ' . $fmt->getTimezoneId();

?>
```

以上例程会输出：

    timezone_id of the formatter is : America/Los_Angeles
    Now timezone_id of the formatter is : CN

### 参见

-   <span class="function">datefmt\_set\_timezone\_id</span>
-   <span class="function">datefmt\_create</span>

IntlDateFormatter::getCalendarObject
====================================

datefmt\_get\_calendar\_object
==============================

Get copy of formatterʼs calendar object

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="type">IntlCalendar</span> <span
class="methodname">IntlDateFormatter::getCalendarObject</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">IntlCalendar</span> <span
class="methodname">datefmt\_get\_calendar\_object</span> ( <span
class="methodparam">void</span> )

Obtain a copy of the calendar object used internally by this formatter.
This calendar will have a type (as in gregorian, japanese, buddhist,
roc, persian, islamic, etc.) and a timezone that match the type and
timezone used by the formatter. The date/time of the object is
unspecified.

### 参数

此函数没有参数。

### 返回值

A copy of the internal calendar object used by this formatter.

### 范例

**示例 \#1 <span
class="function">IntlDateFormatter::getCalendarObject</span> example**

``` php
<?php
$formatter = IntlDateFormatter::create(
    "fr_FR@calendar=islamic", 
    NULL,
    NULL,
    "GMT-01:00",
    IntlDateFormatter::TRADITIONAL
);

$cal = $formatter->getCalendarObject();

var_dump(
    $cal->getType(),
    $cal->getTimeZone(),
    $cal->getLocale(Locale::VALID_LOCALE)
);
```

以上例程会输出：

    string(7) "islamic"
    object(IntlTimeZone)#3 (4) {
      ["valid"]=>
      bool(true)
      ["id"]=>
      string(9) "GMT-01:00"
      ["rawOffset"]=>
      int(-3600000)
      ["currentOffset"]=>
      int(-3600000)
    }
    string(5) "fr_FR"

### 参见

-   <span class="function">IntlDateFormatter::getCalendar</span>
-   <span class="function">IntlDateFormatter::setCalendar</span>
-   <span class="classname">IntlCalendar</span>

IntlDateFormatter::getTimeZone
==============================

datefmt\_get\_timezone
======================

Get formatterʼs timezone

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="type">IntlTimeZone</span> <span
class="methodname">IntlDateFormatter::getTimeZone</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">IntlTimeZone</span> <span
class="methodname">datefmt\_get\_timezone</span> ( <span
class="methodparam">void</span> )

Returns an <span class="classname">IntlTimeZone</span> object
representing the timezone that will be used by this object to format
dates and times. When formatting <span
class="classname">IntlCalendar</span> and <span
class="classname">DateTime</span> objects with this <span
class="classname">IntlDateFormatter</span>, the timezone used will be
the one returned by this method, not the one associated with the objects
being formatted.

### 参数

此函数没有参数。

### 返回值

The associated <span class="classname">IntlTimeZone</span> object
或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 <span class="function">IntlDateFormatter::getTimeZone</span>
examples**

``` php
<?php

$madrid = IntlDateFormatter::create(NULL, NULL, NULL, 'Europe/Madrid');
$lisbon = IntlDateFormatter::create(NULL, NULL, NULL, 'Europe/Lisbon');

var_dump($madrid->getTimezone());
echo $madrid->getTimezone()->getDisplayName(
        false, IntlTimeZone::DISPLAY_GENERIC_LOCATION, "en_US"), "\n";
echo $lisbon->getTimeZone()->getId(), "\n";
//The id can also be retrieved with ->getTimezoneId()
echo $lisbon->getTimeZoneId(), "\n";
```

以上例程会输出：

    object(IntlTimeZone)#4 (4) {
      ["valid"]=>
      bool(true)
      ["id"]=>
      string(13) "Europe/Madrid"
      ["rawOffset"]=>
      int(3600000)
      ["currentOffset"]=>
      int(7200000)
    }
    Spain Time
    Europe/Lisbon
    Europe/Lisbon

### 参见

-   <span class="function">IntlDateFormatter::getTimeZoneId</span>
-   <span class="function">IntlDateFormatter::setTimeZone</span>
-   <span class="classname">IntlTimeZone</span>

IntlDateFormatter::isLenient
============================

datefmt\_is\_lenient
====================

Get the lenient used for the IntlDateFormatter

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlDateFormatter::isLenient</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">datefmt\_is\_lenient</span> ( <span
class="methodparam"><span class="type">IntlDateFormatter</span>
`$fmt`</span> )

Check if the parser is strict or lenient in interpreting inputs that do
not match the pattern exactly.

### 参数

`fmt`  
The formatter resource.

### 返回值

**`TRUE`** if parser is lenient, **`FALSE`** if parser is strict. By
default the parser is lenient.

### 范例

**示例 \#1 <span class="function">datefmt\_is\_lenient</span> example**

``` php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN,
    'dd/mm/yyyy'
);
echo 'lenient of the formatter is : ';
if ($fmt->isLenient()) {
    echo 'TRUE';
} else {
    echo 'FALSE';
}
datefmt_parse($fmt, '35/13/1971');
echo "\n Trying to do parse('35/13/1971').\nResult is : " . datefmt_parse($fmt, '35/13/1971');
if (intl_get_error_code() != 0) {
    echo "\nError_msg is : " . intl_get_error_message();
    echo "\nError_code is : " . intl_get_error_code();
}
datefmt_set_lenient($fmt,false);
echo 'Now lenient of the formatter is : ';
if ($fmt->isLenient()) {
    echo 'TRUE';
} else {
    echo 'FALSE';
}
datefmt_parse($fmt, '35/13/1971');
echo "\n Trying to do parse('35/13/1971').Result is : " . datefmt_parse($fmt, '35/13/1971');
if (intl_get_error_code() != 0) {
    echo "\nError_msg is : " . intl_get_error_message();
    echo "\nError_code is : " . intl_get_error_code();
}

?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN,
    "dd/mm/yyyy"
);
echo "lenient of the formatter is : ";
if ($fmt->isLenient()) {
    echo 'TRUE';
} else {
    echo 'FALSE';
}
$fmt->parse('35/13/1971');
echo "\n Trying to do parse('35/13/1971').\nResult is : " . $fmt->parse('35/13/1971');
if (intl_get_error_code() != 0){
    echo "\nError_msg is : " . intl_get_error_message();
    echo "\nError_code is : " . intl_get_error_code();
}

$fmt->setLenient(FALSE);
echo 'Now lenient of the formatter is : ';
if ($fmt->isLenient()) {
    echo 'TRUE';
} else {
    echo 'FALSE';
}
$fmt->parse('35/13/1971');
echo "\n Trying to do parse('35/13/1971').\nResult is : " . $fmt->parse('35/13/1971');
if (intl_get_error_code() != 0) {
    echo "\nError_msg is : " . intl_get_error_message();
    echo "\nError_code is : " . intl_get_error_code();
}

?>
```

以上例程会输出：

    lenient of the formatter is : TRUE
    Trying to do parse('35/13/1971').
    Result is : -2147483
    Now lenient of the formatter is : FALSE
    Trying to do parse('35/13/1971').
    Result is : 
    Error_msg is : Date parsing failed: U_PARSE_ERROR 
    Error_code is : 9

### 参见

-   <span class="function">datefmt\_set\_lenient</span>
-   <span class="function">datefmt\_create</span>

IntlDateFormatter::localtime
============================

datefmt\_localtime
==================

Parse string to a field-based time value

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">IntlDateFormatter::localtime</span> ( <span
class="methodparam"><span class="type">string</span> `$value`</span> \[,
<span class="methodparam"><span class="type">int</span>
`&$position`</span> \] )

过程化风格

<span class="type">array</span> <span
class="methodname">datefmt\_localtime</span> ( <span
class="methodparam"><span class="type">IntlDateFormatter</span>
`$fmt`</span> , <span class="methodparam"><span
class="type">string</span> `$value`</span> \[, <span
class="methodparam"><span class="type">int</span> `&$position`</span> \]
)

Converts string $value to a field-based time value ( an array of various
fields), starting at $parse\_pos and consuming as much of the input
value as possible.

### 参数

`fmt`  
The formatter resource

`value`  
string to convert to a time

`position`  
Position at which to start the parsing in $value (zero-based). If no
error occurs before $value is consumed, $parse\_pos will contain -1
otherwise it will contain the position at which parsing ended . If
$parse\_pos \> strlen($value), the parse fails immediately.

### 返回值

Localtime compatible array of integers : contains 24 hour clock value in
tm\_hour field

### 范例

**示例 \#1 <span class="function">datefmt\_localtime</span> example**

``` php
<?php

$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
$arr = datefmt_localtime($fmt, 'Wednesday, December 31, 1969 4:00:00 PM PT', 0);
echo 'First parsed output is ';
if ($arr) {
    foreach ($arr as $key => $value) {
        echo "$key : $value , ";
    }
}

?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
$arr = $fmt->localtime('Wednesday, December 31, 1969 4:00:00 PM PT', 0);
echo 'First parsed output is ';
if ($arr) {
    foreach ($arr as $key => $value) {
        echo "$key : $value , ";
    }
}

?>
```

以上例程会输出：

    First parsed output is tm_sec : 0 , tm_min : 0 , tm_hour : 16 , tm_year : 1969 , 
    tm_mday : 31 , tm_wday : 4 , tm_yday : 365 , tm_mon : 11 , tm_isdst : 0 , 

### 参见

-   <span class="function">datefmt\_create</span>
-   <span class="function">datefmt\_format</span>
-   <span class="function">datefmt\_parse</span>
-   <span class="function">datefmt\_get\_error\_code</span>
-   <span class="function">datefmt\_get\_error\_message</span>

IntlDateFormatter::parse
========================

datefmt\_parse
==============

Parse string to a timestamp value

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlDateFormatter::parse</span> ( <span
class="methodparam"><span class="type">string</span> `$value`</span> \[,
<span class="methodparam"><span class="type">int</span>
`&$position`</span> \] )

过程化风格

<span class="type">int</span> <span
class="methodname">datefmt\_parse</span> ( <span
class="methodparam"><span class="type">IntlDateFormatter</span>
`$fmt`</span> , <span class="methodparam"><span
class="type">string</span> `$value`</span> \[, <span
class="methodparam"><span class="type">int</span> `&$position`</span> \]
)

Converts string $value to an incremental time value, starting at
$parse\_pos and consuming as much of the input value as possible.

### 参数

`fmt`  
The formatter resource

`value`  
string to convert to a time

`position`  
Position at which to start the parsing in $value (zero-based). If no
error occurs before $value is consumed, $parse\_pos will contain -1
otherwise it will contain the position at which parsing ended (and the
error occurred). This variable will contain the end position if the
parse fails. If $parse\_pos \> strlen($value), the parse fails
immediately.

### 返回值

timestamp parsed value, or **`FALSE`** if value can't be parsed.

### 范例

**示例 \#1 OO example**

``` php
<?php
$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'First parsed output is ' . $fmt->parse('Wednesday, December 20, 1989 4:00:00 PM PT');
$fmt = new IntlDateFormatter(
    'de-DE',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
?>
```

**示例 \#2 <span class="function">datefmt\_parse</span> example**

``` php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'First parsed output is ' . datefmt_parse($fmt, 'Wednesday, December 20, 1989 4:00:00 PM PT');
$fmt = datefmt_create(
    'de-DE',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Second parsed output is ' . datefmt_parse($fmt, 'Mittwoch, 20. Dezember 1989 16:00 Uhr GMT-08:00');
?
```

以上例程会输出：

    First parsed output is 630201600
    Second parsed output is 630201600

### 参见

-   <span class="function">datefmt\_create</span>
-   <span class="function">datefmt\_format</span>
-   <span class="function">datefmt\_localtime</span>
-   <span class="function">datefmt\_get\_error\_code</span>
-   <span class="function">datefmt\_get\_error\_message</span>

IntlDateFormatter::setCalendar
==============================

datefmt\_set\_calendar
======================

Sets the calendar type used by the formatter

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlDateFormatter::setCalendar</span> ( <span
class="methodparam"><span class="type">mixed</span> `$which`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">datefmt\_set\_calendar</span> ( <span
class="methodparam"><span class="type">IntlDateFormatter</span>
`$fmt`</span> , <span class="methodparam"><span
class="type">mixed</span> `$which`</span> )

Sets the calendar or calendar type used by the formatter.

### 参数

`fmt`  
The formatter resource.

`which`  
This can either be: the
<a href="/class/intldateformatter.html#" class="link">calendar type</a>
to use (default is **`IntlDateFormatter::GREGORIAN`**, which is also
used if **`NULL`** is specified) or an <span
class="classname">IntlCalendar</span> object.

Any <span class="classname">IntlCalendar</span> object passed in will be
cloned; no modifications will be made to the argument object.

The timezone of the formatter will only be kept if an <span
class="classname">IntlCalendar</span> object is not passed, otherwise
the new timezone will be that of the passed object.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本             | 说明                                                                              |
|------------------|-----------------------------------------------------------------------------------|
| 5.5.0/PECL 3.0.0 | It became possible to pass an <span class="classname">IntlCalendar</span> object. |

### 范例

**示例 \#1 <span class="function">datefmt\_set\_calendar</span>
example**

``` php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'calendar of the formatter is : ' . datefmt_get_calendar($fmt);
datefmt_set_calendar($fmt, IntlDateFormatter::TRADITIONAL);
echo 'Now calendar of the formatter is : ' . datefmt_get_calendar($fmt);
?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN  
);
echo 'calendar of the formatter is : ' . $fmt->getCalendar();
$fmt->setCalendar(IntlDateFormatter::TRADITIONAL);
echo 'Now calendar of the formatter is : ' . $fmt->getCalendar();
?>
```

以上例程会输出：

    calendar of the formatter is : 1
    Now calendar of the formatter is : 0

**示例 \#3 Example with <span class="classname">IntlCalendar</span>
argument**

``` php
<?php
$time = strtotime("2013-03-03 00:00:00 UTC");
$formatter = IntlDateFormatter::create("en_US", NULL, NULL, "Europe/Amsterdam");

echo "before: ", $formatter->format($time), "\n";

/* note that the calendar's locale is not used! */
$formatter->setCalendar(IntlCalendar::createInstance(
               "America/New_York", "pt_PT@calendar=islamic"));

echo "after:  ", $formatter->format($time), "\n";
```

以上例程会输出：

    before: Sunday, March 3, 2013 at 1:00:00 AM Central European Standard Time
    after:  Saturday, Rabiʻ II 20, 1434 at 7:00:00 PM Eastern Standard Time

### 参见

-   <span class="function">datefmt\_get\_calendar</span>
-   <span class="function">datefmt\_get\_calendar\_object</span>
-   <span class="function">datefmt\_create</span>

IntlDateFormatter::setLenient
=============================

datefmt\_set\_lenient
=====================

Set the leniency of the parser

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlDateFormatter::setLenient</span> ( <span
class="methodparam"><span class="type">bool</span> `$lenient`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">datefmt\_set\_lenient</span> ( <span
class="methodparam"><span class="type">IntlDateFormatter</span>
`$fmt`</span> , <span class="methodparam"><span class="type">bool</span>
`$lenient`</span> )

Define if the parser is strict or lenient in interpreting inputs that do
not match the pattern exactly. Enabling lenient parsing allows the
parser to accept otherwise flawed date or time patterns, parsing as much
as possible to obtain a value. Extra space, unrecognized tokens, or
invalid values ("February 30th") are not accepted.

### 参数

`fmt`  
The formatter resource

`lenient`  
Sets whether the parser is lenient or not, default is **`TRUE`**
(lenient).

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">datefmt\_set\_lenient</span> example**

``` php
<?php
$fmt = datefmt_create(
    'en_US', 
    IntlDateFormatter::FULL, 
    IntlDateFormatter::FULL, 
    'America/Los_Angeles', 
    IntlDateFormatter::GREGORIAN, 
    'dd/MM/yyyy'
);
echo 'lenient of the formatter is : ';
if ($fmt->isLenient()) {
    echo 'TRUE';
} else {
    echo 'FALSE';
}
datefmt_parse($fmt, '35/13/1971');
echo "\n Trying to do parse('35/13/1971').\nResult is : " . datefmt_parse($fmt, '35/13/1971');
if (intl_get_error_code() != 0) {
    echo "\nError_msg is : " . intl_get_error_message();
    echo "\nError_code is : " . intl_get_error_code();
}
datefmt_set_lenient($fmt, false);
echo "\nNow lenient of the formatter is : ";
if ($fmt->isLenient()) {
    echo 'TRUE';
} else {
    echo 'FALSE';
}
datefmt_parse($fmt, '35/13/1971');
echo "\nTrying to do parse('35/13/1971').\nResult is : " . datefmt_parse($fmt, '35/13/1971');
if (intl_get_error_code() != 0) {
    echo "\nError_msg is : ".intl_get_error_message();
    echo "\nError_code is : ".intl_get_error_code();
}

?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN,
    'dd/MM/yyyy'
);
echo 'lenient of the formatter is : ';
if ($fmt->isLenient()) {
    echo 'TRUE';
} else {
    echo 'FALSE';
}
$fmt->parse('35/13/1971');
echo "\n Trying to do parse('35/13/1971').\nResult is : " . $fmt->parse('35/13/1971');
if (intl_get_error_code() != 0) {
    echo "\nError_msg is : " . intl_get_error_message();
    echo "\nError_code is : " . intl_get_error_code();
}

$fmt->setLenient(FALSE);
echo "\nNow lenient of the formatter is : ";
if ($fmt->isLenient()) {
    echo 'TRUE';
} else {
    echo 'FALSE';
}
$fmt->parse('35/13/1971');
echo "\n Trying to do parse('35/13/1971').\nResult is : " . $fmt->parse('35/13/1971');
if (intl_get_error_code() != 0) {
    echo "\nError_msg is : " . intl_get_error_message();
    echo "\nError_code is : " . intl_get_error_code();
}

?>
```

以上例程会输出：

    lenient of the formatter is : TRUE
    Trying to do parse('35/13/1971').
    Result is : 66038400
    Now lenient of the formatter is : FALSE
    Trying to do parse('35/13/1971').
    Result is : 
    Error_msg is : Date parsing failed: U_PARSE_ERROR
    Error_code is : 9

### 参见

-   <span class="function">datefmt\_is\_lenient</span>
-   <span class="function">datefmt\_create</span>

IntlDateFormatter::setPattern
=============================

datefmt\_set\_pattern
=====================

Set the pattern used for the IntlDateFormatter

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlDateFormatter::setPattern</span> ( <span
class="methodparam"><span class="type">string</span> `$pattern`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">datefmt\_set\_pattern</span> ( <span
class="methodparam"><span class="type">IntlDateFormatter</span>
`$fmt`</span> , <span class="methodparam"><span
class="type">string</span> `$pattern`</span> )

Set the pattern used for the IntlDateFormatter.

### 参数

`fmt`  
The formatter resource.

`pattern`  
New pattern string to use. Possible patterns are documented at
<a href="http://userguide.icu-project.org/formatparse/datetime" class="link external">» http://userguide.icu-project.org/formatparse/datetime</a>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 Bad formatstrings
are usually the cause of the failure.

### 范例

**示例 \#1 <span class="function">datefmt\_set\_pattern</span> example**

``` php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN,
    'MM/dd/yyyy'
);
echo 'pattern of the formatter is : ' . datefmt_get_pattern($fmt);
echo 'First Formatted output with pattern is ' . datefmt_format($fmt, 0);
datefmt_set_pattern($fmt, 'yyyymmdd hh:mm:ss z');
echo 'Now pattern of the formatter is : ' . datefmt_get_pattern($fmt);
echo 'Second Formatted output with pattern is ' . datefmt_format($fmt, 0);

?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::FULL,IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN,
    'MM/dd/yyyy'
);
echo 'pattern of the formatter is : ' . $fmt->getPattern();
echo 'First Formatted output is ' . $fmt->format(0);
$fmt->setPattern('yyyymmdd hh:mm:ss z');
echo 'Now pattern of the formatter is : ' . $fmt->getPattern();
echo 'Second Formatted output is ' . $fmt->format(0);

?>
```

以上例程会输出：

    pattern of the formatter is : MM/dd/yyyy
    First Formatted output with pattern is 12/31/1969
    Now pattern of the formatter is : yyyymmdd hh:mm:ss z
    Second Formatted output with pattern is 19690031 04:00:00 PST

### 参见

-   <span class="function">datefmt\_get\_pattern</span>
-   <span class="function">datefmt\_create</span>

IntlDateFormatter::setTimeZoneId
================================

datefmt\_set\_timezone\_id
==========================

Sets the time zone to use

**Warning**

This function was *DEPRECATED* in PHP 5.5.0, and *REMOVED* in PHP 7.0.0.

Alternatives to this function include:

-   <span class="function">IntlDateFormatter::setTimeZone</span>

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlDateFormatter::setTimeZoneId</span> ( <span
class="methodparam"><span class="type">string</span> `$zone`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">datefmt\_set\_timezone\_id</span> ( <span
class="methodparam"><span class="type">IntlDateFormatter</span>
`$fmt`</span> , <span class="methodparam"><span
class="type">string</span> `$zone`</span> )

Sets the time zone to use.

### 参数

`fmt`  
The formatter resource.

`zone`  
The time zone ID string of the time zone to use. If **`NULL`** or the
empty string, the default time zone for the runtime is used.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                               |
|-------|------------------------------------|
| 7.0.0 | This function has been removed.    |
| 5.5.0 | This function has been deprecated. |

### 范例

**示例 \#1 <span class="function">datefmt\_set\_timezone\_id</span>
example**

``` php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'timezone_id of the formatter is : ' . datefmt_get_timezone_id($fmt);
datefmt_set_timezone_id($fmt, 'CN');
echo 'Now timezone_id of the formatter is : ' . datefmt_get_timezone_id($fmt);
?>
```

**示例 \#2 OO example**

``` php
<?php
$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'timezone_id of the formatter is : ' . $fmt->getTimezoneId();
$fmt->setTimezoneId('CN');
echo 'Now timezone_id of the formatter is : ' . $fmt->getTimezoneId();

?>
```

以上例程会输出：

    timezone_id of the formatter is : America/Los_Angeles
    Now timezone_id of the formatter is : CN

### 参见

-   <span class="function">datefmt\_get\_timezone\_id</span>
-   <span class="function">datefmt\_create</span>

IntlDateFormatter::setTimeZone
==============================

datefmt\_set\_timezone
======================

Sets formatterʼs timezone

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlDateFormatter::setTimeZone</span> ( <span
class="methodparam"><span class="type">mixed</span> `$zone`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">datefmt\_set\_timezone</span> ( <span
class="methodparam"><span class="type">IntlDateFormatter</span>
`$fmt`</span> , <span class="methodparam"><span
class="type">mixed</span> `$zone`</span> )

Sets the timezone used for the IntlDateFormatter. object.

### 参数

`fmt`  
The formatter resource.

`zone`  
The timezone to use for this formatter. This can be specified in the
following forms:

-   **`NULL`**, in which case the default timezone will be used, as
    specified in the ini setting
    <a href="/datetime/setup.html#" class="link">date.timezone</a> or
    through the function <span
    class="function">date\_default\_timezone\_set</span> and as returned
    by <span class="function">date\_default\_timezone\_get</span>.

-   An <span class="classname">IntlTimeZone</span>, which will be used
    directly.

-   A <span class="classname">DateTimeZone</span>. Its identifier will
    be extracted and an ICU timezone object will be created; the
    timezone will be backed by ICUʼs database, not PHPʼs.

-   A <span class="type">string</span>, which should be a valid ICU
    timezone identifier. See <span
    class="function">IntlTimeZone::createTimeZoneIDEnumeration</span>.
    Raw offsets such as *"GMT+08:30"* are also accepted.

### 返回值

Returns **`TRUE`** on success and **`FALSE`** on failure.

### 范例

**示例 \#1 <span class="function">IntlDateFormatter::setTimeZone</span>
examples**

``` php
<?php
ini_set('date.timezone', 'Europe/Amsterdam');

$formatter = IntlDateFormatter::create(NULL, NULL, NULL, "UTC");

$formatter->setTimeZone(NULL);
echo "NULL\n    ", $formatter->getTimeZone()->getId(), "\n";

$formatter->setTimeZone(IntlTimeZone::createTimeZone('Europe/Lisbon'));
echo "IntlTimeZone\n    ", $formatter->getTimeZone()->getId(), "\n";

$formatter->setTimeZone(new DateTimeZone('Europe/Paris'));
echo "DateTimeZone\n    ", $formatter->getTimeZone()->getId(), "\n";

$formatter->setTimeZone('Europe/Rome');
echo "String\n    ", $formatter->getTimeZone()->getId(), "\n";

$formatter->setTimeZone('GMT+00:30');
print_r($formatter->getTimeZone());
```

以上例程会输出：

    NULL
        Europe/Amsterdam
    IntlTimeZone
        Europe/Lisbon
    DateTimeZone
        Europe/Paris
    String
        Europe/Rome
    IntlTimeZone Object
    (
        [valid] => 1
        [id] => GMT+00:30
        [rawOffset] => 1800000
        [currentOffset] => 1800000
    )

### 参见

-   <span class="function">IntlDateFormatter::getTimeZone</span>

简介
----

Localized software products often require sets of data that are to be
customized depending on current locale, e.g.: messages, labels,
formatting patterns. ICU resource mechanism allows to define sets of
resources that the application can load on locale basis, while accessing
them in unified locale-independent fashion.

This class implements access to ICU resource data files. These files are
binary data arrays which ICU uses to store the localized data.

ICU resource bundle can hold simple resources and complex resources.
Complex resources are containers which can be either integer-indexed or
string-indexed (just like PHP arrays). Simple resources can be of the
following types: string, integer, binary data field or integer array.

<span class="classname">ResourceBundle</span> supports direct access to
the data through array access pattern and iteration via
<a href="/control-structures/foreach.html" class="link">foreach</a>, as
well as access via class methods. The result will be PHP value for
simple resources and <span class="classname">ResourceBundle</span>
object for complex ones. All resources are read-only.

类摘要
------

**ResourceBundle**

<span class="ooclass"> class **ResourceBundle** </span> {

/\* Methods \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> ,
<span class="methodparam"><span class="type">string</span>
`$bundlename`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$fallback`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">count</span> ( <span class="methodparam">void</span>
)

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">ResourceBundle</span>
<span class="methodname">create</span> ( <span class="methodparam"><span
class="type">string</span> `$locale`</span> , <span
class="methodparam"><span class="type">string</span>
`$bundlename`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$fallback`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getErrorCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getErrorMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">get</span> ( <span class="methodparam"><span
class="type">string\|int</span> `$index`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$fallback`<span
class="initializer"> = **`TRUE`**</span></span> \] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getLocales</span> ( <span
class="methodparam"><span class="type">string</span>
`$bundlename`</span> )

}

参见
----

-   <a href="http://userguide.icu-project.org/locale/resources" class="link external">»  ICU Resource Management</a>
-   <a href="http://userguide.icu-project.org/icudata" class="link external">» ICU Data</a>

ResourceBundle::count
=====================

resourcebundle\_count
=====================

Get number of elements in the bundle

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ResourceBundle::count</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">int</span> <span
class="methodname">resourcebundle\_count</span> ( <span
class="methodparam"><span class="type">ResourceBundle</span> `$r`</span>
)

Get the number of elements in the bundle.

### 参数

`r`  
<span class="classname">ResourceBundle</span> object.

### 返回值

Returns number of elements in the bundle.

### 范例

**示例 \#1 <span class="function">resourcebundle\_count</span> example**

``` php
<?php
$r = resourcebundle_create( 'es', "/usr/share/data/myapp");
echo resourcebundle_count($r);
?>
```

**示例 \#2 OO example**

``` php
<?php
$r = new ResourceBundle( 'es', "/usr/share/data/myapp");
echo $r->count();
?>
```

以上例程会输出：

    42

### 参见

-   <span class="function">resourcebundle\_get</span>

ResourceBundle::create
======================

resourcebundle\_create
======================

ResourceBundle::\_\_construct
=============================

Create a resource bundle

### 说明

面向对象风格 (method)

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">ResourceBundle</span>
<span class="methodname">ResourceBundle::create</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> ,
<span class="methodparam"><span class="type">string</span>
`$bundlename`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$fallback`</span> \] )

过程化风格

<span class="type">ResourceBundle</span> <span
class="methodname">resourcebundle\_create</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> ,
<span class="methodparam"><span class="type">string</span>
`$bundlename`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$fallback`</span> \] )

面向对象风格 (constructor):

<span class="modifier">public</span> <span
class="methodname">ResourceBundle::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$locale`</span> ,
<span class="methodparam"><span class="type">string</span>
`$bundlename`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$fallback`</span> \] )

Creates a resource bundle.

### 参数

`locale`  
Locale for which the resources should be loaded (locale name, e.g.
en\_CA).

`bundlename`  
The directory where the data is stored or the name of the .dat file.

`fallback`  
Whether locale should match exactly or fallback to parent locale is
allowed.

### 返回值

Returns <span class="classname">ResourceBundle</span> object or
**`NULL`** on error.

### 范例

**示例 \#1 <span class="function">resourcebundle\_create</span>
example**

``` php
<?php
$r = resourcebundle_create( 'es', "/usr/share/data/myapp");
echo $r['teststring'];
?>
```

**示例 \#2 <span class="function">ResourceBundle::create</span>
example**

``` php
<?php
$r = ResourceBundle::create( 'es', "/usr/share/data/myapp");
echo $r['teststring'];
?>
```

以上例程会输出：

    ¡Hola, mundo!

### 参见

-   <span class="function">resourcebundle\_get</span>

ResourceBundle::getErrorCode
============================

resourcebundle\_get\_error\_code
================================

Get bundle's last error code

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ResourceBundle::getErrorCode</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">int</span> <span
class="methodname">resourcebundle\_get\_error\_code</span> ( <span
class="methodparam"><span class="type">ResourceBundle</span> `$r`</span>
)

Get error code from the last function performed by the bundle object.

### 参数

`r`  
<span class="classname">ResourceBundle</span> object.

### 返回值

Returns error code from last bundle object call.

### 范例

**示例 \#1 <span
class="function">resourcebundle\_get\_error\_code</span> example**

``` php
<?php
$r = resourcebundle_create( 'es', "/usr/share/data/myapp");
echo $r['somestring'];
if(intl_is_failure(resourcebundle_get_error_code($r))) {
    report_error("Bundle error");
}
?>
```

**示例 \#2 OO example**

``` php
<?php
$r = new ResourceBundle( 'es', "/usr/share/data/myapp");
echo $r['somestring'];
if(intl_is_failure(ResourceBundle::getErrorCode($r))) {
    report_error("Bundle error");
}
?>
```

### 参见

-   <span class="function">resourcebundle\_get\_error\_message</span>
-   <span class="function">intl\_get\_error\_code</span>
-   <span class="function">intl\_is\_failure</span>

ResourceBundle::getErrorMessage
===============================

resourcebundle\_get\_error\_message
===================================

Get bundle's last error message

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ResourceBundle::getErrorMessage</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">string</span> <span
class="methodname">resourcebundle\_get\_error\_message</span> ( <span
class="methodparam"><span class="type">ResourceBundle</span> `$r`</span>
)

Get error message from the last function performed by the bundle object.

### 参数

`r`  
<span class="classname">ResourceBundle</span> object.

### 返回值

Returns error message from last bundle object's call.

### 范例

**示例 \#1 <span
class="function">resourcebundle\_get\_error\_message</span> example**

``` php
<?php
$r = resourcebundle_create( 'es', "/usr/share/data/myapp");
echo $r['somestring'];
if(intl_is_failure(resourcebundle_get_error_code($r))) {
    report_error("Bundle error: ".resourcebundle_get_error_message($r));
}
?>
```

**示例 \#2 OO example**

``` php
<?php
$r = new ResourceBundle( 'es', "/usr/share/data/myapp");
echo $r['somestring'];
if(intl_is_failure(ResourceBundle::getErrorCode($r))) {
    report_error("Bundle error: ".ResourceBundle::getErrorMessage($r));
}
?>
```

### 参见

-   <span class="function">resourcebundle\_get\_error\_code</span>
-   <span class="function">intl\_get\_error\_code</span>
-   <span class="function">intl\_is\_failure</span>

ResourceBundle::get
===================

resourcebundle\_get
===================

Get data from the bundle

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">ResourceBundle::get</span> ( <span
class="methodparam"><span class="type">string\|int</span>
`$index`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$fallback`<span class="initializer"> =
**`TRUE`**</span></span> \] )

过程化风格

<span class="type">mixed</span> <span
class="methodname">resourcebundle\_get</span> ( <span
class="methodparam"><span class="type">ResourceBundle</span> `$r`</span>
, <span class="methodparam"><span class="type">string\|int</span>
`$index`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$fallback`<span class="initializer"> =
**`TRUE`**</span></span> \] )

Get the data from the bundle by index or string key.

### 参数

`r`  
<span class="classname">ResourceBundle</span> object.

`index`  
Data index, must be string or integer.

`fallback`  
Whether locale should match exactly or fallback to parent locale is
allowed.

### 返回值

Returns the data located at the index or **`NULL`** on error. Strings,
integers and binary data strings are returned as corresponding PHP
types, integer array is returned as PHP array. Complex types are
returned as <span class="classname">ResourceBundle</span> object.

### 范例

**示例 \#1 <span class="function">resourcebundle\_get</span> example**

``` php
<?php
$r = resourcebundle_create( 'es', "/usr/share/data/myapp");
echo resourcebundle_get($r, 'somestring');
?>
```

**示例 \#2 OO example**

``` php
<?php
$r = new ResourceBundle( 'es', "/usr/share/data/myapp");
echo $r->get('somestring');
?>
```

以上例程会输出：

    ?Hola, mundo!

### 参见

-   <span class="function">resourcebundle\_count</span>

ResourceBundle::getLocales
==========================

resourcebundle\_locales
=======================

Get supported locales

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ResourceBundle::getLocales</span> ( <span
class="methodparam"><span class="type">string</span>
`$bundlename`</span> )

过程化风格

<span class="type">array</span> <span
class="methodname">resourcebundle\_locales</span> ( <span
class="methodparam"><span class="type">string</span>
`$bundlename`</span> )

Get available locales from ResourceBundle name.

### 参数

`bundlename`  
Path of ResourceBundle for which to get available locales, or empty
string for default locales list.

### 返回值

Returns the list of locales supported by the bundle.

### 范例

**示例 \#1 <span class="function">resourcebundle\_locales</span>
example**

``` php
<?php
$bundle = "/user/share/data/myapp";
echo join(PHP_EOL, resourcebundle_locales($bundle));
?>
```

以上例程的输出类似于：

    es
    root

**示例 \#2 OO example**

``` php
<?php
$bundle = "/usr/share/data/myapp";
$r = new ResourceBundle( 'es', $bundle);
echo join("\n", $r->getLocales($bundle));
?>
```

以上例程的输出类似于：

    es
    root

### 参见

-   <span class="function">resourcebundle\_get</span>

简介
----

This class is provided because Unicode contains large number of
characters and incorporates the varied writing systems of the world and
their incorrect usage can expose programs or systems to possible
security attacks using characters similarity.

Provided methods allow to check whether an individual string is likely
an attempt at confusing the reader (*spoof detection*), such as "pаypаl"
spelled with Cyrillic 'а' characters.

类摘要
------

**Spoofchecker**

<span class="ooclass"> class **Spoofchecker** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">number</span>
`Spoofchecker::ASCII` <span class="initializer"> = 0x10000000</span> ;

<span class="modifier">const</span> <span class="type">number</span>
`Spoofchecker::HIGHLY_RESTRICTIVE` <span class="initializer"> =
0x30000000</span> ;

<span class="modifier">const</span> <span class="type">number</span>
`Spoofchecker::MODERATELY_RESTRICTIVE` <span class="initializer"> =
0x40000000</span> ;

<span class="modifier">const</span> <span class="type">number</span>
`Spoofchecker::MINIMALLY_RESTRICTIVE` <span class="initializer"> =
0x50000000</span> ;

<span class="modifier">const</span> <span class="type">number</span>
`Spoofchecker::UNRESTRICTIVE` <span class="initializer"> =
0x60000000</span> ;

<span class="modifier">const</span> <span class="type">number</span>
`Spoofchecker::SINGLE_SCRIPT_RESTRICTIVE` <span class="initializer"> =
0x20000000</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Spoofchecker::SINGLE_SCRIPT_CONFUSABLE` <span class="initializer"> =
1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Spoofchecker::MIXED_SCRIPT_CONFUSABLE` <span class="initializer"> =
2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Spoofchecker::WHOLE_SCRIPT_CONFUSABLE` <span class="initializer"> =
4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Spoofchecker::ANY_CASE` <span class="initializer"> = 8</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Spoofchecker::SINGLE_SCRIPT` <span class="initializer"> = 16</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Spoofchecker::INVISIBLE` <span class="initializer"> = 32</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Spoofchecker::CHAR_LIMIT` <span class="initializer"> = 64</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">areConfusable</span> ( <span
class="methodparam"><span class="type">string</span> `$str1`</span> ,
<span class="methodparam"><span class="type">string</span>
`$str2`</span> \[, <span class="methodparam"><span
class="type">string</span> `&$error`</span> \] )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isSuspicious</span> ( <span
class="methodparam"><span class="type">string</span> `$text`</span> \[,
<span class="methodparam"><span class="type">string</span>
`&$error`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setAllowedLocales</span> ( <span
class="methodparam"><span class="type">string</span>
`$locale_list`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setChecks</span> ( <span
class="methodparam"><span class="type">int</span> `$checks`</span> )

}

预定义常量
----------

**`Spoofchecker::ASCII`**  

**`Spoofchecker::HIGHLY_RESTRICTIVE`**  

**`Spoofchecker::MODERATELY_RESTRICTIVE`**  

**`Spoofchecker::MINIMALLY_RESTRICTIVE`**  

**`Spoofchecker::UNRESTRICTIVE`**  

**`Spoofchecker::SINGLE_SCRIPT_RESTRICTIVE`**  

**`Spoofchecker::SINGLE_SCRIPT_CONFUSABLE`**  

**`Spoofchecker::MIXED_SCRIPT_CONFUSABLE`**  

**`Spoofchecker::WHOLE_SCRIPT_CONFUSABLE`**  

**`Spoofchecker::ANY_CASE`**  

**`Spoofchecker::SINGLE_SCRIPT`**  

**`Spoofchecker::INVISIBLE`**  

**`Spoofchecker::CHAR_LIMIT`**  

更新日志
--------

| 版本  | 说明                                                                                                                                                                                                                                                                                                                                                       |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 7.3.0 | Class constants used by <span class="function">Spoofchecker::setRestrictionLevel</span> such as **`Spoofchecker::ASCII`**, **`Spoofchecker::HIGHLY_RESTRICTIVE`**, **`Spoofchecker::MODERATELY_RESTRICTIVE`**, **`Spoofchecker::MINIMALLY_RESTRICTIVE`**, **`Spoofchecker::UNRESTRICTIVE`**, **`Spoofchecker::SINGLE_SCRIPT_RESTRICTIVE`** has been added. |

Spoofchecker::areConfusable
===========================

Checks if given strings can be confused

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Spoofchecker::areConfusable</span> ( <span
class="methodparam"><span class="type">string</span> `$str1`</span> ,
<span class="methodparam"><span class="type">string</span>
`$str2`</span> \[, <span class="methodparam"><span
class="type">string</span> `&$error`</span> \] )

Checks whether two given strings can easily be mistaken.

### 参数

`str1`  
First string to check.

`str2`  
Second string to check.

`error`  
This variable is set by-reference to string containing an error, if
there were any.

### 返回值

Returns **`TRUE`** if two given strings can be confused, **`FALSE`**
otherwise.

### 范例

**示例 \#1 <span class="function">Spoofchecker::areConfusable</span>
example**

``` php
<?php
$checker = new Spoofchecker();

$checker->areConfusable('google.com', 'goog1e.com'); // true
// Lower l can be confused with digit one

$checker->areConfusable('google.com', 'g00g1e.com'); // false
// Zero (0) cannot be easily confused with "o" letter
```

Spoofchecker::\_\_construct
===========================

Constructor

### 说明

<span class="modifier">public</span> <span
class="methodname">Spoofchecker::\_\_construct</span> ( <span
class="methodparam">void</span> )

Creates new instance of Spoofchecker.

### 参数

此函数没有参数。

### 返回值

Returns Spoofchecker instance.

Spoofchecker::isSuspicious
==========================

Checks if a given text contains any suspicious characters

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Spoofchecker::isSuspicious</span> ( <span
class="methodparam"><span class="type">string</span> `$text`</span> \[,
<span class="methodparam"><span class="type">string</span>
`&$error`</span> \] )

Checks if given string contains any suspicious characters like letters
which are almost identical visually, but are Unicode characters from
different sets.

### 参数

`text`  
String to test.

`error`  
This variable is set by-reference to string containing an error, if
there were any.

### 返回值

Returns **`TRUE`** if there are suspicious characters, **`FALSE`**
otherwise.

### 范例

**示例 \#1 <span class="function">Spoofchecker::isSuspicious</span>
example**

``` php
<?php
$checker = new Spoofchecker();

$checker->isSuspicious('google.com'); // FALSE: only ASCII characters

$checker->isSuspicious('Рaypal.com'); // TRUE
// The first letter is from Cyrylic, not a regular latin "P"
```

Spoofchecker::setAllowedLocales
===============================

Locales to use when running checks

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Spoofchecker::setAllowedLocales</span> ( <span
class="methodparam"><span class="type">string</span>
`$locale_list`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`locale_list`  

### 返回值

Spoofchecker::setChecks
=======================

Set the checks to run

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Spoofchecker::setChecks</span> ( <span
class="methodparam"><span class="type">int</span> `$checks`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`checks`  

### 返回值

简介
----

Transliterator provides transliteration of strings.

类摘要
------

**Transliterator**

<span class="ooclass"> class **Transliterator** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`Transliterator::FORWARD` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Transliterator::REVERSE` <span class="initializer"> = 1</span> ;

/\* 属性 \*/

<span class="modifier">public</span> `$id` ;

/\* 方法 \*/

<span class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">Transliterator</span>
<span class="methodname">create</span> ( <span class="methodparam"><span
class="type">string</span> `$id`</span> \[, <span
class="methodparam"><span class="type">int</span> `$direction`</span> \]
)

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">Transliterator</span>
<span class="methodname">createFromRules</span> ( <span
class="methodparam"><span class="type">string</span> `$rules`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$direction`</span> \] )

<span class="modifier">public</span> <span
class="type">Transliterator</span> <span
class="methodname">createInverse</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getErrorCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getErrorMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">listIDs</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">transliterate</span> ( <span
class="methodparam"><span class="type">string</span> `$subject`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$start`</span> \[, <span class="methodparam"><span
class="type">int</span> `$end`</span> \]\] )

}

属性
----

`id`  

预定义常量
----------

**`Transliterator::FORWARD`**  

**`Transliterator::REVERSE`**  

Transliterator::\_\_construct
=============================

Private constructor to deny instantiation

### 说明

<span class="methodname">Transliterator::\_\_construct</span> ( <span
class="methodparam">void</span> )

This method should not be called. Its only purpose is to deny
instantiation with the
<a href="/language/oop5/basic.html#language.oop5.basic.new" class="link">new</a>
operator.

Use the factory methods <span
class="methodname">Transliterator::create</span> or <span
class="methodname">Transliterator::createFromRules</span> instead.

### 参数

此函数没有参数。

### 返回值

This method should not be executed. If it is (e.g. through reflection),
then its return value is unspecified.

### 参见

-   <span class="methodname">Transliterator::create</span>
-   <span class="methodname">Transliterator::createFromRules</span>

Transliterator::create
======================

transliterator\_create
======================

Create a transliterator

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">Transliterator</span>
<span class="methodname">Transliterator::create</span> ( <span
class="methodparam"><span class="type">string</span> `$id`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$direction`</span> \] )

过程化风格

<span class="type">Transliterator</span> <span
class="methodname">transliterator\_create</span> ( <span
class="methodparam"><span class="type">string</span> `$id`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$direction`</span> \] )

Opens a Transliterator by id.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`id`  
The id.

`direction`  
The direction, defaults to
<a href="/class/transliterator.html#" class="link">&gt;Transliterator::FORWARD</a>.
May also be set to
<a href="/class/transliterator.html#" class="link">Transliterator::REVERSE</a>.

### 返回值

Returns a <span class="classname">Transliterator</span> object on
success, or **`NULL`** on failure.

### 参见

-   <span class="methodname">Transliterator::getErrorMessage</span>
-   <span class="methodname">Transliterator::\_\_construct</span>

Transliterator::createFromRules
===============================

transliterator\_create\_from\_rules
===================================

Create transliterator from rules

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">Transliterator</span>
<span class="methodname">Transliterator::createFromRules</span> ( <span
class="methodparam"><span class="type">string</span> `$rules`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$direction`</span> \] )

过程化风格

<span class="type">Transliterator</span> <span
class="methodname">transliterator\_create\_from\_rules</span> ( <span
class="methodparam"><span class="type">string</span> `$id`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$direction`</span> \] )

Creates a Transliterator from rules.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`rules`  
The rules as defined in Transform Rules Syntax of UTS \#35: Unicode
LDML.

`direction`  
The direction, defaults to
<a href="/class/transliterator.html#" class="link">&gt;Transliterator::FORWARD</a>.
May also be set to
<a href="/class/transliterator.html#" class="link">Transliterator::REVERSE</a>.

### 返回值

Returns a <span class="classname">Transliterator</span> object on
success, or **`NULL`** on failure.

### 参见

-   <span class="methodname">Transliterator::getErrorMessage</span>
-   <span class="methodname">Transliterator::create</span>

Transliterator::createInverse
=============================

transliterator\_create\_inverse
===============================

Create an inverse transliterator

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="type">Transliterator</span> <span
class="methodname">Transliterator::createInverse</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">Transliterator</span> <span
class="methodname">transliterator\_create\_inverse</span> ( <span
class="methodparam">void</span> )

Opens the inverse transliterator.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Returns a <span class="classname">Transliterator</span> object on
success, or **`NULL`** on failure

### 参见

-   <span class="methodname">Transliterator::getErrorMessage</span>
-   <span class="methodname">Transliterator::create</span>

Transliterator::getErrorCode
============================

transliterator\_get\_error\_code
================================

Get last error code

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Transliterator::getErrorCode</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">int</span> <span
class="methodname">transliterator\_get\_error\_code</span> ( <span
class="methodparam"><span class="type">Transliterator</span>
`$trans`</span> )

Gets the last error code for this transliterator.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`trans`  

### 返回值

The error code on success, or **`FALSE`** if none exists, or on failure.

### 参见

-   <span class="methodname">Transliterator::getErrorMessage</span>
-   <span class="methodname">Transliterator::listIDs</span>

Transliterator::getErrorMessage
===============================

transliterator\_get\_error\_message
===================================

Get last error message

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Transliterator::getErrorMessage</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">string</span> <span
class="methodname">transliterator\_get\_error\_message</span> ( <span
class="methodparam"><span class="type">Transliterator</span>
`$trans`</span> )

Gets the last error message for this transliterator.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`trans`  

### 返回值

The error message on success, or **`FALSE`** if none exists, or on
failure.

### 参见

-   <span class="methodname">Transliterator::getErrorCode</span>
-   <span class="methodname">Transliterator::listIDs</span>

Transliterator::listIDs
=======================

transliterator\_list\_ids
=========================

Get transliterator IDs

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">Transliterator::listIDs</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">array</span> <span
class="methodname">transliterator\_list\_ids</span> ( <span
class="methodparam">void</span> )

Returns an array with the registered transliterator IDs.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

An <span class="type">array</span> of registered transliterator IDs on
success, 或者在失败时返回 **`FALSE`**.

### 参见

-   <span class="methodname">Transliterator::getErrorMessage</span>
-   <span class="methodname">Transliterator::transliterate</span>

Transliterator::transliterate
=============================

transliterator\_transliterate
=============================

Transliterate a string

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Transliterator::transliterate</span> ( <span
class="methodparam"><span class="type">string</span> `$subject`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$start`</span> \[, <span class="methodparam"><span
class="type">int</span> `$end`</span> \]\] )

过程化风格

<span class="methodname">transliterator\_transliterate</span> ( <span
class="methodparam"><span class="type">mixed</span>
`$transliterator`</span> , <span class="methodparam"><span
class="type">string</span> `$subject`</span> \[, <span
class="methodparam"><span class="type">int</span> `$start`</span> \[,
<span class="methodparam"><span class="type">int</span> `$end`</span>
\]\] )

Transforms a string or part thereof using an ICU transliterator.

### 参数

`transliterator`  
In the procedural version, either a <span
class="classname">Transliterator</span> or a <span
class="type">string</span> from which a <span
class="classname">Transliterator</span> can be built.

`subject`  
The string to be transformed.

`start`  
The start index (in UTF-16 code units) from which the string will start
to be transformed, inclusive. Indexing starts at 0. The text before will
be left as is.

`end`  
The end index (in UTF-16 code units) until which the string will be
transformed, exclusive. Indexing starts at 0. The text after will be
left as is.

### 返回值

The transformed string on success, 或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 Converting escaped UTF-16 code units**

``` php
<?php
$s = "\u304A\u65E9\u3046\u3054\u3056\u3044\u307E\u3059";
echo transliterator_transliterate("Hex-Any/Java", $s), "\n";

//now the reverse operation with a supplementary character
$supplChar = html_entity_decode('&#x1D11E;');
echo mb_strlen($supplChar, "UTF-8"), "\n";
$encSupplChar = transliterator_transliterate("Any-Hex/Java", $supplChar);
//echoes two encoded UTF-16 code units
echo $encSupplChar, "\n";
//and back
echo transliterator_transliterate("Hex-Any/Java", $encSupplChar), "\n";
?>
```

以上例程的输出类似于：

    お早うございます
    1
    \uD834\uDD1E
    𝄞

### 参见

-   <span class="methodname">Transliterator::getErrorMessage</span>
-   <span class="methodname">Transliterator::\_\_construct</span>

简介
----

A “break iterator” is an ICU object that exposes methods for locating
boundaries in text (e.g. word or sentence boundaries). The PHP <span
class="classname">IntlBreakIterator</span> serves as the base class for
all types of ICU break iterators. Where extra functionality is
available, the intl extension may expose the ICU break iterator with
suitable subclasses, such as <span
class="classname">IntlRuleBasedBreakIterator</span> or <span
class="classname">IntlCodePointBreakIterator</span>.

This class implements <span class="classname">Traversable</span>.
Traversing an <span class="classname">IntlBreakIterator</span> yields
non-negative integer values representing the successive locations of the
text boundaries, expressed as UTF-8 code units (byte) counts, taken from
the beginning of the text (which has the location *0*). The keys yielded
by the iterator simply form the sequence of natural numbers *{0, 1, 2,
…}*.

类摘要
------

**IntlBreakIterator**

<span class="ooclass"> class **IntlBreakIterator** </span> <span
class="oointerface">implements <span
class="interfacename">Traversable</span> </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::DONE` <span class="initializer"> = -1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::WORD_NONE` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::WORD_NONE_LIMIT` <span class="initializer"> =
100</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::WORD_NUMBER` <span class="initializer"> = 100</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::WORD_NUMBER_LIMIT` <span class="initializer"> =
200</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::WORD_LETTER` <span class="initializer"> = 200</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::WORD_LETTER_LIMIT` <span class="initializer"> =
300</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::WORD_KANA` <span class="initializer"> = 300</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::WORD_KANA_LIMIT` <span class="initializer"> =
400</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::WORD_IDEO` <span class="initializer"> = 400</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::WORD_IDEO_LIMIT` <span class="initializer"> =
500</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::LINE_SOFT` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::LINE_SOFT_LIMIT` <span class="initializer"> =
100</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::LINE_HARD` <span class="initializer"> = 100</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::LINE_HARD_LIMIT` <span class="initializer"> =
200</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::SENTENCE_TERM` <span class="initializer"> = 0</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::SENTENCE_TERM_LIMIT` <span class="initializer"> =
100</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::SENTENCE_SEP` <span class="initializer"> =
100</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::SENTENCE_SEP_LIMIT` <span class="initializer"> =
200</span> ;

/\* 方法 \*/

<span class="modifier">private</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">IntlBreakIterator</span> <span
class="methodname">createCharacterInstance</span> (\[ <span
class="methodparam"><span class="type">string</span> `$locale`</span> \]
)

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">IntlBreakIterator</span> <span
class="methodname">createCodePointInstance</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">IntlBreakIterator</span> <span
class="methodname">createLineInstance</span> (\[ <span
class="methodparam"><span class="type">string</span> `$locale`</span> \]
)

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">IntlBreakIterator</span> <span
class="methodname">createSentenceInstance</span> (\[ <span
class="methodparam"><span class="type">string</span> `$locale`</span> \]
)

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">IntlBreakIterator</span> <span
class="methodname">createTitleInstance</span> (\[ <span
class="methodparam"><span class="type">string</span> `$locale`</span> \]
)

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">IntlBreakIterator</span> <span
class="methodname">createWordInstance</span> (\[ <span
class="methodparam"><span class="type">string</span> `$locale`</span> \]
)

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">first</span> ( <span class="methodparam">void</span>
)

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">following</span> ( <span class="methodparam"><span
class="type">int</span> `$offset`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getErrorCode</span> ( <span
class="methodparam">void</span> )

<span class="type">int</span> <span
class="methodname">intl\_get\_error\_code</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getErrorMessage</span> ( <span
class="methodparam">void</span> )

<span class="type">string</span> <span
class="methodname">intl\_get\_error\_message</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getLocale</span> ( <span
class="methodparam"><span class="type">string</span>
`$locale_type`</span> )

<span class="modifier">public</span> <span
class="type">IntlPartsIterator</span> <span
class="methodname">getPartsIterator</span> (\[ <span
class="methodparam"><span class="type">int</span> `$key_type`<span
class="initializer"> = IntlPartsIterator::KEY\_SEQUENTIAL</span></span>
\] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getText</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isBoundary</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">last</span> ( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">next</span> (\[ <span class="methodparam"><span
class="type">int</span> `$offset`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">preceding</span> ( <span class="methodparam"><span
class="type">int</span> `$offset`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">previous</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setText</span> ( <span
class="methodparam"><span class="type">string</span> `$text`</span> )

}

预定义常量
----------

**`IntlBreakIterator::DONE`**  

**`IntlBreakIterator::WORD_NONE`**  

**`IntlBreakIterator::WORD_NONE_LIMIT`**  

**`IntlBreakIterator::WORD_NUMBER`**  

**`IntlBreakIterator::WORD_NUMBER_LIMIT`**  

**`IntlBreakIterator::WORD_LETTER`**  

**`IntlBreakIterator::WORD_LETTER_LIMIT`**  

**`IntlBreakIterator::WORD_KANA`**  

**`IntlBreakIterator::WORD_KANA_LIMIT`**  

**`IntlBreakIterator::WORD_IDEO`**  

**`IntlBreakIterator::WORD_IDEO_LIMIT`**  

**`IntlBreakIterator::LINE_SOFT`**  

**`IntlBreakIterator::LINE_SOFT_LIMIT`**  

**`IntlBreakIterator::LINE_HARD`**  

**`IntlBreakIterator::LINE_HARD_LIMIT`**  

**`IntlBreakIterator::SENTENCE_TERM`**  

**`IntlBreakIterator::SENTENCE_TERM_LIMIT`**  

**`IntlBreakIterator::SENTENCE_SEP`**  

**`IntlBreakIterator::SENTENCE_SEP_LIMIT`**  

IntlBreakIterator::\_\_construct
================================

Private constructor for disallowing instantiation

### 说明

<span class="modifier">private</span> <span
class="methodname">IntlBreakIterator::\_\_construct</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

IntlBreakIterator::createCharacterInstance
==========================================

Create break iterator for boundaries of combining character sequences

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">IntlBreakIterator</span> <span
class="methodname">IntlBreakIterator::createCharacterInstance</span> (\[
<span class="methodparam"><span class="type">string</span>
`$locale`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`locale`  

### 返回值

IntlBreakIterator::createCodePointInstance
==========================================

Create break iterator for boundaries of code points

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">IntlBreakIterator</span> <span
class="methodname">IntlBreakIterator::createCodePointInstance</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

IntlBreakIterator::createLineInstance
=====================================

Create break iterator for logically possible line breaks

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">IntlBreakIterator</span> <span
class="methodname">IntlBreakIterator::createLineInstance</span> (\[
<span class="methodparam"><span class="type">string</span>
`$locale`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`locale`  

### 返回值

IntlBreakIterator::createSentenceInstance
=========================================

Create break iterator for sentence breaks

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">IntlBreakIterator</span> <span
class="methodname">IntlBreakIterator::createSentenceInstance</span> (\[
<span class="methodparam"><span class="type">string</span>
`$locale`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`locale`  

### 返回值

IntlBreakIterator::createTitleInstance
======================================

Create break iterator for title-casing breaks

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">IntlBreakIterator</span> <span
class="methodname">IntlBreakIterator::createTitleInstance</span> (\[
<span class="methodparam"><span class="type">string</span>
`$locale`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`locale`  

### 返回值

IntlBreakIterator::createWordInstance
=====================================

Create break iterator for word breaks

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">IntlBreakIterator</span> <span
class="methodname">IntlBreakIterator::createWordInstance</span> (\[
<span class="methodparam"><span class="type">string</span>
`$locale`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`locale`  

### 返回值

IntlBreakIterator::current
==========================

Get index of current position

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlBreakIterator::current</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

IntlBreakIterator::first
========================

Set position to the first character in the text

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlBreakIterator::first</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

IntlBreakIterator::following
============================

Advance the iterator to the first boundary following specified offset

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlBreakIterator::following</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`offset`  

### 返回值

IntlBreakIterator::getErrorCode
===============================

intl\_get\_error\_code
======================

Get last error code on the object

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlBreakIterator::getErrorCode</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">int</span> <span
class="methodname">intl\_get\_error\_code</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

IntlBreakIterator::getErrorMessage
==================================

intl\_get\_error\_message
=========================

Get last error message on the object

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">IntlBreakIterator::getErrorMessage</span> (
<span class="methodparam">void</span> )

过程化风格:

<span class="type">string</span> <span
class="methodname">intl\_get\_error\_message</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

IntlBreakIterator::getLocale
============================

Get the locale associated with the object

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">IntlBreakIterator::getLocale</span> ( <span
class="methodparam"><span class="type">string</span>
`$locale_type`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`locale_type`  

### 返回值

IntlBreakIterator::getPartsIterator
===================================

Create iterator for navigating fragments between boundaries

### 说明

<span class="modifier">public</span> <span
class="type">IntlPartsIterator</span> <span
class="methodname">IntlBreakIterator::getPartsIterator</span> (\[ <span
class="methodparam"><span class="type">int</span> `$key_type`<span
class="initializer"> = IntlPartsIterator::KEY\_SEQUENTIAL</span></span>
\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`key_type`  
Optional key type. Possible values are:

-   **`IntlPartsIterator::KEY_SEQUENTIAL`** - The default. Sequentially
    increasing integers used as key.
-   **`IntlPartsIterator::KEY_LEFT`** - Byte offset left of current part
    used as key.
-   **`IntlPartsIterator::KEY_RIGHT`** - Byte offset right of current
    part used as key.

### 返回值

IntlBreakIterator::getText
==========================

Get the text being scanned

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">IntlBreakIterator::getText</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

IntlBreakIterator::isBoundary
=============================

Tell whether an offset is a boundaryʼs offset

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlBreakIterator::isBoundary</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`offset`  

### 返回值

IntlBreakIterator::last
=======================

Set the iterator position to index beyond the last character

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlBreakIterator::last</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

IntlBreakIterator::next
=======================

Advance the iterator the next boundary

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlBreakIterator::next</span> (\[ <span
class="methodparam"><span class="type">int</span> `$offset`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`offset`  

### 返回值

IntlBreakIterator::preceding
============================

Set the iterator position to the first boundary before an offset

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlBreakIterator::preceding</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`offset`  

### 返回值

IntlBreakIterator::previous
===========================

Set the iterator position to the boundary immediately before the current

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlBreakIterator::previous</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

IntlBreakIterator::setText
==========================

Set the text being scanned

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlBreakIterator::setText</span> ( <span
class="methodparam"><span class="type">string</span> `$text`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`text`  

### 返回值

简介
----

A subclass of <span class="classname">IntlBreakIterator</span> that
encapsulates ICU break iterators whose behavior is specified using a set
of rules. This is the most common kind of break iterators.

These rules are described in the
<a href="http://userguide.icu-project.org/boundaryanalysis#TOC-RBBI-Rules" class="link external">» ICU Boundary Analysis User Guide</a>.

类摘要
------

**IntlRuleBasedBreakIterator**

<span class="ooclass"> class **IntlRuleBasedBreakIterator** </span>
<span class="ooclass"> <span class="modifier">extends</span>
**IntlBreakIterator** </span> <span class="oointerface">implements <span
class="interfacename">Traversable</span> </span> {

/\* 继承的常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::DONE` <span class="initializer"> = -1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::WORD_NONE` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::WORD_NONE_LIMIT` <span class="initializer"> =
100</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::WORD_NUMBER` <span class="initializer"> = 100</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::WORD_NUMBER_LIMIT` <span class="initializer"> =
200</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::WORD_LETTER` <span class="initializer"> = 200</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::WORD_LETTER_LIMIT` <span class="initializer"> =
300</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::WORD_KANA` <span class="initializer"> = 300</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::WORD_KANA_LIMIT` <span class="initializer"> =
400</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::WORD_IDEO` <span class="initializer"> = 400</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::WORD_IDEO_LIMIT` <span class="initializer"> =
500</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::LINE_SOFT` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::LINE_SOFT_LIMIT` <span class="initializer"> =
100</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::LINE_HARD` <span class="initializer"> = 100</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::LINE_HARD_LIMIT` <span class="initializer"> =
200</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::SENTENCE_TERM` <span class="initializer"> = 0</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::SENTENCE_TERM_LIMIT` <span class="initializer"> =
100</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::SENTENCE_SEP` <span class="initializer"> =
100</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::SENTENCE_SEP_LIMIT` <span class="initializer"> =
200</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$rules`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$areCompiled`</span> \] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getBinaryRules</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getRules</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getRuleStatus</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getRuleStatusVec</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">private</span> <span
class="methodname">IntlBreakIterator::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">IntlBreakIterator</span> <span
class="methodname">IntlBreakIterator::createCharacterInstance</span> (\[
<span class="methodparam"><span class="type">string</span>
`$locale`</span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">IntlBreakIterator</span> <span
class="methodname">IntlBreakIterator::createCodePointInstance</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">IntlBreakIterator</span> <span
class="methodname">IntlBreakIterator::createLineInstance</span> (\[
<span class="methodparam"><span class="type">string</span>
`$locale`</span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">IntlBreakIterator</span> <span
class="methodname">IntlBreakIterator::createSentenceInstance</span> (\[
<span class="methodparam"><span class="type">string</span>
`$locale`</span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">IntlBreakIterator</span> <span
class="methodname">IntlBreakIterator::createTitleInstance</span> (\[
<span class="methodparam"><span class="type">string</span>
`$locale`</span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">IntlBreakIterator</span> <span
class="methodname">IntlBreakIterator::createWordInstance</span> (\[
<span class="methodparam"><span class="type">string</span>
`$locale`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlBreakIterator::current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlBreakIterator::first</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlBreakIterator::following</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlBreakIterator::getErrorCode</span> ( <span
class="methodparam">void</span> )

<span class="type">int</span> <span
class="methodname">intl\_get\_error\_code</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">IntlBreakIterator::getErrorMessage</span> (
<span class="methodparam">void</span> )

<span class="type">string</span> <span
class="methodname">intl\_get\_error\_message</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">IntlBreakIterator::getLocale</span> ( <span
class="methodparam"><span class="type">string</span>
`$locale_type`</span> )

<span class="modifier">public</span> <span
class="type">IntlPartsIterator</span> <span
class="methodname">IntlBreakIterator::getPartsIterator</span> (\[ <span
class="methodparam"><span class="type">int</span> `$key_type`<span
class="initializer"> = IntlPartsIterator::KEY\_SEQUENTIAL</span></span>
\] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">IntlBreakIterator::getText</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlBreakIterator::isBoundary</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlBreakIterator::last</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlBreakIterator::next</span> (\[ <span
class="methodparam"><span class="type">int</span> `$offset`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlBreakIterator::preceding</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlBreakIterator::previous</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlBreakIterator::setText</span> ( <span
class="methodparam"><span class="type">string</span> `$text`</span> )

}

IntlRuleBasedBreakIterator::\_\_construct
=========================================

Create iterator from ruleset

### 说明

<span class="modifier">public</span> <span
class="methodname">IntlRuleBasedBreakIterator::\_\_construct</span> (
<span class="methodparam"><span class="type">string</span>
`$rules`</span> \[, <span class="methodparam"><span
class="type">string</span> `$areCompiled`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`rules`  

`areCompiled`  

### 返回值

IntlRuleBasedBreakIterator::getBinaryRules
==========================================

Get the binary form of compiled rules

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span
class="methodname">IntlRuleBasedBreakIterator::getBinaryRules</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

IntlRuleBasedBreakIterator::getRules
====================================

Get the rule set used to create this object

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">IntlRuleBasedBreakIterator::getRules</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

IntlRuleBasedBreakIterator::getRuleStatus
=========================================

Get the largest status value from the break rules that determined the
current break position

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlRuleBasedBreakIterator::getRuleStatus</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

IntlRuleBasedBreakIterator::getRuleStatusVec
============================================

Get the status values from the break rules that determined the current
break position

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span
class="methodname">IntlRuleBasedBreakIterator::getRuleStatusVec</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

简介
----

This
<a href="/class/intlbreakiterator.html" class="link">break iterator</a>
identifies the boundaries between UTF-8 code points.

类摘要
------

**IntlCodePointBreakIterator**

<span class="ooclass"> class **IntlCodePointBreakIterator** </span>
<span class="ooclass"> <span class="modifier">extends</span>
**IntlBreakIterator** </span> <span class="oointerface">implements <span
class="interfacename">Traversable</span> </span> {

/\* 继承的常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::DONE` <span class="initializer"> = -1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::WORD_NONE` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::WORD_NONE_LIMIT` <span class="initializer"> =
100</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::WORD_NUMBER` <span class="initializer"> = 100</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::WORD_NUMBER_LIMIT` <span class="initializer"> =
200</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::WORD_LETTER` <span class="initializer"> = 200</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::WORD_LETTER_LIMIT` <span class="initializer"> =
300</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::WORD_KANA` <span class="initializer"> = 300</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::WORD_KANA_LIMIT` <span class="initializer"> =
400</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::WORD_IDEO` <span class="initializer"> = 400</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::WORD_IDEO_LIMIT` <span class="initializer"> =
500</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::LINE_SOFT` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::LINE_SOFT_LIMIT` <span class="initializer"> =
100</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::LINE_HARD` <span class="initializer"> = 100</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::LINE_HARD_LIMIT` <span class="initializer"> =
200</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::SENTENCE_TERM` <span class="initializer"> = 0</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::SENTENCE_TERM_LIMIT` <span class="initializer"> =
100</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::SENTENCE_SEP` <span class="initializer"> =
100</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlBreakIterator::SENTENCE_SEP_LIMIT` <span class="initializer"> =
200</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getLastCodePoint</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">private</span> <span
class="methodname">IntlBreakIterator::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">IntlBreakIterator</span> <span
class="methodname">IntlBreakIterator::createCharacterInstance</span> (\[
<span class="methodparam"><span class="type">string</span>
`$locale`</span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">IntlBreakIterator</span> <span
class="methodname">IntlBreakIterator::createCodePointInstance</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">IntlBreakIterator</span> <span
class="methodname">IntlBreakIterator::createLineInstance</span> (\[
<span class="methodparam"><span class="type">string</span>
`$locale`</span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">IntlBreakIterator</span> <span
class="methodname">IntlBreakIterator::createSentenceInstance</span> (\[
<span class="methodparam"><span class="type">string</span>
`$locale`</span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">IntlBreakIterator</span> <span
class="methodname">IntlBreakIterator::createTitleInstance</span> (\[
<span class="methodparam"><span class="type">string</span>
`$locale`</span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">IntlBreakIterator</span> <span
class="methodname">IntlBreakIterator::createWordInstance</span> (\[
<span class="methodparam"><span class="type">string</span>
`$locale`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlBreakIterator::current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlBreakIterator::first</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlBreakIterator::following</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlBreakIterator::getErrorCode</span> ( <span
class="methodparam">void</span> )

<span class="type">int</span> <span
class="methodname">intl\_get\_error\_code</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">IntlBreakIterator::getErrorMessage</span> (
<span class="methodparam">void</span> )

<span class="type">string</span> <span
class="methodname">intl\_get\_error\_message</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">IntlBreakIterator::getLocale</span> ( <span
class="methodparam"><span class="type">string</span>
`$locale_type`</span> )

<span class="modifier">public</span> <span
class="type">IntlPartsIterator</span> <span
class="methodname">IntlBreakIterator::getPartsIterator</span> (\[ <span
class="methodparam"><span class="type">int</span> `$key_type`<span
class="initializer"> = IntlPartsIterator::KEY\_SEQUENTIAL</span></span>
\] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">IntlBreakIterator::getText</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlBreakIterator::isBoundary</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlBreakIterator::last</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlBreakIterator::next</span> (\[ <span
class="methodparam"><span class="type">int</span> `$offset`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlBreakIterator::preceding</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlBreakIterator::previous</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlBreakIterator::setText</span> ( <span
class="methodparam"><span class="type">string</span> `$text`</span> )

}

IntlCodePointBreakIterator::getLastCodePoint
============================================

Get last code point passed over after advancing or receding the iterator

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">IntlCodePointBreakIterator::getLastCodePoint</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

简介
----

Objects of this class can be obtained from <span
class="classname">IntlBreakIterator</span> objects. While the break
iterators provide a sequence of boundary positions when iterated, <span
class="classname">IntlPartsIterator</span> objects provide, as a
convenience, the text fragments comprehended between two successive
boundaries.

The keys may represent the offset of the left boundary, right boundary,
or they may just the sequence of non-negative integers. See <span
class="function">IntlBreakIterator::getPartsIterator</span>.

类摘要
------

**IntlPartsIterator**

<span class="ooclass"> class **IntlPartsIterator** </span> <span
class="ooclass"> <span class="modifier">extends</span> **IntlIterator**
</span> <span class="oointerface">implements <span
class="interfacename">Iterator</span> </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">integer</span>
`IntlPartsIterator::KEY_SEQUENTIAL` <span class="initializer"> =
0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlPartsIterator::KEY_LEFT` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlPartsIterator::KEY_RIGHT` <span class="initializer"> = 2</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="type">IntlBreakIterator</span> <span
class="methodname">getBreakIterator</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">IntlIterator::current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">IntlIterator::key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">IntlIterator::next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">IntlIterator::rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlIterator::valid</span> ( <span
class="methodparam">void</span> )

}

预定义常量
----------

**`IntlPartsIterator::KEY_SEQUENTIAL`**  

**`IntlPartsIterator::KEY_LEFT`**  

**`IntlPartsIterator::KEY_RIGHT`**  

IntlPartsIterator::getBreakIterator
===================================

Get IntlBreakIterator backing this parts iterator

### 说明

<span class="modifier">public</span> <span
class="type">IntlBreakIterator</span> <span
class="methodname">IntlPartsIterator::getBreakIterator</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

简介
----

类摘要
------

**UConverter**

<span class="ooclass"> class **UConverter** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::REASON_UNASSIGNED` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::REASON_ILLEGAL` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::REASON_IRREGULAR` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::REASON_RESET` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::REASON_CLOSE` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::REASON_CLONE` <span class="initializer"> = 5</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::UNSUPPORTED_CONVERTER` <span class="initializer"> =
-1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::SBCS` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::DBCS` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::MBCS` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::LATIN_1` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::UTF8` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::UTF16_BigEndian` <span class="initializer"> = 5</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::UTF16_LittleEndian` <span class="initializer"> = 6</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::UTF32_BigEndian` <span class="initializer"> = 7</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::UTF32_LittleEndian` <span class="initializer"> = 8</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::EBCDIC_STATEFUL` <span class="initializer"> = 9</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::ISO_2022` <span class="initializer"> = 10</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::LMBCS_1` <span class="initializer"> = 11</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::LMBCS_2` <span class="initializer"> = 12</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::LMBCS_3` <span class="initializer"> = 13</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::LMBCS_4` <span class="initializer"> = 14</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::LMBCS_5` <span class="initializer"> = 15</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::LMBCS_6` <span class="initializer"> = 16</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::LMBCS_8` <span class="initializer"> = 17</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::LMBCS_11` <span class="initializer"> = 18</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::LMBCS_16` <span class="initializer"> = 19</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::LMBCS_17` <span class="initializer"> = 20</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::LMBCS_18` <span class="initializer"> = 21</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::LMBCS_19` <span class="initializer"> = 22</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::LMBCS_LAST` <span class="initializer"> = 22</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::HZ` <span class="initializer"> = 23</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::SCSU` <span class="initializer"> = 24</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::ISCII` <span class="initializer"> = 25</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::US_ASCII` <span class="initializer"> = 26</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::UTF7` <span class="initializer"> = 27</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::BOCU1` <span class="initializer"> = 28</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::UTF16` <span class="initializer"> = 29</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::UTF32` <span class="initializer"> = 30</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::CESU8` <span class="initializer"> = 31</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`UConverter::IMAP_MAILBOX` <span class="initializer"> = 32</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span>
`$destination_encoding`</span> \[, <span class="methodparam"><span
class="type">string</span> `$source_encoding`</span> \]\] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">convert</span> ( <span
class="methodparam"><span class="type">string</span> `$str`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$reverse`</span> \] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">fromUCallback</span> ( <span
class="methodparam"><span class="type">int</span> `$reason`</span> ,
<span class="methodparam"><span class="type">string</span>
`$source`</span> , <span class="methodparam"><span
class="type">string</span> `$codePoint`</span> , <span
class="methodparam"><span class="type">int</span> `&$error`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">getAliases</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">getAvailable</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getDestinationEncoding</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getDestinationType</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getErrorCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getErrorMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getSourceEncoding</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getSourceType</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">getStandards</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getSubstChars</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">reasonText</span> (\[ <span class="methodparam"><span
class="type">int</span> `$reason`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setDestinationEncoding</span> ( <span
class="methodparam"><span class="type">string</span> `$encoding`</span>
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setSourceEncoding</span> ( <span
class="methodparam"><span class="type">string</span> `$encoding`</span>
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setSubstChars</span> ( <span
class="methodparam"><span class="type">string</span> `$chars`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">toUCallback</span> ( <span
class="methodparam"><span class="type">int</span> `$reason`</span> ,
<span class="methodparam"><span class="type">string</span>
`$source`</span> , <span class="methodparam"><span
class="type">string</span> `$codeUnits`</span> , <span
class="methodparam"><span class="type">int</span> `&$error`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">transcode</span> ( <span class="methodparam"><span
class="type">string</span> `$str`</span> , <span
class="methodparam"><span class="type">string</span>
`$toEncoding`</span> , <span class="methodparam"><span
class="type">string</span> `$fromEncoding`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`</span> \]
)

}

预定义常量
----------

**`UConverter::REASON_UNASSIGNED`**  

**`UConverter::REASON_ILLEGAL`**  

**`UConverter::REASON_IRREGULAR`**  

**`UConverter::REASON_RESET`**  

**`UConverter::REASON_CLOSE`**  

**`UConverter::REASON_CLONE`**  

**`UConverter::UNSUPPORTED_CONVERTER`**  

**`UConverter::SBCS`**  

**`UConverter::DBCS`**  

**`UConverter::MBCS`**  

**`UConverter::LATIN_1`**  

**`UConverter::UTF8`**  

**`UConverter::UTF16_BigEndian`**  

**`UConverter::UTF16_LittleEndian`**  

**`UConverter::UTF32_BigEndian`**  

**`UConverter::UTF32_LittleEndian`**  

**`UConverter::EBCDIC_STATEFUL`**  

**`UConverter::ISO_2022`**  

**`UConverter::LMBCS_1`**  

**`UConverter::LMBCS_2`**  

**`UConverter::LMBCS_3`**  

**`UConverter::LMBCS_4`**  

**`UConverter::LMBCS_5`**  

**`UConverter::LMBCS_6`**  

**`UConverter::LMBCS_8`**  

**`UConverter::LMBCS_11`**  

**`UConverter::LMBCS_16`**  

**`UConverter::LMBCS_17`**  

**`UConverter::LMBCS_18`**  

**`UConverter::LMBCS_19`**  

**`UConverter::LMBCS_LAST`**  

**`UConverter::HZ`**  

**`UConverter::SCSU`**  

**`UConverter::ISCII`**  

**`UConverter::US_ASCII`**  

**`UConverter::UTF7`**  

**`UConverter::BOCU1`**  

**`UConverter::UTF16`**  

**`UConverter::UTF32`**  

**`UConverter::CESU8`**  

**`UConverter::IMAP_MAILBOX`**  

UConverter::\_\_construct
=========================

Create UConverter object

### 说明

<span class="modifier">public</span> <span
class="methodname">UConverter::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span>
`$destination_encoding`</span> \[, <span class="methodparam"><span
class="type">string</span> `$source_encoding`</span> \]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`destination_encoding`  

`source_encoding`  

### 返回值

UConverter::convert
===================

Convert string from one charset to another

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">UConverter::convert</span> ( <span
class="methodparam"><span class="type">string</span> `$str`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$reverse`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`str`  

`reverse`  

### 返回值

UConverter::fromUCallback
=========================

Default "from" callback function

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">UConverter::fromUCallback</span> ( <span
class="methodparam"><span class="type">int</span> `$reason`</span> ,
<span class="methodparam"><span class="type">string</span>
`$source`</span> , <span class="methodparam"><span
class="type">string</span> `$codePoint`</span> , <span
class="methodparam"><span class="type">int</span> `&$error`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`reason`  

`source`  

`codePoint`  

`error`  

### 返回值

UConverter::getAliases
======================

Get the aliases of the given name

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">UConverter::getAliases</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  

### 返回值

UConverter::getAvailable
========================

Get the available canonical converter names

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">UConverter::getAvailable</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

UConverter::getDestinationEncoding
==================================

Get the destination encoding

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">UConverter::getDestinationEncoding</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

UConverter::getDestinationType
==============================

Get the destination converter type

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">UConverter::getDestinationType</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

UConverter::getErrorCode
========================

intl\_get\_error\_code
======================

Get last error code on the object

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">UConverter::getErrorCode</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

UConverter::getErrorMessage
===========================

Get last error message on the object

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">UConverter::getErrorMessage</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

UConverter::getSourceEncoding
=============================

Get the source encoding

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">UConverter::getSourceEncoding</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

UConverter::getSourceType
=========================

Get the source converter type

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">UConverter::getSourceType</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

UConverter::getStandards
========================

Get standards associated to converter names

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">UConverter::getStandards</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

UConverter::getSubstChars
=========================

Get substitution chars

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">UConverter::getSubstChars</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

UConverter::reasonText
======================

Get string representation of the callback reason

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">UConverter::reasonText</span> (\[ <span
class="methodparam"><span class="type">int</span> `$reason`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`reason`  

### 返回值

UConverter::setDestinationEncoding
==================================

Set the destination encoding

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">UConverter::setDestinationEncoding</span> (
<span class="methodparam"><span class="type">string</span>
`$encoding`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`encoding`  

### 返回值

UConverter::setSourceEncoding
=============================

Set the source encoding

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">UConverter::setSourceEncoding</span> ( <span
class="methodparam"><span class="type">string</span> `$encoding`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`encoding`  

### 返回值

UConverter::setSubstChars
=========================

Set the substitution chars

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">UConverter::setSubstChars</span> ( <span
class="methodparam"><span class="type">string</span> `$chars`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`chars`  

### 返回值

UConverter::toUCallback
=======================

Default "to" callback function

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">UConverter::toUCallback</span> ( <span
class="methodparam"><span class="type">int</span> `$reason`</span> ,
<span class="methodparam"><span class="type">string</span>
`$source`</span> , <span class="methodparam"><span
class="type">string</span> `$codeUnits`</span> , <span
class="methodparam"><span class="type">int</span> `&$error`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`reason`  

`source`  

`codeUnits`  

`error`  

### 返回值

UConverter::transcode
=====================

Convert string from one charset to another

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">UConverter::transcode</span> ( <span
class="methodparam"><span class="type">string</span> `$str`</span> ,
<span class="methodparam"><span class="type">string</span>
`$toEncoding`</span> , <span class="methodparam"><span
class="type">string</span> `$fromEncoding`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`</span> \]
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`str`  

`toEncoding`  

`fromEncoding`  

`options`  

### 返回值

简介
----

<span class="classname">IntlChar</span> provides access to a number of
utility methods that can be used to access information about Unicode
characters.

The methods and constants adhere closely to the names and behavior used
by the underlying ICU library.

类摘要
------

**IntlChar**

<span class="ooclass"> class **IntlChar** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">string</span>
`IntlChar::UNICODE_VERSION` <span class="initializer"> = 6.3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CODEPOINT_MIN` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CODEPOINT_MAX` <span class="initializer"> = 1114111</span> ;

<span class="modifier">const</span> <span class="type">float</span>
`IntlChar::NO_NUMERIC_VALUE` <span class="initializer"> =
-123456789</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_ALPHABETIC` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_BINARY_START` <span class="initializer"> = 0</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_ASCII_HEX_DIGIT` <span class="initializer"> =
1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_BIDI_CONTROL` <span class="initializer"> = 2</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_BIDI_MIRRORED` <span class="initializer"> = 3</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_DASH` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_DEFAULT_IGNORABLE_CODE_POINT` <span
class="initializer"> = 5</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_DEPRECATED` <span class="initializer"> = 6</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_DIACRITIC` <span class="initializer"> = 7</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_EXTENDER` <span class="initializer"> = 8</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_FULL_COMPOSITION_EXCLUSION` <span
class="initializer"> = 9</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_GRAPHEME_BASE` <span class="initializer"> =
10</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_GRAPHEME_EXTEND` <span class="initializer"> =
11</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_GRAPHEME_LINK` <span class="initializer"> =
12</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_HEX_DIGIT` <span class="initializer"> = 13</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_HYPHEN` <span class="initializer"> = 14</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_ID_CONTINUE` <span class="initializer"> = 15</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_ID_START` <span class="initializer"> = 16</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_IDEOGRAPHIC` <span class="initializer"> = 17</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_IDS_BINARY_OPERATOR` <span class="initializer"> =
18</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_IDS_TRINARY_OPERATOR` <span class="initializer"> =
19</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_JOIN_CONTROL` <span class="initializer"> = 20</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_LOGICAL_ORDER_EXCEPTION` <span class="initializer">
= 21</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_LOWERCASE` <span class="initializer"> = 22</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_MATH` <span class="initializer"> = 23</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_NONCHARACTER_CODE_POINT` <span class="initializer">
= 24</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_QUOTATION_MARK` <span class="initializer"> =
25</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_RADICAL` <span class="initializer"> = 26</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_SOFT_DOTTED` <span class="initializer"> = 27</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_TERMINAL_PUNCTUATION` <span class="initializer"> =
28</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_UNIFIED_IDEOGRAPH` <span class="initializer"> =
29</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_UPPERCASE` <span class="initializer"> = 30</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_WHITE_SPACE` <span class="initializer"> = 31</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_XID_CONTINUE` <span class="initializer"> = 32</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_XID_START` <span class="initializer"> = 33</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_CASE_SENSITIVE` <span class="initializer"> =
34</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_S_TERM` <span class="initializer"> = 35</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_VARIATION_SELECTOR` <span class="initializer"> =
36</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_NFD_INERT` <span class="initializer"> = 37</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_NFKD_INERT` <span class="initializer"> = 38</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_NFC_INERT` <span class="initializer"> = 39</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_NFKC_INERT` <span class="initializer"> = 40</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_SEGMENT_STARTER` <span class="initializer"> =
41</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_PATTERN_SYNTAX` <span class="initializer"> =
42</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_PATTERN_WHITE_SPACE` <span class="initializer"> =
43</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_POSIX_ALNUM` <span class="initializer"> = 44</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_POSIX_BLANK` <span class="initializer"> = 45</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_POSIX_GRAPH` <span class="initializer"> = 46</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_POSIX_PRINT` <span class="initializer"> = 47</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_POSIX_XDIGIT` <span class="initializer"> = 48</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_CASED` <span class="initializer"> = 49</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_CASE_IGNORABLE` <span class="initializer"> =
50</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_CHANGES_WHEN_LOWERCASED` <span class="initializer">
= 51</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_CHANGES_WHEN_UPPERCASED` <span class="initializer">
= 52</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_CHANGES_WHEN_TITLECASED` <span class="initializer">
= 53</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_CHANGES_WHEN_CASEFOLDED` <span class="initializer">
= 54</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_CHANGES_WHEN_CASEMAPPED` <span class="initializer">
= 55</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_CHANGES_WHEN_NFKC_CASEFOLDED` <span
class="initializer"> = 56</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_BINARY_LIMIT` <span class="initializer"> = 57</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_BIDI_CLASS` <span class="initializer"> = 4096</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_INT_START` <span class="initializer"> = 4096</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_BLOCK` <span class="initializer"> = 4097</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_CANONICAL_COMBINING_CLASS` <span
class="initializer"> = 4098</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_DECOMPOSITION_TYPE` <span class="initializer"> =
4099</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_EAST_ASIAN_WIDTH` <span class="initializer"> =
4100</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_GENERAL_CATEGORY` <span class="initializer"> =
4101</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_JOINING_GROUP` <span class="initializer"> =
4102</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_JOINING_TYPE` <span class="initializer"> =
4103</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_LINE_BREAK` <span class="initializer"> = 4104</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_NUMERIC_TYPE` <span class="initializer"> =
4105</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_SCRIPT` <span class="initializer"> = 4106</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_HANGUL_SYLLABLE_TYPE` <span class="initializer"> =
4107</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_NFD_QUICK_CHECK` <span class="initializer"> =
4108</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_NFKD_QUICK_CHECK` <span class="initializer"> =
4109</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_NFC_QUICK_CHECK` <span class="initializer"> =
4110</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_NFKC_QUICK_CHECK` <span class="initializer"> =
4111</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_LEAD_CANONICAL_COMBINING_CLASS` <span
class="initializer"> = 4112</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_TRAIL_CANONICAL_COMBINING_CLASS` <span
class="initializer"> = 4113</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_GRAPHEME_CLUSTER_BREAK` <span class="initializer"> =
4114</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_SENTENCE_BREAK` <span class="initializer"> =
4115</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_WORD_BREAK` <span class="initializer"> = 4116</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_BIDI_PAIRED_BRACKET_TYPE` <span class="initializer">
= 4117</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_INT_LIMIT` <span class="initializer"> = 4118</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_GENERAL_CATEGORY_MASK` <span class="initializer"> =
8192</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_MASK_START` <span class="initializer"> = 8192</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_MASK_LIMIT` <span class="initializer"> = 8193</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_NUMERIC_VALUE` <span class="initializer"> =
12288</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_DOUBLE_START` <span class="initializer"> =
12288</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_DOUBLE_LIMIT` <span class="initializer"> =
12289</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_AGE` <span class="initializer"> = 16384</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_STRING_START` <span class="initializer"> =
16384</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_BIDI_MIRRORING_GLYPH` <span class="initializer"> =
16385</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_CASE_FOLDING` <span class="initializer"> =
16386</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_ISO_COMMENT` <span class="initializer"> =
16387</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_LOWERCASE_MAPPING` <span class="initializer"> =
16388</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_NAME` <span class="initializer"> = 16389</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_SIMPLE_CASE_FOLDING` <span class="initializer"> =
16390</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_SIMPLE_LOWERCASE_MAPPING` <span class="initializer">
= 16391</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_SIMPLE_TITLECASE_MAPPING` <span class="initializer">
= 16392</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_SIMPLE_UPPERCASE_MAPPING` <span class="initializer">
= 16393</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_TITLECASE_MAPPING` <span class="initializer"> =
16394</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_UNICODE_1_NAME` <span class="initializer"> =
16395</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_UPPERCASE_MAPPING` <span class="initializer"> =
16396</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_BIDI_PAIRED_BRACKET` <span class="initializer"> =
16397</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_STRING_LIMIT` <span class="initializer"> =
16398</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_SCRIPT_EXTENSIONS` <span class="initializer"> =
28672</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_OTHER_PROPERTY_START` <span class="initializer"> =
28672</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_OTHER_PROPERTY_LIMIT` <span class="initializer"> =
28673</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_INVALID_CODE` <span class="initializer"> = -1</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_CATEGORY_UNASSIGNED` <span class="initializer"> =
0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_CATEGORY_GENERAL_OTHER_TYPES` <span class="initializer">
= 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_CATEGORY_UPPERCASE_LETTER` <span class="initializer"> =
1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_CATEGORY_LOWERCASE_LETTER` <span class="initializer"> =
2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_CATEGORY_TITLECASE_LETTER` <span class="initializer"> =
3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_CATEGORY_MODIFIER_LETTER` <span class="initializer"> =
4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_CATEGORY_OTHER_LETTER` <span class="initializer"> =
5</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_CATEGORY_NON_SPACING_MARK` <span class="initializer"> =
6</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_CATEGORY_ENCLOSING_MARK` <span class="initializer"> =
7</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_CATEGORY_COMBINING_SPACING_MARK` <span
class="initializer"> = 8</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_CATEGORY_DECIMAL_DIGIT_NUMBER` <span
class="initializer"> = 9</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_CATEGORY_LETTER_NUMBER` <span class="initializer"> =
10</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_CATEGORY_OTHER_NUMBER` <span class="initializer"> =
11</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_CATEGORY_SPACE_SEPARATOR` <span class="initializer"> =
12</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_CATEGORY_LINE_SEPARATOR` <span class="initializer"> =
13</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_CATEGORY_PARAGRAPH_SEPARATOR` <span class="initializer">
= 14</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_CATEGORY_CONTROL_CHAR` <span class="initializer"> =
15</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_CATEGORY_FORMAT_CHAR` <span class="initializer"> =
16</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_CATEGORY_PRIVATE_USE_CHAR` <span class="initializer"> =
17</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_CATEGORY_SURROGATE` <span class="initializer"> =
18</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_CATEGORY_DASH_PUNCTUATION` <span class="initializer"> =
19</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_CATEGORY_START_PUNCTUATION` <span class="initializer"> =
20</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_CATEGORY_END_PUNCTUATION` <span class="initializer"> =
21</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_CATEGORY_CONNECTOR_PUNCTUATION` <span
class="initializer"> = 22</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_CATEGORY_OTHER_PUNCTUATION` <span class="initializer"> =
23</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_CATEGORY_MATH_SYMBOL` <span class="initializer"> =
24</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_CATEGORY_CURRENCY_SYMBOL` <span class="initializer"> =
25</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_CATEGORY_MODIFIER_SYMBOL` <span class="initializer"> =
26</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_CATEGORY_OTHER_SYMBOL` <span class="initializer"> =
27</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_CATEGORY_INITIAL_PUNCTUATION` <span class="initializer">
= 28</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_CATEGORY_FINAL_PUNCTUATION` <span class="initializer"> =
29</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_CATEGORY_CHAR_CATEGORY_COUNT` <span class="initializer">
= 30</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_DIRECTION_LEFT_TO_RIGHT` <span class="initializer"> =
0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT` <span class="initializer"> =
1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_DIRECTION_EUROPEAN_NUMBER` <span class="initializer"> =
2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_DIRECTION_EUROPEAN_NUMBER_SEPARATOR` <span
class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_DIRECTION_EUROPEAN_NUMBER_TERMINATOR` <span
class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_DIRECTION_ARABIC_NUMBER` <span class="initializer"> =
5</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_DIRECTION_COMMON_NUMBER_SEPARATOR` <span
class="initializer"> = 6</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_DIRECTION_BLOCK_SEPARATOR` <span class="initializer"> =
7</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_DIRECTION_SEGMENT_SEPARATOR` <span class="initializer">
= 8</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_DIRECTION_WHITE_SPACE_NEUTRAL` <span
class="initializer"> = 9</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_DIRECTION_OTHER_NEUTRAL` <span class="initializer"> =
10</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_DIRECTION_LEFT_TO_RIGHT_EMBEDDING` <span
class="initializer"> = 11</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_DIRECTION_LEFT_TO_RIGHT_OVERRIDE` <span
class="initializer"> = 12</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT_ARABIC` <span
class="initializer"> = 13</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT_EMBEDDING` <span
class="initializer"> = 14</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT_OVERRIDE` <span
class="initializer"> = 15</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_DIRECTION_POP_DIRECTIONAL_FORMAT` <span
class="initializer"> = 16</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_DIRECTION_DIR_NON_SPACING_MARK` <span
class="initializer"> = 17</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_DIRECTION_BOUNDARY_NEUTRAL` <span class="initializer"> =
18</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_DIRECTION_FIRST_STRONG_ISOLATE` <span
class="initializer"> = 19</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_DIRECTION_LEFT_TO_RIGHT_ISOLATE` <span
class="initializer"> = 20</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT_ISOLATE` <span
class="initializer"> = 21</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_DIRECTION_POP_DIRECTIONAL_ISOLATE` <span
class="initializer"> = 22</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_DIRECTION_CHAR_DIRECTION_COUNT` <span
class="initializer"> = 23</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_NO_BLOCK` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_BASIC_LATIN` <span class="initializer"> = 1</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_LATIN_1_SUPPLEMENT` <span class="initializer"> =
2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_LATIN_EXTENDED_A` <span class="initializer"> =
3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_LATIN_EXTENDED_B` <span class="initializer"> =
4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_IPA_EXTENSIONS` <span class="initializer"> =
5</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_SPACING_MODIFIER_LETTERS` <span
class="initializer"> = 6</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_COMBINING_DIACRITICAL_MARKS` <span
class="initializer"> = 7</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_GREEK` <span class="initializer"> = 8</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_CYRILLIC` <span class="initializer"> = 9</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_ARMENIAN` <span class="initializer"> = 10</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_HEBREW` <span class="initializer"> = 11</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_ARABIC` <span class="initializer"> = 12</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_SYRIAC` <span class="initializer"> = 13</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_THAANA` <span class="initializer"> = 14</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_DEVANAGARI` <span class="initializer"> = 15</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_BENGALI` <span class="initializer"> = 16</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_GURMUKHI` <span class="initializer"> = 17</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_GUJARATI` <span class="initializer"> = 18</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_ORIYA` <span class="initializer"> = 19</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_TAMIL` <span class="initializer"> = 20</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_TELUGU` <span class="initializer"> = 21</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_KANNADA` <span class="initializer"> = 22</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_MALAYALAM` <span class="initializer"> = 23</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_SINHALA` <span class="initializer"> = 24</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_THAI` <span class="initializer"> = 25</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_LAO` <span class="initializer"> = 26</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_TIBETAN` <span class="initializer"> = 27</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_MYANMAR` <span class="initializer"> = 28</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_GEORGIAN` <span class="initializer"> = 29</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_HANGUL_JAMO` <span class="initializer"> =
30</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_ETHIOPIC` <span class="initializer"> = 31</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_CHEROKEE` <span class="initializer"> = 32</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_UNIFIED_CANADIAN_ABORIGINAL_SYLLABICS` <span
class="initializer"> = 33</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_OGHAM` <span class="initializer"> = 34</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_RUNIC` <span class="initializer"> = 35</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_KHMER` <span class="initializer"> = 36</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_MONGOLIAN` <span class="initializer"> = 37</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_LATIN_EXTENDED_ADDITIONAL` <span
class="initializer"> = 38</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_GREEK_EXTENDED` <span class="initializer"> =
39</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_GENERAL_PUNCTUATION` <span class="initializer"> =
40</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_SUPERSCRIPTS_AND_SUBSCRIPTS` <span
class="initializer"> = 41</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_CURRENCY_SYMBOLS` <span class="initializer"> =
42</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_COMBINING_MARKS_FOR_SYMBOLS` <span
class="initializer"> = 43</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_LETTERLIKE_SYMBOLS` <span class="initializer"> =
44</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_NUMBER_FORMS` <span class="initializer"> =
45</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_ARROWS` <span class="initializer"> = 46</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_MATHEMATICAL_OPERATORS` <span class="initializer">
= 47</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_MISCELLANEOUS_TECHNICAL` <span
class="initializer"> = 48</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_CONTROL_PICTURES` <span class="initializer"> =
49</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_OPTICAL_CHARACTER_RECOGNITION` <span
class="initializer"> = 50</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_ENCLOSED_ALPHANUMERICS` <span class="initializer">
= 51</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_BOX_DRAWING` <span class="initializer"> =
52</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_BLOCK_ELEMENTS` <span class="initializer"> =
53</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_GEOMETRIC_SHAPES` <span class="initializer"> =
54</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_MISCELLANEOUS_SYMBOLS` <span class="initializer">
= 55</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_DINGBATS` <span class="initializer"> = 56</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_BRAILLE_PATTERNS` <span class="initializer"> =
57</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_CJK_RADICALS_SUPPLEMENT` <span
class="initializer"> = 58</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_KANGXI_RADICALS` <span class="initializer"> =
59</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_IDEOGRAPHIC_DESCRIPTION_CHARACTERS` <span
class="initializer"> = 60</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_CJK_SYMBOLS_AND_PUNCTUATION` <span
class="initializer"> = 61</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_HIRAGANA` <span class="initializer"> = 62</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_KATAKANA` <span class="initializer"> = 63</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_BOPOMOFO` <span class="initializer"> = 64</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_HANGUL_COMPATIBILITY_JAMO` <span
class="initializer"> = 65</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_KANBUN` <span class="initializer"> = 66</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_BOPOMOFO_EXTENDED` <span class="initializer"> =
67</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_ENCLOSED_CJK_LETTERS_AND_MONTHS` <span
class="initializer"> = 68</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_CJK_COMPATIBILITY` <span class="initializer"> =
69</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_CJK_UNIFIED_IDEOGRAPHS_EXTENSION_A` <span
class="initializer"> = 70</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_CJK_UNIFIED_IDEOGRAPHS` <span class="initializer">
= 71</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_YI_SYLLABLES` <span class="initializer"> =
72</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_YI_RADICALS` <span class="initializer"> =
73</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_HANGUL_SYLLABLES` <span class="initializer"> =
74</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_HIGH_SURROGATES` <span class="initializer"> =
75</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_HIGH_PRIVATE_USE_SURROGATES` <span
class="initializer"> = 76</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_LOW_SURROGATES` <span class="initializer"> =
77</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_PRIVATE_USE_AREA` <span class="initializer"> =
78</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_PRIVATE_USE` <span class="initializer"> =
78</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_CJK_COMPATIBILITY_IDEOGRAPHS` <span
class="initializer"> = 79</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_ALPHABETIC_PRESENTATION_FORMS` <span
class="initializer"> = 80</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_ARABIC_PRESENTATION_FORMS_A` <span
class="initializer"> = 81</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_COMBINING_HALF_MARKS` <span class="initializer"> =
82</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_CJK_COMPATIBILITY_FORMS` <span
class="initializer"> = 83</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_SMALL_FORM_VARIANTS` <span class="initializer"> =
84</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_ARABIC_PRESENTATION_FORMS_B` <span
class="initializer"> = 85</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_SPECIALS` <span class="initializer"> = 86</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_HALFWIDTH_AND_FULLWIDTH_FORMS` <span
class="initializer"> = 87</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_OLD_ITALIC` <span class="initializer"> = 88</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_GOTHIC` <span class="initializer"> = 89</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_DESERET` <span class="initializer"> = 90</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_BYZANTINE_MUSICAL_SYMBOLS` <span
class="initializer"> = 91</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_MUSICAL_SYMBOLS` <span class="initializer"> =
92</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_MATHEMATICAL_ALPHANUMERIC_SYMBOLS` <span
class="initializer"> = 93</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_CJK_UNIFIED_IDEOGRAPHS_EXTENSION_B` <span
class="initializer"> = 94</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_CJK_COMPATIBILITY_IDEOGRAPHS_SUPPLEMENT` <span
class="initializer"> = 95</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_TAGS` <span class="initializer"> = 96</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_CYRILLIC_SUPPLEMENT` <span class="initializer"> =
97</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_CYRILLIC_SUPPLEMENTARY` <span class="initializer">
= 97</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_TAGALOG` <span class="initializer"> = 98</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_HANUNOO` <span class="initializer"> = 99</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_BUHID` <span class="initializer"> = 100</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_TAGBANWA` <span class="initializer"> = 101</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_MISCELLANEOUS_MATHEMATICAL_SYMBOLS_A` <span
class="initializer"> = 102</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_SUPPLEMENTAL_ARROWS_A` <span class="initializer">
= 103</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_SUPPLEMENTAL_ARROWS_B` <span class="initializer">
= 104</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_MISCELLANEOUS_MATHEMATICAL_SYMBOLS_B` <span
class="initializer"> = 105</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_SUPPLEMENTAL_MATHEMATICAL_OPERATORS` <span
class="initializer"> = 106</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_KATAKANA_PHONETIC_EXTENSIONS` <span
class="initializer"> = 107</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_VARIATION_SELECTORS` <span class="initializer"> =
108</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_SUPPLEMENTARY_PRIVATE_USE_AREA_A` <span
class="initializer"> = 109</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_SUPPLEMENTARY_PRIVATE_USE_AREA_B` <span
class="initializer"> = 110</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_LIMBU` <span class="initializer"> = 111</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_TAI_LE` <span class="initializer"> = 112</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_KHMER_SYMBOLS` <span class="initializer"> =
113</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_PHONETIC_EXTENSIONS` <span class="initializer"> =
114</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_MISCELLANEOUS_SYMBOLS_AND_ARROWS` <span
class="initializer"> = 115</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_YIJING_HEXAGRAM_SYMBOLS` <span
class="initializer"> = 116</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_LINEAR_B_SYLLABARY` <span class="initializer"> =
117</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_LINEAR_B_IDEOGRAMS` <span class="initializer"> =
118</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_AEGEAN_NUMBERS` <span class="initializer"> =
119</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_UGARITIC` <span class="initializer"> = 120</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_SHAVIAN` <span class="initializer"> = 121</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_OSMANYA` <span class="initializer"> = 122</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_CYPRIOT_SYLLABARY` <span class="initializer"> =
123</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_TAI_XUAN_JING_SYMBOLS` <span class="initializer">
= 124</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_VARIATION_SELECTORS_SUPPLEMENT` <span
class="initializer"> = 125</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_ANCIENT_GREEK_MUSICAL_NOTATION` <span
class="initializer"> = 126</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_ANCIENT_GREEK_NUMBERS` <span class="initializer">
= 127</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_ARABIC_SUPPLEMENT` <span class="initializer"> =
128</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_BUGINESE` <span class="initializer"> = 129</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_CJK_STROKES` <span class="initializer"> =
130</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_COMBINING_DIACRITICAL_MARKS_SUPPLEMENT` <span
class="initializer"> = 131</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_COPTIC` <span class="initializer"> = 132</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_ETHIOPIC_EXTENDED` <span class="initializer"> =
133</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_ETHIOPIC_SUPPLEMENT` <span class="initializer"> =
134</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_GEORGIAN_SUPPLEMENT` <span class="initializer"> =
135</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_GLAGOLITIC` <span class="initializer"> =
136</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_KHAROSHTHI` <span class="initializer"> =
137</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_MODIFIER_TONE_LETTERS` <span class="initializer">
= 138</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_NEW_TAI_LUE` <span class="initializer"> =
139</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_OLD_PERSIAN` <span class="initializer"> =
140</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_PHONETIC_EXTENSIONS_SUPPLEMENT` <span
class="initializer"> = 141</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_SUPPLEMENTAL_PUNCTUATION` <span
class="initializer"> = 142</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_SYLOTI_NAGRI` <span class="initializer"> =
143</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_TIFINAGH` <span class="initializer"> = 144</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_VERTICAL_FORMS` <span class="initializer"> =
145</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_NKO` <span class="initializer"> = 146</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_BALINESE` <span class="initializer"> = 147</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_LATIN_EXTENDED_C` <span class="initializer"> =
148</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_LATIN_EXTENDED_D` <span class="initializer"> =
149</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_PHAGS_PA` <span class="initializer"> = 150</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_PHOENICIAN` <span class="initializer"> =
151</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_CUNEIFORM` <span class="initializer"> = 152</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_CUNEIFORM_NUMBERS_AND_PUNCTUATION` <span
class="initializer"> = 153</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_COUNTING_ROD_NUMERALS` <span class="initializer">
= 154</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_SUNDANESE` <span class="initializer"> = 155</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_LEPCHA` <span class="initializer"> = 156</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_OL_CHIKI` <span class="initializer"> = 157</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_CYRILLIC_EXTENDED_A` <span class="initializer"> =
158</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_VAI` <span class="initializer"> = 159</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_CYRILLIC_EXTENDED_B` <span class="initializer"> =
160</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_SAURASHTRA` <span class="initializer"> =
161</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_KAYAH_LI` <span class="initializer"> = 162</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_REJANG` <span class="initializer"> = 163</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_CHAM` <span class="initializer"> = 164</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_ANCIENT_SYMBOLS` <span class="initializer"> =
165</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_PHAISTOS_DISC` <span class="initializer"> =
166</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_LYCIAN` <span class="initializer"> = 167</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_CARIAN` <span class="initializer"> = 168</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_LYDIAN` <span class="initializer"> = 169</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_MAHJONG_TILES` <span class="initializer"> =
170</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_DOMINO_TILES` <span class="initializer"> =
171</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_SAMARITAN` <span class="initializer"> = 172</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_UNIFIED_CANADIAN_ABORIGINAL_SYLLABICS_EXTENDED`
<span class="initializer"> = 173</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_TAI_THAM` <span class="initializer"> = 174</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_VEDIC_EXTENSIONS` <span class="initializer"> =
175</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_LISU` <span class="initializer"> = 176</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_BAMUM` <span class="initializer"> = 177</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_COMMON_INDIC_NUMBER_FORMS` <span
class="initializer"> = 178</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_DEVANAGARI_EXTENDED` <span class="initializer"> =
179</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_HANGUL_JAMO_EXTENDED_A` <span class="initializer">
= 180</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_JAVANESE` <span class="initializer"> = 181</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_MYANMAR_EXTENDED_A` <span class="initializer"> =
182</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_TAI_VIET` <span class="initializer"> = 183</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_MEETEI_MAYEK` <span class="initializer"> =
184</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_HANGUL_JAMO_EXTENDED_B` <span class="initializer">
= 185</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_IMPERIAL_ARAMAIC` <span class="initializer"> =
186</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_OLD_SOUTH_ARABIAN` <span class="initializer"> =
187</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_AVESTAN` <span class="initializer"> = 188</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_INSCRIPTIONAL_PARTHIAN` <span class="initializer">
= 189</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_INSCRIPTIONAL_PAHLAVI` <span class="initializer">
= 190</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_OLD_TURKIC` <span class="initializer"> =
191</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_RUMI_NUMERAL_SYMBOLS` <span class="initializer"> =
192</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_KAITHI` <span class="initializer"> = 193</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_EGYPTIAN_HIEROGLYPHS` <span class="initializer"> =
194</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_ENCLOSED_ALPHANUMERIC_SUPPLEMENT` <span
class="initializer"> = 195</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_ENCLOSED_IDEOGRAPHIC_SUPPLEMENT` <span
class="initializer"> = 196</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_CJK_UNIFIED_IDEOGRAPHS_EXTENSION_C` <span
class="initializer"> = 197</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_MANDAIC` <span class="initializer"> = 198</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_BATAK` <span class="initializer"> = 199</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_ETHIOPIC_EXTENDED_A` <span class="initializer"> =
200</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_BRAHMI` <span class="initializer"> = 201</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_BAMUM_SUPPLEMENT` <span class="initializer"> =
202</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_KANA_SUPPLEMENT` <span class="initializer"> =
203</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_PLAYING_CARDS` <span class="initializer"> =
204</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_MISCELLANEOUS_SYMBOLS_AND_PICTOGRAPHS` <span
class="initializer"> = 205</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_EMOTICONS` <span class="initializer"> = 206</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_TRANSPORT_AND_MAP_SYMBOLS` <span
class="initializer"> = 207</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_ALCHEMICAL_SYMBOLS` <span class="initializer"> =
208</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_CJK_UNIFIED_IDEOGRAPHS_EXTENSION_D` <span
class="initializer"> = 209</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_ARABIC_EXTENDED_A` <span class="initializer"> =
210</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_ARABIC_MATHEMATICAL_ALPHABETIC_SYMBOLS` <span
class="initializer"> = 211</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_CHAKMA` <span class="initializer"> = 212</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_MEETEI_MAYEK_EXTENSIONS` <span
class="initializer"> = 213</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_MEROITIC_CURSIVE` <span class="initializer"> =
214</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_MEROITIC_HIEROGLYPHS` <span class="initializer"> =
215</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_MIAO` <span class="initializer"> = 216</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_SHARADA` <span class="initializer"> = 217</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_SORA_SOMPENG` <span class="initializer"> =
218</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_SUNDANESE_SUPPLEMENT` <span class="initializer"> =
219</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_TAKRI` <span class="initializer"> = 220</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_COUNT` <span class="initializer"> = 221</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BLOCK_CODE_INVALID_CODE` <span class="initializer"> =
-1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BPT_NONE` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BPT_OPEN` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BPT_CLOSE` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::BPT_COUNT` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::EA_NEUTRAL` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::EA_AMBIGUOUS` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::EA_HALFWIDTH` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::EA_FULLWIDTH` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::EA_NARROW` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::EA_WIDE` <span class="initializer"> = 5</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::EA_COUNT` <span class="initializer"> = 6</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::UNICODE_CHAR_NAME` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::UNICODE_10_CHAR_NAME` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::EXTENDED_CHAR_NAME` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_NAME_ALIAS` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::CHAR_NAME_CHOICE_COUNT` <span class="initializer"> = 4</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::SHORT_PROPERTY_NAME` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LONG_PROPERTY_NAME` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::PROPERTY_NAME_CHOICE_COUNT` <span class="initializer"> =
2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::DT_NONE` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::DT_CANONICAL` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::DT_COMPAT` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::DT_CIRCLE` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::DT_FINAL` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::DT_FONT` <span class="initializer"> = 5</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::DT_FRACTION` <span class="initializer"> = 6</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::DT_INITIAL` <span class="initializer"> = 7</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::DT_ISOLATED` <span class="initializer"> = 8</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::DT_MEDIAL` <span class="initializer"> = 9</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::DT_NARROW` <span class="initializer"> = 10</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::DT_NOBREAK` <span class="initializer"> = 11</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::DT_SMALL` <span class="initializer"> = 12</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::DT_SQUARE` <span class="initializer"> = 13</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::DT_SUB` <span class="initializer"> = 14</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::DT_SUPER` <span class="initializer"> = 15</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::DT_VERTICAL` <span class="initializer"> = 16</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::DT_WIDE` <span class="initializer"> = 17</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::DT_COUNT` <span class="initializer"> = 18</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JT_NON_JOINING` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JT_JOIN_CAUSING` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JT_DUAL_JOINING` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JT_LEFT_JOINING` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JT_RIGHT_JOINING` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JT_TRANSPARENT` <span class="initializer"> = 5</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JT_COUNT` <span class="initializer"> = 6</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_NO_JOINING_GROUP` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_AIN` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_ALAPH` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_ALEF` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_BEH` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_BETH` <span class="initializer"> = 5</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_DAL` <span class="initializer"> = 6</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_DALATH_RISH` <span class="initializer"> = 7</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_E` <span class="initializer"> = 8</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_FEH` <span class="initializer"> = 9</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_FINAL_SEMKATH` <span class="initializer"> = 10</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_GAF` <span class="initializer"> = 11</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_GAMAL` <span class="initializer"> = 12</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_HAH` <span class="initializer"> = 13</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_TEH_MARBUTA_GOAL` <span class="initializer"> = 14</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_HAMZA_ON_HEH_GOAL` <span class="initializer"> = 14</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_HE` <span class="initializer"> = 15</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_HEH` <span class="initializer"> = 16</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_HEH_GOAL` <span class="initializer"> = 17</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_HETH` <span class="initializer"> = 18</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_KAF` <span class="initializer"> = 19</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_KAPH` <span class="initializer"> = 20</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_KNOTTED_HEH` <span class="initializer"> = 21</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_LAM` <span class="initializer"> = 22</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_LAMADH` <span class="initializer"> = 23</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_MEEM` <span class="initializer"> = 24</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_MIM` <span class="initializer"> = 25</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_NOON` <span class="initializer"> = 26</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_NUN` <span class="initializer"> = 27</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_PE` <span class="initializer"> = 28</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_QAF` <span class="initializer"> = 29</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_QAPH` <span class="initializer"> = 30</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_REH` <span class="initializer"> = 31</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_REVERSED_PE` <span class="initializer"> = 32</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_SAD` <span class="initializer"> = 33</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_SADHE` <span class="initializer"> = 34</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_SEEN` <span class="initializer"> = 35</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_SEMKATH` <span class="initializer"> = 36</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_SHIN` <span class="initializer"> = 37</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_SWASH_KAF` <span class="initializer"> = 38</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_SYRIAC_WAW` <span class="initializer"> = 39</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_TAH` <span class="initializer"> = 40</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_TAW` <span class="initializer"> = 41</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_TEH_MARBUTA` <span class="initializer"> = 42</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_TETH` <span class="initializer"> = 43</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_WAW` <span class="initializer"> = 44</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_YEH` <span class="initializer"> = 45</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_YEH_BARREE` <span class="initializer"> = 46</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_YEH_WITH_TAIL` <span class="initializer"> = 47</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_YUDH` <span class="initializer"> = 48</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_YUDH_HE` <span class="initializer"> = 49</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_ZAIN` <span class="initializer"> = 50</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_FE` <span class="initializer"> = 51</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_KHAPH` <span class="initializer"> = 52</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_ZHAIN` <span class="initializer"> = 53</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_BURUSHASKI_YEH_BARREE` <span class="initializer"> =
54</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_FARSI_YEH` <span class="initializer"> = 55</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_NYA` <span class="initializer"> = 56</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_ROHINGYA_YEH` <span class="initializer"> = 57</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::JG_COUNT` <span class="initializer"> = 58</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::GCB_OTHER` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::GCB_CONTROL` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::GCB_CR` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::GCB_EXTEND` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::GCB_L` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::GCB_LF` <span class="initializer"> = 5</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::GCB_LV` <span class="initializer"> = 6</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::GCB_LVT` <span class="initializer"> = 7</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::GCB_T` <span class="initializer"> = 8</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::GCB_V` <span class="initializer"> = 9</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::GCB_SPACING_MARK` <span class="initializer"> = 10</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::GCB_PREPEND` <span class="initializer"> = 11</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::GCB_REGIONAL_INDICATOR` <span class="initializer"> =
12</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::GCB_COUNT` <span class="initializer"> = 13</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::WB_OTHER` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::WB_ALETTER` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::WB_FORMAT` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::WB_KATAKANA` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::WB_MIDLETTER` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::WB_MIDNUM` <span class="initializer"> = 5</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::WB_NUMERIC` <span class="initializer"> = 6</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::WB_EXTENDNUMLET` <span class="initializer"> = 7</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::WB_CR` <span class="initializer"> = 8</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::WB_EXTEND` <span class="initializer"> = 9</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::WB_LF` <span class="initializer"> = 10</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::WB_MIDNUMLET` <span class="initializer"> = 11</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::WB_NEWLINE` <span class="initializer"> = 12</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::WB_REGIONAL_INDICATOR` <span class="initializer"> = 13</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::WB_HEBREW_LETTER` <span class="initializer"> = 14</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::WB_SINGLE_QUOTE` <span class="initializer"> = 15</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::WB_DOUBLE_QUOTE` <span class="initializer"> = 16</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::WB_COUNT` <span class="initializer"> = 17</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::SB_OTHER` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::SB_ATERM` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::SB_CLOSE` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::SB_FORMAT` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::SB_LOWER` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::SB_NUMERIC` <span class="initializer"> = 5</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::SB_OLETTER` <span class="initializer"> = 6</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::SB_SEP` <span class="initializer"> = 7</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::SB_SP` <span class="initializer"> = 8</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::SB_STERM` <span class="initializer"> = 9</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::SB_UPPER` <span class="initializer"> = 10</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::SB_CR` <span class="initializer"> = 11</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::SB_EXTEND` <span class="initializer"> = 12</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::SB_LF` <span class="initializer"> = 13</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::SB_SCONTINUE` <span class="initializer"> = 14</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::SB_COUNT` <span class="initializer"> = 15</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_UNKNOWN` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_AMBIGUOUS` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_ALPHABETIC` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_BREAK_BOTH` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_BREAK_AFTER` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_BREAK_BEFORE` <span class="initializer"> = 5</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_MANDATORY_BREAK` <span class="initializer"> = 6</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_CONTINGENT_BREAK` <span class="initializer"> = 7</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_CLOSE_PUNCTUATION` <span class="initializer"> = 8</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_COMBINING_MARK` <span class="initializer"> = 9</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_CARRIAGE_RETURN` <span class="initializer"> = 10</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_EXCLAMATION` <span class="initializer"> = 11</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_GLUE` <span class="initializer"> = 12</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_HYPHEN` <span class="initializer"> = 13</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_IDEOGRAPHIC` <span class="initializer"> = 14</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_INSEPARABLE` <span class="initializer"> = 15</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_INSEPERABLE` <span class="initializer"> = 15</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_INFIX_NUMERIC` <span class="initializer"> = 16</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_LINE_FEED` <span class="initializer"> = 17</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_NONSTARTER` <span class="initializer"> = 18</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_NUMERIC` <span class="initializer"> = 19</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_OPEN_PUNCTUATION` <span class="initializer"> = 20</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_POSTFIX_NUMERIC` <span class="initializer"> = 21</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_PREFIX_NUMERIC` <span class="initializer"> = 22</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_QUOTATION` <span class="initializer"> = 23</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_COMPLEX_CONTEXT` <span class="initializer"> = 24</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_SURROGATE` <span class="initializer"> = 25</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_SPACE` <span class="initializer"> = 26</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_BREAK_SYMBOLS` <span class="initializer"> = 27</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_ZWSPACE` <span class="initializer"> = 28</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_NEXT_LINE` <span class="initializer"> = 29</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_WORD_JOINER` <span class="initializer"> = 30</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_H2` <span class="initializer"> = 31</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_H3` <span class="initializer"> = 32</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_JL` <span class="initializer"> = 33</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_JT` <span class="initializer"> = 34</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_JV` <span class="initializer"> = 35</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_CLOSE_PARENTHESIS` <span class="initializer"> = 36</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_CONDITIONAL_JAPANESE_STARTER` <span class="initializer"> =
37</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_HEBREW_LETTER` <span class="initializer"> = 38</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_REGIONAL_INDICATOR` <span class="initializer"> = 39</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::LB_COUNT` <span class="initializer"> = 40</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::NT_NONE` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::NT_DECIMAL` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::NT_DIGIT` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::NT_NUMERIC` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::NT_COUNT` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::HST_NOT_APPLICABLE` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::HST_LEADING_JAMO` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::HST_VOWEL_JAMO` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::HST_TRAILING_JAMO` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::HST_LV_SYLLABLE` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::HST_LVT_SYLLABLE` <span class="initializer"> = 5</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`IntlChar::HST_COUNT` <span class="initializer"> = 6</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">charAge</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">charDigitValue</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">charDirection</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">charFromName</span> ( <span class="methodparam"><span
class="type">string</span> `$characterName`</span> \[, <span
class="methodparam"><span class="type">int</span> `$nameChoice`<span
class="initializer"> = **`IntlChar::UNICODE_CHAR_NAME`**</span></span>
\] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">mixed</span> <span
class="methodname">charMirror</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">charName</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> \[, <span
class="methodparam"><span class="type">int</span> `$nameChoice`<span
class="initializer"> = **`IntlChar::UNICODE_CHAR_NAME`**</span></span>
\] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">charType</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">chr</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">digit</span> ( <span class="methodparam"><span
class="type">string</span> `$codepoint`</span> \[, <span
class="methodparam"><span class="type">int</span> `$radix`<span
class="initializer"> = 10</span></span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">enumCharNames</span> ( <span
class="methodparam"><span class="type">mixed</span> `$start`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$limit`</span> , <span class="methodparam"><span
class="type">callable</span> `$callback`</span> \[, <span
class="methodparam"><span class="type">int</span> `$nameChoice`<span
class="initializer"> = **`IntlChar::UNICODE_CHAR_NAME`**</span></span>
\] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">enumCharTypes</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">mixed</span> <span
class="methodname">foldCase</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> \[, <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = **`IntlChar::FOLD_CASE_DEFAULT`**</span></span>
\] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">forDigit</span> ( <span class="methodparam"><span
class="type">int</span> `$digit`</span> \[, <span
class="methodparam"><span class="type">int</span> `$radix`<span
class="initializer"> = 10</span></span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">mixed</span> <span
class="methodname">getBidiPairedBracket</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">getBlockCode</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">getCombiningClass</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">getFC\_NFKC\_Closure</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">getIntPropertyMaxValue</span> ( <span
class="methodparam"><span class="type">int</span> `$property`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">getIntPropertyMinValue</span> ( <span
class="methodparam"><span class="type">int</span> `$property`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">getIntPropertyValue</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
, <span class="methodparam"><span class="type">int</span>
`$property`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">float</span> <span
class="methodname">getNumericValue</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">getPropertyEnum</span> ( <span
class="methodparam"><span class="type">string</span> `$alias`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">getPropertyName</span> ( <span
class="methodparam"><span class="type">int</span> `$property`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$nameChoice`<span class="initializer"> =
**`IntlChar::LONG_PROPERTY_NAME`**</span></span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">getPropertyValueEnum</span> ( <span
class="methodparam"><span class="type">int</span> `$property`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">getPropertyValueName</span> ( <span
class="methodparam"><span class="type">int</span> `$property`</span> ,
<span class="methodparam"><span class="type">int</span> `$value`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$nameChoice`<span class="initializer"> =
**`IntlChar::LONG_PROPERTY_NAME`**</span></span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">getUnicodeVersion</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">hasBinaryProperty</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
, <span class="methodparam"><span class="type">int</span>
`$property`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">isalnum</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">isalpha</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">isbase</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">isblank</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">iscntrl</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">isdefined</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">isdigit</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">isgraph</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">isIDIgnorable</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">isIDPart</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">isIDStart</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">isISOControl</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">isJavaIDPart</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">isJavaIDStart</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">isJavaSpaceChar</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">islower</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">isMirrored</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">isprint</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">ispunct</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">isspace</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">istitle</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">isUAlphabetic</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">isULowercase</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">isupper</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">isUUppercase</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">isUWhiteSpace</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">isWhitespace</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">isxdigit</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">ord</span> ( <span class="methodparam"><span
class="type">mixed</span> `$character`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">mixed</span> <span
class="methodname">tolower</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">mixed</span> <span
class="methodname">totitle</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">mixed</span> <span
class="methodname">toupper</span> ( <span class="methodparam"><span
class="type">mixed</span> `$codepoint`</span> )

}

预定义常量
----------

**`IntlChar::UNICODE_VERSION`**  

**`IntlChar::CODEPOINT_MIN`**  

**`IntlChar::CODEPOINT_MAX`**  

**`IntlChar::NO_NUMERIC_VALUE`**  
Special value that is returned by <span
class="methodname">IntlChar::getNumericValue</span> when no numeric
value is defined for a code point.

**`IntlChar::PROPERTY_ALPHABETIC`**  

**`IntlChar::PROPERTY_BINARY_START`**  

**`IntlChar::PROPERTY_ASCII_HEX_DIGIT`**  

**`IntlChar::PROPERTY_BIDI_CONTROL`**  

**`IntlChar::PROPERTY_BIDI_MIRRORED`**  

**`IntlChar::PROPERTY_DASH`**  

**`IntlChar::PROPERTY_DEFAULT_IGNORABLE_CODE_POINT`**  

**`IntlChar::PROPERTY_DEPRECATED`**  

**`IntlChar::PROPERTY_DIACRITIC`**  

**`IntlChar::PROPERTY_EXTENDER`**  

**`IntlChar::PROPERTY_FULL_COMPOSITION_EXCLUSION`**  

**`IntlChar::PROPERTY_GRAPHEME_BASE`**  

**`IntlChar::PROPERTY_GRAPHEME_EXTEND`**  

**`IntlChar::PROPERTY_GRAPHEME_LINK`**  

**`IntlChar::PROPERTY_HEX_DIGIT`**  

**`IntlChar::PROPERTY_HYPHEN`**  

**`IntlChar::PROPERTY_ID_CONTINUE`**  

**`IntlChar::PROPERTY_ID_START`**  

**`IntlChar::PROPERTY_IDEOGRAPHIC`**  

**`IntlChar::PROPERTY_IDS_BINARY_OPERATOR`**  

**`IntlChar::PROPERTY_IDS_TRINARY_OPERATOR`**  

**`IntlChar::PROPERTY_JOIN_CONTROL`**  

**`IntlChar::PROPERTY_LOGICAL_ORDER_EXCEPTION`**  

**`IntlChar::PROPERTY_LOWERCASE`**  

**`IntlChar::PROPERTY_MATH`**  

**`IntlChar::PROPERTY_NONCHARACTER_CODE_POINT`**  

**`IntlChar::PROPERTY_QUOTATION_MARK`**  

**`IntlChar::PROPERTY_RADICAL`**  

**`IntlChar::PROPERTY_SOFT_DOTTED`**  

**`IntlChar::PROPERTY_TERMINAL_PUNCTUATION`**  

**`IntlChar::PROPERTY_UNIFIED_IDEOGRAPH`**  

**`IntlChar::PROPERTY_UPPERCASE`**  

**`IntlChar::PROPERTY_WHITE_SPACE`**  

**`IntlChar::PROPERTY_XID_CONTINUE`**  

**`IntlChar::PROPERTY_XID_START`**  

**`IntlChar::PROPERTY_CASE_SENSITIVE`**  

**`IntlChar::PROPERTY_S_TERM`**  

**`IntlChar::PROPERTY_VARIATION_SELECTOR`**  

**`IntlChar::PROPERTY_NFD_INERT`**  

**`IntlChar::PROPERTY_NFKD_INERT`**  

**`IntlChar::PROPERTY_NFC_INERT`**  

**`IntlChar::PROPERTY_NFKC_INERT`**  

**`IntlChar::PROPERTY_SEGMENT_STARTER`**  

**`IntlChar::PROPERTY_PATTERN_SYNTAX`**  

**`IntlChar::PROPERTY_PATTERN_WHITE_SPACE`**  

**`IntlChar::PROPERTY_POSIX_ALNUM`**  

**`IntlChar::PROPERTY_POSIX_BLANK`**  

**`IntlChar::PROPERTY_POSIX_GRAPH`**  

**`IntlChar::PROPERTY_POSIX_PRINT`**  

**`IntlChar::PROPERTY_POSIX_XDIGIT`**  

**`IntlChar::PROPERTY_CASED`**  

**`IntlChar::PROPERTY_CASE_IGNORABLE`**  

**`IntlChar::PROPERTY_CHANGES_WHEN_LOWERCASED`**  

**`IntlChar::PROPERTY_CHANGES_WHEN_UPPERCASED`**  

**`IntlChar::PROPERTY_CHANGES_WHEN_TITLECASED`**  

**`IntlChar::PROPERTY_CHANGES_WHEN_CASEFOLDED`**  

**`IntlChar::PROPERTY_CHANGES_WHEN_CASEMAPPED`**  

**`IntlChar::PROPERTY_CHANGES_WHEN_NFKC_CASEFOLDED`**  

**`IntlChar::PROPERTY_BINARY_LIMIT`**  

**`IntlChar::PROPERTY_BIDI_CLASS`**  

**`IntlChar::PROPERTY_INT_START`**  

**`IntlChar::PROPERTY_BLOCK`**  

**`IntlChar::PROPERTY_CANONICAL_COMBINING_CLASS`**  

**`IntlChar::PROPERTY_DECOMPOSITION_TYPE`**  

**`IntlChar::PROPERTY_EAST_ASIAN_WIDTH`**  

**`IntlChar::PROPERTY_GENERAL_CATEGORY`**  

**`IntlChar::PROPERTY_JOINING_GROUP`**  

**`IntlChar::PROPERTY_JOINING_TYPE`**  

**`IntlChar::PROPERTY_LINE_BREAK`**  

**`IntlChar::PROPERTY_NUMERIC_TYPE`**  

**`IntlChar::PROPERTY_SCRIPT`**  

**`IntlChar::PROPERTY_HANGUL_SYLLABLE_TYPE`**  

**`IntlChar::PROPERTY_NFD_QUICK_CHECK`**  

**`IntlChar::PROPERTY_NFKD_QUICK_CHECK`**  

**`IntlChar::PROPERTY_NFC_QUICK_CHECK`**  

**`IntlChar::PROPERTY_NFKC_QUICK_CHECK`**  

**`IntlChar::PROPERTY_LEAD_CANONICAL_COMBINING_CLASS`**  

**`IntlChar::PROPERTY_TRAIL_CANONICAL_COMBINING_CLASS`**  

**`IntlChar::PROPERTY_GRAPHEME_CLUSTER_BREAK`**  

**`IntlChar::PROPERTY_SENTENCE_BREAK`**  

**`IntlChar::PROPERTY_WORD_BREAK`**  

**`IntlChar::PROPERTY_BIDI_PAIRED_BRACKET_TYPE`**  

**`IntlChar::PROPERTY_INT_LIMIT`**  

**`IntlChar::PROPERTY_GENERAL_CATEGORY_MASK`**  

**`IntlChar::PROPERTY_MASK_START`**  

**`IntlChar::PROPERTY_MASK_LIMIT`**  

**`IntlChar::PROPERTY_NUMERIC_VALUE`**  

**`IntlChar::PROPERTY_DOUBLE_START`**  

**`IntlChar::PROPERTY_DOUBLE_LIMIT`**  

**`IntlChar::PROPERTY_AGE`**  

**`IntlChar::PROPERTY_STRING_START`**  

**`IntlChar::PROPERTY_BIDI_MIRRORING_GLYPH`**  

**`IntlChar::PROPERTY_CASE_FOLDING`**  

**`IntlChar::PROPERTY_ISO_COMMENT`**  

**`IntlChar::PROPERTY_LOWERCASE_MAPPING`**  

**`IntlChar::PROPERTY_NAME`**  

**`IntlChar::PROPERTY_SIMPLE_CASE_FOLDING`**  

**`IntlChar::PROPERTY_SIMPLE_LOWERCASE_MAPPING`**  

**`IntlChar::PROPERTY_SIMPLE_TITLECASE_MAPPING`**  

**`IntlChar::PROPERTY_SIMPLE_UPPERCASE_MAPPING`**  

**`IntlChar::PROPERTY_TITLECASE_MAPPING`**  

**`IntlChar::PROPERTY_UNICODE_1_NAME`**  

**`IntlChar::PROPERTY_UPPERCASE_MAPPING`**  

**`IntlChar::PROPERTY_BIDI_PAIRED_BRACKET`**  

**`IntlChar::PROPERTY_STRING_LIMIT`**  

**`IntlChar::PROPERTY_SCRIPT_EXTENSIONS`**  

**`IntlChar::PROPERTY_OTHER_PROPERTY_START`**  

**`IntlChar::PROPERTY_OTHER_PROPERTY_LIMIT`**  

**`IntlChar::PROPERTY_INVALID_CODE`**  

**`IntlChar::CHAR_CATEGORY_UNASSIGNED`**  

**`IntlChar::CHAR_CATEGORY_GENERAL_OTHER_TYPES`**  

**`IntlChar::CHAR_CATEGORY_UPPERCASE_LETTER`**  

**`IntlChar::CHAR_CATEGORY_LOWERCASE_LETTER`**  

**`IntlChar::CHAR_CATEGORY_TITLECASE_LETTER`**  

**`IntlChar::CHAR_CATEGORY_MODIFIER_LETTER`**  

**`IntlChar::CHAR_CATEGORY_OTHER_LETTER`**  

**`IntlChar::CHAR_CATEGORY_NON_SPACING_MARK`**  

**`IntlChar::CHAR_CATEGORY_ENCLOSING_MARK`**  

**`IntlChar::CHAR_CATEGORY_COMBINING_SPACING_MARK`**  

**`IntlChar::CHAR_CATEGORY_DECIMAL_DIGIT_NUMBER`**  

**`IntlChar::CHAR_CATEGORY_LETTER_NUMBER`**  

**`IntlChar::CHAR_CATEGORY_OTHER_NUMBER`**  

**`IntlChar::CHAR_CATEGORY_SPACE_SEPARATOR`**  

**`IntlChar::CHAR_CATEGORY_LINE_SEPARATOR`**  

**`IntlChar::CHAR_CATEGORY_PARAGRAPH_SEPARATOR`**  

**`IntlChar::CHAR_CATEGORY_CONTROL_CHAR`**  

**`IntlChar::CHAR_CATEGORY_FORMAT_CHAR`**  

**`IntlChar::CHAR_CATEGORY_PRIVATE_USE_CHAR`**  

**`IntlChar::CHAR_CATEGORY_SURROGATE`**  

**`IntlChar::CHAR_CATEGORY_DASH_PUNCTUATION`**  

**`IntlChar::CHAR_CATEGORY_START_PUNCTUATION`**  

**`IntlChar::CHAR_CATEGORY_END_PUNCTUATION`**  

**`IntlChar::CHAR_CATEGORY_CONNECTOR_PUNCTUATION`**  

**`IntlChar::CHAR_CATEGORY_OTHER_PUNCTUATION`**  

**`IntlChar::CHAR_CATEGORY_MATH_SYMBOL`**  

**`IntlChar::CHAR_CATEGORY_CURRENCY_SYMBOL`**  

**`IntlChar::CHAR_CATEGORY_MODIFIER_SYMBOL`**  

**`IntlChar::CHAR_CATEGORY_OTHER_SYMBOL`**  

**`IntlChar::CHAR_CATEGORY_INITIAL_PUNCTUATION`**  

**`IntlChar::CHAR_CATEGORY_FINAL_PUNCTUATION`**  

**`IntlChar::CHAR_CATEGORY_CHAR_CATEGORY_COUNT`**  

**`IntlChar::CHAR_DIRECTION_LEFT_TO_RIGHT`**  

**`IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT`**  

**`IntlChar::CHAR_DIRECTION_EUROPEAN_NUMBER`**  

**`IntlChar::CHAR_DIRECTION_EUROPEAN_NUMBER_SEPARATOR`**  

**`IntlChar::CHAR_DIRECTION_EUROPEAN_NUMBER_TERMINATOR`**  

**`IntlChar::CHAR_DIRECTION_ARABIC_NUMBER`**  

**`IntlChar::CHAR_DIRECTION_COMMON_NUMBER_SEPARATOR`**  

**`IntlChar::CHAR_DIRECTION_BLOCK_SEPARATOR`**  

**`IntlChar::CHAR_DIRECTION_SEGMENT_SEPARATOR`**  

**`IntlChar::CHAR_DIRECTION_WHITE_SPACE_NEUTRAL`**  

**`IntlChar::CHAR_DIRECTION_OTHER_NEUTRAL`**  

**`IntlChar::CHAR_DIRECTION_LEFT_TO_RIGHT_EMBEDDING`**  

**`IntlChar::CHAR_DIRECTION_LEFT_TO_RIGHT_OVERRIDE`**  

**`IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT_ARABIC`**  

**`IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT_EMBEDDING`**  

**`IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT_OVERRIDE`**  

**`IntlChar::CHAR_DIRECTION_POP_DIRECTIONAL_FORMAT`**  

**`IntlChar::CHAR_DIRECTION_DIR_NON_SPACING_MARK`**  

**`IntlChar::CHAR_DIRECTION_BOUNDARY_NEUTRAL`**  

**`IntlChar::CHAR_DIRECTION_FIRST_STRONG_ISOLATE`**  

**`IntlChar::CHAR_DIRECTION_LEFT_TO_RIGHT_ISOLATE`**  

**`IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT_ISOLATE`**  

**`IntlChar::CHAR_DIRECTION_POP_DIRECTIONAL_ISOLATE`**  

**`IntlChar::CHAR_DIRECTION_CHAR_DIRECTION_COUNT`**  

**`IntlChar::BLOCK_CODE_NO_BLOCK`**  

**`IntlChar::BLOCK_CODE_BASIC_LATIN`**  

**`IntlChar::BLOCK_CODE_LATIN_1_SUPPLEMENT`**  

**`IntlChar::BLOCK_CODE_LATIN_EXTENDED_A`**  

**`IntlChar::BLOCK_CODE_LATIN_EXTENDED_B`**  

**`IntlChar::BLOCK_CODE_IPA_EXTENSIONS`**  

**`IntlChar::BLOCK_CODE_SPACING_MODIFIER_LETTERS`**  

**`IntlChar::BLOCK_CODE_COMBINING_DIACRITICAL_MARKS`**  

**`IntlChar::BLOCK_CODE_GREEK`**  

**`IntlChar::BLOCK_CODE_CYRILLIC`**  

**`IntlChar::BLOCK_CODE_ARMENIAN`**  

**`IntlChar::BLOCK_CODE_HEBREW`**  

**`IntlChar::BLOCK_CODE_ARABIC`**  

**`IntlChar::BLOCK_CODE_SYRIAC`**  

**`IntlChar::BLOCK_CODE_THAANA`**  

**`IntlChar::BLOCK_CODE_DEVANAGARI`**  

**`IntlChar::BLOCK_CODE_BENGALI`**  

**`IntlChar::BLOCK_CODE_GURMUKHI`**  

**`IntlChar::BLOCK_CODE_GUJARATI`**  

**`IntlChar::BLOCK_CODE_ORIYA`**  

**`IntlChar::BLOCK_CODE_TAMIL`**  

**`IntlChar::BLOCK_CODE_TELUGU`**  

**`IntlChar::BLOCK_CODE_KANNADA`**  

**`IntlChar::BLOCK_CODE_MALAYALAM`**  

**`IntlChar::BLOCK_CODE_SINHALA`**  

**`IntlChar::BLOCK_CODE_THAI`**  

**`IntlChar::BLOCK_CODE_LAO`**  

**`IntlChar::BLOCK_CODE_TIBETAN`**  

**`IntlChar::BLOCK_CODE_MYANMAR`**  

**`IntlChar::BLOCK_CODE_GEORGIAN`**  

**`IntlChar::BLOCK_CODE_HANGUL_JAMO`**  

**`IntlChar::BLOCK_CODE_ETHIOPIC`**  

**`IntlChar::BLOCK_CODE_CHEROKEE`**  

**`IntlChar::BLOCK_CODE_UNIFIED_CANADIAN_ABORIGINAL_SYLLABICS`**  

**`IntlChar::BLOCK_CODE_OGHAM`**  

**`IntlChar::BLOCK_CODE_RUNIC`**  

**`IntlChar::BLOCK_CODE_KHMER`**  

**`IntlChar::BLOCK_CODE_MONGOLIAN`**  

**`IntlChar::BLOCK_CODE_LATIN_EXTENDED_ADDITIONAL`**  

**`IntlChar::BLOCK_CODE_GREEK_EXTENDED`**  

**`IntlChar::BLOCK_CODE_GENERAL_PUNCTUATION`**  

**`IntlChar::BLOCK_CODE_SUPERSCRIPTS_AND_SUBSCRIPTS`**  

**`IntlChar::BLOCK_CODE_CURRENCY_SYMBOLS`**  

**`IntlChar::BLOCK_CODE_COMBINING_MARKS_FOR_SYMBOLS`**  

**`IntlChar::BLOCK_CODE_LETTERLIKE_SYMBOLS`**  

**`IntlChar::BLOCK_CODE_NUMBER_FORMS`**  

**`IntlChar::BLOCK_CODE_ARROWS`**  

**`IntlChar::BLOCK_CODE_MATHEMATICAL_OPERATORS`**  

**`IntlChar::BLOCK_CODE_MISCELLANEOUS_TECHNICAL`**  

**`IntlChar::BLOCK_CODE_CONTROL_PICTURES`**  

**`IntlChar::BLOCK_CODE_OPTICAL_CHARACTER_RECOGNITION`**  

**`IntlChar::BLOCK_CODE_ENCLOSED_ALPHANUMERICS`**  

**`IntlChar::BLOCK_CODE_BOX_DRAWING`**  

**`IntlChar::BLOCK_CODE_BLOCK_ELEMENTS`**  

**`IntlChar::BLOCK_CODE_GEOMETRIC_SHAPES`**  

**`IntlChar::BLOCK_CODE_MISCELLANEOUS_SYMBOLS`**  

**`IntlChar::BLOCK_CODE_DINGBATS`**  

**`IntlChar::BLOCK_CODE_BRAILLE_PATTERNS`**  

**`IntlChar::BLOCK_CODE_CJK_RADICALS_SUPPLEMENT`**  

**`IntlChar::BLOCK_CODE_KANGXI_RADICALS`**  

**`IntlChar::BLOCK_CODE_IDEOGRAPHIC_DESCRIPTION_CHARACTERS`**  

**`IntlChar::BLOCK_CODE_CJK_SYMBOLS_AND_PUNCTUATION`**  

**`IntlChar::BLOCK_CODE_HIRAGANA`**  

**`IntlChar::BLOCK_CODE_KATAKANA`**  

**`IntlChar::BLOCK_CODE_BOPOMOFO`**  

**`IntlChar::BLOCK_CODE_HANGUL_COMPATIBILITY_JAMO`**  

**`IntlChar::BLOCK_CODE_KANBUN`**  

**`IntlChar::BLOCK_CODE_BOPOMOFO_EXTENDED`**  

**`IntlChar::BLOCK_CODE_ENCLOSED_CJK_LETTERS_AND_MONTHS`**  

**`IntlChar::BLOCK_CODE_CJK_COMPATIBILITY`**  

**`IntlChar::BLOCK_CODE_CJK_UNIFIED_IDEOGRAPHS_EXTENSION_A`**  

**`IntlChar::BLOCK_CODE_CJK_UNIFIED_IDEOGRAPHS`**  

**`IntlChar::BLOCK_CODE_YI_SYLLABLES`**  

**`IntlChar::BLOCK_CODE_YI_RADICALS`**  

**`IntlChar::BLOCK_CODE_HANGUL_SYLLABLES`**  

**`IntlChar::BLOCK_CODE_HIGH_SURROGATES`**  

**`IntlChar::BLOCK_CODE_HIGH_PRIVATE_USE_SURROGATES`**  

**`IntlChar::BLOCK_CODE_LOW_SURROGATES`**  

**`IntlChar::BLOCK_CODE_PRIVATE_USE_AREA`**  

**`IntlChar::BLOCK_CODE_PRIVATE_USE`**  

**`IntlChar::BLOCK_CODE_CJK_COMPATIBILITY_IDEOGRAPHS`**  

**`IntlChar::BLOCK_CODE_ALPHABETIC_PRESENTATION_FORMS`**  

**`IntlChar::BLOCK_CODE_ARABIC_PRESENTATION_FORMS_A`**  

**`IntlChar::BLOCK_CODE_COMBINING_HALF_MARKS`**  

**`IntlChar::BLOCK_CODE_CJK_COMPATIBILITY_FORMS`**  

**`IntlChar::BLOCK_CODE_SMALL_FORM_VARIANTS`**  

**`IntlChar::BLOCK_CODE_ARABIC_PRESENTATION_FORMS_B`**  

**`IntlChar::BLOCK_CODE_SPECIALS`**  

**`IntlChar::BLOCK_CODE_HALFWIDTH_AND_FULLWIDTH_FORMS`**  

**`IntlChar::BLOCK_CODE_OLD_ITALIC`**  

**`IntlChar::BLOCK_CODE_GOTHIC`**  

**`IntlChar::BLOCK_CODE_DESERET`**  

**`IntlChar::BLOCK_CODE_BYZANTINE_MUSICAL_SYMBOLS`**  

**`IntlChar::BLOCK_CODE_MUSICAL_SYMBOLS`**  

**`IntlChar::BLOCK_CODE_MATHEMATICAL_ALPHANUMERIC_SYMBOLS`**  

**`IntlChar::BLOCK_CODE_CJK_UNIFIED_IDEOGRAPHS_EXTENSION_B`**  

**`IntlChar::BLOCK_CODE_CJK_COMPATIBILITY_IDEOGRAPHS_SUPPLEMENT`**  

**`IntlChar::BLOCK_CODE_TAGS`**  

**`IntlChar::BLOCK_CODE_CYRILLIC_SUPPLEMENT`**  

**`IntlChar::BLOCK_CODE_CYRILLIC_SUPPLEMENTARY`**  

**`IntlChar::BLOCK_CODE_TAGALOG`**  

**`IntlChar::BLOCK_CODE_HANUNOO`**  

**`IntlChar::BLOCK_CODE_BUHID`**  

**`IntlChar::BLOCK_CODE_TAGBANWA`**  

**`IntlChar::BLOCK_CODE_MISCELLANEOUS_MATHEMATICAL_SYMBOLS_A`**  

**`IntlChar::BLOCK_CODE_SUPPLEMENTAL_ARROWS_A`**  

**`IntlChar::BLOCK_CODE_SUPPLEMENTAL_ARROWS_B`**  

**`IntlChar::BLOCK_CODE_MISCELLANEOUS_MATHEMATICAL_SYMBOLS_B`**  

**`IntlChar::BLOCK_CODE_SUPPLEMENTAL_MATHEMATICAL_OPERATORS`**  

**`IntlChar::BLOCK_CODE_KATAKANA_PHONETIC_EXTENSIONS`**  

**`IntlChar::BLOCK_CODE_VARIATION_SELECTORS`**  

**`IntlChar::BLOCK_CODE_SUPPLEMENTARY_PRIVATE_USE_AREA_A`**  

**`IntlChar::BLOCK_CODE_SUPPLEMENTARY_PRIVATE_USE_AREA_B`**  

**`IntlChar::BLOCK_CODE_LIMBU`**  

**`IntlChar::BLOCK_CODE_TAI_LE`**  

**`IntlChar::BLOCK_CODE_KHMER_SYMBOLS`**  

**`IntlChar::BLOCK_CODE_PHONETIC_EXTENSIONS`**  

**`IntlChar::BLOCK_CODE_MISCELLANEOUS_SYMBOLS_AND_ARROWS`**  

**`IntlChar::BLOCK_CODE_YIJING_HEXAGRAM_SYMBOLS`**  

**`IntlChar::BLOCK_CODE_LINEAR_B_SYLLABARY`**  

**`IntlChar::BLOCK_CODE_LINEAR_B_IDEOGRAMS`**  

**`IntlChar::BLOCK_CODE_AEGEAN_NUMBERS`**  

**`IntlChar::BLOCK_CODE_UGARITIC`**  

**`IntlChar::BLOCK_CODE_SHAVIAN`**  

**`IntlChar::BLOCK_CODE_OSMANYA`**  

**`IntlChar::BLOCK_CODE_CYPRIOT_SYLLABARY`**  

**`IntlChar::BLOCK_CODE_TAI_XUAN_JING_SYMBOLS`**  

**`IntlChar::BLOCK_CODE_VARIATION_SELECTORS_SUPPLEMENT`**  

**`IntlChar::BLOCK_CODE_ANCIENT_GREEK_MUSICAL_NOTATION`**  

**`IntlChar::BLOCK_CODE_ANCIENT_GREEK_NUMBERS`**  

**`IntlChar::BLOCK_CODE_ARABIC_SUPPLEMENT`**  

**`IntlChar::BLOCK_CODE_BUGINESE`**  

**`IntlChar::BLOCK_CODE_CJK_STROKES`**  

**`IntlChar::BLOCK_CODE_COMBINING_DIACRITICAL_MARKS_SUPPLEMENT`**  

**`IntlChar::BLOCK_CODE_COPTIC`**  

**`IntlChar::BLOCK_CODE_ETHIOPIC_EXTENDED`**  

**`IntlChar::BLOCK_CODE_ETHIOPIC_SUPPLEMENT`**  

**`IntlChar::BLOCK_CODE_GEORGIAN_SUPPLEMENT`**  

**`IntlChar::BLOCK_CODE_GLAGOLITIC`**  

**`IntlChar::BLOCK_CODE_KHAROSHTHI`**  

**`IntlChar::BLOCK_CODE_MODIFIER_TONE_LETTERS`**  

**`IntlChar::BLOCK_CODE_NEW_TAI_LUE`**  

**`IntlChar::BLOCK_CODE_OLD_PERSIAN`**  

**`IntlChar::BLOCK_CODE_PHONETIC_EXTENSIONS_SUPPLEMENT`**  

**`IntlChar::BLOCK_CODE_SUPPLEMENTAL_PUNCTUATION`**  

**`IntlChar::BLOCK_CODE_SYLOTI_NAGRI`**  

**`IntlChar::BLOCK_CODE_TIFINAGH`**  

**`IntlChar::BLOCK_CODE_VERTICAL_FORMS`**  

**`IntlChar::BLOCK_CODE_NKO`**  

**`IntlChar::BLOCK_CODE_BALINESE`**  

**`IntlChar::BLOCK_CODE_LATIN_EXTENDED_C`**  

**`IntlChar::BLOCK_CODE_LATIN_EXTENDED_D`**  

**`IntlChar::BLOCK_CODE_PHAGS_PA`**  

**`IntlChar::BLOCK_CODE_PHOENICIAN`**  

**`IntlChar::BLOCK_CODE_CUNEIFORM`**  

**`IntlChar::BLOCK_CODE_CUNEIFORM_NUMBERS_AND_PUNCTUATION`**  

**`IntlChar::BLOCK_CODE_COUNTING_ROD_NUMERALS`**  

**`IntlChar::BLOCK_CODE_SUNDANESE`**  

**`IntlChar::BLOCK_CODE_LEPCHA`**  

**`IntlChar::BLOCK_CODE_OL_CHIKI`**  

**`IntlChar::BLOCK_CODE_CYRILLIC_EXTENDED_A`**  

**`IntlChar::BLOCK_CODE_VAI`**  

**`IntlChar::BLOCK_CODE_CYRILLIC_EXTENDED_B`**  

**`IntlChar::BLOCK_CODE_SAURASHTRA`**  

**`IntlChar::BLOCK_CODE_KAYAH_LI`**  

**`IntlChar::BLOCK_CODE_REJANG`**  

**`IntlChar::BLOCK_CODE_CHAM`**  

**`IntlChar::BLOCK_CODE_ANCIENT_SYMBOLS`**  

**`IntlChar::BLOCK_CODE_PHAISTOS_DISC`**  

**`IntlChar::BLOCK_CODE_LYCIAN`**  

**`IntlChar::BLOCK_CODE_CARIAN`**  

**`IntlChar::BLOCK_CODE_LYDIAN`**  

**`IntlChar::BLOCK_CODE_MAHJONG_TILES`**  

**`IntlChar::BLOCK_CODE_DOMINO_TILES`**  

**`IntlChar::BLOCK_CODE_SAMARITAN`**  

**`IntlChar::BLOCK_CODE_UNIFIED_CANADIAN_ABORIGINAL_SYLLABICS_EXTENDED`**  

**`IntlChar::BLOCK_CODE_TAI_THAM`**  

**`IntlChar::BLOCK_CODE_VEDIC_EXTENSIONS`**  

**`IntlChar::BLOCK_CODE_LISU`**  

**`IntlChar::BLOCK_CODE_BAMUM`**  

**`IntlChar::BLOCK_CODE_COMMON_INDIC_NUMBER_FORMS`**  

**`IntlChar::BLOCK_CODE_DEVANAGARI_EXTENDED`**  

**`IntlChar::BLOCK_CODE_HANGUL_JAMO_EXTENDED_A`**  

**`IntlChar::BLOCK_CODE_JAVANESE`**  

**`IntlChar::BLOCK_CODE_MYANMAR_EXTENDED_A`**  

**`IntlChar::BLOCK_CODE_TAI_VIET`**  

**`IntlChar::BLOCK_CODE_MEETEI_MAYEK`**  

**`IntlChar::BLOCK_CODE_HANGUL_JAMO_EXTENDED_B`**  

**`IntlChar::BLOCK_CODE_IMPERIAL_ARAMAIC`**  

**`IntlChar::BLOCK_CODE_OLD_SOUTH_ARABIAN`**  

**`IntlChar::BLOCK_CODE_AVESTAN`**  

**`IntlChar::BLOCK_CODE_INSCRIPTIONAL_PARTHIAN`**  

**`IntlChar::BLOCK_CODE_INSCRIPTIONAL_PAHLAVI`**  

**`IntlChar::BLOCK_CODE_OLD_TURKIC`**  

**`IntlChar::BLOCK_CODE_RUMI_NUMERAL_SYMBOLS`**  

**`IntlChar::BLOCK_CODE_KAITHI`**  

**`IntlChar::BLOCK_CODE_EGYPTIAN_HIEROGLYPHS`**  

**`IntlChar::BLOCK_CODE_ENCLOSED_ALPHANUMERIC_SUPPLEMENT`**  

**`IntlChar::BLOCK_CODE_ENCLOSED_IDEOGRAPHIC_SUPPLEMENT`**  

**`IntlChar::BLOCK_CODE_CJK_UNIFIED_IDEOGRAPHS_EXTENSION_C`**  

**`IntlChar::BLOCK_CODE_MANDAIC`**  

**`IntlChar::BLOCK_CODE_BATAK`**  

**`IntlChar::BLOCK_CODE_ETHIOPIC_EXTENDED_A`**  

**`IntlChar::BLOCK_CODE_BRAHMI`**  

**`IntlChar::BLOCK_CODE_BAMUM_SUPPLEMENT`**  

**`IntlChar::BLOCK_CODE_KANA_SUPPLEMENT`**  

**`IntlChar::BLOCK_CODE_PLAYING_CARDS`**  

**`IntlChar::BLOCK_CODE_MISCELLANEOUS_SYMBOLS_AND_PICTOGRAPHS`**  

**`IntlChar::BLOCK_CODE_EMOTICONS`**  

**`IntlChar::BLOCK_CODE_TRANSPORT_AND_MAP_SYMBOLS`**  

**`IntlChar::BLOCK_CODE_ALCHEMICAL_SYMBOLS`**  

**`IntlChar::BLOCK_CODE_CJK_UNIFIED_IDEOGRAPHS_EXTENSION_D`**  

**`IntlChar::BLOCK_CODE_ARABIC_EXTENDED_A`**  

**`IntlChar::BLOCK_CODE_ARABIC_MATHEMATICAL_ALPHABETIC_SYMBOLS`**  

**`IntlChar::BLOCK_CODE_CHAKMA`**  

**`IntlChar::BLOCK_CODE_MEETEI_MAYEK_EXTENSIONS`**  

**`IntlChar::BLOCK_CODE_MEROITIC_CURSIVE`**  

**`IntlChar::BLOCK_CODE_MEROITIC_HIEROGLYPHS`**  

**`IntlChar::BLOCK_CODE_MIAO`**  

**`IntlChar::BLOCK_CODE_SHARADA`**  

**`IntlChar::BLOCK_CODE_SORA_SOMPENG`**  

**`IntlChar::BLOCK_CODE_SUNDANESE_SUPPLEMENT`**  

**`IntlChar::BLOCK_CODE_TAKRI`**  

**`IntlChar::BLOCK_CODE_COUNT`**  

**`IntlChar::BLOCK_CODE_INVALID_CODE`**  

**`IntlChar::BPT_NONE`**  

**`IntlChar::BPT_OPEN`**  

**`IntlChar::BPT_CLOSE`**  

**`IntlChar::BPT_COUNT`**  

**`IntlChar::EA_NEUTRAL`**  

**`IntlChar::EA_AMBIGUOUS`**  

**`IntlChar::EA_HALFWIDTH`**  

**`IntlChar::EA_FULLWIDTH`**  

**`IntlChar::EA_NARROW`**  

**`IntlChar::EA_WIDE`**  

**`IntlChar::EA_COUNT`**  

**`IntlChar::UNICODE_CHAR_NAME`**  

**`IntlChar::UNICODE_10_CHAR_NAME`**  

**`IntlChar::EXTENDED_CHAR_NAME`**  

**`IntlChar::CHAR_NAME_ALIAS`**  

**`IntlChar::CHAR_NAME_CHOICE_COUNT`**  

**`IntlChar::SHORT_PROPERTY_NAME`**  

**`IntlChar::LONG_PROPERTY_NAME`**  

**`IntlChar::PROPERTY_NAME_CHOICE_COUNT`**  

**`IntlChar::DT_NONE`**  

**`IntlChar::DT_CANONICAL`**  

**`IntlChar::DT_COMPAT`**  

**`IntlChar::DT_CIRCLE`**  

**`IntlChar::DT_FINAL`**  

**`IntlChar::DT_FONT`**  

**`IntlChar::DT_FRACTION`**  

**`IntlChar::DT_INITIAL`**  

**`IntlChar::DT_ISOLATED`**  

**`IntlChar::DT_MEDIAL`**  

**`IntlChar::DT_NARROW`**  

**`IntlChar::DT_NOBREAK`**  

**`IntlChar::DT_SMALL`**  

**`IntlChar::DT_SQUARE`**  

**`IntlChar::DT_SUB`**  

**`IntlChar::DT_SUPER`**  

**`IntlChar::DT_VERTICAL`**  

**`IntlChar::DT_WIDE`**  

**`IntlChar::DT_COUNT`**  

**`IntlChar::JT_NON_JOINING`**  

**`IntlChar::JT_JOIN_CAUSING`**  

**`IntlChar::JT_DUAL_JOINING`**  

**`IntlChar::JT_LEFT_JOINING`**  

**`IntlChar::JT_RIGHT_JOINING`**  

**`IntlChar::JT_TRANSPARENT`**  

**`IntlChar::JT_COUNT`**  

**`IntlChar::JG_NO_JOINING_GROUP`**  

**`IntlChar::JG_AIN`**  

**`IntlChar::JG_ALAPH`**  

**`IntlChar::JG_ALEF`**  

**`IntlChar::JG_BEH`**  

**`IntlChar::JG_BETH`**  

**`IntlChar::JG_DAL`**  

**`IntlChar::JG_DALATH_RISH`**  

**`IntlChar::JG_E`**  

**`IntlChar::JG_FEH`**  

**`IntlChar::JG_FINAL_SEMKATH`**  

**`IntlChar::JG_GAF`**  

**`IntlChar::JG_GAMAL`**  

**`IntlChar::JG_HAH`**  

**`IntlChar::JG_TEH_MARBUTA_GOAL`**  

**`IntlChar::JG_HAMZA_ON_HEH_GOAL`**  

**`IntlChar::JG_HE`**  

**`IntlChar::JG_HEH`**  

**`IntlChar::JG_HEH_GOAL`**  

**`IntlChar::JG_HETH`**  

**`IntlChar::JG_KAF`**  

**`IntlChar::JG_KAPH`**  

**`IntlChar::JG_KNOTTED_HEH`**  

**`IntlChar::JG_LAM`**  

**`IntlChar::JG_LAMADH`**  

**`IntlChar::JG_MEEM`**  

**`IntlChar::JG_MIM`**  

**`IntlChar::JG_NOON`**  

**`IntlChar::JG_NUN`**  

**`IntlChar::JG_PE`**  

**`IntlChar::JG_QAF`**  

**`IntlChar::JG_QAPH`**  

**`IntlChar::JG_REH`**  

**`IntlChar::JG_REVERSED_PE`**  

**`IntlChar::JG_SAD`**  

**`IntlChar::JG_SADHE`**  

**`IntlChar::JG_SEEN`**  

**`IntlChar::JG_SEMKATH`**  

**`IntlChar::JG_SHIN`**  

**`IntlChar::JG_SWASH_KAF`**  

**`IntlChar::JG_SYRIAC_WAW`**  

**`IntlChar::JG_TAH`**  

**`IntlChar::JG_TAW`**  

**`IntlChar::JG_TEH_MARBUTA`**  

**`IntlChar::JG_TETH`**  

**`IntlChar::JG_WAW`**  

**`IntlChar::JG_YEH`**  

**`IntlChar::JG_YEH_BARREE`**  

**`IntlChar::JG_YEH_WITH_TAIL`**  

**`IntlChar::JG_YUDH`**  

**`IntlChar::JG_YUDH_HE`**  

**`IntlChar::JG_ZAIN`**  

**`IntlChar::JG_FE`**  

**`IntlChar::JG_KHAPH`**  

**`IntlChar::JG_ZHAIN`**  

**`IntlChar::JG_BURUSHASKI_YEH_BARREE`**  

**`IntlChar::JG_FARSI_YEH`**  

**`IntlChar::JG_NYA`**  

**`IntlChar::JG_ROHINGYA_YEH`**  

**`IntlChar::JG_COUNT`**  

**`IntlChar::GCB_OTHER`**  

**`IntlChar::GCB_CONTROL`**  

**`IntlChar::GCB_CR`**  

**`IntlChar::GCB_EXTEND`**  

**`IntlChar::GCB_L`**  

**`IntlChar::GCB_LF`**  

**`IntlChar::GCB_LV`**  

**`IntlChar::GCB_LVT`**  

**`IntlChar::GCB_T`**  

**`IntlChar::GCB_V`**  

**`IntlChar::GCB_SPACING_MARK`**  

**`IntlChar::GCB_PREPEND`**  

**`IntlChar::GCB_REGIONAL_INDICATOR`**  

**`IntlChar::GCB_COUNT`**  

**`IntlChar::WB_OTHER`**  

**`IntlChar::WB_ALETTER`**  

**`IntlChar::WB_FORMAT`**  

**`IntlChar::WB_KATAKANA`**  

**`IntlChar::WB_MIDLETTER`**  

**`IntlChar::WB_MIDNUM`**  

**`IntlChar::WB_NUMERIC`**  

**`IntlChar::WB_EXTENDNUMLET`**  

**`IntlChar::WB_CR`**  

**`IntlChar::WB_EXTEND`**  

**`IntlChar::WB_LF`**  

**`IntlChar::WB_MIDNUMLET`**  

**`IntlChar::WB_NEWLINE`**  

**`IntlChar::WB_REGIONAL_INDICATOR`**  

**`IntlChar::WB_HEBREW_LETTER`**  

**`IntlChar::WB_SINGLE_QUOTE`**  

**`IntlChar::WB_DOUBLE_QUOTE`**  

**`IntlChar::WB_COUNT`**  

**`IntlChar::SB_OTHER`**  

**`IntlChar::SB_ATERM`**  

**`IntlChar::SB_CLOSE`**  

**`IntlChar::SB_FORMAT`**  

**`IntlChar::SB_LOWER`**  

**`IntlChar::SB_NUMERIC`**  

**`IntlChar::SB_OLETTER`**  

**`IntlChar::SB_SEP`**  

**`IntlChar::SB_SP`**  

**`IntlChar::SB_STERM`**  

**`IntlChar::SB_UPPER`**  

**`IntlChar::SB_CR`**  

**`IntlChar::SB_EXTEND`**  

**`IntlChar::SB_LF`**  

**`IntlChar::SB_SCONTINUE`**  

**`IntlChar::SB_COUNT`**  

**`IntlChar::LB_UNKNOWN`**  

**`IntlChar::LB_AMBIGUOUS`**  

**`IntlChar::LB_ALPHABETIC`**  

**`IntlChar::LB_BREAK_BOTH`**  

**`IntlChar::LB_BREAK_AFTER`**  

**`IntlChar::LB_BREAK_BEFORE`**  

**`IntlChar::LB_MANDATORY_BREAK`**  

**`IntlChar::LB_CONTINGENT_BREAK`**  

**`IntlChar::LB_CLOSE_PUNCTUATION`**  

**`IntlChar::LB_COMBINING_MARK`**  

**`IntlChar::LB_CARRIAGE_RETURN`**  

**`IntlChar::LB_EXCLAMATION`**  

**`IntlChar::LB_GLUE`**  

**`IntlChar::LB_HYPHEN`**  

**`IntlChar::LB_IDEOGRAPHIC`**  

**`IntlChar::LB_INSEPARABLE`**  

**`IntlChar::LB_INSEPERABLE`**  

**`IntlChar::LB_INFIX_NUMERIC`**  

**`IntlChar::LB_LINE_FEED`**  

**`IntlChar::LB_NONSTARTER`**  

**`IntlChar::LB_NUMERIC`**  

**`IntlChar::LB_OPEN_PUNCTUATION`**  

**`IntlChar::LB_POSTFIX_NUMERIC`**  

**`IntlChar::LB_PREFIX_NUMERIC`**  

**`IntlChar::LB_QUOTATION`**  

**`IntlChar::LB_COMPLEX_CONTEXT`**  

**`IntlChar::LB_SURROGATE`**  

**`IntlChar::LB_SPACE`**  

**`IntlChar::LB_BREAK_SYMBOLS`**  

**`IntlChar::LB_ZWSPACE`**  

**`IntlChar::LB_NEXT_LINE`**  

**`IntlChar::LB_WORD_JOINER`**  

**`IntlChar::LB_H2`**  

**`IntlChar::LB_H3`**  

**`IntlChar::LB_JL`**  

**`IntlChar::LB_JT`**  

**`IntlChar::LB_JV`**  

**`IntlChar::LB_CLOSE_PARENTHESIS`**  

**`IntlChar::LB_CONDITIONAL_JAPANESE_STARTER`**  

**`IntlChar::LB_HEBREW_LETTER`**  

**`IntlChar::LB_REGIONAL_INDICATOR`**  

**`IntlChar::LB_COUNT`**  

**`IntlChar::NT_NONE`**  

**`IntlChar::NT_DECIMAL`**  

**`IntlChar::NT_DIGIT`**  

**`IntlChar::NT_NUMERIC`**  

**`IntlChar::NT_COUNT`**  

**`IntlChar::HST_NOT_APPLICABLE`**  

**`IntlChar::HST_LEADING_JAMO`**  

**`IntlChar::HST_VOWEL_JAMO`**  

**`IntlChar::HST_TRAILING_JAMO`**  

**`IntlChar::HST_LV_SYLLABLE`**  

**`IntlChar::HST_LVT_SYLLABLE`**  

**`IntlChar::HST_COUNT`**  

**`IntlChar::FOLD_CASE_DEFAULT`**  

**`IntlChar::FOLD_CASE_EXCLUDE_SPECIAL_I`**  

更新日志
--------

| 版本  | 说明                                                     |
|-------|----------------------------------------------------------|
| 7.0.6 | The **`IntlChar::NO_NUMERIC_VALUE`** constant was added. |

IntlChar::charAge
=================

Get the "age" of the code point

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">IntlChar::charAge</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Gets the "age" of the code point.

The "age" is the Unicode version when the code point was first
designated (as a non-character or for Private Use) or assigned a
character. This can be useful to avoid emitting code points to receiving
processes that do not accept newer characters.

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

The Unicode version number, as an <span class="type">array</span>. For
example, version *1.3.31.2* would be represented as *\[1, 3, 31, 2\]*.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::charage("\u{2603}"));
var_dump(IntlChar::charage("\u{1F576}"));
?>
```

以上例程会输出：

    array(4) {
      [0]=>
      int(1)
      [1]=>
      int(1)
      [2]=>
      int(0)
      [3]=>
      int(0)
    }
    array(4) {
      [0]=>
      int(7)
      [1]=>
      int(0)
      [2]=>
      int(0)
      [3]=>
      int(0)
    }

### 参见

-   <span class="function">IntlChar::getUnicodeVersion</span>
-   <span class="function">IntlChar::getIntPropertyMinValue</span>
-   <span class="function">IntlChar::getIntPropertyValue</span>

IntlChar::charDigitValue
========================

Get the decimal digit value of a decimal digit character

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">IntlChar::charDigitValue</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Returns the decimal digit value of a decimal digit character.

Such characters have the general category "Nd" (decimal digit numbers)
and a Numeric\_Type of Decimal.

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

The decimal digit value of `codepoint`, or *-1* if it is not a decimal
digit character.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::charDigitValue("1"));
var_dump(IntlChar::charDigitValue("\u{0662}"));
var_dump(IntlChar::charDigitValue("\u{0E53}"));
?>
```

以上例程会输出：

    int(1)
    int(2)
    int(3)

### 参见

-   <span class="function">IntlChar::getNumericValue</span>

IntlChar::charDirection
=======================

Get bidirectional category value for a code point

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">IntlChar::charDirection</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Returns the bidirectional category value for the code point, which is
used in the
<a href="http://www.unicode.org/reports/tr9/" class="link external">» Unicode bidirectional algorithm (UAX #9)</a>.

> **Note**:
>
> Some unassigned code points have bidi values of R or AL because they
> are in blocks that are reserved for Right-To-Left scripts.

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

The bidirectional category value; one of the following constants:

-   **`IntlChar::CHAR_DIRECTION_LEFT_TO_RIGHT`**
-   **`IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT`**
-   **`IntlChar::CHAR_DIRECTION_EUROPEAN_NUMBER`**
-   **`IntlChar::CHAR_DIRECTION_EUROPEAN_NUMBER_SEPARATOR`**
-   **`IntlChar::CHAR_DIRECTION_EUROPEAN_NUMBER_TERMINATOR`**
-   **`IntlChar::CHAR_DIRECTION_ARABIC_NUMBER`**
-   **`IntlChar::CHAR_DIRECTION_COMMON_NUMBER_SEPARATOR`**
-   **`IntlChar::CHAR_DIRECTION_BLOCK_SEPARATOR`**
-   **`IntlChar::CHAR_DIRECTION_SEGMENT_SEPARATOR`**
-   **`IntlChar::CHAR_DIRECTION_WHITE_SPACE_NEUTRAL`**
-   **`IntlChar::CHAR_DIRECTION_OTHER_NEUTRAL`**
-   **`IntlChar::CHAR_DIRECTION_LEFT_TO_RIGHT_EMBEDDING`**
-   **`IntlChar::CHAR_DIRECTION_LEFT_TO_RIGHT_OVERRIDE`**
-   **`IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT_ARABIC`**
-   **`IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT_EMBEDDING`**
-   **`IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT_OVERRIDE`**
-   **`IntlChar::CHAR_DIRECTION_POP_DIRECTIONAL_FORMAT`**
-   **`IntlChar::CHAR_DIRECTION_DIR_NON_SPACING_MARK`**
-   **`IntlChar::CHAR_DIRECTION_BOUNDARY_NEUTRAL`**
-   **`IntlChar::CHAR_DIRECTION_FIRST_STRONG_ISOLATE`**
-   **`IntlChar::CHAR_DIRECTION_LEFT_TO_RIGHT_ISOLATE`**
-   **`IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT_ISOLATE`**
-   **`IntlChar::CHAR_DIRECTION_POP_DIRECTIONAL_ISOLATE`**
-   **`IntlChar::CHAR_DIRECTION_CHAR_DIRECTION_COUNT`**

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::charDirection("A") === IntlChar::CHAR_DIRECTION_LEFT_TO_RIGHT);
var_dump(IntlChar::charDirection("\u{05E9}") === IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT);
var_dump(IntlChar::charDirection("+") === IntlChar::CHAR_DIRECTION_EUROPEAN_NUMBER_SEPARATOR);
var_dump(IntlChar::charDirection(".") === IntlChar::CHAR_DIRECTION_COMMON_NUMBER_SEPARATOR);
?>
```

以上例程会输出：

    bool(true)
    bool(true)
    bool(true)
    bool(true)

IntlChar::charFromName
======================

Find Unicode character by name and return its code point value

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">IntlChar::charFromName</span> ( <span
class="methodparam"><span class="type">string</span>
`$characterName`</span> \[, <span class="methodparam"><span
class="type">int</span> `$nameChoice`<span class="initializer"> =
**`IntlChar::UNICODE_CHAR_NAME`**</span></span> \] )

Finds a Unicode character by its name and returns its code point value.

The name is matched exactly and completely. If the name does not
correspond to a code point, **`NULL`** is returned.

A Unicode 1.0 name is matched only if it differs from the modern name.
Unicode names are all uppercase. Extended names are lowercase followed
by an uppercase hexadecimal number, and within angle brackets.

### 参数

`characterName`  
Full name of the Unicode character.

`nameChoice`  
Which set of names to use for the lookup. Can be any of these constants:

-   **`IntlChar::UNICODE_CHAR_NAME`** (default)
-   **`IntlChar::UNICODE_10_CHAR_NAME`**
-   **`IntlChar::EXTENDED_CHAR_NAME`**
-   **`IntlChar::CHAR_NAME_ALIAS`**
-   **`IntlChar::CHAR_NAME_CHOICE_COUNT`**

### 返回值

The Unicode value of the code point with the given name (as an <span
class="type">integer</span>), or **`NULL`** if there is no such code
point.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::charFromName("LATIN CAPITAL LETTER A"));
var_dump(IntlChar::charFromName("SNOWMAN"));
var_dump(IntlChar::charFromName("RECYCLING SYMBOL FOR TYPE-1 PLASTICS"));
var_dump(IntlChar::charFromName("A RANDOM STRING WHICH DOESN'T CORRESPOND TO ANY UNICODE CHARACTER"));
?>
```

以上例程会输出：

    int(65)
    int(9731)
    int(9843)
    bool(false)

### 参见

-   <span class="function">IntlChar::charName</span>
-   <span class="function">IntlChar::enumCharNames</span>

IntlChar::charMirror
====================

Get the "mirror-image" character for a code point

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">mixed</span> <span
class="methodname">IntlChar::charMirror</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Maps the specified character to a "mirror-image" character.

For characters with the *Bidi\_Mirrored* property, implementations
sometimes need a "poor man's" mapping to another Unicode character (code
point) such that the default glyph may serve as the mirror-image of the
default glyph of the specified character. This is useful for text
conversion to and from codepages with visual order, and for displays
without glyph selection capabilities.

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns another Unicode code point that may serve as a mirror-image
substitute, or `codepoint` itself if there is no such mapping or
`codepoint` does not have the *Bidi\_Mirrored* property.

The return type will be <span class="type">integer</span> unless the
code point was passed as a UTF-8 <span class="type">string</span>, in
which case a <span class="type">string</span> will be returned.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::charMirror("A"));
var_dump(IntlChar::charMirror("<"));
var_dump(IntlChar::charMirror("("));
?>
```

以上例程会输出：

    string(1) "A"
    string(1) ">"
    string(2) ")"

### 参见

-   <span class="function">IntlChar::isMirrored</span>
-   **`IntlChar::PROPERTY_BIDI_MIRRORED`**

IntlChar::charName
==================

Retrieve the name of a Unicode character

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">IntlChar::charName</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$nameChoice`<span class="initializer"> =
**`IntlChar::UNICODE_CHAR_NAME`**</span></span> \] )

Retrieves the name of a Unicode character.

Depending on `nameChoice`, the resulting character name is the "modern"
name or the name that was defined in Unicode version 1.0. The name
contains only "invariant" characters like A-Z, 0-9, space, and '-'.
Unicode 1.0 names are only retrieved if they are different from the
modern names and if ICU contains the data for them.

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

`nameChoice`  
Which set of names to use for the lookup. Can be any of these constants:

-   **`IntlChar::UNICODE_CHAR_NAME`** (default)
-   **`IntlChar::UNICODE_10_CHAR_NAME`**
-   **`IntlChar::EXTENDED_CHAR_NAME`**
-   **`IntlChar::CHAR_NAME_ALIAS`**
-   **`IntlChar::CHAR_NAME_CHOICE_COUNT`**

### 返回值

The corresponding name, or an empty string if there is no name for this
character, or **`NULL`** if there is no such code point.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::charName("."));
var_dump(IntlChar::charName(".", IntlChar::UNICODE_CHAR_NAME));
var_dump(IntlChar::charName("\u{2603}"));
var_dump(IntlChar::charName("\u{0000}"));
?>
```

以上例程会输出：

    string(9) "FULL STOP"
    string(9) "FULL STOP"
    string(7) "SNOWMAN"
    string(0) ""

### 参见

-   <span class="function">IntlChar::charFromName</span>
-   <span class="function">IntlChar::enumCharNames</span>

IntlChar::charType
==================

Get the general category value for a code point

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">IntlChar::charType</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Returns the general category value for the code point.

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns the general category type, which may be one of the following
constants:

-   **`IntlChar::CHAR_CATEGORY_UNASSIGNED`**
-   **`IntlChar::CHAR_CATEGORY_GENERAL_OTHER_TYPES`**
-   **`IntlChar::CHAR_CATEGORY_UPPERCASE_LETTER`**
-   **`IntlChar::CHAR_CATEGORY_LOWERCASE_LETTER`**
-   **`IntlChar::CHAR_CATEGORY_TITLECASE_LETTER`**
-   **`IntlChar::CHAR_CATEGORY_MODIFIER_LETTER`**
-   **`IntlChar::CHAR_CATEGORY_OTHER_LETTER`**
-   **`IntlChar::CHAR_CATEGORY_NON_SPACING_MARK`**
-   **`IntlChar::CHAR_CATEGORY_ENCLOSING_MARK`**
-   **`IntlChar::CHAR_CATEGORY_COMBINING_SPACING_MARK`**
-   **`IntlChar::CHAR_CATEGORY_DECIMAL_DIGIT_NUMBER`**
-   **`IntlChar::CHAR_CATEGORY_LETTER_NUMBER`**
-   **`IntlChar::CHAR_CATEGORY_OTHER_NUMBER`**
-   **`IntlChar::CHAR_CATEGORY_SPACE_SEPARATOR`**
-   **`IntlChar::CHAR_CATEGORY_LINE_SEPARATOR`**
-   **`IntlChar::CHAR_CATEGORY_PARAGRAPH_SEPARATOR`**
-   **`IntlChar::CHAR_CATEGORY_CONTROL_CHAR`**
-   **`IntlChar::CHAR_CATEGORY_FORMAT_CHAR`**
-   **`IntlChar::CHAR_CATEGORY_PRIVATE_USE_CHAR`**
-   **`IntlChar::CHAR_CATEGORY_SURROGATE`**
-   **`IntlChar::CHAR_CATEGORY_DASH_PUNCTUATION`**
-   **`IntlChar::CHAR_CATEGORY_START_PUNCTUATION`**
-   **`IntlChar::CHAR_CATEGORY_END_PUNCTUATION`**
-   **`IntlChar::CHAR_CATEGORY_CONNECTOR_PUNCTUATION`**
-   **`IntlChar::CHAR_CATEGORY_OTHER_PUNCTUATION`**
-   **`IntlChar::CHAR_CATEGORY_MATH_SYMBOL`**
-   **`IntlChar::CHAR_CATEGORY_CURRENCY_SYMBOL`**
-   **`IntlChar::CHAR_CATEGORY_MODIFIER_SYMBOL`**
-   **`IntlChar::CHAR_CATEGORY_OTHER_SYMBOL`**
-   **`IntlChar::CHAR_CATEGORY_INITIAL_PUNCTUATION`**
-   **`IntlChar::CHAR_CATEGORY_FINAL_PUNCTUATION`**
-   **`IntlChar::CHAR_CATEGORY_CHAR_CATEGORY_COUNT`**

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::charType("A") === IntlChar::CHAR_CATEGORY_UPPERCASE_LETTER);
var_dump(IntlChar::charType(".") === IntlChar::CHAR_CATEGORY_OTHER_PUNCTUATION);
var_dump(IntlChar::charType("\t") === IntlChar::CHAR_CATEGORY_CONTROL_CHAR);
var_dump(IntlChar::charType("\u{2603}") === IntlChar::CHAR_CATEGORY_OTHER_SYMBOL);
?>
```

以上例程会输出：

    bool(true)
    bool(true)
    bool(true)
    bool(true)

IntlChar::chr
=============

Return Unicode character by code point value

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">IntlChar::chr</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Returns a string containing the character specified by the Unicode code
point value.

This function compliments <span class="function">IntlChar::ord</span>.

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

A string containing the single character specified by the Unicode code
point value.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
$values = ["A", 63, 123, 9731];
foreach ($values as $value) {
    var_dump(IntlChar::chr($value));
}
?>
```

以上例程会输出：

    string(1) "A"
    string(1) "?"
    string(1) "{"
    string(3) "☃"

### 参见

-   <span class="function">IntlChar::ord</span>
-   <span class="function">chr</span>

IntlChar::digit
===============

Get the decimal digit value of a code point for a given radix

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">IntlChar::digit</span> ( <span
class="methodparam"><span class="type">string</span> `$codepoint`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$radix`<span class="initializer"> = 10</span></span> \] )

Returns the decimal digit value of the code point in the specified
radix.

If the radix is not in the range *2\<=radix\<=36* or if the value of
`codepoint` is not a valid digit in the specified radix, **`FALSE`** is
returned. A character is a valid digit if at least one of the following
is true:

-   The character has a decimal digit value. Such characters have the
    general category "Nd" (decimal digit numbers) and a Numeric\_Type of
    Decimal. In this case the value is the character's decimal digit
    value.
-   The character is one of the uppercase Latin letters 'A' through 'Z'.
    In this case the value is c-'A'+10.
-   The character is one of the lowercase Latin letters 'a' through 'z'.
    In this case the value is ch-'a'+10.
-   Latin letters from both the ASCII range (0061..007A, 0041..005A) as
    well as from the Fullwidth ASCII range (FF41..FF5A, FF21..FF3A) are
    recognized.

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

`radix`  
The radix (defaults to *10*).

### 返回值

Returns the numeric value represented by the character in the specified
radix, or **`FALSE`** if there is no value or if the value exceeds the
radix.

**Warning**

此函数可能返回布尔值 **`FALSE`**，但也可能返回等同于 **`FALSE`**
的非布尔值。请阅读
<a href="/language/types/boolean.html" class="link">布尔类型</a>章节以获取更多信息。应使用
<a href="/language/operators/comparison.html" class="link">=== 运算符</a>来测试此函数的返回值。

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::digit("0"));
var_dump(IntlChar::digit("3"));
var_dump(IntlChar::digit("A"));
var_dump(IntlChar::digit("A", 16));
?>
```

以上例程会输出：

    int(0)
    int(3)
    bool(false)
    int(10)

### 参见

-   <span class="function">IntlChar::forDigit</span>
-   <span class="function">IntlChar::charDigitValue</span>
-   <span class="function">IntlChar::isdigit</span>
-   **`IntlChar::PROPERTY_NUMERIC_TYPE`**

IntlChar::enumCharNames
=======================

Enumerate all assigned Unicode characters within a range

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">IntlChar::enumCharNames</span> ( <span
class="methodparam"><span class="type">mixed</span> `$start`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$limit`</span> , <span class="methodparam"><span
class="type">callable</span> `$callback`</span> \[, <span
class="methodparam"><span class="type">int</span> `$nameChoice`<span
class="initializer"> = **`IntlChar::UNICODE_CHAR_NAME`**</span></span>
\] )

Enumerate all assigned Unicode characters between the start and limit
code points (start inclusive, limit exclusive) and call a function for
each, passing the code point value and the character name.

For Unicode 1.0 names, only those are enumerated that differ from the
modern names.

### 参数

`start`  
The first code point in the enumeration range.

`limit`  
One more than the last code point in the enumeration range (the first
one after the range).

`callback`  
The function that is to be called for each character name. The following
three arguments will be passed into it:

-   <span class="type">integer</span> *$codepoint* - The numeric code
    point value
-   <span class="type">integer</span> *$nameChoice* - The same value as
    the `nameChoice` parameter below
-   <span class="type">string</span> *$name* - The name of the character

`nameChoice`  
Selector for which kind of names to enumerate. Can be any of these
constants:

-   **`IntlChar::UNICODE_CHAR_NAME`** (default)
-   **`IntlChar::UNICODE_10_CHAR_NAME`**
-   **`IntlChar::EXTENDED_CHAR_NAME`**
-   **`IntlChar::CHAR_NAME_ALIAS`**
-   **`IntlChar::CHAR_NAME_CHOICE_COUNT`**

### 返回值

没有返回值。

### 范例

**示例 \#1 Enumerating over a sample range of code points**

``` php
<?php
IntlChar::enumCharNames(0x2600, 0x2610, function($codepoint, $nameChoice, $name) {
    printf("U+%04x %s\n", $codepoint, $name);
});
?>
```

以上例程会输出：

    U+2600 BLACK SUN WITH RAYS
    U+2601 CLOUD
    U+2602 UMBRELLA
    U+2603 SNOWMAN
    U+2604 COMET
    U+2605 BLACK STAR
    U+2606 WHITE STAR
    U+2607 LIGHTNING
    U+2608 THUNDERSTORM
    U+2609 SUN
    U+260a ASCENDING NODE
    U+260b DESCENDING NODE
    U+260c CONJUNCTION
    U+260d OPPOSITION
    U+260e BLACK TELEPHONE
    U+260f WHITE TELEPHONE

### 参见

-   <span class="function">IntlChar::charName</span>
-   <span class="function">IntlChar::charFromName</span>

IntlChar::enumCharTypes
=======================

Enumerate all code points with their Unicode general categories

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">IntlChar::enumCharTypes</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

Enumerates efficiently all code points with their Unicode general
categories. This is useful for building data structures, for enumerating
all assigned code points, etc.

For each contiguous range of code points with a given general category
("character type"), the `callback` function is called. Adjacent ranges
have different types. The Unicode Standard guarantees that the numeric
value of the type is 0..31.

### 参数

`callback`  
The function that is to be called for each contiguous range of code
points with the same general category. The following three arguments
will be passed into it:

-   <span class="type">integer</span> *$start* - The starting code point
    of the range
-   <span class="type">integer</span> *$end* - The ending code point of
    the range
-   <span class="type">integer</span> *$name* - The category type (one
    of the *IntlChar::CHAR\_CATEGORY\_\** constants)

### 返回值

没有返回值。

### 范例

**示例 \#1 Enumerating over a sample range of code points**

``` php
<?php
IntlChar::enumCharTypes(function($start, $end, $type) {
    printf("U+%04x through U+%04x are in category %d\n", $start, $end, $type);
});
?>
```

以上例程会输出：

    U+0000 through U+0020 are in category 15
    U+0020 through U+0021 are in category 12
    U+0021 through U+0024 are in category 23
    U+0024 through U+0025 are in category 25
    U+0025 through U+0028 are in category 23
    U+0028 through U+0029 are in category 20
    U+0029 through U+002a are in category 21
    U+002a through U+002b are in category 23
    U+002b through U+002c are in category 24
    U+002c through U+002d are in category 23
    U+002d through U+002e are in category 19
    U+002e through U+0030 are in category 23
    U+0030 through U+003a are in category 9
    ...

IntlChar::foldCase
==================

Perform case folding on a code point

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">mixed</span> <span
class="methodname">IntlChar::foldCase</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$options`<span class="initializer"> =
**`IntlChar::FOLD_CASE_DEFAULT`**</span></span> \] )

The given character is mapped to its case folding equivalent; if the
character has no case folding equivalent, the character itself is
returned.

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

`options`  
Either **`IntlChar::FOLD_CASE_DEFAULT`** (default) or
**`IntlChar::FOLD_CASE_EXCLUDE_SPECIAL_I`**.

### 返回值

Returns the *Simple\_Case\_Folding* of the code point, if any; otherwise
the code point itself.

IntlChar::forDigit
==================

Get character representation for a given digit and radix

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">IntlChar::forDigit</span> ( <span
class="methodparam"><span class="type">int</span> `$digit`</span> \[,
<span class="methodparam"><span class="type">int</span> `$radix`<span
class="initializer"> = 10</span></span> \] )

Determines the character representation for a specific digit in the
specified radix.

If the value of radix is not a valid radix, or the value of digit is not
a valid digit in the specified radix, the null character (*U+0000*) is
returned.

The radix argument is valid if it is greater than or equal to *2* and
less than or equal to *36*. The digit argument is valid if *0 \<= digit
\< radix*.

If the digit is less than *10*, then '0' + digit is returned. Otherwise,
the value 'a' + digit - 10 is returned.

### 参数

`digit`  
The number to convert to a character.

`radix`  
The radix (defaults to *10*).

### 返回值

The character representation (as a <span class="type">string</span>) of
the specified digit in the specified radix.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::forDigit(0));
var_dump(IntlChar::forDigit(3));
var_dump(IntlChar::forDigit(3, 10));
var_dump(IntlChar::forDigit(10));
var_dump(IntlChar::forDigit(10, 16));
?>
```

以上例程会输出：

    int(48)
    int(51)
    int(51)
    int(0)
    int(97)

### 参见

-   <span class="function">IntlChar::digit</span>
-   <span class="function">IntlChar::charDigitValue</span>
-   <span class="function">IntlChar::isdigit</span>
-   **`IntlChar::PROPERTY_NUMERIC_TYPE`**

IntlChar::getBidiPairedBracket
==============================

Get the paired bracket character for a code point

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">mixed</span> <span
class="methodname">IntlChar::getBidiPairedBracket</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Maps the specified character to its paired bracket character.

For *Bidi\_Paired\_Bracket\_Type!=None*, this is the same as <span
class="function">IntlChar::charMirror</span>. Otherwise `codepoint`
itself is returned.

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns the paired bracket code point, or `codepoint` itself if there is
no such mapping.

The return type will be <span class="type">integer</span> unless the
code point was passed as a UTF-8 <span class="type">string</span>, in
which case a <span class="type">string</span> will be returned.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::getBidiPairedBracket(91));
var_dump(IntlChar::getBidiPairedBracket('['));
?>
```

以上例程会输出：

    int(93)
    string(1) "]"

### 参见

-   <span class="function">IntlChar::charMirror</span>
-   **`IntlChar::PROPERTY_BIDI_PAIRED_BRACKET`**
-   **`IntlChar::PROPERTY_BIDI_PAIRED_BRACKET_TYPE`**

IntlChar::getBlockCode
======================

Get the Unicode allocation block containing a code point

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">IntlChar::getBlockCode</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Returns the Unicode allocation block that contains the character.

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns the block value for `codepoint`. See the
*IntlChar::BLOCK\_CODE\_\** constants for possible return values.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::getBlockCode("A") === IntlChar::BLOCK_CODE_BASIC_LATIN);
var_dump(IntlChar::getBlockCode("Φ") === IntlChar::BLOCK_CODE_GREEK);
var_dump(IntlChar::getBlockCode("\u{2603}") === IntlChar::BLOCK_CODE_MISCELLANEOUS_SYMBOLS);
?>
```

以上例程会输出：

    bool(true)
    bool(true)
    bool(true)

IntlChar::getCombiningClass
===========================

Get the combining class of a code point

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">IntlChar::getCombiningClass</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Returns the combining class of the code point.

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns the combining class of the character.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::getCombiningClass("A"));
var_dump(IntlChar::getCombiningClass("\u{0334}"));
var_dump(IntlChar::getCombiningClass("\u{0358}"));
?>
```

以上例程会输出：

    int(0)
    int(1)
    int(232)

IntlChar::getFC\_NFKC\_Closure
==============================

Get the FC\_NFKC\_Closure property for a code point

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">IntlChar::getFC\_NFKC\_Closure</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Gets the FC\_NFKC\_Closure property string for a character.

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns the FC\_NFKC\_Closure property string for the `codepoint`, or an
empty string if there is none.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::getFC_NFKC_Closure("\u{2121}"));
var_dump(IntlChar::getFC_NFKC_Closure("\u{1D2D}"));
?>
```

以上例程会输出：

    string(3) "tel"
    string(2) "æ"

IntlChar::getIntPropertyMaxValue
================================

Get the max value for a Unicode property

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">IntlChar::getIntPropertyMaxValue</span> ( <span
class="methodparam"><span class="type">int</span> `$property`</span> )

Gets the maximum value for an enumerated/integer/binary Unicode
property.

### 参数

`property`  
The Unicode property to lookup (see the *IntlChar::PROPERTY\_\**
constants).

### 返回值

The maximum value returned by <span
class="function">IntlChar::getIntPropertyValue</span> for a Unicode
property. *\<=0* if the property selector is out of range.

### 范例

**示例 \#1 Testing different properties**

``` php
<?php
var_dump(IntlChar::getIntPropertyMaxValue(IntlChar::PROPERTY_BIDI_CLASS));
var_dump(IntlChar::getIntPropertyMaxValue(IntlChar::PROPERTY_SCRIPT));
var_dump(IntlChar::getIntPropertyMaxValue(IntlChar::PROPERTY_IDEOGRAPHIC));
var_dump(IntlChar::getIntPropertyMaxValue(999999999)); // Some made-up value
?>
```

以上例程会输出：

    int(22)
    int(166)
    int(1)
    int(-1)

### 参见

-   <span class="function">IntlChar::hasBinaryProperty</span>
-   <span class="function">IntlChar::getIntPropertyMinValue</span>
-   <span class="function">IntlChar::getIntPropertyValue</span>
-   <span class="function">IntlChar::getUnicodeVersion</span>

IntlChar::getIntPropertyMinValue
================================

Get the min value for a Unicode property

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">IntlChar::getIntPropertyMinValue</span> ( <span
class="methodparam"><span class="type">int</span> `$property`</span> )

Gets the minimum value for an enumerated/integer/binary Unicode
property.

### 参数

`property`  
The Unicode property to lookup (see the *IntlChar::PROPERTY\_\**
constants).

### 返回值

The minimum value returned by <span
class="function">IntlChar::getIntPropertyValue</span> for a Unicode
property. *0* if the property selector is out of range.

### 范例

**示例 \#1 Testing different properties**

``` php
<?php
var_dump(IntlChar::getIntPropertyMinValue(IntlChar::PROPERTY_BIDI_CLASS));
var_dump(IntlChar::getIntPropertyMinValue(IntlChar::PROPERTY_SCRIPT));
var_dump(IntlChar::getIntPropertyMinValue(IntlChar::PROPERTY_IDEOGRAPHIC));
var_dump(IntlChar::getIntPropertyMinValue(999999999)); // Some made-up value
?>
```

以上例程会输出：

    int(0)
    int(0)
    int(0)
    int(0)

### 参见

-   <span class="function">IntlChar::hasBinaryProperty</span>
-   <span class="function">IntlChar::getIntPropertyMaxValue</span>
-   <span class="function">IntlChar::getIntPropertyValue</span>
-   <span class="function">IntlChar::getUnicodeVersion</span>

IntlChar::getIntPropertyValue
=============================

Get the value for a Unicode property for a code point

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">IntlChar::getIntPropertyValue</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
, <span class="methodparam"><span class="type">int</span>
`$property`</span> )

Gets the property value for an enumerated or integer Unicode property
for a code point. Also returns binary and mask property values.

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

`property`  
The Unicode property to lookup (see the *IntlChar::PROPERTY\_\**
constants).

### 返回值

Returns the numeric value that is directly the property value or, for
enumerated properties, corresponds to the numeric value of the
enumerated constant of the respective property value enumeration type.

Returns *0* or *1* (for **`FALSE`**/**`TRUE`**) for binary Unicode
properties.

Returns a bit-mask for mask properties.

Returns *0* if `property` is out of bounds or if the Unicode version
does not have data for the property at all, or not for this code point.

### 范例

**示例 \#1 Testing different properties**

``` php
<?php
var_dump(IntlChar::getIntPropertyValue("A", IntlChar::PROPERTY_ALPHABETIC) === 1);
var_dump(IntlChar::getIntPropertyValue("[", IntlChar::PROPERTY_BIDI_MIRRORED) === 1);
var_dump(IntlChar::getIntPropertyValue("Φ", IntlChar::PROPERTY_BLOCK) === IntlChar::BLOCK_CODE_GREEK);
?>
```

以上例程会输出：

    bool(true)
    bool(true)
    bool(true)

### 参见

-   <span class="function">IntlChar::hasBinaryProperty</span>
-   <span class="function">IntlChar::getIntPropertyMinValue</span>
-   <span class="function">IntlChar::getIntPropertyMaxValue</span>
-   <span class="function">IntlChar::getUnicodeVersion</span>

IntlChar::getNumericValue
=========================

Get the numeric value for a Unicode code point

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">float</span> <span
class="methodname">IntlChar::getNumericValue</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Gets the numeric value for a Unicode code point as defined in the
Unicode Character Database.

For characters without any numeric values in the Unicode Character
Database, this function will return **`IntlChar::NO_NUMERIC_VALUE`**.

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Numeric value of `codepoint`, or **`IntlChar::NO_NUMERIC_VALUE`** if
none is defined. This constant was added in PHP 7.0.6, prior to this
version the literal value (<span class="type">float</span>)*-123456789*
may be used instead.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::getNumericValue("4"));
var_dump(IntlChar::getNumericValue("x"));
var_dump(IntlChar::getNumericValue("\u{216C}"));
?>
```

以上例程会输出：

    float(4)
    float(-123456789)
    float(50)

IntlChar::getPropertyEnum
=========================

Get the property constant value for a given property name

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">IntlChar::getPropertyEnum</span> ( <span
class="methodparam"><span class="type">string</span> `$alias`</span> )

Returns the property constant value for a given property name, as
specified in the Unicode database file PropertyAliases.txt. Short, long,
and any other variants are recognized.

In addition, this function maps the synthetic names "gcm" /
"General\_Category\_Mask" to the property
**`IntlChar::PROPERTY_GENERAL_CATEGORY_MASK`**. These names are not in
PropertyAliases.txt.

This function compliments <span
class="function">IntlChar::getPropertyName</span>.

### 参数

`alias`  
The property name to be matched. The name is compared using "loose
matching" as described in PropertyAliases.txt.

### 返回值

Returns an *IntlChar::PROPERTY\_* constant value, or
**`IntlChar::PROPERTY_INVALID_CODE`** if the given name does not match
any property.

### 范例

**示例 \#1 Testing different properties**

``` php
<?php
var_dump(IntlChar::getPropertyEnum('Bidi_Class') === IntlChar::PROPERTY_BIDI_CLASS);
var_dump(IntlChar::getPropertyEnum('script') === IntlChar::PROPERTY_SCRIPT);
var_dump(IntlChar::getPropertyEnum('IDEOGRAPHIC') === IntlChar::PROPERTY_IDEOGRAPHIC);
var_dump(IntlChar::getPropertyEnum('Some made-up string') === IntlChar::PROPERTY_INVALID_CODE);
?>
```

以上例程会输出：

    bool(true)
    bool(true)
    bool(true)
    bool(true)

### 参见

-   <span class="function">IntlChar::getPropertyName</span>

IntlChar::getPropertyName
=========================

Get the Unicode name for a property

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">IntlChar::getPropertyName</span> ( <span
class="methodparam"><span class="type">int</span> `$property`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$nameChoice`<span class="initializer"> =
**`IntlChar::LONG_PROPERTY_NAME`**</span></span> \] )

Returns the Unicode name for a given property, as given in the Unicode
database file PropertyAliases.txt.

In addition, this function maps the property
**`IntlChar::PROPERTY_GENERAL_CATEGORY_MASK`** to the synthetic names
"gcm" / "General\_Category\_Mask". These names are not in
PropertyAliases.txt.

This function compliments <span
class="function">IntlChar::getPropertyEnum</span>.

### 参数

`property`  
The Unicode property to lookup (see the *IntlChar::PROPERTY\_\**
constants).

**`IntlChar::PROPERTY_INVALID_CODE`** should not be used. Also, if
`property` is out of range, **`FALSE`** is returned.

`nameChoice`  
Selector for which name to get. If out of range, **`FALSE`** is
returned.

All properties have a long name. Most have a short name, but some do
not. Unicode allows for additional names; if present these will be
returned by adding 1, 2, etc. to **`IntlChar::LONG_PROPERTY_NAME`**.

### 返回值

Returns the name, or **`FALSE`** if either the `property` or the
`nameChoice` is out of range.

If a given `nameChoice` returns **`FALSE`**, then all larger values of
`nameChoice` will return **`FALSE`**, with one exception: if **`FALSE`**
is returned for **`IntlChar::SHORT_PROPERTY_NAME`**, then
**`IntlChar::LONG_PROPERTY_NAME`** (and higher) may still return a
non-**`FALSE`** value.

### 范例

**示例 \#1 Testing different properties**

``` php
<?php
var_dump(IntlChar::getPropertyName(IntlChar::PROPERTY_BIDI_CLASS));
var_dump(IntlChar::getPropertyName(IntlChar::PROPERTY_BIDI_CLASS, IntlChar::SHORT_PROPERTY_NAME));
var_dump(IntlChar::getPropertyName(IntlChar::PROPERTY_BIDI_CLASS, IntlChar::LONG_PROPERTY_NAME));
var_dump(IntlChar::getPropertyName(IntlChar::PROPERTY_BIDI_CLASS, IntlChar::LONG_PROPERTY_NAME + 1));
?>
```

以上例程会输出：

    string(10) "Bidi_Class"
    string(2) "bc"
    string(10) "Bidi_Class"
    bool(false)

### 参见

-   <span class="function">IntlChar::getPropertyEnum</span>

IntlChar::getPropertyValueEnum
==============================

Get the property value for a given value name

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">IntlChar::getPropertyValueEnum</span> ( <span
class="methodparam"><span class="type">int</span> `$property`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> )

Returns the property value integer for a given value name, as specified
in the Unicode database file PropertyValueAliases.txt. Short, long, and
any other variants are recognized.

> **Note**:
>
> Some of the names in PropertyValueAliases.txt will only be recognized
> with **`IntlChar::PROPERTY_GENERAL_CATEGORY_MASK`**, not
> **`IntlChar::PROPERTY_GENERAL_CATEGORY`**. These include:
>
> -   "C" / "Other"
> -   "L" / "Letter"
> -   "LC" / "Cased\_Letter"
> -   "M" / "Mark"
> -   "N" / "Number"
> -   "P" / "Punctuation"
> -   "S" / "Symbol"
> -   "Z" / "Separator"

### 参数

`property`  
The Unicode property to lookup (see the *IntlChar::PROPERTY\_\**
constants).

If out of range, or this method doesn't work with the given value,
**`IntlChar::PROPERTY_INVALID_CODE`** is returned.

`name`  
The value name to be matched. The name is compared using "loose
matching" as described in PropertyValueAliases.txt.

### 返回值

Returns the corresponding value integer, or
**`IntlChar::PROPERTY_INVALID_CODE`** if the given name does not match
any value of the given property, or if the property is invalid.

### 范例

**示例 \#1 Testing different properties**

``` php
<?php
var_dump(IntlChar::getPropertyValueEnum(IntlChar::PROPERTY_BLOCK, 'greek') === IntlChar::BLOCK_CODE_GREEK);
var_dump(IntlChar::getPropertyValueEnum(IntlChar::PROPERTY_BIDI_CLASS, 'RIGHT_TO_LEFT') === IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT);
var_dump(IntlChar::getPropertyValueEnum(IntlChar::PROPERTY_BIDI_CLASS, 'some made-up string') === IntlChar::PROPERTY_INVALID_CODE);
var_dump(IntlChar::getPropertyValueEnum(123456789, 'RIGHT_TO_LEFT') === IntlChar::PROPERTY_INVALID_CODE);
?>
```

以上例程会输出：

    bool(true)
    bool(true)
    bool(true)
    bool(true)

IntlChar::getPropertyValueName
==============================

Get the Unicode name for a property value

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">IntlChar::getPropertyValueName</span> ( <span
class="methodparam"><span class="type">int</span> `$property`</span> ,
<span class="methodparam"><span class="type">int</span> `$value`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$nameChoice`<span class="initializer"> =
**`IntlChar::LONG_PROPERTY_NAME`**</span></span> \] )

Returns the Unicode name for a given property value, as given in the
Unicode database file PropertyValueAliases.txt.

> **Note**:
>
> Some of the names in PropertyValueAliases.txt can only be retrieved
> using **`IntlChar::PROPERTY_GENERAL_CATEGORY_MASK`**, not
> **`IntlChar::PROPERTY_GENERAL_CATEGORY`**. These include:
>
> -   "C" / "Other"
> -   "L" / "Letter"
> -   "LC" / "Cased\_Letter"
> -   "M" / "Mark"
> -   "N" / "Number"
> -   "P" / "Punctuation"
> -   "S" / "Symbol"
> -   "Z" / "Separator"

### 参数

`property`  
The Unicode property to lookup (see the *IntlChar::PROPERTY\_\**
constants).

If out of range, or this method doesn't work with the given value,
**`FALSE`** is returned.

`value`  
Selector for a value for the given property. If out of range,
**`FALSE`** is returned.

In general, valid values range from *0* up to some maximum. There are a
couple exceptions:

-   **`IntlChar::PROPERTY_BLOCK`** values begin at the non-zero value
    **`IntlChar::BLOCK_CODE_BASIC_LATIN`**
-   **`IntlChar::PROPERTY_CANONICAL_COMBINING_CLASS`** values are not
    contiguous and range from 0..240.

`nameChoice`  
Selector for which name to get. If out of range, **`FALSE`** is
returned.

All values have a long name. Most have a short name, but some do not.
Unicode allows for additional names; if present these will be returned
by adding 1, 2, etc. to **`IntlChar::LONG_PROPERTY_NAME`**.

### 返回值

Returns the name, or **`FALSE`** if either the `property` or the
`nameChoice` is out of range.

If a given `nameChoice` returns **`FALSE`**, then all larger values of
`nameChoice` will return **`FALSE`**, with one exception: if **`FALSE`**
is returned for **`IntlChar::SHORT_PROPERTY_NAME`**, then
**`IntlChar::LONG_PROPERTY_NAME`** (and higher) may still return a
non-**`FALSE`** value.

### 范例

**示例 \#1 Testing different properties**

``` php
<?php
var_dump(IntlChar::getPropertyValueName(IntlChar::PROPERTY_BLOCK, IntlChar::BLOCK_CODE_GREEK));
var_dump(IntlChar::getPropertyValueName(IntlChar::PROPERTY_BLOCK, IntlChar::BLOCK_CODE_GREEK, IntlChar::SHORT_PROPERTY_NAME));
var_dump(IntlChar::getPropertyValueName(IntlChar::PROPERTY_BLOCK, IntlChar::BLOCK_CODE_GREEK, IntlChar::LONG_PROPERTY_NAME));
var_dump(IntlChar::getPropertyValueName(IntlChar::PROPERTY_BLOCK, IntlChar::BLOCK_CODE_GREEK, IntlChar::LONG_PROPERTY_NAME + 1));
?>
```

以上例程会输出：

    string(16) "Greek_And_Coptic"
    string(5) "Greek"
    string(16) "Greek_And_Coptic"
    bool(false)

IntlChar::getUnicodeVersion
===========================

Get the Unicode version

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">IntlChar::getUnicodeVersion</span> ( <span
class="methodparam">void</span> )

Gets the Unicode version information.

The version array is filled in with the version information for the
Unicode standard that is currently used by ICU. For example, Unicode
version 3.1.1 is represented as an array with the values *\[3, 1, 1,
0\]*.

### 参数

此函数没有参数。

### 返回值

An array containing the Unicode version number.

### 范例

**示例 \#1 Testing different properties**

``` php
<?php
var_dump(IntlChar::getUnicodeVersion());
?>
```

以上例程会输出：

    array(4) {
      [0]=>
      int(7)
      [1]=>
      int(0)
      [2]=>
      int(0)
      [3]=>
      int(0)
    }

### 参见

-   <span class="function">IntlChar::charAge</span>

IntlChar::hasBinaryProperty
===========================

Check a binary Unicode property for a code point

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">IntlChar::hasBinaryProperty</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
, <span class="methodparam"><span class="type">int</span>
`$property`</span> )

Checks a binary Unicode property for a code point.

Unicode, especially in version 3.2, defines many more properties than
the original set in UnicodeData.txt.

The properties APIs are intended to reflect Unicode properties as
defined in the Unicode Character Database (UCD) and Unicode Technical
Reports (UTR). For details about the properties see
<a href="http://www.unicode.org/ucd/" class="link external">» http://www.unicode.org/ucd/</a>.
For names of Unicode properties see the UCD file PropertyAliases.txt.

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

`property`  
The Unicode property to lookup (see the *IntlChar::PROPERTY\_\**
constants).

### 返回值

Returns **`TRUE`** or **`FALSE`** according to the binary Unicode
property value for `codepoint`. Also **`FALSE`** if `property` is out of
bounds or if the Unicode version does not have data for the property at
all, or not for this code point.

### 范例

**示例 \#1 Testing different properties**

``` php
<?php
var_dump(IntlChar::hasBinaryProperty("A", IntlChar::PROPERTY_ALPHABETIC));
var_dump(IntlChar::hasBinaryProperty("A", IntlChar::PROPERTY_CASE_SENSITIVE));
var_dump(IntlChar::hasBinaryProperty("A", IntlChar::PROPERTY_BIDI_MIRRORED));
var_dump(IntlChar::hasBinaryProperty("[", IntlChar::PROPERTY_ALPHABETIC));
var_dump(IntlChar::hasBinaryProperty("[", IntlChar::PROPERTY_CASE_SENSITIVE));
var_dump(IntlChar::hasBinaryProperty("[", IntlChar::PROPERTY_BIDI_MIRRORED));
?>
```

以上例程会输出：

    bool(true)
    bool(true)
    bool(false)
    bool(false)
    bool(false)
    bool(true)

### 参见

-   <span class="function">IntlChar::getIntPropertyValue</span>
-   <span class="function">IntlChar::getUnicodeVersion</span>

IntlChar::isalnum
=================

Check if code point is an alphanumeric character

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">IntlChar::isalnum</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Determines whether the specified code point is an alphanumeric character
(letter or digit). **`TRUE`** for characters with general categories "L"
(letters) and "Nd" (decimal digit numbers).

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns **`TRUE`** if `codepoint` is an alphanumeric character,
**`FALSE`** if not.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::isalnum("A"));
var_dump(IntlChar::isalnum("1"));
var_dump(IntlChar::isalnum("\u{2603}"));
?>
```

以上例程会输出：

    bool(true)
    bool(true)
    bool(false)

### 参见

-   <span class="function">IntlChar::isalpha</span>
-   <span class="function">IntlChar::isdigit</span>

IntlChar::isalpha
=================

Check if code point is a letter character

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">IntlChar::isalpha</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Determines whether the specified code point is a letter character.
**`TRUE`** for general categories "L" (letters).

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns **`TRUE`** if `codepoint` is a letter character, **`FALSE`** if
not.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::isalpha("A"));
var_dump(IntlChar::isalpha("1"));
var_dump(IntlChar::isalpha("\u{2603}"));
?>
```

以上例程会输出：

    bool(true)
    bool(false)
    bool(false)

### 参见

-   <span class="function">IntlChar::isalnum</span>
-   <span class="function">IntlChar::isdigit</span>

IntlChar::isbase
================

Check if code point is a base character

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">IntlChar::isbase</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Determines whether the specified code point is a base character.
**`TRUE`** for general categories "L" (letters), "N" (numbers), "Mc"
(spacing combining marks), and "Me" (enclosing marks).

> **Note**:
>
> This is different from the Unicode definition in chapter 3.5,
> conformance clause D13, which defines base characters to be all
> characters (not Cn) that do not graphically combine with preceding
> characters (M) and that are neither control (Cc) or format (Cf)
> characters.

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns **`TRUE`** if `codepoint` is a base character, **`FALSE`** if
not.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::isbase("A"));
var_dump(IntlChar::isbase("1"));
var_dump(IntlChar::isbase("\u{2603}"));
?>
```

以上例程会输出：

    bool(true)
    bool(true)
    bool(false)

### 参见

-   <span class="function">IntlChar::isalpha</span>
-   <span class="function">IntlChar::isdigit</span>

IntlChar::isblank
=================

Check if code point is a "blank" or "horizontal space" character

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">IntlChar::isblank</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Determines whether the specified code point is a "blank" or "horizontal
space", a character that visibly separates words on a line.

The following are equivalent definitions:

-   **`TRUE`** for Unicode White\_Space characters except for "vertical
    space controls" where "vertical space controls" are the following
    characters: U+000A (LF) U+000B (VT) U+000C (FF) U+000D (CR) U+0085
    (NEL) U+2028 (LS) U+2029 (PS)
-   **`TRUE`** for U+0009 (TAB) and characters with general category
    "Zs" (space separators) except Zero Width Space (ZWSP, U+200B).

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns **`TRUE`** if `codepoint` is either a "blank" or "horizontal
space" character, **`FALSE`** if not.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::isblank("A"));
var_dump(IntlChar::isblank(" "));
var_dump(IntlChar::isblank("\t"));
?>
```

以上例程会输出：

    bool(false)
    bool(true)
    bool(true)

### 参见

-   <span class="function">IntlChar::isspace</span>
-   <span class="function">IntlChar::isJavaSpaceChar</span>
-   <span class="function">IntlChar::isUWhiteSpace</span>
-   <span class="function">IntlChar::isWhitespace</span>

IntlChar::iscntrl
=================

Check if code point is a control character

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">IntlChar::iscntrl</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Determines whether the specified code point is a control character.

A control character is one of the following:

-   ISO 8-bit control character (U+0000..U+001f and U+007f..U+009f)
-   **`IntlChar::CHAR_CATEGORY_CONTROL_CHAR`** (Cc)
-   **`IntlChar::CHAR_CATEGORY_FORMAT_CHAR`** (Cf)
-   **`IntlChar::CHAR_CATEGORY_LINE_SEPARATOR`** (Zl)
-   **`IntlChar::CHAR_CATEGORY_PARAGRAPH_SEPARATOR`** (Zp)

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns **`TRUE`** if `codepoint` is a control character, **`FALSE`** if
not.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::iscntrl("A"));
var_dump(IntlChar::iscntrl(" "));
var_dump(IntlChar::iscntrl("\n"));
var_dump(IntlChar::iscntrl("\u{200e}"));
?>
```

以上例程会输出：

    bool(false)
    bool(false)
    bool(true)
    bool(true)

### 参见

-   <span class="function">IntlChar::isprint</span>
-   **`IntlChar::PROPERTY_DEFAULT_IGNORABLE_CODE_POINT`**

IntlChar::isdefined
===================

Check whether the code point is defined

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">IntlChar::isdefined</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Determines whether the specified code point is "defined", which usually
means that it is assigned a character.

**`TRUE`** for general categories other than "Cn" (other, not assigned).

> **Note**:
>
> Note that non-character code points (e.g., U+FDD0) are not "defined"
> (they are Cn), but surrogate code points are "defined" (Cs).

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns **`TRUE`** if `codepoint` is a defined character, **`FALSE`** if
not.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::isdefined("A"));
var_dump(IntlChar::isdefined(" "));
var_dump(IntlChar::isdefined("\u{FDD0}"));
?>
```

以上例程会输出：

    bool(true)
    bool(true)
    bool(false)

### 参见

-   <span class="function">IntlChar::isdigit</span>
-   <span class="function">IntlChar::isalpha</span>
-   <span class="function">IntlChar::isalnum</span>
-   <span class="function">IntlChar::isupper</span>
-   <span class="function">IntlChar::islower</span>
-   <span class="function">IntlChar::istitle</span>

IntlChar::isdigit
=================

Check if code point is a digit character

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">IntlChar::isdigit</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Determines whether the specified code point is a digit character.

**`TRUE`** for characters with general category "Nd" (decimal digit
numbers). Beginning with Unicode 4, this is the same as testing for the
Numeric\_Type of Decimal.

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns **`TRUE`** if `codepoint` is a digit character, **`FALSE`** if
not.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::isdigit("A"));
var_dump(IntlChar::isdigit("1"));
var_dump(IntlChar::isdigit("\t"));
?>
```

以上例程会输出：

    bool(false)
    bool(true)
    bool(false)

### 参见

-   <span class="function">IntlChar::isalpha</span>
-   <span class="function">IntlChar::isalnum</span>
-   <span class="function">IntlChar::isxdigit</span>

IntlChar::isgraph
=================

Check if code point is a graphic character

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">IntlChar::isgraph</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Determines whether the specified code point is a "graphic" character
(printable, excluding spaces).

**`TRUE`** for all characters except those with general categories "Cc"
(control codes), "Cf" (format controls), "Cs" (surrogates), "Cn"
(unassigned), and "Z" (separators).

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns **`TRUE`** if `codepoint` is a "graphic" character, **`FALSE`**
if not.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::isgraph("A"));
var_dump(IntlChar::isgraph("1"));
var_dump(IntlChar::isgraph("\u{2603}"));
var_dump(IntlChar::isgraph("\n"));
?>
```

以上例程会输出：

    bool(true)
    bool(true)
    bool(true)
    bool(false)

IntlChar::isIDIgnorable
=======================

Check if code point is an ignorable character

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">IntlChar::isIDIgnorable</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Determines if the specified character should be regarded as an ignorable
character in an identifier.

**`TRUE`** for characters with general category "Cf" (format controls)
as well as non-whitespace ISO controls (U+0000..U+0008, U+000E..U+001B,
U+007F..U+009F).

> **Note**:
>
> Note that Unicode just recommends to ignore Cf (format controls).

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns **`TRUE`** if `codepoint` is ignorable in identifiers,
**`FALSE`** if not.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::isIDIgnorable("A"));
var_dump(IntlChar::isIDIgnorable(" "));
var_dump(IntlChar::isIDIgnorable("\u{007F}"));
?>
```

以上例程会输出：

    bool(false)
    bool(false)
    bool(true)

### 参见

-   <span class="function">IntlChar::isIDStart</span>
-   <span class="function">IntlChar::isIDPart</span>
-   **`IntlChar::PROPERTY_DEFAULT_IGNORABLE_CODE_POINT`**

IntlChar::isIDPart
==================

Check if code point is permissible in an identifier

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">IntlChar::isIDPart</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Determines if the specified character is permissible in an identifier.

**`TRUE`** for characters with general categories "L" (letters), "Nl"
(letter numbers), "Nd" (decimal digits), "Mc" and "Mn" (combining
marks), "Pc" (connecting punctuation), and u\_isIDIgnorable(c).

> **Note**:
>
> This is almost the same as Unicode's ID\_Continue
> (**`IntlChar::PROPERTY_ID_CONTINUE`**) except that Unicode recommends
> to ignore Cf which is less than <span
> class="function">IntlChar::isIDIgnorable</span>.

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns **`TRUE`** if `codepoint` is the code point may occur in an
identifier, **`FALSE`** if not.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::isIDPart("A"));
var_dump(IntlChar::isIDPart("$"));
var_dump(IntlChar::isIDPart("\n"));
var_dump(IntlChar::isIDPart("\u{2603}"));
?>
```

以上例程会输出：

    bool(true)
    bool(false)
    bool(false)
    bool(false)

### 参见

-   <span class="function">IntlChar::isIDIgnorable</span>
-   <span class="function">IntlChar::isIDStart</span>
-   **`IntlChar::PROPERTY_ID_CONTINUE`**

IntlChar::isIDStart
===================

Check if code point is permissible as the first character in an
identifier

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">IntlChar::isIDStart</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Determines if the specified character is permissible as the first
character in an identifier according to Unicode (The Unicode Standard,
Version 3.0, chapter 5.16 Identifiers).

**`TRUE`** for characters with general categories "L" (letters) and "Nl"
(letter numbers).

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns **`TRUE`** if `codepoint` may start an identifier, **`FALSE`**
if not.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::isIDStart("A"));
var_dump(IntlChar::isIDStart("$"));
var_dump(IntlChar::isIDStart("\n"));
var_dump(IntlChar::isIDStart("\u{2603}"));
?>
```

以上例程会输出：

    bool(true)
    bool(false)
    bool(false)
    bool(false)

### 参见

-   <span class="function">IntlChar::isalpha</span>
-   <span class="function">IntlChar::isIDPart</span>
-   **`IntlChar::PROPERTY_ID_START`**

IntlChar::isISOControl
======================

Check if code point is an ISO control code

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">IntlChar::isISOControl</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Determines whether the specified code point is an ISO control code.

**`TRUE`** for U+0000..U+001f and U+007f..U+009f (general category
"Cc").

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns **`TRUE`** if `codepoint` is an ISO control code, **`FALSE`** if
not.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::isISOControl(" "));
var_dump(IntlChar::isISOControl("\n"));
var_dump(IntlChar::isISOControl("\u{200e}"));
?>
```

以上例程会输出：

    bool(false)
    bool(true)
    bool(false)

### 参见

-   <span class="function">IntlChar::iscntrl</span>

IntlChar::isJavaIDPart
======================

Check if code point is permissible in a Java identifier

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">IntlChar::isJavaIDPart</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Determines if the specified character is permissible in a Java
identifier.

In addition to <span class="function">IntlChar::isIDPart</span>,
**`TRUE`** for characters with general category "Sc" (currency symbols).

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns **`TRUE`** if `codepoint` may occur in a Java identifier,
**`FALSE`** if not.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::isJavaIDPart("A"));
var_dump(IntlChar::isJavaIDPart("$"));
var_dump(IntlChar::isJavaIDPart("\n"));
var_dump(IntlChar::isJavaIDPart("\u{2603}"));
?>
```

以上例程会输出：

    bool(true)
    bool(true)
    bool(false)
    bool(false)

### 参见

-   <span class="function">IntlChar::isIDIgnorable</span>
-   <span class="function">IntlChar::isIDPart</span>
-   <span class="function">IntlChar::isJavaIDStart</span>
-   <span class="function">IntlChar::isalpha</span>
-   <span class="function">IntlChar::isdigit</span>

IntlChar::isJavaIDStart
=======================

Check if code point is permissible as the first character in a Java
identifier

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">IntlChar::isJavaIDStart</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Determines if the specified character is permissible as the start of a
Java identifier.

In addition to <span class="function">IntlChar::isIDStart</span>,
**`TRUE`** for characters with general categories "Sc" (currency
symbols) and "Pc" (connecting punctuation).

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns **`TRUE`** if `codepoint` may start a Java identifier,
**`FALSE`** if not.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::isJavaIDStart("A"));
var_dump(IntlChar::isJavaIDStart("$"));
var_dump(IntlChar::isJavaIDStart("\n"));
var_dump(IntlChar::isJavaIDStart("\u{2603}"));
?>
```

以上例程会输出：

    bool(true)
    bool(true)
    bool(false)
    bool(false)

### 参见

-   <span class="function">IntlChar::isIDStart</span>
-   <span class="function">IntlChar::isJavaIDPart</span>
-   <span class="function">IntlChar::isalpha</span>

IntlChar::isJavaSpaceChar
=========================

Check if code point is a space character according to Java

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">IntlChar::isJavaSpaceChar</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Determine if the specified code point is a space character according to
Java.

**`TRUE`** for characters with general categories "Z" (separators),
which does not include control codes (e.g., TAB or Line Feed).

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns **`TRUE`** if `codepoint` is a space character according to
Java, **`FALSE`** if not.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::isJavaSpaceChar("A"));
var_dump(IntlChar::isJavaSpaceChar(" "));
var_dump(IntlChar::isJavaSpaceChar("\n"));
var_dump(IntlChar::isJavaSpaceChar("\t"));
var_dump(IntlChar::isJavaSpaceChar("\u{00A0}"));
?>
```

以上例程会输出：

    bool(false)
    bool(true)
    bool(false)
    bool(false)
    bool(true)

### 参见

-   <span class="function">IntlChar::isspace</span>
-   <span class="function">IntlChar::isWhitespace</span>
-   <span class="function">IntlChar::isUWhiteSpace</span>

IntlChar::islower
=================

Check if code point is a lowercase letter

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">IntlChar::islower</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Determines whether the specified code point has the general category
"Ll" (lowercase letter).

> **Note**:
>
> This misses some characters that are also lowercase but have a
> different general category value. In order to include those, use <span
> class="function">IntlChar::isULowercase</span>.

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns **`TRUE`** if `codepoint` is an Ll lowercase letter, **`FALSE`**
if not.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::islower("A"));
var_dump(IntlChar::islower("a"));
var_dump(IntlChar::islower("Φ"));
var_dump(IntlChar::islower("φ"));
var_dump(IntlChar::islower("1"));
?>
```

以上例程会输出：

    bool(false)
    bool(true)
    bool(false)
    bool(true)
    bool(false)

### 参见

-   <span class="function">IntlChar::isupper</span>
-   <span class="function">IntlChar::istitle</span>
-   <span class="function">IntlChar::tolower</span>
-   <span class="function">IntlChar::toupper</span>
-   **`IntlChar::PROPERTY_LOWERCASE`**

IntlChar::isMirrored
====================

Check if code point has the Bidi\_Mirrored property

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">IntlChar::isMirrored</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Determines whether the code point has the Bidi\_Mirrored property.

This property is set for characters that are commonly used in
Right-To-Left contexts and need to be displayed with a "mirrored" glyph.

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns **`TRUE`** if `codepoint` has the Bidi\_Mirrored property,
**`FALSE`** if not.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::isMirrored("A"));
var_dump(IntlChar::isMirrored("<"));
var_dump(IntlChar::isMirrored("("));
?>
```

以上例程会输出：

    bool(false)
    bool(true)
    bool(true)

### 参见

-   <span class="function">IntlChar::charMirror</span>
-   **`IntlChar::PROPERTY_BIDI_MIRRORED`**

IntlChar::isprint
=================

Check if code point is a printable character

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">IntlChar::isprint</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Determines whether the specified code point is a printable character.

**`TRUE`** for general categories other than "C" (controls).

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns **`TRUE`** if `codepoint` is a printable character, **`FALSE`**
if not.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::isprint("A"));
var_dump(IntlChar::isprint(" "));
var_dump(IntlChar::isprint("\n"));
var_dump(IntlChar::isprint("\u{200e}"));
?>
```

以上例程会输出：

    bool(true)
    bool(true)
    bool(false)
    bool(false)

### 参见

-   <span class="function">IntlChar::iscntrl</span>
-   **`IntlChar::PROPERTY_DEFAULT_IGNORABLE_CODE_POINT`**

IntlChar::ispunct
=================

Check if code point is punctuation character

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">IntlChar::ispunct</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Determines whether the specified code point is a punctuation character.

**`TRUE`** for characters with general categories "P" (punctuation).

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns **`TRUE`** if `codepoint` is a punctuation character,
**`FALSE`** if not.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::ispunct("."));
var_dump(IntlChar::ispunct(","));
var_dump(IntlChar::ispunct("\n"));
var_dump(IntlChar::ispunct("$"));
```

以上例程会输出：

    bool(true)
    bool(true)
    bool(false)
    bool(false)

IntlChar::isspace
=================

Check if code point is a space character

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">IntlChar::isspace</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Determines if the specified character is a space character or not.

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns **`TRUE`** if `codepoint` is a space character, **`FALSE`** if
not.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::isspace("A"));
var_dump(IntlChar::isspace(" "));
var_dump(IntlChar::isspace("\n"));
var_dump(IntlChar::isspace("\t"));
var_dump(IntlChar::isspace("\u{00A0}"));
?>
```

以上例程会输出：

    bool(false)
    bool(true)
    bool(true)
    bool(true)
    bool(true)

### 参见

-   <span class="function">IntlChar::isJavaSpaceChar</span>
-   <span class="function">IntlChar::isWhitespace</span>
-   <span class="function">IntlChar::isUWhiteSpace</span>

IntlChar::istitle
=================

Check if code point is a titlecase letter

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">IntlChar::istitle</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Determines whether the specified code point is a titlecase letter.

**`TRUE`** for general category "Lt" (titlecase letter).

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns **`TRUE`** if `codepoint` is a titlecase letter, **`FALSE`** if
not.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::istitle("A"));
var_dump(IntlChar::istitle("a"));
var_dump(IntlChar::istitle("Φ"));
var_dump(IntlChar::istitle("φ"));
var_dump(IntlChar::istitle("1"));
?>
```

以上例程会输出：

    bool(false)
    bool(true)
    bool(false)
    bool(true)
    bool(false)

### 参见

-   <span class="function">IntlChar::isupper</span>
-   <span class="function">IntlChar::islower</span>
-   <span class="function">IntlChar::totitle</span>

IntlChar::isUAlphabetic
=======================

Check if code point has the Alphabetic Unicode property

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">IntlChar::isUAlphabetic</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Check if a code point has the Alphabetic Unicode property.

This is the same as *IntlChar::hasBinaryProperty($codepoint,
IntlChar::PROPERTY\_ALPHABETIC)*

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns **`TRUE`** if `codepoint` has the Alphabetic Unicode property,
**`FALSE`** if not.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::isUAlphabetic("A"));
var_dump(IntlChar::isUAlphabetic("1"));
var_dump(IntlChar::isUAlphabetic("\u{2603}"));
?>
```

以上例程会输出：

    bool(true)
    bool(false)
    bool(false)

### 参见

-   <span class="function">IntlChar::isalpha</span>
-   <span class="function">IntlChar::hasBinaryProperty</span>
-   **`IntlChar::PROPERTY_ALPHABETIC`**

IntlChar::isULowercase
======================

Check if code point has the Lowercase Unicode property

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">IntlChar::isULowercase</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Check if a code point has the Lowercase Unicode property.

This is the same as *IntlChar::hasBinaryProperty($codepoint,
IntlChar::PROPERTY\_LOWERCASE)*

> **Note**:
>
> This is different than <span class="function">IntlChar::islower</span>
> and will return **`TRUE`** for more characters.

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns **`TRUE`** if `codepoint` has the Lowercase Unicode property,
**`FALSE`** if not.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::isULowercase("A"));
var_dump(IntlChar::isULowercase("a"));
var_dump(IntlChar::isULowercase("Φ"));
var_dump(IntlChar::isULowercase("φ"));
var_dump(IntlChar::isULowercase("1"));
?>
```

以上例程会输出：

    bool(false)
    bool(true)
    bool(false)
    bool(true)
    bool(false)

### 参见

-   <span class="function">IntlChar::islower</span>
-   <span class="function">IntlChar::hasBinaryProperty</span>
-   **`IntlChar::PROPERTY_LOWERCASE`**

IntlChar::isupper
=================

Check if code point has the general category "Lu" (uppercase letter)

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">IntlChar::isupper</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Determines whether the specified code point has the general category
"Lu" (uppercase letter).

> **Note**:
>
> This misses some characters that are also uppercase but have a
> different general category value. In order to include those, use <span
> class="function">IntlChar::isUUppercase</span>.

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns **`TRUE`** if `codepoint` is an Lu uppercase letter, **`FALSE`**
if not.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::isupper("A"));
var_dump(IntlChar::isupper("a"));
var_dump(IntlChar::isupper("Φ"));
var_dump(IntlChar::isupper("φ"));
var_dump(IntlChar::isupper("1"));
?>
```

以上例程会输出：

    bool(true)
    bool(false)
    bool(true)
    bool(false)
    bool(false)

### 参见

-   <span class="function">IntlChar::islower</span>
-   <span class="function">IntlChar::istitle</span>
-   <span class="function">IntlChar::tolower</span>
-   <span class="function">IntlChar::toupper</span>
-   **`IntlChar::PROPERTY_UPPERCASE`**

IntlChar::isUUppercase
======================

Check if code point has the Uppercase Unicode property

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">IntlChar::isUUppercase</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Check if a code point has the Uppercase Unicode property.

This is the same as *IntlChar::hasBinaryProperty($codepoint,
IntlChar::PROPERTY\_UPPERCASE)*

> **Note**:
>
> This is different than <span class="function">IntlChar::isupper</span>
> and will return **`TRUE`** for more characters.

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns **`TRUE`** if `codepoint` has the Uppercase Unicode property,
**`FALSE`** if not.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::isUUppercase("A"));
var_dump(IntlChar::isUUppercase("a"));
var_dump(IntlChar::isUUppercase("Φ"));
var_dump(IntlChar::isUUppercase("φ"));
var_dump(IntlChar::isUUppercase("1"));
?>
```

以上例程会输出：

    bool(true)
    bool(false)
    bool(true)
    bool(false)
    bool(false)

### 参见

-   <span class="function">IntlChar::isupper</span>
-   <span class="function">IntlChar::hasBinaryProperty</span>
-   **`IntlChar::PROPERTY_UPPERCASE`**

IntlChar::isUWhiteSpace
=======================

Check if code point has the White\_Space Unicode property

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">IntlChar::isUWhiteSpace</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Check if a code point has the White\_Space Unicode property.

This is the same as *IntlChar::hasBinaryProperty($codepoint,
IntlChar::PROPERTY\_WHITE\_SPACE)*

> **Note**:
>
> This is different from both <span
> class="function">IntlChar::isspace</span> and <span
> class="function">IntlChar::isWhitespace</span>.

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns **`TRUE`** if `codepoint` has the White\_Space Unicode property,
**`FALSE`** if not.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::isUWhiteSpace("A"));
var_dump(IntlChar::isUWhiteSpace(" "));
var_dump(IntlChar::isUWhiteSpace("\n"));
var_dump(IntlChar::isUWhiteSpace("\t"));
var_dump(IntlChar::isUWhiteSpace("\u{00A0}"));
?>
```

以上例程会输出：

    bool(false)
    bool(true)
    bool(true)
    bool(true)
    bool(true)

### 参见

-   <span class="function">IntlChar::isspace</span>
-   <span class="function">IntlChar::isWhitespace</span>
-   <span class="function">IntlChar::isJavaSpaceChar</span>
-   <span class="function">IntlChar::hasBinaryProperty</span>
-   **`IntlChar::PROPERTY_WHITE_SPACE`**

IntlChar::isWhitespace
======================

Check if code point is a whitespace character according to ICU

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">IntlChar::isWhitespace</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Determines if the specified code point is a whitespace character
according to ICU.

A character is considered to be a ICU whitespace character if and only
if it satisfies one of the following criteria:

-   It is a Unicode Separator character (categories "Z" = "Zs" or "Zl"
    or "Zp"), but is not also a non-breaking space (U+00A0 NBSP or
    U+2007 Figure Space or U+202F Narrow NBSP).
-   It is U+0009 HORIZONTAL TABULATION.
-   It is U+000A LINE FEED.
-   It is U+000B VERTICAL TABULATION.
-   It is U+000C FORM FEED.
-   It is U+000D CARRIAGE RETURN.
-   It is U+001C FILE SEPARATOR.
-   It is U+001D GROUP SEPARATOR.
-   It is U+001E RECORD SEPARATOR.
-   It is U+001F UNIT SEPARATOR.

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns **`TRUE`** if `codepoint` is a whitespace character according to
ICU, **`FALSE`** if not.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::iswhitespace("A"));
var_dump(IntlChar::iswhitespace(" "));
var_dump(IntlChar::iswhitespace("\n"));
var_dump(IntlChar::iswhitespace("\t"));
var_dump(IntlChar::iswhitespace("\u{00A0}"));
?>
```

以上例程会输出：

    bool(false)
    bool(true)
    bool(true)
    bool(true)
    bool(false)

### 参见

-   <span class="function">IntlChar::isspace</span>
-   <span class="function">IntlChar::isJavaSpaceChar</span>
-   <span class="function">IntlChar::isUWhiteSpace</span>

IntlChar::isxdigit
==================

Check if code point is a hexadecimal digit

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">IntlChar::isxdigit</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

Determines whether the specified code point is a hexadecimal digit.

**`TRUE`** for characters with general category "Nd" (decimal digit
numbers) as well as Latin letters a-f and A-F in both ASCII and
Fullwidth ASCII. (That is, for letters with code points 0041..0046,
0061..0066, FF21..FF26, FF41..FF46.)

This is equivalent to *IntlChar::digit($codepoint, 16) \>= 0*.

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns **`TRUE`** if `codepoint` is a hexadecimal character,
**`FALSE`** if not.

### 注释

> **Note**:
>
> In order to narrow the definition of hexadecimal digits to only ASCII
> characters use:
>
> ``` php
> <?php
> $isASCIIHexadecimal = IntlChar::ord($codepoint) <= 0x7F && IntlChar::isxdigit($codepoint);
> ?>
> ```

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::isxdigit("A"));
var_dump(IntlChar::isxdigit("1"));
var_dump(IntlChar::isxdigit("\u{2603}"));
?>
```

以上例程会输出：

    bool(true)
    bool(true)
    bool(false)

### 参见

-   <span class="function">IntlChar::isdigit</span>

IntlChar::ord
=============

Return Unicode code point value of character

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">IntlChar::ord</span> ( <span
class="methodparam"><span class="type">mixed</span> `$character`</span>
)

Returns the Unicode code point value of the given character.

This function compliments <span class="function">IntlChar::chr</span>.

### 参数

`character`  
A Unicode character.

### 返回值

Returns the Unicode code point value as an integer.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::ord("A"));
var_dump(IntlChar::ord(" "));
var_dump(IntlChar::ord("\u{2603}"));
?>
```

以上例程会输出：

    int(65)
    int(32)
    int(9731)

### 参见

-   <span class="function">IntlChar::isalnum</span>
-   <span class="function">IntlChar::isdigit</span>
-   <span class="function">IntlChar::chr</span>
-   <span class="function">ord</span>

IntlChar::tolower
=================

Make Unicode character lowercase

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">mixed</span> <span
class="methodname">IntlChar::tolower</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

The given character is mapped to its lowercase equivalent. If the
character has no lowercase equivalent, the original character itself is
returned.

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns the Simple\_Lowercase\_Mapping of the code point, if any;
otherwise the code point itself.

The return type will be <span class="type">integer</span> unless the
code point was passed as a UTF-8 <span class="type">string</span>, in
which case a <span class="type">string</span> will be returned.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::tolower("A"));
var_dump(IntlChar::tolower("a"));
var_dump(IntlChar::tolower("Φ"));
var_dump(IntlChar::tolower("φ"));
var_dump(IntlChar::tolower("1"));
var_dump(IntlChar::tolower(ord("A")));
var_dump(IntlChar::tolower(ord("a")));
?>
```

以上例程会输出：

    string(1) "a"
    string(1) "a"
    string(2) "φ"
    string(2) "φ"
    string(1) "1"
    int(97)
    int(97)

### 参见

-   <span class="function">IntlChar::totitle</span>
-   <span class="function">IntlChar::toupper</span>
-   <span class="function">mb\_strtolower</span>

IntlChar::totitle
=================

Make Unicode character titlecase

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">mixed</span> <span
class="methodname">IntlChar::totitle</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

The given character is mapped to its titlecase equivalent. If the
character has no titlecase equivalent, the original character itself is
returned.

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns the Simple\_Titlecase\_Mapping of the code point, if any;
otherwise the code point itself.

The return type will be <span class="type">integer</span> unless the
code point was passed as a UTF-8 <span class="type">string</span>, in
which case a <span class="type">string</span> will be returned.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::totitle("A"));
var_dump(IntlChar::totitle("a"));
var_dump(IntlChar::totitle("Φ"));
var_dump(IntlChar::totitle("φ"));
var_dump(IntlChar::totitle("1"));
var_dump(IntlChar::totitle(ord("A")));
var_dump(IntlChar::totitle(ord("a")));
?>
```

以上例程会输出：

    string(1) "A"
    string(1) "A"
    string(2) "Φ"
    string(2) "Φ"
    string(1) "1"
    int(65)
    int(65)

### 参见

-   <span class="function">IntlChar::tolower</span>
-   <span class="function">IntlChar::toupper</span>
-   <span class="function">mb\_convert\_case</span>

IntlChar::toupper
=================

Make Unicode character uppercase

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">mixed</span> <span
class="methodname">IntlChar::toupper</span> ( <span
class="methodparam"><span class="type">mixed</span> `$codepoint`</span>
)

The given character is mapped to its uppercase equivalent. If the
character has no uppercase equivalent, the character itself is returned.

### 参数

`codepoint`  
The <span class="type">integer</span> codepoint value (e.g. *0x2603* for
*U+2603 SNOWMAN*), or the character encoded as a UTF-8 <span
class="type">string</span> (e.g. *"\\u{2603}"*)

### 返回值

Returns the Simple\_Uppercase\_Mapping of the code point, if any;
otherwise the code point itself.

The return type will be <span class="type">integer</span> unless the
code point was passed as a UTF-8 <span class="type">string</span>, in
which case a <span class="type">string</span> will be returned.

### 范例

**示例 \#1 Testing different code points**

``` php
<?php
var_dump(IntlChar::toupper("A"));
var_dump(IntlChar::toupper("a"));
var_dump(IntlChar::toupper("Φ"));
var_dump(IntlChar::toupper("φ"));
var_dump(IntlChar::toupper("1"));
var_dump(IntlChar::toupper(ord("A")));
var_dump(IntlChar::toupper(ord("a")));
?>
```

以上例程会输出：

    string(1) "A"
    string(1) "A"
    string(2) "Φ"
    string(2) "Φ"
    string(1) "1"
    int(65)
    int(65)

### 参见

-   <span class="function">IntlChar::tolower</span>
-   <span class="function">IntlChar::totitle</span>
-   <span class="function">mb\_strtoupper</span>

简介
----

This class is used for generating exceptions when errors occur inside
intl functions. Such exceptions are only generated when
<a href="/intl/setup.html#" class="link">intl.use_exceptions</a> is
enabled.

类摘要
------

**IntlException**

<span class="ooclass"> class **IntlException** </span> <span
class="ooclass"> <span class="modifier">extends</span> **Exception**
</span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Exception::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Exception::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Exception::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

简介
----

This class represents iterator objects throughout the intl extension
whenever the iterator cannot be identified with any other object
provided by the extension. The distinct iterator object used internally
by the
<a href="/control-structures/foreach.html" class="link"><em>foreach</em> construct</a>
can only be obtained (in the relevant part here) from objects, so
objects of this class serve the purpose of providing the hook through
which this internal object can be obtained. As a convenience, this class
also implements the <span class="classname">Iterator</span> interface,
allowing the collection of values to be navigated using the methods
defined in that interface. Both these methods and the internal iterator
objects provided to *foreach* are backed by the same state (e.g. the
position of the iterator and its current value).

Subclasses may provide richer functionality.

类摘要
------

**IntlIterator**

<span class="ooclass"> class **IntlIterator** </span> <span
class="oointerface">implements <span
class="interfacename">Iterator</span> </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">valid</span> ( <span
class="methodparam">void</span> )

}

IntlIterator::current
=====================

Get the current element

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">IntlIterator::current</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

IntlIterator::key
=================

Get the current key

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">IntlIterator::key</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

IntlIterator::next
==================

Move forward to the next element

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">IntlIterator::next</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

IntlIterator::rewind
====================

Rewind the iterator to the first element

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">IntlIterator::rewind</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

IntlIterator::valid
===================

Check if current position is valid

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IntlIterator::valid</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值
