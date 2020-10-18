用 PHP 进行 HTTP 认证
=====================

可以用 <span class="function">header</span>
函数来向客户端浏览器发送“*Authentication
Required*”信息，使其弹出一个用户名／密码输入窗口。当用户输入用户名和密码后，包含有
URL 的 PHP
脚本将会加上<a href="/reserved/variables.html" class="link">预定义变量</a>
`PHP_AUTH_USER`，`PHP_AUTH_PW` 和 `AUTH_TYPE`
被再次调用，这三个变量分别被设定为用户名，密码和认证类型。预定义变量保存在
`$_SERVER` 数组中。支持“Basic”和“Digest”（自 PHP 5.1.0
起）认证方法。请参阅 <span class="function">header</span>
函数以获取更多信息。

以下是在页面上强迫客户端认证的脚本范例：

**示例 \#1 Basic HTTP 认证范例**

``` php
<?php
  if (!isset($_SERVER['PHP_AUTH_USER'])) {
    header('WWW-Authenticate: Basic realm="My Realm"');
    header('HTTP/1.0 401 Unauthorized');
    echo 'Text to send if user hits Cancel button';
    exit;
  } else {
    echo "<p>Hello {$_SERVER['PHP_AUTH_USER']}.</p>";
    echo "<p>You entered {$_SERVER['PHP_AUTH_PW']} as your password.</p>";
  }
?>
```

**示例 \#2 Digest HTTP 认证范例**

本例演示怎样实现一个简单的 Digest HTTP 认证脚本。更多信息请参考
<a href="http://www.faqs.org/rfcs/rfc2617" class="link external">» RFC 2617</a>。

``` php
<?php
$realm = 'Restricted area';

//user => password
$users = array('admin' => 'mypass', 'guest' => 'guest');


if (empty($_SERVER['PHP_AUTH_DIGEST'])) {
    header('HTTP/1.1 401 Unauthorized');
    header('WWW-Authenticate: Digest realm="'.$realm.
           '",qop="auth",nonce="'.uniqid().'",opaque="'.md5($realm).'"');

    die('Text to send if user hits Cancel button');
}


// analyze the PHP_AUTH_DIGEST variable
if (!($data = http_digest_parse($_SERVER['PHP_AUTH_DIGEST'])) ||
    !isset($users[$data['username']]))
    die('Wrong Credentials!');


// generate the valid response
$A1 = md5($data['username'] . ':' . $realm . ':' . $users[$data['username']]);
$A2 = md5($_SERVER['REQUEST_METHOD'].':'.$data['uri']);
$valid_response = md5($A1.':'.$data['nonce'].':'.$data['nc'].':'.$data['cnonce'].':'.$data['qop'].':'.$A2);

if ($data['response'] != $valid_response)
    die('Wrong Credentials!');

// ok, valid username & password
echo 'You are logged in as: ' . $data['username'];


// function to parse the http auth header
function http_digest_parse($txt)
{
    // protect against missing data
    $needed_parts = array('nonce'=>1, 'nc'=>1, 'cnonce'=>1, 'qop'=>1, 'username'=>1, 'uri'=>1, 'response'=>1);
    $data = array();
    $keys = implode('|', array_keys($needed_parts));

    preg_match_all('@(' . $keys . ')=(?:([\'"])([^\2]+?)\2|([^\s,]+))@', $txt, $matches, PREG_SET_ORDER);

    foreach ($matches as $m) {
        $data[$m[1]] = $m[3] ? $m[3] : $m[4];
        unset($needed_parts[$m[1]]);
    }

    return $needed_parts ? false : $data;
}
?>
```

> **Note**: **兼容性问题**  
>
> 在编写 HTTP
> 标头代码时请格外小心。为了对所有的客户端保证兼容性，关键字“Basic”的第一个字母必须大写为“B”，分界字符串必须用双引号（不是单引号）引用；并且在标头行
> *HTTP/1.0 401* 中，在 *401* 前必须有且仅有一个空格。

在以上例子中，仅仅只打印出了 `PHP_AUTH_USER` 和 `PHP_AUTH_PW`
的值，但在实际运用中，可能需要对用户名和密码的合法性进行检查。或许进行数据库的查询，或许从
dbm 文件中检索。

注意有些 Internet Explorer
浏览器本身有问题。它对标头的顺序显得似乎有点吹毛求疵。目前看来在发送
*HTTP/1.0 401* 之前先发送 *WWW-Authenticate* 标头似乎可以解决此问题。

> **Note**: **配置说明**  
>
> PHP 用是否有 *AuthType* 指令来判断外部认证机制是否有效。

注意，这仍然不能防止有人通过未认证的 URL 来从同一服务器上认证的 URL
上偷取密码。

Netscape Navigator 和 Internet Explorer 浏览器都会在收到 401
的服务端返回信息时清空所有的本地浏览器整个域的 Windows
认证缓存。这能够有效的注销一个用户，并迫使他们重新输入他们的用户名和密码。有些人用这种方法来使登录状态“过期”，或者作为“注销”按钮的响应行为。

**示例 \#3 强迫重新输入用户名和密码的 HTTP 认证的范例**

``` php
<?php
  function authenticate() {
    header('WWW-Authenticate: Basic realm="Test Authentication System"');
    header('HTTP/1.0 401 Unauthorized');
    echo "You must enter a valid login ID and password to access this resource\n";
    exit;
  }

  if (!isset($_SERVER['PHP_AUTH_USER']) ||
      ($_POST['SeenBefore'] == 1 && $_POST['OldAuth'] == $_SERVER['PHP_AUTH_USER'])) {
   authenticate();
  }
  else {
   echo "<p>Welcome: {$_SERVER['PHP_AUTH_USER']}<br />";
   echo "Old: {$_REQUEST['OldAuth']}";
   echo "<form action='{$_SERVER['PHP_SELF']}' METHOD='post'>\n";
   echo "<input type='hidden' name='SeenBefore' value='1' />\n";
   echo "<input type='hidden' name='OldAuth' value='{$_SERVER['PHP_AUTH_USER']}' />\n";
   echo "<input type='submit' value='Re Authenticate' />\n";
   echo "</form></p>\n";
  }
```

该行为对于 HTTP 的 Basic
认证标准来说并不是必须的，因此不能依靠这种方法。对 Lynx 浏览器的测试表明
Lynx 在收到 401
的服务端返回信息时不会清空认证文件，因此只要对认证文件的检查要求没有变化，只要用户点击“后退”按钮，再点击“前进”按钮，其原有资源仍然能够被访问。不过，用户可以通过按“\_”键来清空他们的认证信息。

为了能够使HTTP工作在 IIS 服务器的 CGI 模式下。 你需要编辑
IIS的设置“*目录安全*”。点击“*编辑*”并且只选择“*匿名访问*”，其它所有的复选框都应该留空。

> **Note**: **IIS 注意事项**  
> <span class="simpara"> 要 HTTP 认证能够在 IIS 下工作，PHP 配置选项
> <a href="/ini/core.html#ini.cgi.rfc2616-headers" class="link">cgi.rfc2616_headers</a>
> 必须设置成 *0*（默认值）。 </span>
