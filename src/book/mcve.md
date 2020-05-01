MCVE (Monetra) Payment
======================

**目录**

-   [简介](/intro/mcve.html)
-   [安装／配置](/mcve/setup.html)
    -   [需求](/mcve/setup.html#需求)
    -   [安装](/mcve/setup.html#安装)
    -   [运行时配置](/mcve/setup.html#运行时配置)
    -   [资源类型](/mcve/setup.html#资源类型)
-   [预定义常量](/mcve/constants.html)
-   [MCVE 函数](/ref/mcve.html)
    -   [m\_checkstatus](/ref/mcve.html#m_checkstatus) — Check to see if
        a transaction has completed
    -   [m\_completeauthorizations](/ref/mcve.html#m_completeauthorizations)
        — Number of complete authorizations in queue, returning an array
        of their identifiers
    -   [m\_connect](/ref/mcve.html#m_connect) — Establish the
        connection to MCVE
    -   [m\_connectionerror](/ref/mcve.html#m_connectionerror) — Get a
        textual representation of why a connection failed
    -   [m\_deletetrans](/ref/mcve.html#m_deletetrans) — Delete
        specified transaction from MCVE\_CONN structure
    -   [m\_destroyconn](/ref/mcve.html#m_destroyconn) — Destroy the
        connection and MCVE\_CONN structure
    -   [m\_destroyengine](/ref/mcve.html#m_destroyengine) — Free memory
        associated with IP/SSL connectivity
    -   [m\_getcell](/ref/mcve.html#m_getcell) — Get a specific cell
        from a comma delimited response by column name
    -   [m\_getcellbynum](/ref/mcve.html#m_getcellbynum) — Get a
        specific cell from a comma delimited response by column number
    -   [m\_getcommadelimited](/ref/mcve.html#m_getcommadelimited) — Get
        the RAW comma delimited data returned from MCVE
    -   [m\_getheader](/ref/mcve.html#m_getheader) — Get the name of the
        column in a comma-delimited response
    -   [m\_initconn](/ref/mcve.html#m_initconn) — Create and initialize
        an MCVE\_CONN structure
    -   [m\_initengine](/ref/mcve.html#m_initengine) — Ready the client
        for IP/SSL Communication
    -   [m\_iscommadelimited](/ref/mcve.html#m_iscommadelimited) —
        Checks to see if response is comma delimited
    -   [m\_maxconntimeout](/ref/mcve.html#m_maxconntimeout) — The
        maximum amount of time the API will attempt a connection to MCVE
    -   [m\_monitor](/ref/mcve.html#m_monitor) — Perform communication
        with MCVE (send/receive data) Non-blocking
    -   [m\_numcolumns](/ref/mcve.html#m_numcolumns) — Number of columns
        returned in a comma delimited response
    -   [m\_numrows](/ref/mcve.html#m_numrows) — Number of rows returned
        in a comma delimited response
    -   [m\_parsecommadelimited](/ref/mcve.html#m_parsecommadelimited) —
        Parse the comma delimited response so m\_getcell, etc will work
    -   [m\_responsekeys](/ref/mcve.html#m_responsekeys) — Returns array
        of strings which represents the keys that can be used for
        response parameters on this transaction
    -   [m\_responseparam](/ref/mcve.html#m_responseparam) — Get a
        custom response parameter
    -   [m\_returnstatus](/ref/mcve.html#m_returnstatus) — Check to see
        if the transaction was successful
    -   [m\_setblocking](/ref/mcve.html#m_setblocking) — Set
        blocking/non-blocking mode for connection
    -   [m\_setdropfile](/ref/mcve.html#m_setdropfile) — Set the
        connection method to Drop-File
    -   [m\_setip](/ref/mcve.html#m_setip) — Set the connection method
        to IP
    -   [m\_setssl\_cafile](/ref/mcve.html#m_setssl_cafile) — Set SSL CA
        (Certificate Authority) file for verification of server
        certificate
    -   [m\_setssl\_files](/ref/mcve.html#m_setssl_files) — Set
        certificate key files and certificates if server requires client
        certificate verification
    -   [m\_setssl](/ref/mcve.html#m_setssl) — Set the connection method
        to SSL
    -   [m\_settimeout](/ref/mcve.html#m_settimeout) — Set maximum
        transaction time (per trans)
    -   [m\_sslcert\_gen\_hash](/ref/mcve.html#m_sslcert_gen_hash) —
        Generate hash for SSL client certificate verification
    -   [m\_transactionssent](/ref/mcve.html#m_transactionssent) — Check
        to see if outgoing buffer is clear
    -   [m\_transinqueue](/ref/mcve.html#m_transinqueue) — Number of
        transactions in client-queue
    -   [m\_transkeyval](/ref/mcve.html#m_transkeyval) — Add key/value
        pair to a transaction. Replaces deprecated transparam()
    -   [m\_transnew](/ref/mcve.html#m_transnew) — Start a new
        transaction
    -   [m\_transsend](/ref/mcve.html#m_transsend) — Finalize and send
        the transaction
    -   [m\_uwait](/ref/mcve.html#m_uwait) — Wait x microsecs
    -   [m\_validateidentifier](/ref/mcve.html#m_validateidentifier) —
        Whether or not to validate the passed identifier on any
        transaction it is passed to
    -   [m\_verifyconnection](/ref/mcve.html#m_verifyconnection) — Set
        whether or not to PING upon connect to verify connection
    -   [m\_verifysslcert](/ref/mcve.html#m_verifysslcert) — Set whether
        or not to verify the server ssl certificate
