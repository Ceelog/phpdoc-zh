范例
====

**目录**

-   [DateTime Arithmetic](/datetime/examples.html#DateTime%20Arithmetic)

DateTime Arithmetic
-------------------

The following examples show some pitfalls of DateTime arithmetic with
regard to DST transitions and months having different numbers of days.

**示例 \#1 DateTime::add/sub add intervals which cover elapsed time**

Adding PT24H over a DST transition will appear to add 23/25 hours (for
most timezones).

``` php
<?php
$dt = new DateTime("2015-11-01 00:00:00", new DateTimeZone("America/New_York"));
echo "Start: ", $dt->format("Y-m-d H:i:s P"), PHP_EOL;
$dt->add(new DateInterval("PT3H"));
echo "End:   ", $dt->format("Y-m-d H:i:s P"), PHP_EOL;
?>
```

以上例程会输出：

    Start: 2015-11-01 00:00:00 -04:00
    End:   2015-11-01 02:00:00 -05:00

**示例 \#2 DateTime::modify and strtotime increment or decrement
individual component values**

Adding +24 hours over a DST transition will add exactly 24 hours as seen
in the date/time string (unless the start or end time is on a transition
point).

``` php
<?php
$dt = new DateTime("2015-11-01 00:00:00", new DateTimeZone("America/New_York"));
echo "Start: ", $dt->format("Y-m-d H:i:s P"), PHP_EOL;
$dt->modify("+24 hours");
echo "End:   ", $dt->format("Y-m-d H:i:s P"), PHP_EOL;
?>
```

以上例程会输出：

    Start: 2015-11-01 00:00:00 -04:00
    End:   2015-11-02 00:00:00 -05:00

**示例 \#3 Adding or subtracting times can over- or underflow dates**

Like where January 31st + 1 month will result in March 2nd (leap year)
or 3rd (normal year).

``` php
<?php
echo "Normal year:\n"; // February has 28 days
$dt = new DateTime("2015-01-31 00:00:00", new DateTimeZone("America/New_York"));
echo "Start: ", $dt->format("Y-m-d H:i:s P"), PHP_EOL;
$dt->modify("+1 month");
echo "End:   ", $dt->format("Y-m-d H:i:s P"), PHP_EOL;

echo "Leap year:\n"; // February has 29 days
$dt = new DateTime("2016-01-31 00:00:00", new DateTimeZone("America/New_York"));
echo "Start: ", $dt->format("Y-m-d H:i:s P"), PHP_EOL;
$dt->modify("+1 month");
echo "End:   ", $dt->format("Y-m-d H:i:s P"), PHP_EOL;
?>
```

以上例程会输出：

    Normal year:
    Start: 2015-01-31 00:00:00 -05:00
    End:   2015-03-03 00:00:00 -05:00
    Leap year:
    Start: 2016-01-31 00:00:00 -05:00
    End:   2016-03-02 00:00:00 -05:00

To get the last day of the next month (i.e. to prevent the overflow),
the *last day of* format is available as of PHP 5.3.0.

``` php
<?php
echo "Normal year:\n"; // February has 28 days
$dt = new DateTime("2015-01-31 00:00:00", new DateTimeZone("America/New_York"));
echo "Start: ", $dt->format("Y-m-d H:i:s P"), PHP_EOL;
$dt->modify("last day of next month");
echo "End:   ", $dt->format("Y-m-d H:i:s P"), PHP_EOL;

echo "Leap year:\n"; // February has 29 days
$dt = new DateTime("2016-01-31 00:00:00", new DateTimeZone("America/New_York"));
echo "Start: ", $dt->format("Y-m-d H:i:s P"), PHP_EOL;
$dt->modify("last day of next month");
echo "End:   ", $dt->format("Y-m-d H:i:s P"), PHP_EOL;
?>
```

以上例程会输出：

    Normal year:
    Start: 2015-01-31 00:00:00 -05:00
    End:   2015-02-28 00:00:00 -05:00
    Leap year:
    Start: 2016-01-31 00:00:00 -05:00
    End:   2016-02-29 00:00:00 -05:00
