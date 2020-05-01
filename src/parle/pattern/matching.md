Parle pattern matching
======================

**目录**

-   [Character
    representations](/parle/pattern/matching.html#Character%20representations)
-   [Character
    classes](/parle/pattern/matching.html#Character%20classes)
-   [Unicode character
    classes](/parle/pattern/matching.html#Unicode%20character%20classes)
-   [Alternation and
    repetition](/parle/pattern/matching.html#Alternation%20and%20repetition)
-   [Anchors](/parle/pattern/matching.html#Anchors)
-   [Grouping](/parle/pattern/matching.html#Grouping)

Parle supports regex matching similar to flex. Also supported are the
following POSIX character sets: *\[:alnum:\]*, *\[:alpha:\]*,
*\[:blank:\]*, *\[:cntrl:\]*, *\[:digit:\]*, *\[:graph:\]*,
*\[:lower:\]*, *\[:print:\]*, *\[:punct:\]*, *\[:space:\]*,
*\[:upper:\]* and *\[:xdigit:\]*.

The Unicode character classes are currently not enabled by default, pass
--enable-parle-utf32 to make them available. A particular encoding can
be mapped with a correctly constructed regex. For example, to match the
EURO symbol encoded in UTF-8, the regular expression
*\[\\xe2\]\[\\x82\]\[\\xac\]* can be used. The pattern for an UTF-8
encoded string could be *\[
-\\x7f\]{+}\[\\x80-\\xbf\]{+}\[\\xc2-\\xdf\]{+}\[\\xe0-\\xef\]{+}\[\\xf0-\\xff\]+*.

Character representations
-------------------------

| Sequence | Description                                      |
|----------|--------------------------------------------------|
| \\a      | Alert (bell).                                    |
| \\b      | Backspace.                                       |
| \\e      | ESC character, \\x1b.                            |
| \\n      | Newline.                                         |
| \\r      | Carriage return.                                 |
| \\f      | Form feed, \\x0c.                                |
| \\t      | Horizontal tab, \\x09.                           |
| \\v      | Vertical tab, \\x0b.                             |
| \\oct    | Character specified by a three-digit octal code. |
| \\xhex   | Character specified by a hex code.               |
| \\cchar  | Named control character.                         |

Character classes
-----------------

| Sequence | Description                                                                                                                                                                                                                                          |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[...\]  | A single character listed or contained within a listed range. Ranges can be combined with the *{+}* and *{-}* operators. For example *\[a-z\]{+}\[0-9\]* is the same as *\[0-9a-z\]* and *\[a-z\]{-}\[aeiou\]* is the same as *\[b-df-hj-np-tv-z\]*. |
| \[^...\] | A single character not listed and not contained within a listed range.                                                                                                                                                                               |
| .        | Any character, default *\[^\\n\].*                                                                                                                                                                                                                   |
| \\d      | Digit character, *\[0-9\]*.                                                                                                                                                                                                                          |
| \\D      | Non-digit character, *\[^0-9\]*.                                                                                                                                                                                                                     |
| \\s      | White space character, *\[ \\t\\n\\r\\f\\v\]*.                                                                                                                                                                                                       |
| \\S      | Non-white space character, *\[^ \\t\\n\\r\\f\\v\]*.                                                                                                                                                                                                  |
| \\w      | Word caracter, *\[a-zA-Z0-9\_\]*.                                                                                                                                                                                                                    |
| \\W      | Non-word caracter, *\[^a-zA-Z0-9\_\]*.                                                                                                                                                                                                               |

Unicode character classes
-------------------------

| Sequence | Description                 |
|----------|-----------------------------|
| \\p{C}   | Other.                      |
| \\p{Cc}  | Other, control.             |
| \\p{Cf}  | Other, format.              |
| \\p{Co}  | Other, private use.         |
| \\p{Cs}  | Other, surrogate.           |
| \\p{L}   | Letter.                     |
| \\p{LC}  | Letter, cased.              |
| \\p{Ll}  | Letter, lowercase.          |
| \\p{Lm}  | Letter, modifier.           |
| \\p{Lo}  | Letter, other.              |
| \\p{Lt}  | Letter, titlecase.          |
| \\p{Lu}  | Letter, uppercase.          |
| \\p{M}   | Mark.                       |
| \\p{Mc}  | Mark, space combining.      |
| \\p{Me}  | Mark, enclosing.            |
| \\p{Mn}  | Mark, nonspacing.           |
| \\p{N}   | Number.                     |
| \\p{Nd}  | Number, decimal digit.      |
| \\p{Nl}  | Number, letter.             |
| \\p{No}  | Number, other.              |
| \\p{P}   | Punctuation.                |
| \\p{Pc}  | Punctiation, connector.     |
| \\p{Pd}  | Punctuation, dash.          |
| \\p{Pe}  | Punctuation, close.         |
| \\p{Pf}  | Punctuation, final quote.   |
| \\p{Pi}  | Punctuation, initial quote. |
| \\p{Po}  | Punctuation, other.         |
| \\p{Ps}  | Punctuation, open.          |
| \\p{S}   | Symbol.                     |
| \\p{Sc}  | Symbol, currency.           |
| \\p{Sk}  | Symbol, modifier.           |
| \\p{Sm}  | Symbol, math.               |
| \\p{So}  | Symbol, other.              |
| \\p{Z}   | Separator.                  |
| \\p{Zl}  | Separator, line.            |
| \\p{Zp}  | Separator, paragraph.       |
| \\p{Zs}  | Separator, space.           |

These character clasess are only available, if the option
--enable-parle-utf32 was passed at the compilation time.

Alternation and repetition
--------------------------

| Sequence | Greedy | Description                                      |
|----------|--------|--------------------------------------------------|
| ...\|... | \-     | Try subpatterns in alternation.                  |
| \*       | yes    | Match 0 or more times.                           |
| \+       | yes    | Match 1 or more times.                           |
| ?        | yes    | Match 0 or 1 times.                              |
| {n}      | no     | Match exactly n times.                           |
| {n,}     | yes    | Match at least n times.                          |
| {n,m}    | yes    | Match at least n times but no more than m times. |
| \*?      | no     | Match 0 or more times.                           |
| +?       | no     | Match 1 or more times.                           |
| ??       | no     | Match 0 or 1 times.                              |
| {n,}?    | no     | Match at least n times.                          |
| {n,m}?   | no     | Match at least n times but no more than m times. |
| {MACRO}  | \-     | Include the regex MACRO in the current regex.    |

Anchors
-------

| Sequence | Description                         |
|----------|-------------------------------------|
| ^        | Start of string or after a newline. |
| $        | End of string or before a newline.  |

Grouping
--------

<table>
<caption><strong>Grouping</strong></caption>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Sequence</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>(...)</td>
<td>Group a regular expression to override default operator precedence.</td>
</tr>
<tr class="even">
<td>(?r-s:pattern)</td>
<td>Apply option r and omit option s while interpreting pattern. Options may be zero or more of the characters i, s, or x.
<table>
<caption><strong>Options</strong></caption>
<thead>
<tr class="header">
<th>Option</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>i</td>
<td>Case insensitive.</td>
</tr>
<tr class="even">
<td>-i</td>
<td>Case sensitive.</td>
</tr>
<tr class="odd">
<td>s</td>
<td>Alters the meaning of '.' to match any character whatsoever.</td>
</tr>
<tr class="even">
<td>-s</td>
<td>"lters the meaning of '.' to match any character except '\n'.</td>
</tr>
<tr class="odd">
<td>x</td>
<td>Ignores comments and whitespace in patterns. Whitespace is ignored unless it is backslash-escaped, contained within ""s, or appears inside a character range.</td>
</tr>
</tbody>
</table>
These options can be applied globally at the rules level by passing a combination of the bit flags to the lexer.</td>
</tr>
<tr class="odd">
<td>(?# comment )</td>
<td>Omit everything within (). The first ) character encountered ends the pattern. It is not possible for the comment to contain a ) character. The comment may span lines.</td>
</tr>
</tbody>
</table>
