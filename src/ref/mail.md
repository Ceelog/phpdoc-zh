ezmlm\_hash
===========

计算 EZMLM 所需的散列值

### 说明

<span class="type">int</span> <span
class="methodname">ezmlm\_hash</span> ( <span class="methodparam"><span
class="type">string</span> `$addr`</span> )

<span class="function">ezmlm\_hash</span> 计算用于在 MySQL 数据库中保存
EZMLM 邮件列表的散列值。

### 参数

`addr`  
要进行散列算法的电子邮件地址。

### 返回值

`addr` 的散列值。

### 范例

**示例 \#1 计算散列值并订阅一个用户**

``` php
<?php

$user = "joecool@example.com";
$hash = ezmlm_hash($user);
$query = sprintf("INSERT INTO sample VALUES (%s, '%s')", $hash, $user);
$db->query($query); // using PHPLIB db interface

?>
```

mail
====

发送邮件

### 说明

<span class="type">bool</span> <span class="methodname">mail</span> (
<span class="methodparam"><span class="type">string</span> `$to`</span>
, <span class="methodparam"><span class="type">string</span>
`$subject`</span> , <span class="methodparam"><span
class="type">string</span> `$message`</span> \[, <span
class="methodparam"><span class="type">string</span>
`$additional_headers`</span> \[, <span class="methodparam"><span
class="type">string</span> `$additional_parameters`</span> \]\] )

发送一封电子邮件。

### 参数

`to`  
电子邮件收件人，或收件人列表。

本字符串的格式必须符合
<a href="http://www.faqs.org/rfcs/rfc2822" class="link external">» RFC 2822</a>。例如：

-   user@example.com
-   user@example.com, anotheruser@example.com
-   User \<user@example.com\>
-   User \<user@example.com\>, Another User \<anotheruser@example.com\>

`subject`  
电子邮件的主题。

**Caution**
本项不能包含任何换行符，否则邮件可能无法正确发送。

`message`  
所要发送的消息。

行之间必须以一个 LF（\\n）分隔。每行不能超过 70 个字符。

**Caution**
（Windows 下）当 PHP 直接连接到 SMTP
服务器时，如果在一行开头发现一个句号，则会被删掉。要避免此问题，将单个句号替换成两个句号。

``` php
<?php
$text = str_replace("\n.", "\n..", $text);
?>
```

`additional_headers`（可选项）  
String to be inserted at the end of the email header.

This is typically used to add extra headers (From, Cc, and Bcc).
Multiple extra headers should be separated with a CRLF (\\r\\n).

> **Note**:
>
> When sending mail, the mail *must* contain a *From* header. This can
> be set with the `additional_headers` parameter, or a default can be
> set in `php.ini`.
>
> Failing to do this will result in an error message similar to
> *Warning: mail(): "sendmail\_from" not set in php.ini or custom
> "From:" header missing*.

> **Note**:
>
> If messages are not received, try using a LF (\\n) only. Some poor
> quality Unix mail transfer agents replace LF by CRLF automatically
> (which leads to doubling CR if CRLF is used). This should be a last
> resort, as it does not comply with
> <a href="http://www.faqs.org/rfcs/rfc2822" class="link external">» RFC 2822</a>.

`additional_parameters` (optional)  
The `additional_parameters` parameter can be used to pass an additional
parameter to the program configured to use when sending mail using the
*sendmail\_path* configuration setting. For example, this can be used to
set the envelope sender address when using sendmail with the *-f*
sendmail option.

The user that the webserver runs as should be added as a trusted user to
the sendmail configuration to prevent a 'X-Warning' header from being
added to the message when the envelope sender (-f) is set using this
method. For sendmail users, this file is `/etc/mail/trusted-users`.

### 返回值

Returns **`true`** if the mail was successfully accepted for delivery,
**`false`** otherwise.

It is important to note that just because the mail was accepted for
delivery, it does NOT mean the mail will actually reach the intended
destination.

### 更新日志

| 版本  | 说明                                                                     |
|-------|--------------------------------------------------------------------------|
| 7.2.0 | 现在 `additional_headers` 参数开始支持 <span class="type">array</span>。 |

### 范例

**示例 \#1 Sending mail.**

Using <span class="function">mail</span> to send a simple email:

``` php
<?php
// The message
$message = "Line 1\nLine 2\nLine 3";

// In case any of our lines are larger than 70 characters, we should use wordwrap()
$message = wordwrap($message, 70);

// Send
mail('caffinated@example.com', 'My Subject', $message);
?>
```

**示例 \#2 Sending mail with extra headers.**

The addition of basic headers, telling the MUA the From and Reply-To
addresses:

