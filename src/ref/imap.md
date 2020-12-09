This document can't go into detail on all the topics touched by the
provided functions. Further information is provided by the documentation
of the c-client library source (`docs/internal.txt`). and the following
RFC documents:

-   <span class="simpara">
    <a href="http://www.faqs.org/rfcs/rfc2821" class="link external">» RFC2821</a>:
    *Simple Mail Transfer Protocol* (SMTP). </span>
-   <span class="simpara">
    <a href="http://www.faqs.org/rfcs/rfc2822" class="link external">» RFC2822</a>:
    *Standard for ARPA internet text messages*. </span>
-   <span class="simpara">
    <a href="http://www.faqs.org/rfcs/rfc2060" class="link external">» RFC2060</a>:
    *Internet Message Access Protocol* (IMAP) Version 4rev1. </span>
-   <span class="simpara">
    <a href="http://www.faqs.org/rfcs/rfc1939" class="link external">» RFC1939</a>:
    *Post Office Protocol Version 3* (POP3). </span>
-   <span class="simpara">
    <a href="http://www.faqs.org/rfcs/rfc977" class="link external">» RFC977</a>:
    *Network News Transfer Protocol* (NNTP). </span>
-   <span class="simpara">
    <a href="http://www.faqs.org/rfcs/rfc2076" class="link external">» RFC2076</a>:
    *Common Internet Message Headers*. </span>
-   <span class="simpara">
    <a href="http://www.faqs.org/rfcs/rfc2045" class="link external">» RFC2045</a>
    ,
    <a href="http://www.faqs.org/rfcs/rfc2046" class="link external">» RFC2046</a>
    ,
    <a href="http://www.faqs.org/rfcs/rfc2047" class="link external">» RFC2047</a>
    ,
    <a href="http://www.faqs.org/rfcs/rfc2048" class="link external">» RFC2048</a>
    &
    <a href="http://www.faqs.org/rfcs/rfc2049" class="link external">» RFC2049</a>:
    *Multipurpose Internet Mail Extensions* (MIME). </span>

A detailed overview is also available in the books
<a href="http://www.oreilly.com/catalog/progintemail/noframes.html" class="link external">» <em>Programming Internet Email</em></a>
by David Wood and
<a href="http://oreilly.com/catalog/9780596000127/" class="link external">» Managing IMAP</a>
by Dianna Mullet & Kevin Mullet.

imap\_8bit
==========

Convert an 8bit string to a quoted-printable string

### 说明

<span class="type">string</span> <span
class="methodname">imap\_8bit</span> ( <span class="methodparam"><span
class="type">string</span> `$string`</span> )

Convert an 8bit string to a quoted-printable string (according to
<a href="http://www.faqs.org/rfcs/rfc2045" class="link external">» RFC2045</a>,
section 6.7).

### 参数

`string`  
The 8bit string to convert

### 返回值

Returns a quoted-printable string.

### 参见

-   <span class="function">imap\_qprint</span>

imap\_alerts
============

Returns all IMAP alert messages that have occurred

### 说明

<span class="type">array</span> <span
class="methodname">imap\_alerts</span> ( <span
class="methodparam">void</span> )

Returns all of the IMAP alert messages generated since the last <span
class="function">imap\_alerts</span> call, or the beginning of the page.

When <span class="function">imap\_alerts</span> is called, the alert
stack is subsequently cleared. The IMAP specification requires that
these messages be passed to the user.

### 返回值

Returns an array of all of the IMAP alert messages generated or
**`false`** if no alert messages are available.

### 参见

-   <span class="function">imap\_errors</span>

imap\_append
============

Append a string message to a specified mailbox

### 说明

<span class="type">bool</span> <span
class="methodname">imap\_append</span> ( <span class="methodparam"><span
class="type">resource</span> `$imap_stream`</span> , <span
class="methodparam"><span class="type">string</span> `$mailbox`</span> ,
<span class="methodparam"><span class="type">string</span>
`$message`</span> \[, <span class="methodparam"><span
class="type">string</span> `$options`<span class="initializer"> =
**`null`**</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$internal_date`<span class="initializer"> =
**`null`**</span></span> \]\] )

Appends a string `message` to the specified `mailbox`.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`mailbox`  
The mailbox name, see <span class="function">imap\_open</span> for more
information

**Warning**
Passing untrusted data to this parameter is *insecure*, unless
<a href="/imap/setup.html#" class="link">imap.enable_insecure_rsh</a> is
disabled.

`message`  
The message to be append, as a string

When talking to the Cyrus IMAP server, you must use "\\r\\n" as your
end-of-line terminator instead of "\\n" or the operation will fail

`options`  
If provided, the `options` will also be written to the `mailbox`

`internal_date`  
If this parameter is set, it will set the INTERNALDATE on the appended
message. The parameter should be a date string that conforms to the
rfc2060 specifications for a date\_time value.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">imap\_append</span> example**

``` php
<?php
$stream = imap_open("{imap.example.org}INBOX.Drafts", "username", "password");

$check = imap_check($stream);
echo "Msg Count before append: ". $check->Nmsgs . "\n";

imap_append($stream, "{imap.example.org}INBOX.Drafts"
                   , "From: me@example.com\r\n"
                   . "To: you@example.com\r\n"
                   . "Subject: test\r\n"
                   . "\r\n"
                   . "this is a test message, please ignore\r\n"
                   );

$check = imap_check($stream);
echo "Msg Count after append : ". $check->Nmsgs . "\n";

imap_close($stream);
?>
```

imap\_base64
============

Decode BASE64 encoded text

### 说明

<span class="type">string</span> <span
class="methodname">imap\_base64</span> ( <span class="methodparam"><span
class="type">string</span> `$text`</span> )

Decodes the given BASE-64 encoded `text`.

### 参数

`text`  
The encoded text

### 返回值

Returns the decoded message as a string.

### 参见

-   <span class="function">imap\_binary</span>
-   <span class="function">base64\_encode</span>
-   <span class="function">base64\_decode</span>
-   <a href="http://www.faqs.org/rfcs/rfc2045" class="link external">» RFC2045</a>,
    Section 6.8

imap\_binary
============

Convert an 8bit string to a base64 string

### 说明

<span class="type">string</span> <span
class="methodname">imap\_binary</span> ( <span class="methodparam"><span
class="type">string</span> `$string`</span> )

Convert an 8bit string to a base64 string according to
<a href="http://www.faqs.org/rfcs/rfc2045" class="link external">» RFC2045</a>,
Section 6.8.

### 参数

`string`  
The 8bit string

### 返回值

Returns a base64 encoded string.

### 参见

-   <span class="function">imap\_base64</span>

imap\_body
==========

Read the message body

### 说明

<span class="type">string</span> <span
class="methodname">imap\_body</span> ( <span class="methodparam"><span
class="type">resource</span> `$imap_stream`</span> , <span
class="methodparam"><span class="type">int</span> `$msg_number`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$options`<span class="initializer"> = 0</span></span> \] )

<span class="function">imap\_body</span> returns the body of the
message, numbered `msg_number` in the current mailbox.

<span class="function">imap\_body</span> will only return a verbatim
copy of the message body. To extract single parts of a multipart
MIME-encoded message you have to use <span
class="function">imap\_fetchstructure</span> to analyze its structure
and <span class="function">imap\_fetchbody</span> to extract a copy of a
single body component.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`msg_number`  
The message number

`options`  
The optional `options` are a bit mask with one or more of the following:

-   <span class="simpara"> **`FT_UID`** - The `msg_number` is a UID
    </span>
-   <span class="simpara"> **`FT_PEEK`** - Do not set the \\Seen flag if
    not already set </span>
-   <span class="simpara"> **`FT_INTERNAL`** - The return string is in
    internal format, will not canonicalize to CRLF. </span>

### 返回值

Returns the body of the specified message, as a string.

imap\_bodystruct
================

Read the structure of a specified body section of a specific message

### 说明

<span class="type">object</span> <span
class="methodname">imap\_bodystruct</span> ( <span
class="methodparam"><span class="type">resource</span>
`$imap_stream`</span> , <span class="methodparam"><span
class="type">int</span> `$msg_number`</span> , <span
class="methodparam"><span class="type">string</span> `$section`</span> )

Read the structure of a specified body section of a specific message.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`msg_number`  
The message number

`section`  
The body section to read

### 返回值

Returns the information in an object, for a detailed description of the
object structure and properties see <span
class="function">imap\_fetchstructure</span>.

### 参见

-   <span class="function">imap\_fetchstructure</span>

imap\_check
===========

Check current mailbox

### 说明

<span class="type">object</span> <span
class="methodname">imap\_check</span> ( <span class="methodparam"><span
class="type">resource</span> `$imap_stream`</span> )

Checks information about the current mailbox.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

### 返回值

Returns the information in an object with following properties:

-   <span class="simpara"> **`Date`** - current system time formatted
    according to
    <a href="http://www.faqs.org/rfcs/rfc2822" class="link external">» RFC2822</a>
    </span>
-   <span class="simpara"> **`Driver`** - protocol used to access this
    mailbox: POP3, IMAP, NNTP </span>
-   <span class="simpara"> **`Mailbox`** - the mailbox name </span>
-   <span class="simpara"> **`Nmsgs`** - number of messages in the
    mailbox </span>
-   <span class="simpara"> **`Recent`** - number of recent messages in
    the mailbox </span>

Returns **`false`** on failure.

### 范例

**示例 \#1 <span class="function">imap\_check</span> example**

``` php
<?php

$imap_obj = imap_check($imap_stream);
var_dump($imap_obj);

?>
```

以上例程的输出类似于：

    object(stdClass)(5) {
      ["Date"]=>
      string(37) "Wed, 10 Dec 2003 17:56:54 +0100 (CET)"
      ["Driver"]=>
      string(4) "imap"
      ["Mailbox"]=>
      string(54)
      "{www.example.com:143/imap/user="foo@example.com"}INBOX"
      ["Nmsgs"]=>
      int(1)
      ["Recent"]=>
      int(0)
    }

imap\_clearflag\_full
=====================

Clears flags on messages

### 说明

<span class="type">bool</span> <span
class="methodname">imap\_clearflag\_full</span> ( <span
class="methodparam"><span class="type">resource</span>
`$imap_stream`</span> , <span class="methodparam"><span
class="type">string</span> `$sequence`</span> , <span
class="methodparam"><span class="type">string</span> `$flag`</span> \[,
<span class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = 0</span></span> \] )

This function causes a store to delete the specified `flag` to the flags
set for the messages in the specified `sequence`.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`sequence`  
A sequence of message numbers. You can enumerate desired messages with
the *X,Y* syntax, or retrieve all messages within an interval with the
*X:Y* syntax

`flag`  
The flags which you can unset are "\\\\Seen", "\\\\Answered",
"\\\\Flagged", "\\\\Deleted", and "\\\\Draft" (as defined by
<a href="http://www.faqs.org/rfcs/rfc2060" class="link external">» RFC2060</a>)

`options`  
`options` are a bit mask and may contain the single option:

-   <span class="simpara"> **`ST_UID`** - The sequence argument contains
    UIDs instead of sequence numbers </span>

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">imap\_setflag\_full</span>

imap\_close
===========

Close an IMAP stream

### 说明

<span class="type">bool</span> <span
class="methodname">imap\_close</span> ( <span class="methodparam"><span
class="type">resource</span> `$imap_stream`</span> \[, <span
class="methodparam"><span class="type">int</span> `$flag`<span
class="initializer"> = 0</span></span> \] )

Closes the imap stream.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`flag`  
If set to **`CL_EXPUNGE`**, the function will silently expunge the
mailbox before closing, removing all messages marked for deletion. You
can achieve the same thing by using <span
class="function">imap\_expunge</span>

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">imap\_open</span>

imap\_create
============

别名 <span class="function">imap\_createmailbox</span>

### 说明

此函数是该函数的别名： <span
class="function">imap\_createmailbox</span>.

imap\_createmailbox
===================

Create a new mailbox

### 说明

<span class="type">bool</span> <span
class="methodname">imap\_createmailbox</span> ( <span
class="methodparam"><span class="type">resource</span>
`$imap_stream`</span> , <span class="methodparam"><span
class="type">string</span> `$mailbox`</span> )

Creates a new mailbox specified by `mailbox`.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`mailbox`  
The mailbox name, see <span class="function">imap\_open</span> for more
information. Names containing international characters should be encoded
by <span class="function">imap\_utf7\_encode</span>

**Warning**
Passing untrusted data to this parameter is *insecure*, unless
<a href="/imap/setup.html#" class="link">imap.enable_insecure_rsh</a> is
disabled.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">imap\_createmailbox</span> example**

``` php
<?php
$mbox = imap_open("{imap.example.org}", "username", "password", OP_HALFOPEN)
     or die("can't connect: " . imap_last_error());

$name1 = "phpnewbox";
$name2 = imap_utf7_encode("phpnewböx"); // phpnewb&w7Y-x

$newname = $name1;

echo "Newname will be '$name1'<br />\n";

// we will now create a new mailbox "phptestbox" in your inbox folder,
// check its status after creation and finally remove it to restore
// your inbox to its initial state

if (@imap_createmailbox($mbox, imap_utf7_encode("{imap.example.org}INBOX.$newname"))) {
    $status = @imap_status($mbox, "{imap.example.org}INBOX.$newname", SA_ALL);
    if ($status) {
        echo "your new mailbox '$name1' has the following status:<br />\n";
        echo "Messages:   " . $status->messages    . "<br />\n";
        echo "Recent:     " . $status->recent      . "<br />\n";
        echo "Unseen:     " . $status->unseen      . "<br />\n";
        echo "UIDnext:    " . $status->uidnext     . "<br />\n";
        echo "UIDvalidity:" . $status->uidvalidity . "<br />\n";

        if (imap_renamemailbox($mbox, "{imap.example.org}INBOX.$newname", "{imap.example.org}INBOX.$name2")) {
            echo "renamed new mailbox from '$name1' to '$name2'<br />\n";
            $newname = $name2;
        } else {
            echo "imap_renamemailbox on new mailbox failed: " . imap_last_error() . "<br />\n";
        }
    } else {
        echo "imap_status on new mailbox failed: " . imap_last_error() . "<br />\n";
    }

    if (@imap_deletemailbox($mbox, "{imap.example.org}INBOX.$newname")) {
        echo "new mailbox removed to restore initial state<br />\n";
    } else {
        echo "imap_deletemailbox on new mailbox failed: " . implode("<br />\n", imap_errors()) . "<br />\n";
    }

} else {
    echo "could not create new mailbox: " . implode("<br />\n", imap_errors()) . "<br />\n";
}

imap_close($mbox);
?>
```

