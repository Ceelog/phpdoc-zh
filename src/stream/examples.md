范例
====

**目录**

-   [Example class registered as stream
    wrapper](/stream/examples.html#Example%20class%20registered%20as%20stream%20wrapper)

**示例 \#1 Using <span class="function">file\_get\_contents</span> to
retrieve data from multiple sources**

``` php
<?php
/* Read local file from /home/bar */
$localfile = file_get_contents("/home/bar/foo.txt");

/* Identical to above, explicitly naming FILE scheme */
$localfile = file_get_contents("file:///home/bar/foo.txt");

/* Read remote file from www.example.com using HTTP */
$httpfile  = file_get_contents("http://www.example.com/foo.txt");

/* Read remote file from www.example.com using HTTPS */
$httpsfile = file_get_contents("https://www.example.com/foo.txt");

/* Read remote file from ftp.example.com using FTP */
$ftpfile   = file_get_contents("ftp://user:pass@ftp.example.com/foo.txt");

/* Read remote file from ftp.example.com using FTPS */
$ftpsfile  = file_get_contents("ftps://user:pass@ftp.example.com/foo.txt");
?>
```

**示例 \#2 Making a POST request to an https server**

``` php
<?php
/* Send POST request to https://secure.example.com/form_action.php
* Include form elements named "foo" and "bar" with dummy values
*/

$sock = fsockopen("ssl://secure.example.com", 443, $errno, $errstr, 30);
if (!$sock) die("$errstr ($errno)\n");

$data = "foo=" . urlencode("Value for Foo") . "&bar=" . urlencode("Value for Bar");

fwrite($sock, "POST /form_action.php HTTP/1.0\r\n");
fwrite($sock, "Host: secure.example.com\r\n");
fwrite($sock, "Content-type: application/x-www-form-urlencoded\r\n");
fwrite($sock, "Content-length: " . strlen($data) . "\r\n");
fwrite($sock, "Accept: */*\r\n");
fwrite($sock, "\r\n");
fwrite($sock, $data);

$headers = "";
while ($str = trim(fgets($sock, 4096)))
$headers .= "$str\n";

echo "\n";

$body = "";
while (!feof($sock))
$body .= fgets($sock, 4096);

fclose($sock);
?>
```

**示例 \#3 Writing data to a compressed file**

``` php
<?php
/* Create a compressed file containing an arbitrarty string
* File can be read back using compress.zlib stream or just
* decompressed from the command line using 'gzip -d foo-bar.txt.gz'
*/
$fp = fopen("compress.zlib://foo-bar.txt.gz", "wb");
if (!$fp) die("Unable to create file.");

fwrite($fp, "This is a test.\n");

fclose($fp);
?>
```

Example class registered as stream wrapper
------------------------------------------

The example below implements a var:// protocol handler that allows
read/write access to a named global variable using standard filesystem
stream functions such as <span class="function">fread</span>. The var://
protocol implemented below, given the URL "var://foo" will read/write
data to/from $GLOBALS\["foo"\].

**示例 \#1 A Stream for reading/writing global variables**

``` php
<?php

class VariableStream {
    var $position;
    var $varname;

    function stream_open($path, $mode, $options, &$opened_path)
    {
        $url = parse_url($path);
        $this->varname = $url["host"];
        $this->position = 0;

        return true;
    }

    function stream_read($count)
    {
        $ret = substr($GLOBALS[$this->varname], $this->position, $count);
        $this->position += strlen($ret);
        return $ret;
    }

    function stream_write($data)
    {
        $left = substr($GLOBALS[$this->varname], 0, $this->position);
        $right = substr($GLOBALS[$this->varname], $this->position + strlen($data));
        $GLOBALS[$this->varname] = $left . $data . $right;
        $this->position += strlen($data);
        return strlen($data);
    }

    function stream_tell()
    {
        return $this->position;
    }

    function stream_eof()
    {
        return $this->position >= strlen($GLOBALS[$this->varname]);
    }

    function stream_seek($offset, $whence)
    {
        switch ($whence) {
            case SEEK_SET:
                if ($offset < strlen($GLOBALS[$this->varname]) && $offset >= 0) {
                     $this->position = $offset;
                     return true;
                } else {
                     return false;
                }
                break;

            case SEEK_CUR:
                if ($offset >= 0) {
                     $this->position += $offset;
                     return true;
                } else {
                     return false;
                }
                break;

            case SEEK_END:
                if (strlen($GLOBALS[$this->varname]) + $offset >= 0) {
                     $this->position = strlen($GLOBALS[$this->varname]) + $offset;
                     return true;
                } else {
                     return false;
                }
                break;

            default:
                return false;
        }
    }

    function stream_metadata($path, $option, $var) 
    {
        if($option == STREAM_META_TOUCH) {
            $url = parse_url($path);
            $varname = $url["host"];
            if(!isset($GLOBALS[$varname])) {
                $GLOBALS[$varname] = '';
            }
            return true;
        }
        return false;
    }
}

stream_wrapper_register("var", "VariableStream")
    or die("Failed to register protocol");

$myvar = "";

$fp = fopen("var://myvar", "r+");

fwrite($fp, "line1\n");
fwrite($fp, "line2\n");
fwrite($fp, "line3\n");

rewind($fp);
while (!feof($fp)) {
    echo fgets($fp);
}
fclose($fp);
var_dump($myvar);

?>
```

以上例程会输出：

    line1
    line2
    line3
    string(18) "line1
    line2
    line3
    "
