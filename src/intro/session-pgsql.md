> **Note**: <span class="simpara">此扩展在 Windows 平台上不可用。</span>

This module provides an additional session save handler for the
<a href="/book/session.html" class="link">session</a> module using
<a href="http://www.postgresql.org/" class="link external">» PostgreSQL</a>
as a storage system. A *user-level* session storage function may also be
used - <span class="function">session\_set\_save\_handler</span>, but
this module is written in C and therefore could be twice as fast,
compared to a session save handler written in PHP.

Session PgSQL is designed to scale any size of web sites and offers some
advanced features:

-   session tables are created automatically
-   automatic session table vacuum
-   better garbage collection
-   multiple PostgreSQL servers support
-   automatic database server failover (switching)
-   automatic database server load balancing if there are multiple
    PostgreSQL servers.
-   short circuit UPDATE