### 参见

-   <span class="function">imap\_renamemailbox</span>
-   <span class="function">imap\_deletemailbox</span>

imap\_delete
============

Mark a message for deletion from current mailbox

### 说明

<span class="type">bool</span> <span
class="methodname">imap\_delete</span> ( <span class="methodparam"><span
class="type">resource</span> `$imap_stream`</span> , <span
class="methodparam"><span class="type">int</span> `$msg_number`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$options`<span class="initializer"> = 0</span></span> \] )

Marks messages listed in `msg_number` for deletion. Messages marked for
deletion will stay in the mailbox until either <span
class="function">imap\_expunge</span> is called or <span
class="function">imap\_close</span> is called with the optional
parameter **`CL_EXPUNGE`**.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`msg_number`  
The message number

`options`  
You can set the **`FT_UID`** which tells the function to treat the
`msg_number` argument as a *UID*.

### 返回值

Returns **`true`**.

### 范例

**示例 \#1 <span class="function">imap\_delete</span> example**

``` php
<?php

$mbox = imap_open("{imap.example.org}INBOX", "username", "password")
    or die("Can't connect: " . imap_last_error());

$check = imap_mailboxmsginfo($mbox);
echo "Messages before delete: " . $check->Nmsgs . "<br />\n";

imap_delete($mbox, 1);

$check = imap_mailboxmsginfo($mbox);
echo "Messages after  delete: " . $check->Nmsgs . "<br />\n";

imap_expunge($mbox);

$check = imap_mailboxmsginfo($mbox);
echo "Messages after expunge: " . $check->Nmsgs . "<br />\n";

imap_close($mbox);
?>
```

### 注释

> **Note**:
>
> IMAP mailboxes may not have their message flags saved between
> connections, so <span class="function">imap\_expunge</span> should be
> called during the same connection in order to guarantee that messages
> marked for deletion will actually be purged.

### 参见

-   <span class="function">imap\_undelete</span>
-   <span class="function">imap\_expunge</span>
-   <span class="function">imap\_close</span>

imap\_deletemailbox
===================

Delete a mailbox

### 说明

<span class="type">bool</span> <span
class="methodname">imap\_deletemailbox</span> ( <span
class="methodparam"><span class="type">resource</span>
`$imap_stream`</span> , <span class="methodparam"><span
class="type">string</span> `$mailbox`</span> )

Deletes the specified `mailbox`.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`mailbox`  
The mailbox name, see <span class="function">imap\_open</span> for more
information

**Warning**
Passing untrusted data to this parameter is *insecure*, unless
<a href="/imap/setup.html#" class="link">imap.enable_insecure_rsh</a> is
disabled.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">imap\_createmailbox</span>
-   <span class="function">imap\_renamemailbox</span>
-   <span class="function">imap\_open</span> for the format of `mbox`

imap\_errors
============

Returns all of the IMAP errors that have occurred

### 说明

<span class="type">array</span> <span
class="methodname">imap\_errors</span> ( <span
class="methodparam">void</span> )

Gets all of the IMAP errors (if any) that have occurred during this page
request or since the error stack was reset.

When <span class="function">imap\_errors</span> is called, the error
stack is subsequently cleared.

### 返回值

This function returns an array of all of the IMAP error messages
generated since the last <span class="function">imap\_errors</span>
call, or the beginning of the page. Returns **`false`** if no error
messages are available.

### 参见

-   <span class="function">imap\_last\_error</span>
-   <span class="function">imap\_alerts</span>

imap\_expunge
=============

Delete all messages marked for deletion

### 说明

<span class="type">bool</span> <span
class="methodname">imap\_expunge</span> ( <span
class="methodparam"><span class="type">resource</span>
`$imap_stream`</span> )

Deletes all the messages marked for deletion by <span
class="function">imap\_delete</span>, <span
class="function">imap\_mail\_move</span>, or <span
class="function">imap\_setflag\_full</span>.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

### 返回值

Returns **`true`**.

imap\_fetch\_overview
=====================

Read an overview of the information in the headers of the given message

### 说明

<span class="type">array</span> <span
class="methodname">imap\_fetch\_overview</span> ( <span
class="methodparam"><span class="type">resource</span>
`$imap_stream`</span> , <span class="methodparam"><span
class="type">string</span> `$sequence`</span> \[, <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = 0</span></span> \] )

This function fetches mail headers for the given `sequence` and returns
an overview of their contents.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`sequence`  
A message sequence description. You can enumerate desired messages with
the *X,Y* syntax, or retrieve all messages within an interval with the
*X:Y* syntax

`options`  
`sequence` will contain a sequence of message indices or UIDs, if this
parameter is set to **`FT_UID`**.

### 返回值

Returns an array of objects describing one message header each. The
object will only define a property if it exists. The possible properties
are:

-   <span class="simpara"> *subject* - the messages subject </span>
-   <span class="simpara"> *from* - who sent it </span>
-   <span class="simpara"> *to* - recipient </span>
-   <span class="simpara"> *date* - when was it sent </span>
-   <span class="simpara"> *message\_id* - Message-ID </span>
-   <span class="simpara"> *references* - is a reference to this message
    id </span>
-   <span class="simpara"> *in\_reply\_to* - is a reply to this message
    id </span>
-   <span class="simpara"> *size* - size in bytes </span>
-   <span class="simpara"> *uid* - UID the message has in the mailbox
    </span>
-   <span class="simpara"> *msgno* - message sequence number in the
    mailbox </span>
-   <span class="simpara"> *recent* - this message is flagged as recent
    </span>
-   <span class="simpara"> *flagged* - this message is flagged </span>
-   <span class="simpara"> *answered* - this message is flagged as
    answered </span>
-   <span class="simpara"> *deleted* - this message is flagged for
    deletion </span>
-   <span class="simpara"> *seen* - this message is flagged as already
    read </span>
-   <span class="simpara"> *draft* - this message is flagged as being a
    draft </span>
-   <span class="simpara"> *udate* - the UNIX timestamp of the arrival
    date </span>

### 范例

**示例 \#1 <span class="function">imap\_fetch\_overview</span> example**

``` php
<?php
$mbox = imap_open("{imap.example.org:143}INBOX", "username", "password")
     or die("can't connect: " . imap_last_error());

$MC = imap_check($mbox);

// Fetch an overview for all messages in INBOX
$result = imap_fetch_overview($mbox,"1:{$MC->Nmsgs}",0);
foreach ($result as $overview) {
    echo "#{$overview->msgno} ({$overview->date}) - From: {$overview->from}
    {$overview->subject}\n";
}
imap_close($mbox);
?>
```

### 参见

-   <span class="function">imap\_fetchheader</span>

imap\_fetchbody
===============

Fetch a particular section of the body of the message

### 说明

<span class="type">string</span> <span
class="methodname">imap\_fetchbody</span> ( <span
class="methodparam"><span class="type">resource</span>
`$imap_stream`</span> , <span class="methodparam"><span
class="type">int</span> `$msg_number`</span> , <span
class="methodparam"><span class="type">string</span> `$section`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$options`<span class="initializer"> = 0</span></span> \] )

Fetch of a particular section of the body of the specified messages.
Body parts are not decoded by this function.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`msg_number`  
The message number

`section`  
The part number. It is a string of integers delimited by period which
index into a body part list as per the IMAP4 specification

`options`  
A bitmask with one or more of the following:

-   <span class="simpara"> **`FT_UID`** - The `msg_number` is a UID
    </span>
-   <span class="simpara"> **`FT_PEEK`** - Do not set the \\Seen flag if
    not already set </span>
-   <span class="simpara"> **`FT_INTERNAL`** - The return string is in
    internal format, will not canonicalize to CRLF. </span>

### 返回值

Returns a particular section of the body of the specified messages as a
text string.

### 参见

-   <span class="function">imap\_savebody</span>
-   <span class="function">imap\_fetchstructure</span>

imap\_fetchheader
=================

Returns header for a message

### 说明

<span class="type">string</span> <span
class="methodname">imap\_fetchheader</span> ( <span
class="methodparam"><span class="type">resource</span>
`$imap_stream`</span> , <span class="methodparam"><span
class="type">int</span> `$msg_number`</span> \[, <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = 0</span></span> \] )

This function causes a fetch of the complete, unfiltered
<a href="http://www.faqs.org/rfcs/rfc2822" class="link external">» RFC2822</a>
format header of the specified message.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`msg_number`  
The message number

`options`  
The possible `options` are:

-   <span class="simpara"> **`FT_UID`** - The `msgno` argument is a UID
    </span>
-   <span class="simpara"> **`FT_INTERNAL`** - The return string is in
    "internal" format, without any attempt to canonicalize to CRLF
    newlines </span>
-   <span class="simpara"> **`FT_PREFETCHTEXT`** - The RFC822.TEXT
    should be pre-fetched at the same time. This avoids an extra RTT on
    an IMAP connection if a full message text is desired (e.g. in a
    "save to local file" operation) </span>

### 返回值

Returns the header of the specified message as a text string.

### 参见

-   <span class="function">imap\_fetch\_overview</span>

imap\_fetchmime
===============

Fetch MIME headers for a particular section of the message

### 说明

