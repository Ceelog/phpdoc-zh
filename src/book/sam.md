Simple Asynchronous Messaging
=============================

**目录**

-   [简介](/intro/sam.html)
-   [安装／配置](/sam/setup.html)
    -   [需求](/sam/setup.html#需求)
    -   [安装](/sam/setup.html#安装)
    -   [运行时配置](/sam/setup.html#运行时配置)
    -   [资源类型](/sam/setup.html#资源类型)
-   [预定义常量](/sam/constants.html)
-   [范例](/sam/examples.html)
    -   [Connections](/sam/examples.html#Connections)
    -   [Messages](/sam/examples.html#Messages)
    -   [Messaging
        operations](/sam/examples.html#Messaging%20operations)
    -   [Publish/Subscribe and subscriptions to
        topics](/sam/examples.html#Publish/Subscribe%20and%20subscriptions%20to%20topics)
    -   [Error handling](/sam/examples.html#Error%20handling)
-   [SAM 函数](/ref/sam.html)
    -   [SAMConnection::commit](/ref/sam.html#SAMConnection::commit) —
        Commits (completes) the current unit of work
    -   [SAMConnection::connect](/ref/sam.html#SAMConnection::connect) —
        Establishes a connection to a Messaging Server
    -   [SAMConnection::\_\_construct](/ref/sam.html#SAMConnection::__construct)
        — Creates a new connection to a Messaging Server
    -   [SAMConnection::disconnect](/ref/sam.html#SAMConnection::disconnect)
        — Disconnects from a Messaging Server
    -   [SAMConnection::errno](/ref/sam.html#SAMConnection::errno) —
        Contains the unique numeric error code of the last executed SAM
        operation
    -   [SAMConnection::error](/ref/sam.html#SAMConnection::error) —
        Contains the text description of the last failed SAM operation
    -   [SAMConnection::isConnected](/ref/sam.html#SAMConnection::isConnected)
        — Queries whether a connection is established to a Messaging
        Server
    -   [SAMConnection::peek](/ref/sam.html#SAMConnection::peek) — Read
        a message from a queue without removing it from the queue
    -   [SAMConnection::peekAll](/ref/sam.html#SAMConnection::peekAll) —
        Read one or more messages from a queue without removing it from
        the queue
    -   [SAMConnection::receive](/ref/sam.html#SAMConnection::receive) —
        Receive a message from a queue or subscription
    -   [SAMConnection::remove](/ref/sam.html#SAMConnection::remove) —
        Remove a message from a queue
    -   [SAMConnection::rollback](/ref/sam.html#SAMConnection::rollback)
        — Cancels (rolls back) an in-flight unit of work
    -   [SAMConnection::send](/ref/sam.html#SAMConnection::send) — Send
        a message to a queue or publish an item to a topic
    -   [SAMConnection::setDebug](/ref/sam.html#SAMConnection::setDebug)
        — Turn on or off additional debugging output
    -   [SAMConnection::subscribe](/ref/sam.html#SAMConnection::subscribe)
        — Create a subscription to a specified topic
    -   [SAMConnection::unsubscribe](/ref/sam.html#SAMConnection::unsubscribe)
        — Cancel a subscription to a specified topic
    -   [SAMMessage::body](/ref/sam.html#SAMMessage::body) — The body of
        the message
    -   [SAMMessage::\_\_construct](/ref/sam.html#SAMMessage::__construct)
        — Creates a new Message object
    -   [SAMMessage::header](/ref/sam.html#SAMMessage::header) — The
        header properties of the message
