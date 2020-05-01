Limitations
===========

**Implementation Limitations**

The following are limitations in the current SDO implementation:

1.  There is no support for multi-byte character sets. This will be
    considered, depending on community requirements, in a
    Unicode-enabled version of PHP.

**SDO Limitations**

The following SDO 2.0 concepts are not supported in the current PHP
implementation. It is not necessarily the case that these will all be
added over time. Their inclusion will depend on community requirements.

1.  Bi-directional relationships.

2.  Type and property alias names.

3.  Read-only properties.

4.  The Helper classes defined in SDO 2.0 are not directly implemented.
    However equivalent function is provided in a more natural way for
    PHP. For example the function of **CopyHelper::copy()** is provided
    by applying the PHP
    <a href="/language/oop5/cloning.html" class="link">clone</a> keyword
    to a data object.