<span class="type">string</span> <span
class="methodname">imap\_fetchmime</span> ( <span
class="methodparam"><span class="type">resource</span>
`$imap_stream`</span> , <span class="methodparam"><span
class="type">int</span> `$msg_number`</span> , <span
class="methodparam"><span class="type">string</span> `$section`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$options`<span class="initializer"> = 0</span></span> \] )

Fetch the MIME headers of a particular section of the body of the
specified messages.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`msg_number`  
The message number

`section`  
The part number. It is a string of integers delimited by period which
index into a body part list as per the IMAP4 specification

`options`  
A bitmask with one or more of the following:

-   <span class="simpara"> **`FT_UID`** - The `msg_number` is a UID
    </span>
-   <span class="simpara"> **`FT_PEEK`** - Do not set the \\Seen flag if
    not already set </span>
-   <span class="simpara"> **`FT_INTERNAL`** - The return string is in
    internal format, will not canonicalize to CRLF. </span>

### 返回值

Returns the MIME headers of a particular section of the body of the
specified messages as a text string.

### 参见

-   <span class="function">imap\_fetchbody</span>
-   <span class="function">imap\_fetchstructure</span>
-   <span class="function">imap\_fetchheader</span>

imap\_fetchstructure
====================

Read the structure of a particular message

### 说明

<span class="type"><span class="type">object</span><span
class="type">false</span></span> <span
class="methodname">imap\_fetchstructure</span> ( <span
class="methodparam"><span class="type">resource</span>
`$imap_stream`</span> , <span class="methodparam"><span
class="type">int</span> `$msg_number`</span> \[, <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = 0</span></span> \] )

Fetches all the structured information for a given message.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`msg_number`  
The message number

`options`  
This optional parameter only has a single option, **`FT_UID`**, which
tells the function to treat the `msg_number` argument as a *UID*.

### 返回值

Returns an object with properties listed in the table below,
或者在失败时返回 **`false`**.

|               |                                                                                                                                                               |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| type          | Primary body type                                                                                                                                             |
| encoding      | Body transfer encoding                                                                                                                                        |
| ifsubtype     | **`true`** if there is a subtype string                                                                                                                       |
| subtype       | MIME subtype                                                                                                                                                  |
| ifdescription | **`true`** if there is a description string                                                                                                                   |
| description   | Content description string                                                                                                                                    |
| ifid          | **`true`** if there is an identification string                                                                                                               |
| id            | Identification string                                                                                                                                         |
| lines         | Number of lines                                                                                                                                               |
| bytes         | Number of bytes                                                                                                                                               |
| ifdisposition | **`true`** if there is a disposition string                                                                                                                   |
| disposition   | Disposition string                                                                                                                                            |
| ifdparameters | **`true`** if the `dparameters` array exists                                                                                                                  |
| dparameters   | An array of objects where each object has an *"attribute"* and a *"value"* property corresponding to the parameters on the *Content-disposition* MIME header. |
| ifparameters  | **`true`** if the parameters array exists                                                                                                                     |
| parameters    | An array of objects where each object has an *"attribute"* and a *"value"* property.                                                                          |
| parts         | An array of objects identical in structure to the top-level object, each of which corresponds to a MIME body part.                                            |

| Value | Type        | Constant        |
|-------|-------------|-----------------|
| 0     | text        | TYPETEXT        |
| 1     | multipart   | TYPEMULTIPART   |
| 2     | message     | TYPEMESSAGE     |
| 3     | application | TYPEAPPLICATION |
| 4     | audio       | TYPEAUDIO       |
| 5     | image       | TYPEIMAGE       |
| 6     | video       | TYPEVIDEO       |
| 7     | model       | TYPEMODEL       |
| 8     | other       | TYPEOTHER       |

| Value | Type             | Constant           |
|-------|------------------|--------------------|
| 0     | 7bit             | ENC7BIT            |
| 1     | 8bit             | ENC8BIT            |
| 2     | Binary           | ENCBINARY          |
| 3     | Base64           | ENCBASE64          |
| 4     | Quoted-Printable | ENCQUOTEDPRINTABLE |
| 5     | other            | ENCOTHER           |

### 参见

-   <span class="function">imap\_fetchbody</span>
-   <span class="function">imap\_bodystruct</span>

imap\_fetchtext
===============

别名 <span class="function">imap\_body</span>

### 说明

此函数是该函数的别名： <span class="function">imap\_body</span>.

imap\_gc
========

Clears IMAP cache

### 说明

<span class="type">bool</span> <span class="methodname">imap\_gc</span>
( <span class="methodparam"><span class="type">resource</span>
`$imap_stream`</span> , <span class="methodparam"><span
class="type">int</span> `$caches`</span> )

Purges the cache of entries of a specific type.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`caches`  
Specifies the cache to purge. It may one or a combination of the
following constants: **`IMAP_GC_ELT`** (message cache elements),
**`IMAP_GC_ENV`** (envelope and bodies), **`IMAP_GC_TEXTS`** (texts).

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">imap\_gc</span> example**

``` php
<?php

$mbox = imap_open("{imap.example.org:143}", "username", "password");

imap_gc($mbox, IMAP_GC_ELT);

?>
```

imap\_get\_quota
================

Retrieve the quota level settings, and usage statics per mailbox

### 说明

<span class="type">array</span> <span
class="methodname">imap\_get\_quota</span> ( <span
class="methodparam"><span class="type">resource</span>
`$imap_stream`</span> , <span class="methodparam"><span
class="type">string</span> `$quota_root`</span> )

Retrieve the quota level settings, and usage statics per mailbox.

For a non-admin user version of this function, please see the <span
class="function">imap\_get\_quotaroot</span> function of PHP.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`quota_root`  
`quota_root` should normally be in the form of *user.name* where name is
the mailbox you wish to retrieve information about.

### 返回值

Returns an array with integer values limit and usage for the given
mailbox. The value of limit represents the total amount of space allowed
for this mailbox. The usage value represents the mailboxes current level
of capacity. Will return **`false`** in the case of failure.

As of PHP 4.3, the function more properly reflects the functionality as
dictated by the
<a href="http://www.faqs.org/rfcs/rfc2087" class="link external">» RFC2087</a>.
The array return value has changed to support an unlimited number of
returned resources (i.e. messages, or sub-folders) with each named
resource receiving an individual array key. Each key value then contains
an another array with the usage and limit values within it.

For backwards compatibility reasons, the original access methods are
still available for use, although it is suggested to update.

### 范例

**示例 \#1 <span class="function">imap\_get\_quota</span> example**

``` php
<?php
$mbox = imap_open("{imap.example.org}", "mailadmin", "password", OP_HALFOPEN)
      or die("can't connect: " . imap_last_error());

$quota_value = imap_get_quota($mbox, "user.kalowsky");
if (is_array($quota_value)) {
    echo "Usage level is: " . $quota_value['usage'];
    echo "Limit level is: " . $quota_value['limit'];
}

imap_close($mbox);
?>
```

**示例 \#2 <span class="function">imap\_get\_quota</span> 4.3 or greater
example**

``` php
<?php
$mbox = imap_open("{imap.example.org}", "mailadmin", "password", OP_HALFOPEN)
      or die("can't connect: " . imap_last_error());

$quota_values = imap_get_quota($mbox, "user.kalowsky");
if (is_array($quota_values)) {
   $storage = $quota_values['STORAGE'];
   echo "STORAGE usage level is: " .  $storage['usage'];
   echo "STORAGE limit level is: " .  $storage['limit'];

   $message = $quota_values['MESSAGE'];
   echo "MESSAGE usage level is: " .  $message['usage'];
   echo "MESSAGE limit is: " .  $message['limit'];

   /* ...  */
}

imap_close($mbox);
?>
```

### 注释

This function is currently only available to users of the c-client2000
or greater library.

The given `imap_stream` must be opened as the mail administrator,
otherwise this function will fail.

### 参见

-   <span class="function">imap\_open</span>
-   <span class="function">imap\_set\_quota</span>
-   <span class="function">imap\_get\_quotaroot</span>

imap\_get\_quotaroot
====================

Retrieve the quota settings per user

### 说明

<span class="type">array</span> <span
class="methodname">imap\_get\_quotaroot</span> ( <span
class="methodparam"><span class="type">resource</span>
`$imap_stream`</span> , <span class="methodparam"><span
class="type">string</span> `$quota_root`</span> )

Retrieve the quota settings per user. The limit value represents the
total amount of space allowed for this user's total mailbox usage. The
usage value represents the user's current total mailbox capacity.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`quota_root`  
`quota_root` should normally be in the form of which mailbox (i.e.
INBOX).

### 返回值

Returns an array of integer values pertaining to the specified user
mailbox. All values contain a key based upon the resource name, and a
corresponding array with the usage and limit values within.

This function will return **`false`** in the case of call failure, and
an array of information about the connection upon an un-parsable
response from the server.

### 范例

**示例 \#1 <span class="function">imap\_get\_quotaroot</span> example**

``` php
<?php
$mbox = imap_open("{imap.example.org}", "kalowsky", "password", OP_HALFOPEN)
      or die("can't connect: " . imap_last_error());

$quota = imap_get_quotaroot($mbox, "INBOX");
if (is_array($quota)) {
   $storage = $quota['STORAGE'];
   echo "STORAGE usage level is: " .  $storage['usage'];
   echo "STORAGE limit level is: " .  $storage['limit'];

   $message = $quota['MESSAGE'];
   echo "MESSAGE usage level is: " .  $message['usage'];
   echo "MESSAGE limit level is: " .  $message['limit'];

   /* ...  */

}

imap_close($mbox);
?>
```

### 注释

This function is currently only available to users of the c-client2000
or greater library.

The `imap_stream` should be opened as the user whose mailbox you wish to
check.

### 参见

-   <span class="function">imap\_open</span>
-   <span class="function">imap\_set\_quota</span>
-   <span class="function">imap\_get\_quota</span>

imap\_getacl
============

Gets the ACL for a given mailbox

### 说明

<span class="type">array</span> <span
class="methodname">imap\_getacl</span> ( <span class="methodparam"><span
class="type">resource</span> `$imap_stream`</span> , <span
class="methodparam"><span class="type">string</span> `$mailbox`</span> )

Gets the ACL for a given mailbox.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`mailbox`  
The mailbox name, see <span class="function">imap\_open</span> for more
information

**Warning**
Passing untrusted data to this parameter is *insecure*, unless
<a href="/imap/setup.html#" class="link">imap.enable_insecure_rsh</a> is
disabled.

### 返回值

Returns an associative array of "folder" =\> "acl" pairs.

### 范例

**示例 \#1 <span class="function">imap\_getacl</span> example**

``` php
<?php

print_r(imap_getacl($conn_id, 'user.joecool'));

?>
```

以上例程的输出类似于：

    Array
    (
        [asubfolder] => lrswipcda
        [anothersubfolder] => lrswipcda
    )

### 注释

This function is currently only available to users of the c-client2000
or greater library.

### 参见

-   <span class="function">imap\_setacl</span>

imap\_getmailboxes
==================

Read the list of mailboxes, returning detailed information on each one

### 说明

<span class="type">array</span> <span
class="methodname">imap\_getmailboxes</span> ( <span
class="methodparam"><span class="type">resource</span>
`$imap_stream`</span> , <span class="methodparam"><span
class="type">string</span> `$ref`</span> , <span
class="methodparam"><span class="type">string</span> `$pattern`</span> )

Gets information on the mailboxes.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`ref`  
`ref` should normally be just the server specification as described in
<span class="function">imap\_open</span>

**Warning**
Passing untrusted data to this parameter is *insecure*, unless
<a href="/imap/setup.html#" class="link">imap.enable_insecure_rsh</a> is
disabled.

`pattern`  
指定在邮箱层级的何处开始查找。

在组成 `pattern` 的字符中可使用两个特殊字符： '*\**' 和 '*%*'。 '*\**'
是指返回所有邮箱目录. 如果将 '*\**' 作为 `pattern` 参数时,
则会返回整个邮箱层级结构。 '*%*' 是指只返回当前级次。 '*%*' 作为
`pattern` 参数则只会返回顶层邮箱； '*\~/mail/%*' 用于 *UW\_IMAPD*
则会返回名为 `~/mail` 的目录, 但不包含其子目录。

### 返回值

Returns an array of objects containing mailbox information. Each object
has the attributes `name`, specifying the full name of the mailbox;
`delimiter`, which is the hierarchy delimiter for the part of the
hierarchy this mailbox is in; and `attributes`. `Attributes` is a
bitmask that can be tested against:

-   **`LATT_NOINFERIORS`** - This mailbox not contains, and may not
    contain any "children" (there are no mailboxes below this one).
    Calling <span class="function">imap\_createmailbox</span> will not
    work on this mailbox.

-   **`LATT_NOSELECT`** - This is only a container, not a mailbox - you
    cannot open it.

-   **`LATT_MARKED`** - This mailbox is marked. This means that it may
    contain new messages since the last time it was checked. Not
    provided by all IMAP servers.

-   **`LATT_UNMARKED`** - This mailbox is not marked, does not contain
    new messages. If either **`MARKED`** or **`UNMARKED`** is provided,
    you can assume the IMAP server supports this feature for this
    mailbox.

-   **`LATT_REFERRAL`** - This container has a referral to a remote
    mailbox.

-   **`LATT_HASCHILDREN`** - This mailbox has selectable inferiors.

-   **`LATT_HASNOCHILDREN`** - This mailbox has no selectable inferiors.

### 范例

**示例 \#1 <span class="function">imap\_getmailboxes</span> example**

``` php
<?php
$mbox = imap_open("{imap.example.org}", "username", "password", OP_HALFOPEN)
      or die("can't connect: " . imap_last_error());

$list = imap_getmailboxes($mbox, "{imap.example.org}", "*");
if (is_array($list)) {
    foreach ($list as $key => $val) {
        echo "($key) ";
        echo imap_utf7_decode($val->name) . ",";
        echo "'" . $val->delimiter . "',";
        echo $val->attributes . "<br />\n";
    }
} else {
    echo "imap_getmailboxes failed: " . imap_last_error() . "\n";
}

imap_close($mbox);
?>
```

### 参见

-   <span class="function">imap\_getsubscribed</span>

imap\_getsubscribed
===================

List all the subscribed mailboxes

### 说明

<span class="type">array</span> <span
class="methodname">imap\_getsubscribed</span> ( <span
class="methodparam"><span class="type">resource</span>
`$imap_stream`</span> , <span class="methodparam"><span
class="type">string</span> `$ref`</span> , <span
class="methodparam"><span class="type">string</span> `$pattern`</span> )

Gets information about the subscribed mailboxes.

Identical to <span class="function">imap\_getmailboxes</span>, except
that it only returns mailboxes that the user is subscribed to.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`ref`  
`ref` should normally be just the server specification as described in
<span class="function">imap\_open</span>

**Warning**
Passing untrusted data to this parameter is *insecure*, unless
<a href="/imap/setup.html#" class="link">imap.enable_insecure_rsh</a> is
disabled.

`pattern`  
指定在邮箱层级的何处开始查找。

在组成 `pattern` 的字符中可使用两个特殊字符： '*\**' 和 '*%*'。 '*\**'
是指返回所有邮箱目录. 如果将 '*\**' 作为 `pattern` 参数时,
则会返回整个邮箱层级结构。 '*%*' 是指只返回当前级次。 '*%*' 作为
`pattern` 参数则只会返回顶层邮箱； '*\~/mail/%*' 用于 *UW\_IMAPD*
则会返回名为 `~/mail` 的目录, 但不包含其子目录。

### 返回值

Returns an array of objects containing mailbox information. Each object
has the attributes `name`, specifying the full name of the mailbox;
`delimiter`, which is the hierarchy delimiter for the part of the
hierarchy this mailbox is in; and `attributes`. `Attributes` is a
bitmask that can be tested against:

-   <span class="simpara"> **`LATT_NOINFERIORS`** - This mailbox has no
    "children" (there are no mailboxes below this one). </span>
-   <span class="simpara"> **`LATT_NOSELECT`** - This is only a
    container, not a mailbox - you cannot open it. </span>
-   <span class="simpara"> **`LATT_MARKED`** - This mailbox is marked.
    Only used by UW-IMAPD. </span>
-   <span class="simpara"> **`LATT_UNMARKED`** - This mailbox is not
    marked. Only used by UW-IMAPD. </span>
-   <span class="simpara"> **`LATT_REFERRAL`** - This container has a
    referral to a remote mailbox. </span>
-   <span class="simpara"> **`LATT_HASCHILDREN`** - This mailbox has
    selectable inferiors. </span>
-   <span class="simpara"> **`LATT_HASNOCHILDREN`** - This mailbox has
    no selectable inferiors. </span>

imap\_header
============

别名 <span class="function">imap\_headerinfo</span>

### 说明

此函数是该函数的别名： <span class="function">imap\_headerinfo</span>.

imap\_headerinfo
================

Read the header of the message

### 说明

<span class="type">object</span> <span
class="methodname">imap\_headerinfo</span> ( <span
class="methodparam"><span class="type">resource</span>
`$imap_stream`</span> , <span class="methodparam"><span
class="type">int</span> `$msg_number`</span> \[, <span
class="methodparam"><span class="type">int</span> `$fromlength`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$subjectlength`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$defaulthost`<span
class="initializer"> = **`null`**</span></span> \]\]\] )

Gets information about the given message number by reading its headers.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`msg_number`  
The message number

`fromlength`  
Number of characters for the *fetchfrom* property. Must be greater than
or equal to zero.

`subjectlength`  
Number of characters for the *fetchsubject* property Must be greater
than or equal to zero.

`defaulthost`  

### 返回值

Returns **`false`** on error or, if successful, the information in an
object with following properties:

-   <span class="simpara"> toaddress - full to: line, up to 1024
    characters </span>
-   <span class="simpara"> to - an array of objects from the To: line,
    with the following properties: *personal*, *adl*, *mailbox*, and
    *host* </span>
-   <span class="simpara"> fromaddress - full from: line, up to 1024
    characters </span>
-   <span class="simpara"> from - an array of objects from the From:
    line, with the following properties: *personal*, *adl*, *mailbox*,
    and *host* </span>
-   <span class="simpara"> ccaddress - full cc: line, up to 1024
    characters </span>
-   <span class="simpara"> cc - an array of objects from the Cc: line,
    with the following properties: *personal*, *adl*, *mailbox*, and
    *host* </span>
-   <span class="simpara"> bccaddress - full bcc: line, up to 1024
    characters </span>
-   <span class="simpara"> bcc - an array of objects from the Bcc: line,
    with the following properties: *personal*, *adl*, *mailbox*, and
    *host* </span>
-   <span class="simpara"> reply\_toaddress - full Reply-To: line, up to
    1024 characters </span>
-   <span class="simpara"> reply\_to - an array of objects from the
    Reply-To: line, with the following properties: *personal*, *adl*,
    *mailbox*, and *host* </span>
-   <span class="simpara"> senderaddress - full sender: line, up to 1024
    characters </span>
-   <span class="simpara"> sender - an array of objects from the Sender:
    line, with the following properties: *personal*, *adl*, *mailbox*,
    and *host* </span>
-   <span class="simpara"> return\_pathaddress - full Return-Path: line,
    up to 1024 characters </span>
-   <span class="simpara"> return\_path - an array of objects from the
    Return-Path: line, with the following properties: *personal*, *adl*,
    *mailbox*, and *host* </span>
-   <span class="simpara"> remail - </span>
-   <span class="simpara"> date - The message date as found in its
    headers </span>
-   <span class="simpara"> Date - Same as date </span>
-   <span class="simpara"> subject - The message subject </span>
-   <span class="simpara"> Subject - Same as subject </span>
-   <span class="simpara"> in\_reply\_to - </span>
-   <span class="simpara"> message\_id - </span>
-   <span class="simpara"> newsgroups - </span>
-   <span class="simpara"> followup\_to - </span>
-   <span class="simpara"> references - </span>
-   <span class="simpara"> Recent - *R* if recent and seen, *N* if
    recent and not seen, ' ' if not recent. </span>
-   <span class="simpara"> Unseen - *U* if not seen AND not recent, ' '
    if seen OR not seen and recent </span>
-   <span class="simpara"> Flagged - *F* if flagged, ' ' if not flagged
    </span>
-   <span class="simpara"> Answered - *A* if answered, ' ' if unanswered
    </span>
-   <span class="simpara"> Deleted - *D* if deleted, ' ' if not deleted
    </span>
-   <span class="simpara"> Draft - *X* if draft, ' ' if not draft
    </span>
-   <span class="simpara"> Msgno - The message number </span>
-   <span class="simpara"> MailDate - </span>
-   <span class="simpara"> Size - The message size </span>
-   <span class="simpara"> udate - mail message date in Unix time
    </span>
-   <span class="simpara"> fetchfrom - from line formatted to fit
    `fromlength` characters </span>
-   <span class="simpara"> fetchsubject - subject line formatted to fit
    `subjectlength` characters </span>

### 参见

-   <span class="function">imap\_fetch\_overview</span>

imap\_headers
=============

Returns headers for all messages in a mailbox

### 说明

<span class="type">array</span> <span
class="methodname">imap\_headers</span> ( <span
class="methodparam"><span class="type">resource</span>
`$imap_stream`</span> )

Returns headers for all messages in a mailbox.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

### 返回值

Returns an array of string formatted with header info. One element per
mail message.

imap\_last\_error
=================

Gets the last IMAP error that occurred during this page request

### 说明

<span class="type">string</span> <span
class="methodname">imap\_last\_error</span> ( <span
class="methodparam">void</span> )

Gets the full text of the last IMAP error message that occurred on the
current page. The error stack is untouched; calling <span
class="function">imap\_last\_error</span> subsequently, with no
intervening errors, will return the same error.

### 返回值

Returns the full text of the last IMAP error message that occurred on
the current page. Returns **`false`** if no error messages are
available.

### 参见

-   <span class="function">imap\_errors</span>

imap\_list
==========

Read the list of mailboxes

### 说明

<span class="type">array</span> <span
class="methodname">imap\_list</span> ( <span class="methodparam"><span
class="type">resource</span> `$imap_stream`</span> , <span
class="methodparam"><span class="type">string</span> `$ref`</span> ,
<span class="methodparam"><span class="type">string</span>
`$pattern`</span> )

Read the list of mailboxes.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`ref`  
`ref` should normally be just the server specification as described in
<span class="function">imap\_open</span>.

**Warning**
Passing untrusted data to this parameter is *insecure*, unless
<a href="/imap/setup.html#" class="link">imap.enable_insecure_rsh</a> is
disabled.

`pattern`  
指定在邮箱层级的何处开始查找。

在组成 `pattern` 的字符中可使用两个特殊字符： '*\**' 和 '*%*'。 '*\**'
是指返回所有邮箱目录. 如果将 '*\**' 作为 `pattern` 参数时,
则会返回整个邮箱层级结构。 '*%*' 是指只返回当前级次。 '*%*' 作为
`pattern` 参数则只会返回顶层邮箱； '*\~/mail/%*' 用于 *UW\_IMAPD*
则会返回名为 `~/mail` 的目录, 但不包含其子目录。

### 返回值

Returns an array containing the names of the mailboxes or false in case
of failure.

### 范例

**示例 \#1 <span class="function">imap\_list</span> example**

``` php
<?php
$mbox = imap_open("{imap.example.org}", "username", "password", OP_HALFOPEN)
      or die("can't connect: " . imap_last_error());

$list = imap_list($mbox, "{imap.example.org}", "*");
if (is_array($list)) {
    foreach ($list as $val) {
        echo imap_utf7_decode($val) . "\n";
    }
} else {
    echo "imap_list failed: " . imap_last_error() . "\n";
}

imap_close($mbox);
?>
```

### 参见

-   <span class="function">imap\_getmailboxes</span>
-   <span class="function">imap\_lsub</span>

imap\_listmailbox
=================

别名 <span class="function">imap\_list</span>

### 说明

此函数是该函数的别名： <span class="function">imap\_list</span>.

imap\_listscan
==============

Returns the list of mailboxes that matches the given text

### 说明

<span class="type">array</span> <span
class="methodname">imap\_listscan</span> ( <span
class="methodparam"><span class="type">resource</span>
`$imap_stream`</span> , <span class="methodparam"><span
class="type">string</span> `$ref`</span> , <span
class="methodparam"><span class="type">string</span> `$pattern`</span> ,
<span class="methodparam"><span class="type">string</span>
`$content`</span> )

Returns an array containing the names of the mailboxes that have
`content` in the text of the mailbox.

This function is similar to <span
class="function">imap\_listmailbox</span>, but it will additionally
check for the presence of the string `content` inside the mailbox data.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`ref`  
`ref` should normally be just the server specification as described in
<span class="function">imap\_open</span>

**Warning**
Passing untrusted data to this parameter is *insecure*, unless
<a href="/imap/setup.html#" class="link">imap.enable_insecure_rsh</a> is
disabled.

`pattern`  
指定在邮箱层级的何处开始查找。

在组成 `pattern` 的字符中可使用两个特殊字符： '*\**' 和 '*%*'。 '*\**'
是指返回所有邮箱目录. 如果将 '*\**' 作为 `pattern` 参数时,
则会返回整个邮箱层级结构。 '*%*' 是指只返回当前级次。 '*%*' 作为
`pattern` 参数则只会返回顶层邮箱； '*\~/mail/%*' 用于 *UW\_IMAPD*
则会返回名为 `~/mail` 的目录, 但不包含其子目录。

`content`  
The searched string

### 返回值

Returns an array containing the names of the mailboxes that have
`content` in the text of the mailbox.

### 参见

-   <span class="function">imap\_listmailbox</span>
-   <span class="function">imap\_search</span>

imap\_listsubscribed
====================

别名 <span class="function">imap\_lsub</span>

### 说明

此函数是该函数的别名： <span class="function">imap\_lsub</span>.

imap\_lsub
==========

List all the subscribed mailboxes

### 说明

<span class="type">array</span> <span
class="methodname">imap\_lsub</span> ( <span class="methodparam"><span
class="type">resource</span> `$imap_stream`</span> , <span
class="methodparam"><span class="type">string</span> `$ref`</span> ,
<span class="methodparam"><span class="type">string</span>
`$pattern`</span> )

Gets an array of all the mailboxes that you have subscribed.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`ref`  
`ref` should normally be just the server specification as described in
<span class="function">imap\_open</span>

**Warning**
Passing untrusted data to this parameter is *insecure*, unless
<a href="/imap/setup.html#" class="link">imap.enable_insecure_rsh</a> is
disabled.

`pattern`  
指定在邮箱层级的何处开始查找。

在组成 `pattern` 的字符中可使用两个特殊字符： '*\**' 和 '*%*'。 '*\**'
是指返回所有邮箱目录. 如果将 '*\**' 作为 `pattern` 参数时,
则会返回整个邮箱层级结构。 '*%*' 是指只返回当前级次。 '*%*' 作为
`pattern` 参数则只会返回顶层邮箱； '*\~/mail/%*' 用于 *UW\_IMAPD*
则会返回名为 `~/mail` 的目录, 但不包含其子目录。

### 返回值

Returns an array of all the subscribed mailboxes.

### 参见

-   <span class="function">imap\_list</span>
-   <span class="function">imap\_getmailboxes</span>

imap\_mail\_compose
===================

Create a MIME message based on given envelope and body sections

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">imap\_mail\_compose</span> ( <span
class="methodparam"><span class="type">array</span> `$envelope`</span> ,
<span class="methodparam"><span class="type">array</span> `$body`</span>
)

Create a MIME message based on the given `envelope` and `body` sections.

### 参数

`envelope`  
An associative array of header fields. Valid keys are: *"remail"*,
*"return\_path"*, *"date"*, *"from"*, *"reply\_to"*, *"in\_reply\_to"*,
*"subject"*, *"to"*, *"cc"*, *"bcc"* and *"message\_id"*, which set the
respective message headers to the given <span
class="type">string</span>. To set additional headers, the key
*"custom\_headers"* is supported, which expects an array of those
headers, e.g. `["User-Agent: My Mail Client"]`.

`body`  
An indexed array of bodies. The first body is the main body of the
message; only if it has a type of **`TYPEMULTIPART`**, further bodies
are processed; these bodies constitute the bodies of the parts.

| Key                | Type                             | Description                                                                                                                                                                          |
|--------------------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *type*             | <span class="type">int</span>    | The MIME type. One of **`TYPETEXT`** (default), **`TYPEMULTIPART`**, **`TYPEMESSAGE`**, **`TYPEAPPLICATION`**, **`TYPEAUDIO`**, **`TYPEIMAGE`**, **`TYPEMODEL`** or **`TYPEOTHER`**. |
| *encoding*         | <span class="type">int</span>    | The *Content-Transfer-Encoding*. One of **`ENC7BIT`** (default), **`ENC8BIT`**, **`ENCBINARY`**, **`ENCBASE64`**, **`ENCQUOTEDPRINTABLE`** or **`ENCOTHER`**.                        |
| *charset*          | <span class="type">string</span> | The charset parameter of the MIME type.                                                                                                                                              |
| *type.parameters*  | <span class="type">array</span>  | An associative <span class="type">array</span> of *Content-Type* parameter names and their values.                                                                                   |
| *subtype*          | <span class="type">string</span> | The MIME subtype, e.g. *'jpeg'* for **`TYPEIMAGE`**.                                                                                                                                 |
| *id*               | <span class="type">string</span> | The *Content-ID*.                                                                                                                                                                    |
| *description*      | <span class="type">string</span> | The *Content-Description*.                                                                                                                                                           |
| *disposition.type* | <span class="type">string</span> | The *Content-Disposition*, e.g. *'attachment'*.                                                                                                                                      |
| *disposition*      | <span class="type">array</span>  | An associative <span class="type">array</span> of *Content-Disposition* parameter names and values.                                                                                  |
| *contents.data*    | <span class="type">string</span> | The payload.                                                                                                                                                                         |
| *lines*            | <span class="type">int</span>    | The size of the payload in lines.                                                                                                                                                    |
| *bytes*            | <span class="type">int</span>    | The size of the payload in bytes.                                                                                                                                                    |
| *md5*              | <span class="type">string</span> | The MD5 checksum of the payload.                                                                                                                                                     |

### 返回值

Returns the MIME message as <span class="type">string</span>,
或者在失败时返回 **`false`**.

### 范例

**示例 \#1 <span class="function">imap\_mail\_compose</span> example**

``` php
<?php

$envelope["from"]= "joe@example.com";
$envelope["to"]  = "foo@example.com";
$envelope["cc"]  = "bar@example.com";

$part1["type"] = TYPEMULTIPART;
$part1["subtype"] = "mixed";

$filename = "/tmp/imap.c.gz";
$fp = fopen($filename, "r");
$contents = fread($fp, filesize($filename));
fclose($fp);

$part2["type"] = TYPEAPPLICATION;
$part2["encoding"] = ENCBINARY;
$part2["subtype"] = "octet-stream";
$part2["description"] = basename($filename);
$part2["contents.data"] = $contents;

$part3["type"] = TYPETEXT;
$part3["subtype"] = "plain";
$part3["description"] = "description3";
$part3["contents.data"] = "contents.data3\n\n\n\t";

$body[1] = $part1;
$body[2] = $part2;
$body[3] = $part3;

echo nl2br(imap_mail_compose($envelope, $body));

?>
```

imap\_mail\_copy
================

Copy specified messages to a mailbox

### 说明

<span class="type">bool</span> <span
class="methodname">imap\_mail\_copy</span> ( <span
class="methodparam"><span class="type">resource</span>
`$imap_stream`</span> , <span class="methodparam"><span
class="type">string</span> `$msglist`</span> , <span
class="methodparam"><span class="type">string</span> `$mailbox`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$options`<span class="initializer"> = 0</span></span> \] )

