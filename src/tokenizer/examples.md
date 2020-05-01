范例
====

这里是一个简单使用 tokenizer
的PHP脚本例子，它将读取一个PHP文件，去掉代码中全部注释，然后只打印纯代码

**示例 \#1 Strip comments with the tokenizer**

``` php
<?php
/*
* T_ML_COMMENT does not exist in PHP 5.
* The following three lines define it in order to
* preserve backwards compatibility.
*
* The next two lines define the PHP 5 only T_DOC_COMMENT,
* which we will mask as T_ML_COMMENT for PHP 4.
*/
if (!defined('T_ML_COMMENT')) {
   define('T_ML_COMMENT', T_COMMENT);
} else {
   define('T_DOC_COMMENT', T_ML_COMMENT);
}

$source = file_get_contents('example.php');
$tokens = token_get_all($source);

foreach ($tokens as $token) {
   if (is_string($token)) {
       // simple 1-character token
       echo $token;
   } else {
       // token array
       list($id, $text) = $token;

       switch ($id) { 
           case T_COMMENT: 
           case T_ML_COMMENT: // we've defined this
           case T_DOC_COMMENT: // and this
               // no action on comments
               break;

           default:
               // anything else -> output "as is"
               echo $text;
               break;
       }
   }
}
?>
```
