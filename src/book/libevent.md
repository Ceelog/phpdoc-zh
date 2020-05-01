Libevent
========

**目录**

-   [简介](/intro/libevent.html)
-   [安装／配置](/libevent/setup.html)
    -   [需求](/libevent/setup.html#需求)
    -   [安装](/libevent/setup.html#安装)
    -   [运行时配置](/libevent/setup.html#运行时配置)
    -   [资源类型](/libevent/setup.html#资源类型)
-   [预定义常量](/libevent/constants.html)
-   [范例](/libevent/examples.html)
-   [Libevent 函数](/ref/libevent.html)
    -   [event\_add](/ref/libevent.html#event_add) — Add an event to the
        set of monitored events
    -   [event\_base\_free](/ref/libevent.html#event_base_free) —
        Destroy event base
    -   [event\_base\_loop](/ref/libevent.html#event_base_loop) — Handle
        events
    -   [event\_base\_loopbreak](/ref/libevent.html#event_base_loopbreak)
        — Abort event loop
    -   [event\_base\_loopexit](/ref/libevent.html#event_base_loopexit)
        — Exit loop after a time
    -   [event\_base\_new](/ref/libevent.html#event_base_new) — Create
        and initialize new event base
    -   [event\_base\_priority\_init](/ref/libevent.html#event_base_priority_init)
        — Set the number of event priority levels
    -   [event\_base\_reinit](/ref/libevent.html#event_base_reinit) —
        Reinitialize the event base after a fork
    -   [event\_base\_set](/ref/libevent.html#event_base_set) —
        Associate event base with an event
    -   [event\_buffer\_base\_set](/ref/libevent.html#event_buffer_base_set)
        — Associate buffered event with an event base
    -   [event\_buffer\_disable](/ref/libevent.html#event_buffer_disable)
        — Disable a buffered event
    -   [event\_buffer\_enable](/ref/libevent.html#event_buffer_enable)
        — Enable a buffered event
    -   [event\_buffer\_fd\_set](/ref/libevent.html#event_buffer_fd_set)
        — Change a buffered event file descriptor
    -   [event\_buffer\_free](/ref/libevent.html#event_buffer_free) —
        Destroy buffered event
    -   [event\_buffer\_new](/ref/libevent.html#event_buffer_new) —
        Create new buffered event
    -   [event\_buffer\_priority\_set](/ref/libevent.html#event_buffer_priority_set)
        — Assign a priority to a buffered event
    -   [event\_buffer\_read](/ref/libevent.html#event_buffer_read) —
        Read data from a buffered event
    -   [event\_buffer\_set\_callback](/ref/libevent.html#event_buffer_set_callback)
        — Set or reset callbacks for a buffered event
    -   [event\_buffer\_timeout\_set](/ref/libevent.html#event_buffer_timeout_set)
        — Set read and write timeouts for a buffered event
    -   [event\_buffer\_watermark\_set](/ref/libevent.html#event_buffer_watermark_set)
        — Set the watermarks for read and write events
    -   [event\_buffer\_write](/ref/libevent.html#event_buffer_write) —
        Write data to a buffered event
    -   [event\_del](/ref/libevent.html#event_del) — Remove an event
        from the set of monitored events
    -   [event\_free](/ref/libevent.html#event_free) — Free event
        resource
    -   [event\_new](/ref/libevent.html#event_new) — Create new event
    -   [event\_priority\_set](/ref/libevent.html#event_priority_set) —
        Assign a priority to an event
    -   [event\_set](/ref/libevent.html#event_set) — Prepare an event
    -   [event\_timer\_add](/ref/libevent.html#event_timer_add) — 别名
        event\_add
    -   [event\_timer\_del](/ref/libevent.html#event_timer_del) — 别名
        event\_del
    -   [event\_timer\_new](/ref/libevent.html#event_timer_new) — 别名
        event\_new
    -   [event\_timer\_set](/ref/libevent.html#event_timer_set) —
        Prepare a timer event