Copies mail messages specified by `msglist` to specified mailbox.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`msglist`  
`msglist` is a range not just message numbers (as described in
<a href="http://www.faqs.org/rfcs/rfc2060" class="link external">» RFC2060</a>).

`mailbox`  
The mailbox name, see <span class="function">imap\_open</span> for more
information

**Warning**
Passing untrusted data to this parameter is *insecure*, unless
<a href="/imap/setup.html#" class="link">imap.enable_insecure_rsh</a> is
disabled.

`options`  
`options` is a bitmask of one or more of

-   <span class="simpara"> **`CP_UID`** - the sequence numbers contain
    UIDS </span>
-   <span class="simpara"> **`CP_MOVE`** - Delete the messages from the
    current mailbox after copying </span>

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">imap\_mail\_move</span>

imap\_mail\_move
================

Move specified messages to a mailbox

### 说明

<span class="type">bool</span> <span
class="methodname">imap\_mail\_move</span> ( <span
class="methodparam"><span class="type">resource</span>
`$imap_stream`</span> , <span class="methodparam"><span
class="type">string</span> `$msglist`</span> , <span
class="methodparam"><span class="type">string</span> `$mailbox`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$options`<span class="initializer"> = 0</span></span> \] )

Moves mail messages specified by `msglist` to the specified `mailbox`.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`msglist`  
`msglist` is a range not just message numbers (as described in
<a href="http://www.faqs.org/rfcs/rfc2060" class="link external">» RFC2060</a>).

`mailbox`  
The mailbox name, see <span class="function">imap\_open</span> for more
information

**Warning**
Passing untrusted data to this parameter is *insecure*, unless
<a href="/imap/setup.html#" class="link">imap.enable_insecure_rsh</a> is
disabled.

`options`  
`options` is a bitmask and may contain the single option:

-   <span class="simpara"> **`CP_UID`** - the sequence numbers contain
    UIDS </span>

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 注释

> **Note**:
>
> <span class="function">imap\_mail\_move</span> will flag the original
> mail with a delete flag, to successfully delete it a call to the <span
> class="function">imap\_expunge</span> function must be made.

### 参见

-   <span class="function">imap\_mail\_copy</span>

imap\_mail
==========

Send an email message

### 说明

<span class="type">bool</span> <span
class="methodname">imap\_mail</span> ( <span class="methodparam"><span
class="type">string</span> `$to`</span> , <span
class="methodparam"><span class="type">string</span> `$subject`</span> ,
<span class="methodparam"><span class="type">string</span>
`$message`</span> \[, <span class="methodparam"><span
class="type">string</span> `$additional_headers`<span
class="initializer"> = **`null`**</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$cc`<span
class="initializer"> = **`null`**</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$bcc`<span
class="initializer"> = **`null`**</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$rpath`<span
class="initializer"> = **`null`**</span></span> \]\]\]\] )