``` php
<?php
$to      = 'nobody@example.com';
$subject = 'the subject';
$message = 'hello';
$headers = 'From: webmaster@example.com' . "\r\n" .
    'Reply-To: webmaster@example.com' . "\r\n" .
    'X-Mailer: PHP/' . phpversion();

mail($to, $subject, $message, $headers);
?>
```

**示例 \#3 Sending mail with an additional command line parameter.**

The `additional_parameters` parameter can be used to pass an additional
parameter to the program configured to use when sending mail using the
*sendmail\_path*.

``` php
<?php
mail('nobody@example.com', 'the subject', 'the message', null,
   '-fwebmaster@example.com');
?>
```

**示例 \#4 Sending HTML email**

It is also possible to send HTML email with <span
class="function">mail</span>.

``` php
<?php
// multiple recipients
$to  = 'aidan@example.com' . ', '; // note the comma
$to .= 'wez@example.com';

// subject
$subject = 'Birthday Reminders for August';

// message
$message = '
<html>
<head>
  <title>Birthday Reminders for August</title>
</head>
<body>
  <p>Here are the birthdays upcoming in August!</p>
  <table>
    <tr>
      <th>Person</th><th>Day</th><th>Month</th><th>Year</th>
    </tr>
    <tr>
      <td>Joe</td><td>3rd</td><td>August</td><td>1970</td>
    </tr>
    <tr>
      <td>Sally</td><td>17th</td><td>August</td><td>1973</td>
    </tr>
  </table>
</body>
</html>
';

// To send HTML mail, the Content-type header must be set
$headers  = 'MIME-Version: 1.0' . "\r\n";
$headers .= 'Content-type: text/html; charset=iso-8859-1' . "\r\n";

// Additional headers
$headers .= 'To: Mary <mary@example.com>, Kelly <kelly@example.com>' . "\r\n";
$headers .= 'From: Birthday Reminder <birthday@example.com>' . "\r\n";
$headers .= 'Cc: birthdayarchive@example.com' . "\r\n";
$headers .= 'Bcc: birthdaycheck@example.com' . "\r\n";

// Mail it
mail($to, $subject, $message, $headers);
?>
```

> **Note**:
>
> If intending to send HTML or otherwise Complex mails, it is
> recommended to use the PEAR package
> <a href="https://pear.php.net/package/Mail" class="link external">» PEAR::Mail</a>.

### 注释

> **Note**:
>
> The Windows implementation of <span class="function">mail</span>
> differs in many ways from the Unix implementation. First, it doesn't
> use a local binary for composing messages but only operates on direct
> sockets which means a *MTA* is needed listening on a network socket
> (which can either on the localhost or a remote machine).
>
> Second, the custom headers like *From:*, *Cc:*, *Bcc:* and *Date:* are
> *not* interpreted by the *MTA* in the first place, but are parsed by
> PHP.
>
> As such, the `to` parameter should not be an address in the form of
> "Something \<someone@example.com\>". The mail command may not parse
> this properly while talking with the MTA.

> **Note**:
>
> It is worth noting that the <span class="function">mail</span>
> function is not suitable for larger volumes of email in a loop. This
> function opens and closes an SMTP socket for each email, which is not
> very efficient.
>
> For the sending of large amounts of email, see the
> <a href="https://pear.php.net/package/Mail" class="link external">» PEAR::Mail</a>,
> and
> <a href="https://pear.php.net/package/Mail_Queue" class="link external">» PEAR::Mail_Queue</a>
> packages.

> **Note**:
>
> The following RFCs may be useful:
> <a href="http://www.faqs.org/rfcs/rfc1896" class="link external">» RFC 1896</a>,
> <a href="http://www.faqs.org/rfcs/rfc2045" class="link external">» RFC 2045</a>,
> <a href="http://www.faqs.org/rfcs/rfc2046" class="link external">» RFC 2046</a>,
> <a href="http://www.faqs.org/rfcs/rfc2047" class="link external">» RFC 2047</a>,
> <a href="http://www.faqs.org/rfcs/rfc2048" class="link external">» RFC 2048</a>,
> <a href="http://www.faqs.org/rfcs/rfc2049" class="link external">» RFC 2049</a>,
> and
> <a href="http://www.faqs.org/rfcs/rfc2822" class="link external">» RFC 2822</a>.

### 参见

-   <span class="function">imap\_mail</span>
-   <a href="https://pear.php.net/package/Mail" class="link external">» PEAR::Mail</a>
-   <a href="https://pear.php.net/package/Mail_Mime" class="link external">» PEAR::Mail_Mime</a>

**目录**

-   [ezmlm\_hash](/ref/mail.html#ezmlm_hash) — 计算 EZMLM 所需的散列值
-   [mail](/ref/mail.html#mail) — 发送邮件
