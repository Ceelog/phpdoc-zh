This extension filters data by either validating or sanitizing it. This
is especially useful when the data source contains unknown (or foreign)
data, like user supplied input. For example, this data may come from an
HTML form.

There are two main types of filtering: *validation* and *sanitization*.

<a href="/filter/filters.html#Validate%20filters" class="link">Validation</a>
is used to validate or check if the data meets certain qualifications.
For example, passing in **`FILTER_VALIDATE_EMAIL`** will determine if
the data is a valid email address, but will not change the data itself.

<a href="/filter/filters.html#Sanitize%20filters" class="link">Sanitization</a>
will sanitize the data, so it may alter it by removing undesired
characters. For example, passing in **`FILTER_SANITIZE_EMAIL`** will
remove characters that are inappropriate for an email address to
contain. That said, it does not validate the data.

*Flags* are optionally used with both validation and sanitization to
tweak behaviour according to need. For example, passing in
**`FILTER_FLAG_PATH_REQUIRED`** while filtering an URL will require a
path (like */foo* in *http://example.org/foo*) to be present.