This function allows sending of emails with correct handling of Cc and
Bcc receivers.

The parameters `to`, `cc` and `bcc` are all strings and are all parsed
as
<a href="http://www.faqs.org/rfcs/rfc822" class="link external">» RFC822</a>
address lists.

### 参数

`to`  
The receiver

`subject`  
The mail subject

`message`  
The mail body, see <span class="function">imap\_mail\_compose</span>

`additional_headers`  
As string with additional headers to be set on the mail

`cc`  

`bcc`  
The receivers specified in `bcc` will get the mail, but are excluded
from the headers.

`rpath`  
Use this parameter to specify return path upon mail delivery failure.
This is useful when using PHP as a mail client for multiple users.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">mail</span>
-   <span class="function">imap\_mail\_compose</span>

imap\_mailboxmsginfo
====================

Get information about the current mailbox

### 说明

<span class="type">object</span> <span
class="methodname">imap\_mailboxmsginfo</span> ( <span
class="methodparam"><span class="type">resource</span>
`$imap_stream`</span> )

Checks the current mailbox status on the server. It is similar to <span
class="function">imap\_status</span>, but will additionally sum up the
size of all messages in the mailbox, which will take some additional
time to execute.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

### 返回值

Returns the information in an object with following properties:

|         |                                        |
|---------|----------------------------------------|
| Date    | date of last change (current datetime) |
| Driver  | driver                                 |
| Mailbox | name of the mailbox                    |
| Nmsgs   | number of messages                     |
| Recent  | number of recent messages              |
| Unread  | number of unread messages              |
| Deleted | number of deleted messages             |
| Size    | mailbox size                           |

Returns **`false`** on failure.

### 范例

**示例 \#1 <span class="function">imap\_mailboxmsginfo</span> example**

``` php
<?php

$mbox = imap_open("{imap.example.org}INBOX", "username", "password")
      or die("can't connect: " . imap_last_error());

$check = imap_mailboxmsginfo($mbox);

if ($check) {
    echo "Date: "     . $check->Date    . "<br />\n" ;
    echo "Driver: "   . $check->Driver  . "<br />\n" ;
    echo "Mailbox: "  . $check->Mailbox . "<br />\n" ;
    echo "Messages: " . $check->Nmsgs   . "<br />\n" ;
    echo "Recent: "   . $check->Recent  . "<br />\n" ;
    echo "Unread: "   . $check->Unread  . "<br />\n" ;
    echo "Deleted: "  . $check->Deleted . "<br />\n" ;
    echo "Size: "     . $check->Size    . "<br />\n" ;
} else {
    echo "imap_mailboxmsginfo() failed: " . imap_last_error() . "<br />\n";
}

imap_close($mbox);

?>
```

imap\_mime\_header\_decode
==========================

Decode MIME header elements

### 说明

<span class="type">array</span> <span
class="methodname">imap\_mime\_header\_decode</span> ( <span
class="methodparam"><span class="type">string</span> `$text`</span> )

Decodes MIME message header extensions that are non ASCII text (see
<a href="http://www.faqs.org/rfcs/rfc2047" class="link external">» RFC2047</a>).

### 参数

`text`  
The MIME text

### 返回值

The decoded elements are returned in an array of objects, where each
object has two properties, *charset* and *text*.

If the element hasn't been encoded, and in other words is in plain
US-ASCII, the *charset* property of that element is set to *default*.

### 范例

**示例 \#1 <span class="function">imap\_mime\_header\_decode</span>
example**

``` php
<?php
$text = "=?ISO-8859-1?Q?Keld_J=F8rn_Simonsen?= <keld@example.com>";

$elements = imap_mime_header_decode($text);
for ($i=0; $i<count($elements); $i++) {
    echo "Charset: {$elements[$i]->charset}\n";
    echo "Text: {$elements[$i]->text}\n\n";
}
?>
```

以上例程会输出：

    Charset: ISO-8859-1
    Text: Keld Jørn Simonsen

    Charset: default
    Text:  <keld@example.com>

In the above example we would have two elements, whereas the first
element had previously been encoded with ISO-8859-1, and the second
element would be plain US-ASCII.

### 参见

-   <span class="function">imap\_utf8</span>

imap\_msgno
===========

Gets the message sequence number for the given UID

### 说明

<span class="type">int</span> <span
class="methodname">imap\_msgno</span> ( <span class="methodparam"><span
class="type">resource</span> `$imap_stream`</span> , <span
class="methodparam"><span class="type">int</span> `$uid`</span> )

Returns the message sequence number for the given `uid`.

This function is the inverse of <span class="function">imap\_uid</span>.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`uid`  
The message UID

### 返回值

Returns the message sequence number for the given `uid`.

### 参见

-   <span class="function">imap\_uid</span>

imap\_mutf7\_to\_utf8
=====================

Decode a modified UTF-7 string to UTF-8

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">imap\_mutf7\_to\_utf8</span> ( <span
class="methodparam"><span class="type">string</span> `$in`</span> )

Decode a modified UTF-7 (as specified in RFC 2060, section 5.1.3) string
to UTF-8.

> **Note**:
>
> This function is only available, if libcclient exports
> utf8\_to\_mutf7().

### 参数

`in`  
A string encoded in modified UTF-7.

### 返回值

Returns `in` converted to UTF-8, 或者在失败时返回 **`false`**.

### 参见

-   <span class="function">imap\_utf8\_to\_mutf7</span>

imap\_num\_msg
==============

Gets the number of messages in the current mailbox

### 说明

<span class="type">int</span> <span
class="methodname">imap\_num\_msg</span> ( <span
class="methodparam"><span class="type">resource</span>
`$imap_stream`</span> )

Gets the number of messages in the current mailbox.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

### 返回值

Return the number of messages in the current mailbox, as an integer, or
**`false`** on error.

### 参见

-   <span class="function">imap\_num\_recent</span>
-   <span class="function">imap\_status</span>

imap\_num\_recent
=================

Gets the number of recent messages in current mailbox

### 说明

<span class="type">int</span> <span
class="methodname">imap\_num\_recent</span> ( <span
class="methodparam"><span class="type">resource</span>
`$imap_stream`</span> )

Gets the number of recent messages in the current mailbox.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

### 返回值

Returns the number of recent messages in the current mailbox, as an
integer.

### 参见

-   <span class="function">imap\_num\_msg</span>
-   <span class="function">imap\_status</span>

imap\_open
==========

Open an IMAP stream to a mailbox

### 说明

