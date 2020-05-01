Mailparse is an extension for parsing and working with email messages.
It can deal with
<a href="http://www.faqs.org/rfcs/rfc822" class="link external">» RFC 822</a>
and
<a href="http://www.faqs.org/rfcs/rfc2045" class="link external">» RFC 2045</a>
(*MIME*) compliant messages.

Mailparse is stream based, which means that it does not keep in-memory
copies of the files it processes - so it is very resource efficient when
dealing with large messages.

> **Note**:
>
> Mailparse requires the
> <a href="/book/mbstring.html" class="link">mbstring</a> extension, and
> mbstring must be loaded before mailparse.
