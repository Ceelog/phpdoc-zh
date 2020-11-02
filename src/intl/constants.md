预定义常量
==========

**`INTL_ICU_VERSION`** (<span class="type">string</span>)  
<span class="simpara"> The current ICU library version as a
dotted-decimal string. </span>

**`INTL_MAX_LOCALE_LEN`** (<span class="type">int</span>)  
<span class="simpara"> Limit on locale length, set to 80 in PHP code.
Locale names longer than this limit will not be accepted. </span>

**`IDNA_DEFAULT`** (<span class="type">int</span>)  
<span class="simpara"> Prohibit processing of unassigned codepoints in
the input for IDN functions and do not check if the input conforms to
domain name ASCII rules. </span>

**`IDNA_ALLOW_UNASSIGNED`** (<span class="type">int</span>)  
<span class="simpara"> Allow processing of unassigned codepoints in the
input for IDN functions. </span>

**`IDNA_USE_STD3_RULES`** (<span class="type">int</span>)  
<span class="simpara"> Check if the input for IDN functions conforms to
domain name ASCII rules. </span>

**`IDNA_CHECK_BIDI`** (<span class="type">int</span>)  
<span class="simpara"> Check whether the input conforms to the BiDi
rules. Ignored by the IDNA2003 implementation, which always performs
this check. </span>

**`IDNA_CHECK_CONTEXTJ`** (<span class="type">int</span>)  
<span class="simpara"> Check whether the input conforms to the CONTEXTJ
rules. Ignored by the IDNA2003 implementation, as this check is new in
IDNA2008. </span>

**`IDNA_NONTRANSITIONAL_TO_ASCII`** (<span class="type">int</span>)  
<span class="simpara"> Option for nontransitional processing in <span
class="function">idn\_to\_ascii</span>. Transitional processing is
activated by default. This option is ignored by the IDNA2003
implementation. </span>

**`IDNA_NONTRANSITIONAL_TO_UNICODE`** (<span class="type">int</span>)  
<span class="simpara"> Option for nontransitional processing in <span
class="function">idn\_to\_utf8</span>. Transitional processing is
activated by default. This option is ignored by the IDNA2003
implementation. </span>

**`INTL_IDNA_VARIANT_2003`** (<span class="type">int</span>)  
<span class="simpara"> Use IDNA 2003 algorithm in <span
class="function">idn\_to\_utf8</span> and <span
class="function">idn\_to\_ascii</span>. This is the default. This
constant and using the default has been deprecated as of PHP 7.2.0.
</span>

**`INTL_IDNA_VARIANT_UTS46`** (<span class="type">int</span>)  
<span class="simpara"> Use UTS \#46 algorithm in <span
class="function">idn\_to\_utf8</span> and <span
class="function">idn\_to\_ascii</span>. Available as of ICU 4.6. </span>

**`IDNA_ERROR_EMPTY_LABEL`** (<span class="type">int</span>)  
**`IDNA_ERROR_LABEL_TOO_LONG`** (<span class="type">int</span>)  
**`IDNA_ERROR_DOMAIN_NAME_TOO_LONG`** (<span class="type">int</span>)  
**`IDNA_ERROR_LEADING_HYPHEN`** (<span class="type">int</span>)  
**`IDNA_ERROR_TRAILING_HYPHEN`** (<span class="type">int</span>)  
**`IDNA_ERROR_HYPHEN_3_4`** (<span class="type">int</span>)  
**`IDNA_ERROR_LEADING_COMBINING_MARK`** (<span class="type">int</span>)  
**`IDNA_ERROR_DISALLOWED`** (<span class="type">int</span>)  
**`IDNA_ERROR_PUNYCODE`** (<span class="type">int</span>)  
**`IDNA_ERROR_LABEL_HAS_DOT`** (<span class="type">int</span>)  
**`IDNA_ERROR_INVALID_ACE_LABEL`** (<span class="type">int</span>)  
**`IDNA_ERROR_BIDI`** (<span class="type">int</span>)  
**`IDNA_ERROR_CONTEXTJ`** (<span class="type">int</span>)  
<span class="simpara"> Errors reported in a bitset returned by the UTS
\#46 algorithm in <span class="function">idn\_to\_utf8</span> and <span
class="function">idn\_to\_ascii</span>. </span>