<span class="type">resource</span> <span
class="methodname">imap\_open</span> ( <span class="methodparam"><span
class="type">string</span> `$mailbox`</span> , <span
class="methodparam"><span class="type">string</span> `$username`</span>
, <span class="methodparam"><span class="type">string</span>
`$password`</span> \[, <span class="methodparam"><span
class="type">int</span> `$options`<span class="initializer"> =
0</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$n_retries`<span class="initializer"> =
0</span></span> \[, <span class="methodparam"><span
class="type">array</span> `$params`<span class="initializer"> =
array()</span></span> \]\]\] )

Opens an IMAP stream to a `mailbox`.

This function can also be used to open streams to POP3 and NNTP servers,
but some functions and features are only available on IMAP servers.

### 参数

`mailbox`  
A mailbox name consists of a server and a mailbox path on this server.
The special name *INBOX* stands for the current users personal mailbox.
Mailbox names that contain international characters besides those in the
printable ASCII space have to be encoded with <span
class="function">imap\_utf7\_encode</span>.

**Warning**
Passing untrusted data to this parameter is *insecure*, unless
<a href="/imap/setup.html#" class="link">imap.enable_insecure_rsh</a> is
disabled.

The server part, which is enclosed in '{' and '}', consists of the
servers name or ip address, an optional port (prefixed by ':'), and an
optional protocol specification (prefixed by '/').

The server part is mandatory in all mailbox parameters.

All names which start with *{* are remote names, and are in the form
*"{" remote\_system\_name \[":" port\] \[flags\] "}" \[mailbox\_name\]*
where:

-   <span class="simpara"> *remote\_system\_name* - Internet domain name
    or bracketed IP address of server. </span>
-   <span class="simpara"> *port* - optional TCP port number, default is
    the default port for that service </span>
-   <span class="simpara"> *flags* - optional flags, see following
    table. </span>
-   <span class="simpara"> *mailbox\_name* - remote mailbox name,
    default is INBOX </span>

| Flag                                                   | Description                                                                                                |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| */service=service*                                     | mailbox access service, default is "imap"                                                                  |
| */user=user*                                           | remote user name for login on the server                                                                   |
| */authuser=user*                                       | remote authentication user; if specified this is the user name whose password is used (e.g. administrator) |
| */anonymous*                                           | remote access as anonymous user                                                                            |
| */debug*                                               | record protocol telemetry in application's debug log                                                       |
| */secure*                                              | do not transmit a plaintext password over the network                                                      |
| */imap*, */imap2*, */imap2bis*, */imap4*, */imap4rev1* | equivalent to */service=imap*                                                                              |
| */pop3*                                                | equivalent to */service=pop3*                                                                              |
| */nntp*                                                | equivalent to */service=nntp*                                                                              |
| */norsh*                                               | do not use rsh or ssh to establish a preauthenticated IMAP session                                         |
| */ssl*                                                 | use the *Secure Socket Layer* to encrypt the session                                                       |
| */validate-cert*                                       | validate certificates from TLS/SSL server (this is the default behavior)                                   |
| */novalidate-cert*                                     | do not validate certificates from TLS/SSL server, needed if server uses self-signed certificates           |
| */tls*                                                 | force use of *start-TLS* to encrypt the session, and reject connection to servers that do not support it   |
| */notls*                                               | do not do *start-TLS* to encrypt the session, even with servers that support it                            |
| */readonly*                                            | request read-only mailbox open (IMAP only; ignored on NNTP, and an error with SMTP and POP3)               |

`username`  
The user name

`password`  
The password associated with the `username`

`options`  
The `options` are a bit mask with one or more of the following:

-   <span class="simpara"> **`OP_READONLY`** - Open mailbox read-only
    </span>
-   <span class="simpara"> **`OP_ANONYMOUS`** - Don't use or update a
    `.newsrc` for news (NNTP only) </span>
-   <span class="simpara"> **`OP_HALFOPEN`** - For IMAP and NNTP names,
    open a connection but don't open a mailbox. </span>
-   <span class="simpara"> **`CL_EXPUNGE`** - Expunge mailbox
    automatically upon mailbox close (see also <span
    class="function">imap\_delete</span> and <span
    class="function">imap\_expunge</span>) </span>
-   <span class="simpara"> **`OP_DEBUG`** - Debug protocol negotiations
    </span>
-   <span class="simpara"> **`OP_SHORTCACHE`** - Short (*elt*-only)
    caching </span>
-   <span class="simpara"> **`OP_SILENT`** - Don't pass up events
    (internal use) </span>
-   <span class="simpara"> **`OP_PROTOTYPE`** - Return driver prototype
    </span>
-   <span class="simpara"> **`OP_SECURE`** - Don't do non-secure
    authentication </span>

`n_retries`  
Number of maximum connect attempts

`params`  
Connection parameters, the following (string) keys maybe used to set one
or more connection parameters:

-   <span class="simpara"> *DISABLE\_AUTHENTICATOR* - Disable
    authentication properties </span>

### 返回值

Returns an IMAP stream on success or **`false`** on error.

### 范例

**示例 \#1 Different use of <span class="function">imap\_open</span>**

``` php
<?php
// To connect to an IMAP server running on port 143 on the local machine,
// do the following:
$mbox = imap_open("{localhost:143}INBOX", "user_id", "password");

// To connect to a POP3 server on port 110 on the local server, use:
$mbox = imap_open ("{localhost:110/pop3}INBOX", "user_id", "password");

// To connect to an SSL IMAP or POP3 server, add /ssl after the protocol
// specification:
$mbox = imap_open ("{localhost:993/imap/ssl}INBOX", "user_id", "password");

// To connect to an SSL IMAP or POP3 server with a self-signed certificate,
// add /ssl/novalidate-cert after the protocol specification:
$mbox = imap_open ("{localhost:995/pop3/ssl/novalidate-cert}", "user_id", "password");

// To connect to an NNTP server on port 119 on the local server, use:
$nntp = imap_open ("{localhost:119/nntp}comp.test", "", "");
// To connect to a remote server replace "localhost" with the name or the
// IP address of the server you want to connect to.
?>
```

**示例 \#2 <span class="function">imap\_open</span> example**

``` php
<?php
$mbox = imap_open("{imap.example.org:143}", "username", "password");

echo "<h1>Mailboxes</h1>\n";
$folders = imap_listmailbox($mbox, "{imap.example.org:143}", "*");

if ($folders == false) {
    echo "Call failed<br />\n";
} else {
    foreach ($folders as $val) {
        echo $val . "<br />\n";
    }
}

echo "<h1>Headers in INBOX</h1>\n";
$headers = imap_headers($mbox);

if ($headers == false) {
    echo "Call failed<br />\n";
} else {
    foreach ($headers as $val) {
        echo $val . "<br />\n";
    }
}

imap_close($mbox);
?>
```

### 参见

-   <span class="function">imap\_close</span>

imap\_ping
==========

Check if the IMAP stream is still active

### 说明

<span class="type">bool</span> <span
class="methodname">imap\_ping</span> ( <span class="methodparam"><span
class="type">resource</span> `$imap_stream`</span> )

<span class="function">imap\_ping</span> pings the stream to see if it's
still active. It may discover new mail; this is the preferred method for
a periodic "new mail check" as well as a "keep alive" for servers which
have inactivity timeout.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

### 返回值

Returns **`true`** if the stream is still alive, **`false`** otherwise.

### 范例

**示例 \#1 <span class="function">imap\_ping</span> Example**

``` php
<?php

$imap = imap_open("{imap.example.org}", "mailadmin", "password");

// after some sleeping
if (!imap_ping($imap)) {
    // do some stuff to reconnect
}

?>
```

imap\_qprint
============

Convert a quoted-printable string to an 8 bit string

### 说明

<span class="type">string</span> <span
class="methodname">imap\_qprint</span> ( <span class="methodparam"><span
class="type">string</span> `$string`</span> )

Convert a quoted-printable string to an 8 bit string according to
<a href="http://www.faqs.org/rfcs/rfc2045" class="link external">» RFC2045</a>,
section 6.7.

### 参数

`string`  
A quoted-printable string

### 返回值

Returns an 8 bits string.

### 参见

-   <span class="function">imap\_8bit</span>

imap\_rename
============

别名 <span class="function">imap\_renamemailbox</span>

### 说明

此函数是该函数的别名： <span
class="function">imap\_renamemailbox</span>.

imap\_renamemailbox
===================

Rename an old mailbox to new mailbox

### 说明

<span class="type">bool</span> <span
class="methodname">imap\_renamemailbox</span> ( <span
class="methodparam"><span class="type">resource</span>
`$imap_stream`</span> , <span class="methodparam"><span
class="type">string</span> `$old_mbox`</span> , <span
class="methodparam"><span class="type">string</span> `$new_mbox`</span>
)

This function renames on old mailbox to new mailbox (see <span
class="function">imap\_open</span> for the format of `mbox` names).

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`old_mbox`  
The old mailbox name, see <span class="function">imap\_open</span> for
more information

**Warning**
Passing untrusted data to this parameter is *insecure*, unless
<a href="/imap/setup.html#" class="link">imap.enable_insecure_rsh</a> is
disabled.

`new_mbox`  
The new mailbox name, see <span class="function">imap\_open</span> for
more information

**Warning**
Passing untrusted data to this parameter is *insecure*, unless
<a href="/imap/setup.html#" class="link">imap.enable_insecure_rsh</a> is
disabled.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">imap\_createmailbox</span>
-   <span class="function">imap\_deletemailbox</span>

imap\_reopen
============

Reopen IMAP stream to new mailbox

### 说明

<span class="type">bool</span> <span
class="methodname">imap\_reopen</span> ( <span class="methodparam"><span
class="type">resource</span> `$imap_stream`</span> , <span
class="methodparam"><span class="type">string</span> `$mailbox`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$options`<span class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$n_retries`<span
class="initializer"> = 0</span></span> \]\] )

Reopens the specified stream to a new `mailbox` on an IMAP or NNTP
server.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`mailbox`  
The mailbox name, see <span class="function">imap\_open</span> for more
information

**Warning**
Passing untrusted data to this parameter is *insecure*, unless
<a href="/imap/setup.html#" class="link">imap.enable_insecure_rsh</a> is
disabled.

`options`  
The `options` are a bit mask with one or more of the following:

-   <span class="simpara"> **`OP_READONLY`** - Open mailbox read-only
    </span>
-   <span class="simpara"> **`OP_ANONYMOUS`** - Don't use or update a
    `.newsrc` for news (NNTP only) </span>
-   <span class="simpara"> **`OP_HALFOPEN`** - For IMAP and NNTP names,
    open a connection but don't open a mailbox. </span>
-   <span class="simpara"> **`OP_EXPUNGE`** - Silently expunge recycle
    stream </span>
-   <span class="simpara"> **`CL_EXPUNGE`** - Expunge mailbox
    automatically upon mailbox close (see also <span
    class="function">imap\_delete</span> and <span
    class="function">imap\_expunge</span>) </span>

`n_retries`  
Number of maximum connect attempts

### 返回值

Returns **`true`** if the stream is reopened, **`false`** otherwise.

### 范例

**示例 \#1 <span class="function">imap\_reopen</span> example**

``` php
<?php
$mbox = imap_open("{imap.example.org:143}INBOX", "username", "password") or die(implode(", ", imap_errors()));
// ...
imap_reopen($mbox, "{imap.example.org:143}INBOX.Sent") or die(implode(", ", imap_errors()));
// ..
?>
```

imap\_rfc822\_parse\_adrlist
============================

Parses an address string

### 说明

<span class="type">array</span> <span
class="methodname">imap\_rfc822\_parse\_adrlist</span> ( <span
class="methodparam"><span class="type">string</span> `$address`</span> ,
<span class="methodparam"><span class="type">string</span>
`$default_host`</span> )

Parses the address string as defined in
<a href="http://www.faqs.org/rfcs/rfc2822" class="link external">» RFC2822</a>
and for each address.

### 参数

`address`  
A string containing addresses

`default_host`  
The default host name

### 返回值

Returns an array of objects. The objects properties are:

-   <span class="simpara"> mailbox - the mailbox name (username) </span>
-   <span class="simpara"> host - the host name </span>
-   <span class="simpara"> personal - the personal name </span>
-   <span class="simpara"> adl - at domain source route </span>

### 范例

**示例 \#1 <span class="function">imap\_rfc822\_parse\_adrlist</span>
example**

``` php
<?php

$address_string = "Joe Doe <doe@example.com>, postmaster@example.com, root";
$address_array  = imap_rfc822_parse_adrlist($address_string, "example.com");
if (!is_array($address_array) || count($address_array) < 1) {
    die("something is wrong\n");
}

foreach ($address_array as $id => $val) {
    echo "# $id\n";
    echo "  mailbox : " . $val->mailbox . "\n";
    echo "  host    : " . $val->host . "\n";
    echo "  personal: " . $val->personal . "\n";
    echo "  adl     : " . $val->adl . "\n";
}
?>
```

以上例程会输出：

    # 0
      mailbox : doe
      host    : example.com
      personal: Joe Doe
      adl     : 
    # 1
      mailbox : postmaster
      host    : example.com
      personal: 
      adl     : 
    # 2
      mailbox : root
      host    : example.com
      personal: 
      adl     :

### 参见

-   <span class="function">imap\_rfc822\_parse\_headers</span>

imap\_rfc822\_parse\_headers
============================

Parse mail headers from a string

### 说明

<span class="type">object</span> <span
class="methodname">imap\_rfc822\_parse\_headers</span> ( <span
class="methodparam"><span class="type">string</span> `$headers`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$defaulthost`<span class="initializer"> = "UNKNOWN"</span></span> \] )

Gets an object of various header elements, similar to <span
class="function">imap\_header</span>.

### 参数

`headers`  
The parsed headers data

`defaulthost`  
The default host name

### 返回值

Returns an object similar to the one returned by <span
class="function">imap\_header</span>, except for the flags and other
properties that come from the IMAP server.

### 参见

-   <span class="function">imap\_rfc822\_parse\_adrlist</span>

imap\_rfc822\_write\_address
============================

Returns a properly formatted email address given the mailbox, host, and
personal info

### 说明

<span class="type">string</span> <span
class="methodname">imap\_rfc822\_write\_address</span> ( <span
class="methodparam"><span class="type">string</span> `$mailbox`</span> ,
<span class="methodparam"><span class="type">string</span>
`$host`</span> , <span class="methodparam"><span
class="type">string</span> `$personal`</span> )

Returns a properly formatted email address as defined in
<a href="http://www.faqs.org/rfcs/rfc2822" class="link external">» RFC2822</a>
given the needed information.

### 参数

`mailbox`  
The mailbox name, see <span class="function">imap\_open</span> for more
information

**Warning**
Passing untrusted data to this parameter is *insecure*, unless
<a href="/imap/setup.html#" class="link">imap.enable_insecure_rsh</a> is
disabled.

`host`  
The email host part

`personal`  
The name of the account owner

### 返回值

Returns a string properly formatted email address as defined in
<a href="http://www.faqs.org/rfcs/rfc2822" class="link external">» RFC2822</a>.

### 范例

**示例 \#1 <span class="function">imap\_rfc822\_write\_address</span>
example**

``` php
<?php
echo imap_rfc822_write_address("hartmut", "example.com", "Hartmut Holzgraefe");
?>
```

以上例程会输出：

    Hartmut Holzgraefe <hartmut@example.com>

imap\_savebody
==============

Save a specific body section to a file

### 说明

