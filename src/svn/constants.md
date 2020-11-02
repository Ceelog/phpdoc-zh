预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`SVN_REVISION_HEAD`** (<span class="type">int</span>)  
<span class="simpara"> Magic number (-1) specifying the HEAD revision
</span>

<!-- -->

**`SVN_AUTH_PARAM_DEFAULT_USERNAME`** (<span class="type">string</span>)  
<span class="simpara"> Property for default username to use when
performing basic authentication </span>

**`SVN_AUTH_PARAM_DEFAULT_PASSWORD`** (<span class="type">string</span>)  
<span class="simpara"> Property for default password to use when
performing basic authentication </span>

**`SVN_AUTH_PARAM_NON_INTERACTIVE`** (<span class="type">string</span>)  
<span class="simpara"></span>

**`SVN_AUTH_PARAM_DONT_STORE_PASSWORDS`** (<span class="type">string</span>)  
<span class="simpara"></span>

**`SVN_AUTH_PARAM_NO_AUTH_CACHE`** (<span class="type">string</span>)  
<span class="simpara"></span>

**`SVN_AUTH_PARAM_SSL_SERVER_FAILURES`** (<span class="type">string</span>)  
<span class="simpara"></span>

**`SVN_AUTH_PARAM_SSL_SERVER_CERT_INFO`** (<span class="type">string</span>)  
<span class="simpara"></span>

**`SVN_AUTH_PARAM_CONFIG`** (<span class="type">string</span>)  
<span class="simpara"></span>

**`SVN_AUTH_PARAM_SERVER_GROUP`** (<span class="type">string</span>)  
<span class="simpara"></span>

**`SVN_AUTH_PARAM_CONFIG_DIR`** (<span class="type">string</span>)  
<span class="simpara"></span>

**`PHP_SVN_AUTH_PARAM_IGNORE_SSL_VERIFY_ERRORS`** (<span class="type">string</span>)  
<span class="simpara"> Custom property for ignoring SSL cert
verification errors </span>

<!-- -->

**`SVN_FS_CONFIG_FS_TYPE`** (<span class="type">string</span>)  
<span class="simpara"> Configuration key that determines filesystem type
</span>

**`SVN_FS_TYPE_BDB`** (<span class="type">string</span>)  
<span class="simpara"> Filesystem is Berkeley-DB implementation </span>

**`SVN_FS_TYPE_FSFS`** (<span class="type">string</span>)  
<span class="simpara"> Filesystem is native-filesystem implementation
</span>

<!-- -->

**`SVN_PROP_REVISION_DATE`** (<span class="type">string</span>)  
<span class="simpara"> svn:date </span>

**`SVN_PROP_REVISION_ORIG_DATE`** (<span class="type">string</span>)  
<span class="simpara"> svn:original-date </span>

**`SVN_PROP_REVISION_AUTHOR`** (<span class="type">string</span>)  
<span class="simpara"> svn:author </span>

**`SVN_PROP_REVISION_LOG`** (<span class="type">string</span>)  
<span class="simpara"> svn:log </span>

<!-- -->

**`SVN_WC_STATUS_NONE`** (<span class="type">int</span>)  
<span class="simpara"> Status does not exist </span>

**`SVN_WC_STATUS_UNVERSIONED`** (<span class="type">int</span>)  
<span class="simpara"> Item is not versioned in working copy </span>

**`SVN_WC_STATUS_NORMAL`** (<span class="type">int</span>)  
<span class="simpara"> Item exists, nothing else is happening </span>

**`SVN_WC_STATUS_ADDED`** (<span class="type">int</span>)  
<span class="simpara"> Item is scheduled for addition </span>

**`SVN_WC_STATUS_MISSING`** (<span class="type">int</span>)  
<span class="simpara"> Item is versioned but missing from the working
copy </span>

**`SVN_WC_STATUS_DELETED`** (<span class="type">int</span>)  
<span class="simpara"> Item is scheduled for deletion </span>

**`SVN_WC_STATUS_REPLACED`** (<span class="type">int</span>)  
<span class="simpara"> Item was deleted and then re-added </span>

**`SVN_WC_STATUS_MODIFIED`** (<span class="type">int</span>)  
<span class="simpara"> Item (text or properties) was modified </span>

**`SVN_WC_STATUS_MERGED`** (<span class="type">int</span>)  
<span class="simpara"> Item's local modifications were merged with
repository modifications </span>

**`SVN_WC_STATUS_CONFLICTED`** (<span class="type">int</span>)  
<span class="simpara"> Item's local modifications conflicted with
repository modifications </span>

**`SVN_WC_STATUS_IGNORED`** (<span class="type">int</span>)  
<span class="simpara"> Item is unversioned but configured to be ignored
</span>

**`SVN_WC_STATUS_OBSTRUCTED`** (<span class="type">int</span>)  
<span class="simpara"> Unversioned item is in the way of a versioned
resource </span>

**`SVN_WC_STATUS_EXTERNAL`** (<span class="type">int</span>)  
<span class="simpara"> Unversioned path that is populated using
svn:externals </span>

**`SVN_WC_STATUS_INCOMPLETE`** (<span class="type">int</span>)  
<span class="simpara"> Directory does not contain complete entries list
</span>

<!-- -->

**`SVN_NODE_NONE`** (<span class="type">int</span>)  
<span class="simpara"> Absent </span>

**`SVN_NODE_FILE`** (<span class="type">int</span>)  
<span class="simpara"> File </span>

**`SVN_NODE_DIR`** (<span class="type">int</span>)  
<span class="simpara"> Directory </span>

**`SVN_NODE_UNKNOWN`** (<span class="type">int</span>)  
<span class="simpara"> Something Subversion cannot identify </span>
