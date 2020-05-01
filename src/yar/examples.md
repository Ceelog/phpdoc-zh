范例
====

**示例 \#1 Yar Server示例**

``` php
<?php

/* 假设这个页面的访问路径是: http://example.com/operator.php */

class Operator {

    /**
     * Add two operands
     * @param interge 
     * @return interge
     */
    public function add($a, $b) {
        return $this->_add($a, $b);
    }

    /**
     * Sub 
     */
    public function sub($a, $b) {
        return $a - $b;
    }

    /**
     * Mul
     */
    public function mul($a, $b) {
        return $a * $b;
    }

    /**
     * Protected methods will not be exposed
     * @param interge 
     * @return interge
     */
    protected function _add($a, $b) {
        return $a + $b;
    }
}

$server = new Yar_Server(new Operator());
$server->handle();
?>
```

**示例 \#2 通过浏览器访问(GET请求)**

以上例程的输出类似于：

<img src="images/4fd86c7f1b197d1d954ad0f4b033dc93-yar.png" width="700" alt="Yar Server Info" />

**示例 \#3 Yar Client示例**

``` php
<?php
$client = new yar_client("http://example.com/operator.php");

/* call directly */
var_dump($client->add(1, 2));

/* call via call */
var_dump($client->call("add", array(3, 2)));


/* __add can not be called */
var_dump($client->_add(1, 2));
?>
```

以上例程的输出类似于：

    int(3)
    int(5)
    PHP Fatal error:  Uncaught exception 'Yar_Server_Exception' with message 'call to api Operator::_add() failed' in *

**示例 \#4 Yar Concurrent Client示例**

``` php
<?php
function callback($ret, $callinfo) {
    echo $callinfo['method'] , " result: ", $ret , "\n";
}

/* 注册一个异步调用 */
Yar_Concurrent_Client::call("http://example.com/operator.php", "add", array(1, 2), "callback");
Yar_Concurrent_Client::call("http://example.com/operator.php", "sub", array(2, 1), "callback");
Yar_Concurrent_Client::call("http://example.com/operator.php", "mul", array(2, 2), "callback");

/* 发送所有注册的调用, 等待返回, 返回后Yar会调用callback回掉函数 */
Yar_Concurrent_Client::loop();
?>
```

以上例程的输出类似于：

    mul result: 4
    sub result: 1
    add result: 3