<span class="type">bool</span> <span
class="methodname">imap\_savebody</span> ( <span
class="methodparam"><span class="type">resource</span>
`$imap_stream`</span> , <span class="methodparam"><span
class="type">mixed</span> `$file`</span> , <span
class="methodparam"><span class="type">int</span> `$msg_number`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$part_number`<span class="initializer"> = ""</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = 0</span></span> \]\] )

Saves a part or the whole body of the specified message.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`file`  
The path to the saved file as a string, or a valid file descriptor
returned by <span class="function">fopen</span>.

`msg_number`  
The message number

`part_number`  
The part number. It is a string of integers delimited by period which
index into a body part list as per the IMAP4 specification

`options`  
A bitmask with one or more of the following:

-   <span class="simpara"> **`FT_UID`** - The `msg_number` is a UID
    </span>
-   <span class="simpara"> **`FT_PEEK`** - Do not set the \\Seen flag if
    not already set </span>
-   <span class="simpara"> **`FT_INTERNAL`** - The return string is in
    internal format, will not canonicalize to CRLF. </span>

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">imap\_fetchbody</span>

imap\_scan
==========

别名 <span class="function">imap\_listscan</span>

### 说明

此函数是该函数的别名： <span class="function">imap\_listscan</span>.

imap\_scanmailbox
=================

别名 <span class="function">imap\_listscan</span>

### 说明

此函数是该函数的别名： <span class="function">imap\_listscan</span>.

imap\_search
============

This function returns an array of messages matching the given search
criteria

### 说明

<span class="type">array</span> <span
class="methodname">imap\_search</span> ( <span class="methodparam"><span
class="type">resource</span> `$imap_stream`</span> , <span
class="methodparam"><span class="type">string</span> `$criteria`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$options`<span class="initializer"> = SE\_FREE</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$charset`<span
class="initializer"> = **`null`**</span></span> \]\] )

This function performs a search on the mailbox currently opened in the
given IMAP stream.

For example, to match all unanswered messages sent by Mom, you'd use:
"UNANSWERED FROM mom". Searches appear to be case insensitive. This list
of criteria is from a reading of the UW c-client source code and may be
incomplete or inaccurate (see also
<a href="http://www.faqs.org/rfcs/rfc1176" class="link external">» RFC1176</a>,
section "tag SEARCH search\_criteria").

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`criteria`  
A string, delimited by spaces, in which the following keywords are
allowed. Any multi-word arguments (e.g. *FROM "joey smith"*) must be
quoted. Results will match all `criteria` entries.

-   <span class="simpara"> ALL - return all messages matching the rest
    of the criteria </span>
-   <span class="simpara"> ANSWERED - match messages with the
    \\\\ANSWERED flag set </span>
-   <span class="simpara"> BCC "string" - match messages with "string"
    in the Bcc: field </span>
-   <span class="simpara"> BEFORE "date" - match messages with Date:
    before "date" </span>
-   <span class="simpara"> BODY "string" - match messages with "string"
    in the body of the message </span>
-   <span class="simpara"> CC "string" - match messages with "string" in
    the Cc: field </span>
-   <span class="simpara"> DELETED - match deleted messages </span>
-   <span class="simpara"> FLAGGED - match messages with the \\\\FLAGGED
    (sometimes referred to as Important or Urgent) flag set </span>
-   <span class="simpara"> FROM "string" - match messages with "string"
    in the From: field </span>
-   <span class="simpara"> KEYWORD "string" - match messages with
    "string" as a keyword </span>
-   <span class="simpara"> NEW - match new messages </span>
-   <span class="simpara"> OLD - match old messages </span>
-   <span class="simpara"> ON "date" - match messages with Date:
    matching "date" </span>
-   <span class="simpara"> RECENT - match messages with the \\\\RECENT
    flag set </span>
-   <span class="simpara"> SEEN - match messages that have been read
    (the \\\\SEEN flag is set) </span>
-   <span class="simpara"> SINCE "date" - match messages with Date:
    after "date" </span>
-   <span class="simpara"> SUBJECT "string" - match messages with
    "string" in the Subject: </span>
-   <span class="simpara"> TEXT "string" - match messages with text
    "string" </span>
-   <span class="simpara"> TO "string" - match messages with "string" in
    the To: </span>
-   <span class="simpara"> UNANSWERED - match messages that have not
    been answered </span>
-   <span class="simpara"> UNDELETED - match messages that are not
    deleted </span>
-   <span class="simpara"> UNFLAGGED - match messages that are not
    flagged </span>
-   <span class="simpara"> UNKEYWORD "string" - match messages that do
    not have the keyword "string" </span>
-   <span class="simpara"> UNSEEN - match messages which have not been
    read yet </span>

`options`  
Valid values for `options` are **`SE_UID`**, which causes the returned
array to contain UIDs instead of messages sequence numbers.

`charset`  
MIME character set to use when searching strings.

### 返回值

Returns an array of message numbers or UIDs.

Return **`false`** if it does not understand the search `criteria` or no
messages have been found.

### 范例

**示例 \#1 <span class="function">imap\_search</span> example**

``` php
<?php
$conn   = imap_open('{imap.example.com:993/imap/ssl}INBOX', 'foo@example.com', 'pass123', OP_READONLY);

$some   = imap_search($conn, 'SUBJECT "HOWTO be Awesome" SINCE "8 August 2008"', SE_UID);
$msgnos = imap_search($conn, 'ALL');
$uids   = imap_search($conn, 'ALL', SE_UID);

print_r($some);
print_r($msgnos);
print_r($uids);
?>
```

以上例程的输出类似于：

    Array
    (
        [0] => 4
        [1] => 6
        [2] => 11
    )
    Array
    (
        [0] => 1
        [1] => 2
        [2] => 3
        [3] => 4
        [4] => 5
        [5] => 6
    )
    Array
    (
        [0] => 1
        [1] => 4
        [2] => 6
        [3] => 8
        [4] => 11
        [5] => 12
    )

### 参见

-   <span class="function">imap\_listscan</span>

imap\_set\_quota
================

Sets a quota for a given mailbox

### 说明

<span class="type">bool</span> <span
class="methodname">imap\_set\_quota</span> ( <span
class="methodparam"><span class="type">resource</span>
`$imap_stream`</span> , <span class="methodparam"><span
class="type">string</span> `$quota_root`</span> , <span
class="methodparam"><span class="type">int</span> `$quota_limit`</span>
)

Sets an upper limit quota on a per mailbox basis.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`quota_root`  
The mailbox to have a quota set. This should follow the IMAP standard
format for a mailbox: *user.name*.

`quota_limit`  
The maximum size (in KB) for the `quota_root`

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">imap\_set\_quota</span> example**

``` php
<?php
$mbox = imap_open("{imap.example.org:143}", "mailadmin", "password");

if (!imap_set_quota($mbox, "user.kalowsky", 3000)) {
    echo "Error in setting quota\n";
    return;
}

imap_close($mbox);
?>
```

### 注释

This function is currently only available to users of the c-client2000
or greater library.

The given `imap_stream` must be opened as the mail administrator, other
wise this function will fail.

### 参见

-   <span class="function">imap\_open</span>
-   <span class="function">imap\_get\_quota</span>

imap\_setacl
============

Sets the ACL for a given mailbox

### 说明

<span class="type">bool</span> <span
class="methodname">imap\_setacl</span> ( <span class="methodparam"><span
class="type">resource</span> `$imap_stream`</span> , <span
class="methodparam"><span class="type">string</span> `$mailbox`</span> ,
<span class="methodparam"><span class="type">string</span> `$id`</span>
, <span class="methodparam"><span class="type">string</span>
`$rights`</span> )

Sets the ACL for a giving mailbox.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`mailbox`  
The mailbox name, see <span class="function">imap\_open</span> for more
information

**Warning**
Passing untrusted data to this parameter is *insecure*, unless
<a href="/imap/setup.html#" class="link">imap.enable_insecure_rsh</a> is
disabled.

`id`  
The user to give the rights to.

`rights`  
The rights to give to the user. Passing an empty string will delete acl.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 注释

This function is currently only available to users of the c-client2000
or greater library.

### 参见

-   <span class="function">imap\_getacl</span>

imap\_setflag\_full
===================

Sets flags on messages

### 说明

<span class="type">bool</span> <span
class="methodname">imap\_setflag\_full</span> ( <span
class="methodparam"><span class="type">resource</span>
`$imap_stream`</span> , <span class="methodparam"><span
class="type">string</span> `$sequence`</span> , <span
class="methodparam"><span class="type">string</span> `$flag`</span> \[,
<span class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = NIL</span></span> \] )

Causes a store to add the specified `flag` to the flags set for the
messages in the specified `sequence`.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`sequence`  
A sequence of message numbers. You can enumerate desired messages with
the *X,Y* syntax, or retrieve all messages within an interval with the
*X:Y* syntax

`flag`  
The flags which you can set are *\\Seen*, *\\Answered*, *\\Flagged*,
*\\Deleted*, and *\\Draft* as defined by
<a href="http://www.faqs.org/rfcs/rfc2060" class="link external">» RFC2060</a>.

`options`  
A bit mask that may contain the single option:

-   <span class="simpara"> **`ST_UID`** - The sequence argument contains
    UIDs instead of sequence numbers </span>

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">imap\_setflag\_full</span> example**

``` php
<?php
$mbox = imap_open("{imap.example.org:143}", "username", "password")
     or die("can't connect: " . imap_last_error());

$status = imap_setflag_full($mbox, "2,5", "\\Seen \\Flagged");

echo gettype($status) . "\n";
echo $status . "\n";

imap_close($mbox);
?>
```

### 参见

-   <span class="function">imap\_clearflag\_full</span>

imap\_sort
==========

Gets and sort messages

### 说明

<span class="type"><span class="type">array</span><span
class="type">false</span></span> <span
class="methodname">imap\_sort</span> ( <span class="methodparam"><span
class="type">resource</span> `$imap_stream`</span> , <span
class="methodparam"><span class="type">int</span> `$criteria`</span> ,
<span class="methodparam"><span class="type">int</span>
`$reverse`</span> \[, <span class="methodparam"><span
class="type">int</span> `$options`<span class="initializer"> =
0</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$search_criteria`<span class="initializer">
= **`null`**</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$charset`<span class="initializer"> =
**`null`**</span></span> \]\]\] )

Gets and sorts message numbers by the given parameters.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`criteria`  
Criteria can be one (and only one) of the following:

-   <span class="simpara"> **`SORTDATE`** - message Date </span>
-   <span class="simpara"> **`SORTARRIVAL`** - arrival date </span>
-   <span class="simpara"> **`SORTFROM`** - mailbox in first From
    address </span>
-   <span class="simpara"> **`SORTSUBJECT`** - message subject </span>
-   <span class="simpara"> **`SORTTO`** - mailbox in first To address
    </span>
-   <span class="simpara"> **`SORTCC`** - mailbox in first cc address
    </span>
-   <span class="simpara"> **`SORTSIZE`** - size of message in octets
    </span>

`reverse`  
Set this to 1 for reverse sorting

`options`  
The `options` are a bitmask of one or more of the following:

-   <span class="simpara"> **`SE_UID`** - Return UIDs instead of
    sequence numbers </span>
-   <span class="simpara"> **`SE_NOPREFETCH`** - Don't prefetch searched
    messages </span>

`search_criteria`  
IMAP2-format search criteria string. For details see <span
class="function">imap\_search</span>.

`charset`  
MIME character set to use when sorting strings.

### 返回值

Returns an array of message numbers sorted by the given parameters,
或者在失败时返回 **`false`**.

imap\_status
============

Returns status information on a mailbox

### 说明

<span class="type">object</span> <span
class="methodname">imap\_status</span> ( <span class="methodparam"><span
class="type">resource</span> `$imap_stream`</span> , <span
class="methodparam"><span class="type">string</span> `$mailbox`</span> ,
<span class="methodparam"><span class="type">int</span>
`$options`</span> )

Gets status information about the given `mailbox`.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`mailbox`  
The mailbox name, see <span class="function">imap\_open</span> for more
information

**Warning**
Passing untrusted data to this parameter is *insecure*, unless
<a href="/imap/setup.html#" class="link">imap.enable_insecure_rsh</a> is
disabled.

`options`  
Valid flags are:

-   <span class="simpara"> **`SA_MESSAGES`** - set `$status->messages`
    to the number of messages in the mailbox </span>
-   <span class="simpara"> **`SA_RECENT`** - set `$status->recent` to
    the number of recent messages in the mailbox </span>
-   <span class="simpara"> **`SA_UNSEEN`** - set `$status->unseen` to
    the number of unseen (new) messages in the mailbox </span>
-   <span class="simpara"> **`SA_UIDNEXT`** - set `$status->uidnext` to
    the next uid to be used in the mailbox </span>
-   <span class="simpara"> **`SA_UIDVALIDITY`** - set
    `$status->uidvalidity` to a constant that changes when uids for the
    mailbox may no longer be valid </span>
-   <span class="simpara"> **`SA_ALL`** - set all of the above </span>

### 返回值

This function returns an object containing status information. The
object has the following properties: *messages*, *recent*, *unseen*,
*uidnext*, and *uidvalidity*.

*flags* is also set, which contains a bitmask which can be checked
against any of the above constants.

### 范例

**示例 \#1 <span class="function">imap\_status</span> example**

``` php
<?php
$mbox = imap_open("{imap.example.com}", "username", "password", OP_HALFOPEN)
      or die("can't connect: " . imap_last_error());

$status = imap_status($mbox, "{imap.example.org}INBOX", SA_ALL);
if ($status) {
  echo "Messages:   " . $status->messages    . "<br />\n";
  echo "Recent:     " . $status->recent      . "<br />\n";
  echo "Unseen:     " . $status->unseen      . "<br />\n";
  echo "UIDnext:    " . $status->uidnext     . "<br />\n";
  echo "UIDvalidity:" . $status->uidvalidity . "<br />\n";
} else {
  echo "imap_status failed: " . imap_last_error() . "\n";
}

imap_close($mbox);
?>
```

imap\_subscribe
===============

Subscribe to a mailbox

### 说明

<span class="type">bool</span> <span
class="methodname">imap\_subscribe</span> ( <span
class="methodparam"><span class="type">resource</span>
`$imap_stream`</span> , <span class="methodparam"><span
class="type">string</span> `$mailbox`</span> )

Subscribe to a new mailbox.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`mailbox`  
The mailbox name, see <span class="function">imap\_open</span> for more
information

**Warning**
Passing untrusted data to this parameter is *insecure*, unless
<a href="/imap/setup.html#" class="link">imap.enable_insecure_rsh</a> is
disabled.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">imap\_unsubscribe</span>

imap\_thread
============

Returns a tree of threaded message

### 说明

<span class="type">array</span> <span
class="methodname">imap\_thread</span> ( <span class="methodparam"><span
class="type">resource</span> `$imap_stream`</span> \[, <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = SE\_FREE</span></span> \] )

Gets a tree of a threaded message.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`options`  

### 返回值

<span class="function">imap\_thread</span> returns an associative array
containing a tree of messages threaded by *REFERENCES*, or **`false`**
on error.

Every message in the current mailbox will be represented by three
entries in the resulting array:

-   `$thread["XX.num"]` - current message number

-   `$thread["XX.next"]`

-   `$thread["XX.branch"]`

### 范例

**示例 \#1 <span class="function">imap\_thread</span> Example**

``` php
<?php

// Here we're outputting the threads of a newsgroup, in HTML

$nntp = imap_open('{news.example.com:119/nntp}some.newsgroup', '', '');
$threads = imap_thread($nntp);

foreach ($threads as $key => $val) {
  $tree = explode('.', $key);
  if ($tree[1] == 'num') {
    $header = imap_headerinfo($nntp, $val);
    echo "<ul>\n\t<li>" . $header->fromaddress . "\n";
  } elseif ($tree[1] == 'branch') {
    echo "\t</li>\n</ul>\n";
  }
}

imap_close($nntp);

?>
```

imap\_timeout
=============

Set or fetch imap timeout

### 说明

<span class="type">mixed</span> <span
class="methodname">imap\_timeout</span> ( <span
class="methodparam"><span class="type">int</span> `$timeout_type`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$timeout`<span class="initializer"> = -1</span></span> \] )

Sets or fetches the imap timeout.

### 参数

`timeout_type`  
One of the following: **`IMAP_OPENTIMEOUT`**, **`IMAP_READTIMEOUT`**,
**`IMAP_WRITETIMEOUT`**, or **`IMAP_CLOSETIMEOUT`**.

`timeout`  
The timeout, in seconds.

### 返回值

If the `timeout` parameter is set, this function returns **`true`** on
success and **`false`** on failure.

If `timeout` is not provided or evaluates to -1, the current timeout
value of `timeout_type` is returned as an integer.

### 范例

**示例 \#1 <span class="function">imap\_timeout</span> example**

``` php
<?php

echo "The current read timeout is " . imap_timeout(IMAP_READTIMEOUT) . "\n";

?>
```

imap\_uid
=========

This function returns the UID for the given message sequence number

### 说明

<span class="type">int</span> <span class="methodname">imap\_uid</span>
( <span class="methodparam"><span class="type">resource</span>
`$imap_stream`</span> , <span class="methodparam"><span
class="type">int</span> `$msg_number`</span> )

