预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`NIL`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`OP_DEBUG`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`OP_READONLY`** (<span class="type">int</span>)  
<span class="simpara"> Open mailbox read-only </span>

**`OP_ANONYMOUS`** (<span class="type">int</span>)  
<span class="simpara"> Don't use or update a `.newsrc` for news (NNTP
only) </span>

**`OP_SHORTCACHE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`OP_SILENT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`OP_PROTOTYPE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`OP_HALFOPEN`** (<span class="type">int</span>)  
<span class="simpara"> For IMAP and NNTP names, open a connection but
don't open a mailbox. </span>

**`OP_EXPUNGE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`OP_SECURE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`CL_EXPUNGE`** (<span class="type">int</span>)  
<span class="simpara"> silently expunge the mailbox before closing when
calling <span class="function">imap\_close</span> </span>

**`FT_UID`** (<span class="type">int</span>)  
<span class="simpara"> The parameter is a UID </span>

**`FT_PEEK`** (<span class="type">int</span>)  
<span class="simpara"> Do not set the \\Seen flag if not already set
</span>

**`FT_NOT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`FT_INTERNAL`** (<span class="type">int</span>)  
<span class="simpara"> The return string is in internal format, will not
canonicalize to CRLF. </span>

**`FT_PREFETCHTEXT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`ST_UID`** (<span class="type">int</span>)  
<span class="simpara"> The sequence argument contains UIDs instead of
sequence numbers </span>

**`ST_SILENT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`ST_SET`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`CP_UID`** (<span class="type">int</span>)  
<span class="simpara"> the sequence numbers contain UIDS </span>

**`CP_MOVE`** (<span class="type">int</span>)  
<span class="simpara"> Delete the messages from the current mailbox
after copying with <span class="function">imap\_mail\_copy</span>
</span>

**`SE_UID`** (<span class="type">int</span>)  
<span class="simpara"> Return UIDs instead of sequence numbers </span>

**`SE_FREE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SE_NOPREFETCH`** (<span class="type">int</span>)  
<span class="simpara"> Don't prefetch searched messages </span>

**`SO_FREE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SO_NOSERVER`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SA_MESSAGES`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SA_RECENT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SA_UNSEEN`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SA_UIDNEXT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SA_UIDVALIDITY`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SA_ALL`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`LATT_NOINFERIORS`** (<span class="type">int</span>)  
<span class="simpara"> This mailbox has no "children" (there are no
mailboxes below this one). </span>

**`LATT_NOSELECT`** (<span class="type">int</span>)  
<span class="simpara"> This is only a container, not a mailbox - you
cannot open it. </span>

**`LATT_MARKED`** (<span class="type">int</span>)  
<span class="simpara"> This mailbox is marked. Only used by UW-IMAPD.
</span>

**`LATT_UNMARKED`** (<span class="type">int</span>)  
<span class="simpara"> This mailbox is not marked. Only used by
UW-IMAPD. </span>

**`LATT_REFERRAL`** (<span class="type">int</span>)  
<span class="simpara"> This container has a referral to a remote
mailbox. </span>

**`LATT_HASCHILDREN`** (<span class="type">int</span>)  
<span class="simpara"> This mailbox has selectable inferiors. </span>

**`LATT_HASNOCHILDREN`** (<span class="type">int</span>)  
<span class="simpara"> This mailbox has no selectable inferiors. </span>

**`SORTDATE`** (<span class="type">int</span>)  
<span class="simpara"> Sort criteria for <span
class="function">imap\_sort</span>: message Date </span>

**`SORTARRIVAL`** (<span class="type">int</span>)  
<span class="simpara"> Sort criteria for <span
class="function">imap\_sort</span>: arrival date </span>

**`SORTFROM`** (<span class="type">int</span>)  
<span class="simpara"> Sort criteria for <span
class="function">imap\_sort</span>: mailbox in first From address
</span>

**`SORTSUBJECT`** (<span class="type">int</span>)  
<span class="simpara"> Sort criteria for <span
class="function">imap\_sort</span>: message subject </span>

**`SORTTO`** (<span class="type">int</span>)  
<span class="simpara"> Sort criteria for <span
class="function">imap\_sort</span>: mailbox in first To address </span>

**`SORTCC`** (<span class="type">int</span>)  
<span class="simpara"> Sort criteria for <span
class="function">imap\_sort</span>: mailbox in first cc address </span>

**`SORTSIZE`** (<span class="type">int</span>)  
<span class="simpara"> Sort criteria for <span
class="function">imap\_sort</span>: size of message in octets </span>

**`TYPETEXT`** (<span class="type">int</span>)  
<span class="simpara"> Primary body type: unformatted text </span>

**`TYPEMULTIPART`** (<span class="type">int</span>)  
<span class="simpara"> Primary body type: multiple part </span>

**`TYPEMESSAGE`** (<span class="type">int</span>)  
<span class="simpara"> Primary body type: encapsulated message </span>

**`TYPEAPPLICATION`** (<span class="type">int</span>)  
<span class="simpara"> Primary body type: application data </span>

**`TYPEAUDIO`** (<span class="type">int</span>)  
<span class="simpara"> Primary body type: audio </span>

**`TYPEIMAGE`** (<span class="type">int</span>)  
<span class="simpara"> Primary body type: static image </span>

**`TYPEVIDEO`** (<span class="type">int</span>)  
<span class="simpara"> Primary body type: video </span>

**`TYPEMODEL`** (<span class="type">int</span>)  
<span class="simpara"> Primary body type: model </span>

**`TYPEOTHER`** (<span class="type">int</span>)  
<span class="simpara"> Primary body type: unknown </span>

**`ENC7BIT`** (<span class="type">int</span>)  
<span class="simpara"> Body encoding: 7 bit SMTP semantic data </span>

**`ENC8BIT`** (<span class="type">int</span>)  
<span class="simpara"> Body encoding: 8 bit SMTP semantic data </span>

**`ENCBINARY`** (<span class="type">int</span>)  
<span class="simpara"> Body encoding: 8 bit binary data </span>

**`ENCBASE64`** (<span class="type">int</span>)  
<span class="simpara"> Body encoding: base-64 encoded data </span>

**`ENCQUOTEDPRINTABLE`** (<span class="type">int</span>)  
<span class="simpara"> Body encoding: human-readable 8-as-7 bit data
</span>

**`ENCOTHER`** (<span class="type">int</span>)  
<span class="simpara"> Body encoding: unknown </span>

**`IMAP_OPENTIMEOUT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`IMAP_READTIMEOUT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`IMAP_WRITETIMEOUT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`IMAP_CLOSETIMEOUT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`IMAP_GC_ELT`** (<span class="type">int</span>)  
<span class="simpara"> Garbage collector, clear message cache elements.
</span>

**`IMAP_GC_ENV`** (<span class="type">int</span>)  
<span class="simpara"> Garbage collector, clear envelopes and bodies.
</span>

**`IMAP_GC_TEXTS`** (<span class="type">int</span>)  
<span class="simpara"> Garbage collector, clear texts. </span>
