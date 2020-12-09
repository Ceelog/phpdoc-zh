变更的函数
----------

### PHP 核心

-   <span class="simpara"> 使用 **`null`** 作为参数调用 <span
    class="function">set\_error\_handler</span> 将重置错误处理程序。
    </span>
-   <span class="simpara"> 当使用 **`null`** 调用<span
    class="function">set\_error\_handler</span> 和 <span
    class="function">set\_exception\_handler</span> 时，
    现在分别返回上一个错误或异常处理程序。 </span>
-   <span class="simpara"> <span class="function">pack</span> 和 <span
    class="function">unpack</span> 使用
    “a”和“A”格式代码时的行为有所变化。
    <a href="/migration55/incompatible.html#migration55.incompatible.pack" class="link">Detailed notes on these changes are available.</a>
    </span>

### <a href="/book/intl.html" class="link">intl</a>

-   <span class="simpara"> <span
    class="methodname">MessageFormatter::format</span> 及其相关函数现在
    related functions now accept named arguments and mixed numeric and
    named arguments when PHP is linked to ICU 4.8 or later. </span>
-   <span class="simpara"> <span
    class="methodname">MessageFormatter::format</span> and related
    functions no longer error when an insufficient number of arguments
    have been provided. Instead, the placeholders will not be
    substituted. </span>
-   <span class="simpara"> <span
    class="methodname">MessageFormatter::format</span> and <span
    class="methodname">MessageFormatter::parse</span> are no longer
    limited to second precision when dealing with times. </span>
-   <span class="simpara"> <span
    class="methodname">IntlDateFormatter::\_\_construct</span> and <span
    class="function">datefmt\_create</span> now accept <span
    class="classname">IntlTimeZone</span> and <span
    class="classname">DateTimeZone</span> objects for the `timezone`
    argument, and <span class="classname">IntlCalendar</span> objects
    for the `calendar` argument. Furthermore, if the time zone is
    omitted and the `calendar` doesn't specify a time zone, PHP's
    default time zone from <span
    class="function">date\_default\_timezone\_get</span> is now used
    instead of the default ICU time zone. </span>
-   <span class="simpara"> <span
    class="methodname">IntlDateFormatter::getCalendar</span> and <span
    class="function">datefmt\_get\_calendar</span> return false if the
    <span class="classname">IntlDateFormatter</span> object was created
    with an <span class="classname">IntlCalendar</span> instance instead
    of one of the <span class="classname">IntlDateFormatter</span>
    constants. </span>
-   <span class="simpara"> 除 <span
    class="classname">IntlDateFormatter</span> 常量之外， <span
    class="methodname">IntlDateFormatter::setCalendar</span> 和 <span
    class="function">datefmt\_set\_calendar</span>现在接受 <span
    class="classname">IntlCalendar</span> 对象。 </span>
-   <span class="simpara"> <span
    class="methodname">IntlDateFormatter::format</span> 和 <span
    class="function">datefmt\_format</span> 现在接受 <span
    class="classname">IntlCalendar</span> 对象。 </span>