This function returns the UID for the given message sequence number. An
UID is a unique identifier that will not change over time while a
message sequence number may change whenever the content of the mailbox
changes.

This function is the inverse of <span
class="function">imap\_msgno</span>.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`msg_number`  
The message number.

### 返回值

The UID of the given message.

### 注释

> **Note**:
>
> This function is not supported by POP3 mailboxes.

### 参见

-   <span class="function">imap\_msgno</span>

imap\_undelete
==============

Unmark the message which is marked deleted

### 说明

<span class="type">bool</span> <span
class="methodname">imap\_undelete</span> ( <span
class="methodparam"><span class="type">resource</span>
`$imap_stream`</span> , <span class="methodparam"><span
class="type">int</span> `$msg_number`</span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \] )

Removes the deletion flag for a specified message, which is set by <span
class="function">imap\_delete</span> or <span
class="function">imap\_mail\_move</span>.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`msg_number`  
The message number

`flags`  

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">imap\_delete</span>
-   <span class="function">imap\_mail\_move</span>

imap\_unsubscribe
=================

Unsubscribe from a mailbox

### 说明

<span class="type">bool</span> <span
class="methodname">imap\_unsubscribe</span> ( <span
class="methodparam"><span class="type">resource</span>
`$imap_stream`</span> , <span class="methodparam"><span
class="type">string</span> `$mailbox`</span> )

Unsubscribe from the specified `mailbox`.

### 参数

` imap_stream`  
由 <span class="function">imap\_open</span> 返回的 IMAP 流。

`mailbox`  
The mailbox name, see <span class="function">imap\_open</span> for more
information

**Warning**
Passing untrusted data to this parameter is *insecure*, unless
<a href="/imap/setup.html#" class="link">imap.enable_insecure_rsh</a> is
disabled.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">imap\_subscribe</span>

imap\_utf7\_decode
==================

Decodes a modified UTF-7 encoded string

### 说明

<span class="type">string</span> <span
class="methodname">imap\_utf7\_decode</span> ( <span
class="methodparam"><span class="type">string</span> `$text`</span> )

Decodes modified UTF-7 `text` into ISO-8859-1 string.

This function is needed to decode mailbox names that contain certain
characters which are not in range of printable ASCII characters.

### 参数

`text`  
A modified UTF-7 encoding string, as defined in
<a href="http://www.faqs.org/rfcs/rfc2060" class="link external">» RFC 2060</a>,
section 5.1.3 (original UTF-7 was defined in
<a href="http://www.faqs.org/rfcs/rfc1642" class="link external">» RFC1642</a>).

### 返回值

Returns a string that is encoded in ISO-8859-1 and consists of the same
sequence of characters in `text`, or **`false`** if `text` contains
invalid modified UTF-7 sequence or `text` contains a character that is
not part of ISO-8859-1 character set.

### 参见

-   <span class="function">imap\_utf7\_encode</span>

imap\_utf7\_encode
==================

Converts ISO-8859-1 string to modified UTF-7 text

### 说明

<span class="type">string</span> <span
class="methodname">imap\_utf7\_encode</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

Converts `data` to modified UTF-7 text.

This is needed to encode mailbox names that contain certain characters
which are not in range of printable ASCII characters.

### 参数

`data`  
An ISO-8859-1 string.

### 返回值

Returns `data` encoded with the modified UTF-7 encoding as defined in
<a href="http://www.faqs.org/rfcs/rfc2060" class="link external">» RFC 2060</a>,
section 5.1.3 (original UTF-7 was defined in
<a href="http://www.faqs.org/rfcs/rfc1642" class="link external">» RFC1642</a>).

### 参见

-   <span class="function">imap\_utf7\_decode</span>

imap\_utf8\_to\_mutf7
=====================

Encode a UTF-8 string to modified UTF-7

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">imap\_utf8\_to\_mutf7</span> ( <span
class="methodparam"><span class="type">string</span> `$in`</span> )

Encode a UTF-8 string to modified UTF-7 (as specified in RFC 2060,
section 5.1.3).

> **Note**:
>
> This function is only available, if libcclient exports
> utf8\_to\_mutf7().

### 参数

`in`  
A UTF-8 encoded string.

### 返回值

Returns `in` converted to modified UTF-7, 或者在失败时返回 **`false`**.

### 参见

-   <span class="function">imap\_mutf7\_to\_utf8</span>

imap\_utf8
==========

Converts MIME-encoded text to UTF-8

### 说明

<span class="type">string</span> <span
class="methodname">imap\_utf8</span> ( <span class="methodparam"><span
class="type">string</span> `$mime_encoded_text`</span> )

Converts the given `mime_encoded_text` to UTF-8, if the declared charset
is known to libc-client. Otherwise the given text is decoded, but not
converted to UTF-8.

### 参数

`mime_encoded_text`  
A MIME encoded string. MIME encoding method and the UTF-8 specification
are described in
<a href="http://www.faqs.org/rfcs/rfc2047" class="link external">» RFC2047</a>
and
<a href="http://www.faqs.org/rfcs/rfc2044" class="link external">» RFC2044</a>
respectively.

### 返回值

Returns the decoded string, if possible converted to UTF-8.

### 范例

**示例 \#1 Basic <span class="function">imap\_utf8</span> Usage**

``` php
<?php
echo imap_utf8("Johannes =?ISO-8859-1?Q?Schl=FCter?=");
?>
```

以上例程的输出类似于：

    Johannes Schlüter

### 参见

-   <span class="function">imap\_mime\_header\_decode</span>

**目录**

-   [imap\_8bit](/ref/imap.html#imap_8bit) — Convert an 8bit string to a
    quoted-printable string
-   [imap\_alerts](/ref/imap.html#imap_alerts) — Returns all IMAP alert
    messages that have occurred
-   [imap\_append](/ref/imap.html#imap_append) — Append a string message
    to a specified mailbox
-   [imap\_base64](/ref/imap.html#imap_base64) — Decode BASE64 encoded
    text
-   [imap\_binary](/ref/imap.html#imap_binary) — Convert an 8bit string
    to a base64 string
-   [imap\_body](/ref/imap.html#imap_body) — Read the message body
-   [imap\_bodystruct](/ref/imap.html#imap_bodystruct) — Read the
    structure of a specified body section of a specific message
-   [imap\_check](/ref/imap.html#imap_check) — Check current mailbox
-   [imap\_clearflag\_full](/ref/imap.html#imap_clearflag_full) — Clears
    flags on messages
-   [imap\_close](/ref/imap.html#imap_close) — Close an IMAP stream
-   [imap\_create](/ref/imap.html#imap_create) — 别名
    imap\_createmailbox
-   [imap\_createmailbox](/ref/imap.html#imap_createmailbox) — Create a
    new mailbox
-   [imap\_delete](/ref/imap.html#imap_delete) — Mark a message for
    deletion from current mailbox
-   [imap\_deletemailbox](/ref/imap.html#imap_deletemailbox) — Delete a
    mailbox
-   [imap\_errors](/ref/imap.html#imap_errors) — Returns all of the IMAP
    errors that have occurred
-   [imap\_expunge](/ref/imap.html#imap_expunge) — Delete all messages
    marked for deletion
-   [imap\_fetch\_overview](/ref/imap.html#imap_fetch_overview) — Read
    an overview of the information in the headers of the given message
-   [imap\_fetchbody](/ref/imap.html#imap_fetchbody) — Fetch a
    particular section of the body of the message
-   [imap\_fetchheader](/ref/imap.html#imap_fetchheader) — Returns
    header for a message
-   [imap\_fetchmime](/ref/imap.html#imap_fetchmime) — Fetch MIME
    headers for a particular section of the message
-   [imap\_fetchstructure](/ref/imap.html#imap_fetchstructure) — Read
    the structure of a particular message
-   [imap\_fetchtext](/ref/imap.html#imap_fetchtext) — 别名 imap\_body
-   [imap\_gc](/ref/imap.html#imap_gc) — Clears IMAP cache
-   [imap\_get\_quota](/ref/imap.html#imap_get_quota) — Retrieve the
    quota level settings, and usage statics per mailbox
-   [imap\_get\_quotaroot](/ref/imap.html#imap_get_quotaroot) — Retrieve
    the quota settings per user
-   [imap\_getacl](/ref/imap.html#imap_getacl) — Gets the ACL for a
    given mailbox
-   [imap\_getmailboxes](/ref/imap.html#imap_getmailboxes) — Read the
    list of mailboxes, returning detailed information on each one
-   [imap\_getsubscribed](/ref/imap.html#imap_getsubscribed) — List all
    the subscribed mailboxes
-   [imap\_header](/ref/imap.html#imap_header) — 别名 imap\_headerinfo
-   [imap\_headerinfo](/ref/imap.html#imap_headerinfo) — Read the header
    of the message
-   [imap\_headers](/ref/imap.html#imap_headers) — Returns headers for
    all messages in a mailbox
-   [imap\_last\_error](/ref/imap.html#imap_last_error) — Gets the last
    IMAP error that occurred during this page request
-   [imap\_list](/ref/imap.html#imap_list) — Read the list of mailboxes
-   [imap\_listmailbox](/ref/imap.html#imap_listmailbox) — 别名
    imap\_list
-   [imap\_listscan](/ref/imap.html#imap_listscan) — Returns the list of
    mailboxes that matches the given text
-   [imap\_listsubscribed](/ref/imap.html#imap_listsubscribed) — 别名
    imap\_lsub
-   [imap\_lsub](/ref/imap.html#imap_lsub) — List all the subscribed
    mailboxes
-   [imap\_mail\_compose](/ref/imap.html#imap_mail_compose) — Create a
    MIME message based on given envelope and body sections
-   [imap\_mail\_copy](/ref/imap.html#imap_mail_copy) — Copy specified
    messages to a mailbox
-   [imap\_mail\_move](/ref/imap.html#imap_mail_move) — Move specified
    messages to a mailbox
-   [imap\_mail](/ref/imap.html#imap_mail) — Send an email message
-   [imap\_mailboxmsginfo](/ref/imap.html#imap_mailboxmsginfo) — Get
    information about the current mailbox
-   [imap\_mime\_header\_decode](/ref/imap.html#imap_mime_header_decode)
    — Decode MIME header elements
-   [imap\_msgno](/ref/imap.html#imap_msgno) — Gets the message sequence
    number for the given UID
-   [imap\_mutf7\_to\_utf8](/ref/imap.html#imap_mutf7_to_utf8) — Decode
    a modified UTF-7 string to UTF-8
-   [imap\_num\_msg](/ref/imap.html#imap_num_msg) — Gets the number of
    messages in the current mailbox
-   [imap\_num\_recent](/ref/imap.html#imap_num_recent) — Gets the
    number of recent messages in current mailbox
-   [imap\_open](/ref/imap.html#imap_open) — Open an IMAP stream to a
    mailbox
-   [imap\_ping](/ref/imap.html#imap_ping) — Check if the IMAP stream is
    still active
-   [imap\_qprint](/ref/imap.html#imap_qprint) — Convert a
    quoted-printable string to an 8 bit string
-   [imap\_rename](/ref/imap.html#imap_rename) — 别名
    imap\_renamemailbox
-   [imap\_renamemailbox](/ref/imap.html#imap_renamemailbox) — Rename an
    old mailbox to new mailbox
-   [imap\_reopen](/ref/imap.html#imap_reopen) — Reopen IMAP stream to
    new mailbox
-   [imap\_rfc822\_parse\_adrlist](/ref/imap.html#imap_rfc822_parse_adrlist)
    — Parses an address string
-   [imap\_rfc822\_parse\_headers](/ref/imap.html#imap_rfc822_parse_headers)
    — Parse mail headers from a string
-   [imap\_rfc822\_write\_address](/ref/imap.html#imap_rfc822_write_address)
    — Returns a properly formatted email address given the mailbox,
    host, and personal info
-   [imap\_savebody](/ref/imap.html#imap_savebody) — Save a specific
    body section to a file
-   [imap\_scan](/ref/imap.html#imap_scan) — 别名 imap\_listscan
-   [imap\_scanmailbox](/ref/imap.html#imap_scanmailbox) — 别名
    imap\_listscan
-   [imap\_search](/ref/imap.html#imap_search) — This function returns
    an array of messages matching the given search criteria
-   [imap\_set\_quota](/ref/imap.html#imap_set_quota) — Sets a quota for
    a given mailbox
-   [imap\_setacl](/ref/imap.html#imap_setacl) — Sets the ACL for a
    given mailbox
-   [imap\_setflag\_full](/ref/imap.html#imap_setflag_full) — Sets flags
    on messages
-   [imap\_sort](/ref/imap.html#imap_sort) — Gets and sort messages
-   [imap\_status](/ref/imap.html#imap_status) — Returns status
    information on a mailbox
-   [imap\_subscribe](/ref/imap.html#imap_subscribe) — Subscribe to a
    mailbox
-   [imap\_thread](/ref/imap.html#imap_thread) — Returns a tree of
    threaded message
-   [imap\_timeout](/ref/imap.html#imap_timeout) — Set or fetch imap
    timeout
-   [imap\_uid](/ref/imap.html#imap_uid) — This function returns the UID
    for the given message sequence number
-   [imap\_undelete](/ref/imap.html#imap_undelete) — Unmark the message
    which is marked deleted
-   [imap\_unsubscribe](/ref/imap.html#imap_unsubscribe) — Unsubscribe
    from a mailbox
-   [imap\_utf7\_decode](/ref/imap.html#imap_utf7_decode) — Decodes a
    modified UTF-7 encoded string
-   [imap\_utf7\_encode](/ref/imap.html#imap_utf7_encode) — Converts
    ISO-8859-1 string to modified UTF-7 text
-   [imap\_utf8\_to\_mutf7](/ref/imap.html#imap_utf8_to_mutf7) — Encode
    a UTF-8 string to modified UTF-7
-   [imap\_utf8](/ref/imap.html#imap_utf8) — Converts MIME-encoded text
    to UTF-8
