The gopher protocol, as defined by
<a href="http://www.faqs.org/rfcs/rfc1436" class="link external">» RFC 1436</a>,
is generally considered the ancestor of the modern HTTP protocol.
However, gopher was also intended to provide references to non-gopher
resources including telnet, wais, nntp, and even http. This extension
adds gopher support to PHP's
<a href="/wrappers.html" class="link">URL Wrappers</a>, and provides a
helper function <span class="function">gopher\_parsedir</span> to make
sense of gopher formatted directory listings.
