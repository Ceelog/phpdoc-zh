范例
====

**目录**

-   [基本用法](/ftp/examples.html#基本用法)

基本用法
--------

**示例 \#1 FTP 例程**

``` php
<?php
// 建立基础连接
$conn_id = ftp_connect($ftp_server); 

// 使用用户名和口令登录
$login_result = ftp_login($conn_id, $ftp_user_name, $ftp_user_pass); 

// 检查是否成功
if ((!$conn_id) || (!$login_result)) { 
    echo "FTP connection has failed!";
    echo "Attempted to connect to $ftp_server for user $ftp_user_name"; 
    exit; 
} else {
    echo "Connected to $ftp_server, for user $ftp_user_name";
}

// 上传文件
$upload = ftp_put($conn_id, $destination_file, $source_file, FTP_BINARY); 

// 检查上传结果
if (!$upload) { 
    echo "FTP upload has failed!";
} else {
    echo "Uploaded $source_file to $ftp_server as $destination_file";
}

// 关闭 FTP 流
ftp_close($conn_id); 
?>
```
