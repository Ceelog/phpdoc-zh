fann\_cascadetrain\_on\_data
============================

在整个数据集上训练，使用一段时间的 Cascade2 训练算法。

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_cascadetrain\_on\_data</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$data`</span> , <span class="methodparam"><span class="type">int</span>
`$max_neurons`</span> , <span class="methodparam"><span
class="type">int</span> `$neurons_between_reports`</span> , <span
class="methodparam"><span class="type">float</span>
`$desired_error`</span> )

级联输出改变小数是一个0到1之间的数字，表示在输出连接的训练中，为了使训练不停滞的情况下，经过
<span
class="function">fann\_get\_cascade\_output\_stagnation\_epochs</span>
次迭代的后，<span class="function">fann\_get\_MSE</span>
将会改变多大。如果训练停滞了，训练的输出连接将会结束，新的候选神经元将会准备好。

该训练使用由 fann\_set\_cascade\_
前缀设置的参数，但它也采用了另一种训练算法，即内部训练算法。该训练算法要么是
<span class="function">fann\_set\_training\_algorithm</span> 设置的
**`FANN_TRAIN_RPROP`** 算法，要么是
**`FANN_TRAIN_QUICKPROP`**，这些算法设置的参数同样也会影响到级联训练。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`data`  
神经网络训练数据 <span class="type">资源</span>。

`max_neurons`  
被添加入神经网络中最大的神经元数。

`neurons_between_reports`  
打印状态报告之间的神经元数。0表示没有报告会被打印。

`desired_error`  
预期的 <span class="function">fann\_get\_MSE</span> 或 <span
class="function">fann\_get\_bit\_fail</span>, 取决于 <span
class="function">fann\_set\_train\_stop\_function</span> 选择的停止函数

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_train\_on\_data</span>
-   <span class="function">fann\_cascadetrain\_on\_file</span>

fann\_cascadetrain\_on\_file
============================

读取文件并在整个数据集上训练，使用 Cascade2 训练算法训练一段时间。

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_cascadetrain\_on\_file</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">string</span>
`$filename`</span> , <span class="methodparam"><span
class="type">int</span> `$max_neurons`</span> , <span
class="methodparam"><span class="type">int</span>
`$neurons_between_reports`</span> , <span class="methodparam"><span
class="type">float</span> `$desired_error`</span> )

和 <span class="function">fann\_cascadetrain\_on\_data</span>
函数做一样的工作，但是该函数是直接从文件读取训练数据的。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`filename`  
添加在神经网络中神经元的最大数量。

`max_neurons`  
在打印状态报告到标准输出之间的神经元数量。0值表示没有报告打印。

`neurons_between_reports`  
打印状态报告之间的神经元数量。0值表示没有报告打印。

`desired_error`  
期望的 <span class="function">fann\_get\_MSE</span> 值或者 <span
class="function">fann\_get\_bit\_fail</span> 值， 取决于 <span
class="function">fann\_set\_train\_stop\_function</span>
函数选择的停止函数。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_train\_on\_data</span>
-   <span class="function">fann\_cascadetrain\_on\_data</span>

fann\_clear\_scaling\_params
============================

清除缩放参数

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_clear\_scaling\_params</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

清除缩放参数

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

fann\_copy
==========

创建一个 fann 结构体的副本。

### 说明

<span class="type">resource</span> <span
class="methodname">fann\_copy</span> ( <span class="methodparam"><span
class="type">resource</span> `$ann`</span> )

创建一个 fann 结构体的副本。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，返回神经网络资源的副本，失败则返回**`false`**

### 参见

-   <span class="function">fann\_test</span>

fann\_create\_from\_file
========================

从配置文件中构建一个反向传播神经网络。

### 说明

<span class="type">resource</span> <span
class="methodname">fann\_create\_from\_file</span> ( <span
class="methodparam"><span class="type">string</span>
`$configuration_file`</span> )

从一个由 <span class="function">fann\_save</span>
函数保存的配置文件中构建一个反向传播神经网络。

### 参数

`configuration_file`  
配置文件的路径。

### 返回值

成功时返回神经网络 <span class="type">资源</span>，发生错误返回
**`false`**。

### 参见

-   <span class="function">fann\_save</span>

fann\_create\_shortcut\_array
=============================

创建一个含快捷连接而非全连接的标准反向传播神经网络。

### 说明

<span class="type">resource</span> <span
class="methodname">fann\_create\_shortcut\_array</span> ( <span
class="methodparam"><span class="type">int</span> `$num_layers`</span> ,
<span class="methodparam"><span class="type">array</span>
`$layers`</span> )

使用包含各层大小的数组创建一个含快捷连接而非全连接的标准反向传播神经网络。

### 参数

`num_layers`  
网络层数的总数，包含输入输出层。

`layers`  
一个包含各层大小的数组。

### 返回值

成功，返回一个神经网络的资源，错误则返回 **`false`**

### 参见

-   <span class="function">fann\_create\_shortcut</span>
-   <span class="function">fann\_create\_sparse</span>
-   <span class="function">fann\_create\_standard</span>

fann\_create\_shortcut
======================

创建一个含快捷连接而非全连接的标准反向传播神经网络。

### 说明

<span class="type">reference</span> <span
class="methodname">fann\_create\_shortcut</span> ( <span
class="methodparam"><span class="type">int</span> `$num_layers`</span> ,
<span class="methodparam"><span class="type">int</span>
`$num_neurons1`</span> , <span class="methodparam"><span
class="type">int</span> `$num_neurons2`</span> \[, <span
class="methodparam"><span class="type">int</span> `$...`</span> \] )

创建一个含快捷连接而非全连接标准反向传播神经网络。

快捷连接是可以跳过网络层次的连接。一个包含快捷连接的全连接网络，表示在之后的网络层里所有的神经元都是互相连接的。包括输出层直接连接到输出层的连接。

### 参数

`num_layers`  
包括输入输出层在内的网络层的层数。。

`num_neurons1`  
第一层神经元的数量。

`num_neurons2`  
第二层神经元的数量。

`...`  
其它层神经元的数量。

### 返回值

成功，返回神经网络的资源，错误则返回 **`false`** .

### 参见

-   <span class="function">fann\_create\_shortcut\_array</span>
-   <span class="function">fann\_create\_sparse</span>
-   <span class="function">fann\_create\_standard</span>

fann\_create\_sparse\_array
===========================

创建一个标准的反向传播神经网络，该网络使用一个表示每层大小的数组来构造，但是并不是全连接的。

### 说明

<span class="type">ReturnType</span> <span
class="methodname">fann\_create\_sparse\_array</span> ( <span
class="methodparam"><span class="type">float</span>
`$connection_rate`</span> , <span class="methodparam"><span
class="type">int</span> `$num_layers`</span> , <span
class="methodparam"><span class="type">array</span> `$layers`</span> )

创建一个标准的反向传播神经网络，该网络使用一个表示每层大小的数组来构造，但是并不是全连接的。

### 参数

`connection_rate`  
连接率控制着在网络中将会有多少连接，如果连接率设置为1，那么这个网络就是全连接网络，但是如果设置为0.5将会设置一半的连接。连接率为1的结果和使用<span
class="function">fann\_create\_standard</span>函数的效果是一样的。

`num_layers`  
神经网络层数，包括输入输出层。

`layers`  
表示每层大小的数组。

### 返回值

成功，返回神经网络的资源，错误则返回 **`false`** .

### 参见

-   <span class="function">fann\_create\_sparse</span>
-   <span class="function">fann\_create\_standard</span>
-   <span class="function">fann\_create\_shortcut</span>

fann\_create\_sparse
====================

创建一个标准的反向传播神经网络，该网络不是全连接。

### 说明

<span class="type">ReturnType</span> <span
class="methodname">fann\_create\_sparse</span> ( <span
class="methodparam"><span class="type">float</span>
`$connection_rate`</span> , <span class="methodparam"><span
class="type">int</span> `$num_layers`</span> , <span
class="methodparam"><span class="type">int</span> `$num_neurons1`</span>
, <span class="methodparam"><span class="type">int</span>
`$num_neurons2`</span> \[, <span class="methodparam"><span
class="type">int</span> `$...`</span> \] )

创建一个标准的反向传播神经网络，该网络不是全连接。

### 参数

`connection_rate`  
连接率控制着在网络中将会有多少连接，如果连接率设置为1，那么这个网络就是全连接网络，但是如果设置为
0.5 将会设置一半的连接。连接率为1的结果和使用 <span
class="function">fann\_create\_standard</span>函数的效果是一样的。

`num_layers`  
神经网络层数，包括输入输出层。

`num_neurons1`  
第一层网络的神经数。

`num_neurons2`  
第二层网络的神经数。

`...`  
其它层网络的神经数。

### 返回值

返回一个神经网络资源，错误则返回 **`false`** .

### 参见

-   <span class="function">fann\_create\_sparse\_array</span>
-   <span class="function">fann\_create\_standard</span>
-   <span class="function">fann\_create\_shortcut</span>

fann\_create\_standard\_array
=============================

创建一个全连接的反向传播神经网络，该网络使用一个表示每层大小的数组来构造。

### 说明

<span class="type">resource</span> <span
class="methodname">fann\_create\_standard\_array</span> ( <span
class="methodparam"><span class="type">int</span> `$num_layers`</span> ,
<span class="methodparam"><span class="type">array</span>
`$layers`</span> )

创建一个标准的全连接反向传播神经网络。

每一层都将会有一个偏置神经元
(除了输出层),该偏置神经元将会连接下一层所有的神经元。当运行网络时，偏置神经节点一直发出1信号。

请使用 <span class="function">fann\_destroy</span> 函数来销毁神经网络。

### 参数

`num_layers`  
神经网络层数，包括输入输出层。

`layers`  
表示每层大小的数组。

### 返回值

成功则返回神经网络，错误则返回 **`false`** .

### 参见

-   <span class="function">fann\_create\_standard</span>
-   <span class="function">fann\_create\_sparse</span>
-   <span class="function">fann\_create\_shortcut</span>

fann\_create\_standard
======================

创建标准的全连接反向传播神经网络。

### 说明

<span class="type">resource</span> <span
class="methodname">fann\_create\_standard</span> ( <span
class="methodparam"><span class="type">int</span> `$num_layers`</span> ,
<span class="methodparam"><span class="type">int</span>
`$num_neurons1`</span> , <span class="methodparam"><span
class="type">int</span> `$num_neurons2`</span> \[, <span
class="methodparam"><span class="type">int</span> `$...`</span> \] )

创建一个标准的全连接反向传播神经网络。

每一层都将会有一个偏置神经元 (除了输出层),
该偏置神经元将会连接下一层所有的神经元。当运行网络时，偏置神经节点一直发出1信号。

请使用 <span class="function">fann\_destroy</span> 函数来销毁神经网络。

### 参数

`num_layers`  
神经网络层数，包括输入输出层。

`num_neurons1`  
第一层神经元的数量。

`num_neurons2`  
第二层神经元的数量。

`...`  
其他层的神经数量。

### 返回值

成功，返回神经网络的资源，失败则返回 **`false`** .

### 参见

-   <span class="function">fann\_create\_standard\_array</span>
-   <span class="function">fann\_create\_sparse</span>
-   <span class="function">fann\_create\_shortcut</span>

fann\_create\_train\_from\_callback
===================================

从用户提供的函数创建训练数据结构。

### 说明

<span class="type">resource</span> <span
class="methodname">fann\_create\_train\_from\_callback</span> ( <span
class="methodparam"><span class="type">int</span> `$num_data`</span> ,
<span class="methodparam"><span class="type">int</span>
`$num_input`</span> , <span class="methodparam"><span
class="type">int</span> `$num_output`</span> , <span
class="methodparam"><span class="type">callable</span>
`$user_function`</span> )

从用户提供的函数创建训练数据结构。当训练数据可数，用户需要构造一个用来接收训练数据集(包括输入，输出)数量和返回值为集合的函数。

### 参数

`num_data`  
训练数据的数量。

`num_input`  
每个训练数据的输入数。

`num_output`  
每个训练数据的输出数。

`user_function`  
用户提供的函数包含以下参数：

-   *num* - 训练数据集的数量。
-   *num\_input* - 数量数据的输入数。
-   *num\_output* - 数量数据的输出数。

函数应该返回一个包含*input* 和 *output*
键的数组，并且这两个键的值分别表示输入输出的值(皆为数组)。

### 返回值

成功时返回训练数据 <span class="type">资源</span>，发生错误返回
**`false`**。

### 范例

**示例 \#1 <span
class="methodname">fann\_create\_train\_from\_callback</span> example**

``` php
<?php
function create_train_callback($num_data, $num_input, $num_output) {
    return array(
        "input" => array_fill(0, $num_input, 1),
        "output" => array_fill(0, $num_output, 1),
    );
}

$num_data = 3;
$num_input = 2;
$num_output = 1;
$train_data = fann_create_train_from_callback($num_data, $num_input, $num_output, "create_train_callback");
if ($train_data) {
    // Do something with $train_data
}
?>
```

### 参见

-   <span class="function">fann\_read\_train\_from\_file</span>
-   <span class="function">fann\_train\_on\_data</span>
-   <span class="function">fann\_destroy\_train</span>
-   <span class="function">fann\_save\_train</span>

fann\_create\_train
===================

创建一个空的训练数据结构。

### 说明

<span class="type">resource</span> <span
class="methodname">fann\_create\_train</span> ( <span
class="methodparam"><span class="type">int</span> `$num_data`</span> ,
<span class="methodparam"><span class="type">int</span>
`$num_input`</span> , <span class="methodparam"><span
class="type">int</span> `$num_output`</span> )

创建一个空的训练数据结构。

### 参数

`num_data`  
训练数据的数量。

`num_input`  
每个训练数据集输入的数量。

`num_output`  
每个训练数据集输出的数量。

### 返回值

成功时返回训练数据 <span class="type">资源</span>，发生错误返回
**`false`**。

### 参见

-   <span class="function">fann\_read\_train\_from\_file</span>
-   <span class="function">fann\_train\_on\_data</span>
-   <span class="function">fann\_destroy\_train</span>
-   <span class="function">fann\_save\_train</span>

fann\_descale\_input
====================

在获取基于先前计算的参数之后，在输入向量中缩小数据

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_descale\_input</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">array</span>
`$input_vector`</span> )

在获取基于先前计算的参数之后，在输入向量中缩小数据。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`input_vector`  
将要被缩小的输入向量

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_scale\_input</span>
-   <span class="function">fann\_descale\_output</span>

fann\_descale\_output
=====================

在获取基于先前计算的参数之后，在输出向量中缩小数据

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_descale\_output</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">array</span>
`$output_vector`</span> )

在获取基于先前计算的参数之后，在输出向量中缩小数据。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`output_vector`  
将被缩小的输出向量。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_scale\_output</span>
-   <span class="function">fann\_descale\_input</span>

fann\_descale\_train
====================

基于先前计算的参数来缩小输入和输出数据

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_descale\_train</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$train_data`</span> )

基于先前计算的参数来缩小输入和输出数据。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`train_data`  
神经网络训练数据 <span class="type">资源</span>。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_scale\_train</span>
-   <span class="function">fann\_set\_scaling\_params</span>

fann\_destroy\_train
====================

销毁训练数据。

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_destroy\_train</span> ( <span
class="methodparam"><span class="type">resource</span>
`$train_data`</span> )

销毁训练数据。

### 参数

`train_data`  
神经网络训练数据 <span class="type">资源</span>。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

fann\_destroy
=============

销毁整个网络并且适当地释放所有的关联内存。

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_destroy</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

销毁整个网络并且适当地释放所有的关联内存。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

fann\_duplicate\_train\_data
============================

返回 fann 训练数据精确的副本。

### 说明

<span class="type">resource</span> <span
class="methodname">fann\_duplicate\_train\_data</span> ( <span
class="methodparam"><span class="type">resource</span> `$data`</span> )

返回 fann 训练数据精确的副本 <span class="type">resource</span>。

### 参数

`data`  
神经网络训练数据 <span class="type">资源</span>。

### 返回值

成功时返回训练数据 <span class="type">资源</span>，发生错误返回
**`false`**。

fann\_get\_activation\_function
===============================

返回激励函数

### 说明

<span class="type">int</span> <span
class="methodname">fann\_get\_activation\_function</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">int</span> `$layer`</span>
, <span class="methodparam"><span class="type">int</span>
`$neuron`</span> )

获取在层数为 *layer* 的网络中神经元数为 *neuron*的激励函数，输入层被计为
0.

在输入层是不能获取神经元激励函数的。

返回值将会是<a href="/fann/constants.html#Activation%20functions" class="link">激励函数</a>
常量之一。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`layer`  
层数。

`neuron`  
神经元数

### 返回值

<a href="/fann/constants.html#训练算法" class="link">学习函数</a>
常量或者如果神经未在神经网络中定义返回 -1， 错误则返回 **`false`** .

### 参见

-   <span class="function">fann\_set\_activation\_function\_layer</span>
-   <span
    class="function">fann\_set\_activation\_function\_hidden</span>
-   <span
    class="function">fann\_set\_activation\_function\_output</span>
-   <span class="function">fann\_set\_activation\_steepness</span>
-   <span class="function">fann\_set\_activation\_function</span>

fann\_get\_activation\_steepness
================================

为提供的神经和网络层数返回激活陡度

### 说明

<span class="type">float</span> <span
class="methodname">fann\_get\_activation\_steepness</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">int</span> `$layer`</span>
, <span class="methodparam"><span class="type">int</span>
`$neuron`</span> )

获取神经元数为 *neuron* 层数为
*layer*神经网络的激活陡度，将输入层数计为1层。

在输入层中是不可能获取激活陡度。

激活函数的陡度表明了激活函数从最小到最大有多块。一个高值表明将会提供一个更高效的训练。

在训练神经网络时，输出值应该处于极端(通常是 0 和
1，取决于激励函数)，一般陡峭的激活函数将会被使用(比如为1.0时)。

默认的激活陡度是0.5.

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`layer`  
层数

`neuron`  
神经元数

### 返回值

激活陡度，当神经元在神经网络中没定义时为-1，错误时返回 **`false`** .

### 参见

-   <span class="function">fann\_set\_activation\_function</span>
-   <span
    class="function">fann\_set\_activation\_steepness\_layer</span>
-   <span
    class="function">fann\_set\_activation\_steepness\_hidden</span>
-   <span
    class="function">fann\_set\_activation\_steepness\_output</span>
-   <span class="function">fann\_set\_activation\_steepness</span>

fann\_get\_bias\_array
======================

获取网络中每一层的偏差数

### 说明

<span class="type">array</span> <span
class="methodname">fann\_get\_bias\_array</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

获取网络中每一层的偏差数。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

包含每一层偏差数的数组。

fann\_get\_bit\_fail\_limit
===========================

返回训练期间使用的误差限制

### 说明

<span class="type">float</span> <span
class="methodname">fann\_get\_bit\_fail\_limit</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

返回训练期间使用的误差限制。

训练期间使用的误差限制，在
<a href="/fann/constants.html#Stop%20criteria%20used%20during%20training" class="link">停止函数</a>
中设置的 **`FANN_STOPFUNC_BIT`**.

限度是训练过程中期望输出和实际输出之间的最大可接受差值。每个输出偏离超过这个限度将会被算作误差。不同的是在使用对称激活函数的时候这个值要除以2，因此对称或者不对称可以使用同样的限度。

默认的误差限度是 0.35.

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，返回误差限度，错误则返回 **`false`** .

### 参见

-   <span class="function">fann\_set\_bit\_fail\_limit</span>

fann\_get\_bit\_fail
====================

失败位的数量

### 说明

<span class="type">int</span> <span
class="methodname">fann\_get\_bit\_fail</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

失败位的数量：意味着输出神经元的数量多于失败位的限度 (参见 <span
class="function">fann\_get\_bit\_fail\_limit</span>, <span
class="function">fann\_set\_bit\_fail\_limit</span>).
位数将会在所有的训练数据中被计数，因此这个数字将会比训练数据的数量高一点。

该值可以被 <span class="function">fann\_reset\_MSE</span>
函数重置，并且可以被能够更新MSE值的函数更新。(比如 <span
class="function">fann\_test\_data</span>, <span
class="function">fann\_train\_epoch</span>)

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功 ，返回失败位的数量，错误则返回 **`false`** .

### 参见

-   <span class="function">fann\_get\_MSE</span>
-   <span class="function">fann\_reset\_MSE</span>
-   <span class="function">fann\_test\_data</span>
-   <span class="function">fann\_train\_epoch</span>
-   <span class="function">fann\_get\_bit\_fail\_limit</span>
-   <span class="function">fann\_set\_bit\_fail\_limit</span>

fann\_get\_cascade\_activation\_functions\_count
================================================

返回级联激活函数的数量

### 说明

<span class="type">int</span> <span
class="methodname">fann\_get\_cascade\_activation\_functions\_count</span>
( <span class="methodparam"><span class="type">resource</span>
`$ann`</span> )

在 <span
class="function">fann\_get\_cascade\_activation\_functions</span>
函数数组的激活函数的数量。

默认激活函数的数量为6.

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，返回级联激活函数的数量，错误则返回**`false`** .

### 参见

-   <span
    class="function">fann\_get\_cascade\_activation\_functions</span>
-   <span
    class="function">fann\_set\_cascade\_activation\_functions</span>

fann\_get\_cascade\_activation\_functions
=========================================

返回级联激活函数

### 说明

<span class="type">array</span> <span
class="methodname">fann\_get\_cascade\_activation\_functions</span> (
<span class="methodparam"><span class="type">resource</span>
`$ann`</span> )

层级激活函数数组是一个和被候选使用的不同的数组。

参见 <span class="function">fann\_get\_cascade\_num\_candidates</span>
的描述，这个数组将会生成候选神经元。

默认的激活函数是 **`FANN_SIGMOID`**, **`FANN_SIGMOID_SYMMETRIC`**,
**`FANN_GAUSSIAN`**, **`FANN_GAUSSIAN_SYMMETRIC`**, **`FANN_ELLIOT`**,
**`FANN_ELLIOT_SYMMETRIC`**.

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，返回层级激活函数数组，错误则返回 **`false`** .

### 参见

-   <span
    class="function">fann\_get\_cascade\_activation\_functions\_count</span>
-   <span
    class="function">fann\_set\_cascade\_activation\_functions</span>

fann\_get\_cascade\_activation\_steepnesses\_count
==================================================

激活陡度的数量

### 说明

<span class="type">int</span> <span
class="methodname">fann\_get\_cascade\_activation\_steepnesses\_count</span>
( <span class="methodparam"><span class="type">resource</span>
`$ann`</span> )

<span class="function">fann\_get\_cascade\_activation\_functions</span>
数组中激活陡度的数量。

默认的激活陡度的数量是 4.

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功返回激活陡度数量，错误，则返回**`false`** .

### 参见

-   <span
    class="function">fann\_get\_cascade\_activation\_steepnesses</span>
-   <span
    class="function">fann\_set\_cascade\_activation\_functions</span>

fann\_get\_cascade\_activation\_steepnesses
===========================================

返回级联激活陡度

### 说明

<span class="type">array</span> <span
class="methodname">fann\_get\_cascade\_activation\_steepnesses</span> (
<span class="methodparam"><span class="type">resource</span>
`$ann`</span> )

层级激活函数数组是一个和被候选使用的不同的数组。

参见 <span class="function">fann\_get\_cascade\_num\_candidates</span>
的描述，这个数组将会生成候选神经元。

默认的激活陡度是{0.25, 0.50, 0.75, 1.00}.

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，返回级联激活陡度，错误则返回 **`false`**.

### 参见

-   <span
    class="function">fann\_get\_cascade\_activation\_steepnesses\_count</span>
-   <span
    class="function">fann\_set\_cascade\_activation\_steepnesses</span>

fann\_get\_cascade\_candidate\_change\_fraction
===============================================

返回级联候选变化分数

### 说明

<span class="type">float</span> <span
class="methodname">fann\_get\_cascade\_candidate\_change\_fraction</span>
( <span class="methodparam"><span class="type">resource</span>
`$ann`</span> )

返回级联候选变化分数是一个介于0到1之间的数字。该数字决定了在训练候选神经元使用
<span
class="function">fann\_get\_cascade\_candidate\_stagnation\_epochs</span>
函数时 <span class="function">fann\_get\_MSE</span>
将会改变多大的分数,是为了不让这个训练停止。如果训练停止，候选神经元的训练将会被终止并且会选出最好的候选。

这意味在<span
class="function">fann\_get\_cascade\_candidate\_stagnation\_epochs</span>期间如果
MSE 被<span
class="function">fann\_get\_cascade\_candidate\_change\_fraction</span>的分数更改，候选神经元的训练会因为训练的停滞而被停止。

如果级联候选变化分数很低，这个候选神经元将训练越多，如果这个分数很高则训练的越少。

默认的级联候选变化分数是 0.01, 等于 MSE 中1%的变化值。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，则返回级联候选变化分数，错误则返回 **`false`** .

### 参见

-   <span
    class="function">fann\_set\_cascade\_candidate\_change\_fraction</span>
-   <span class="function">fann\_get\_MSE</span>
-   <span
    class="function">fann\_get\_cascade\_candidate\_stagnation\_epochs</span>

fann\_get\_cascade\_candidate\_limit
====================================

返回候选限度

### 说明

<span class="type">float</span> <span
class="methodname">fann\_get\_cascade\_candidate\_limit</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

候选限度表明将会有多少候选神经元被训练。该限度是 MSE
和候选分数之间的比例限度。

将此值设置为低值以避免过于拟合，如果过度拟合并不是问题，则将其设置为更高的值。

默认的候选限度是 1000.0.

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，返回候选限度，错误则返回 **`false`** .

### 参见

-   <span class="function">fann\_set\_cascade\_candidate\_limit</span>

fann\_get\_cascade\_candidate\_stagnation\_epochs
=================================================

返回层叠候选停滞周期的数量

### 说明

<span class="type">float</span> <span
class="methodname">fann\_get\_cascade\_candidate\_stagnation\_epochs</span>
( <span class="methodparam"><span class="type">resource</span>
`$ann`</span> )

层叠候选停滞周期的数量决定了在 <span
class="function">fann\_get\_cascade\_candidate\_change\_fraction</span>
不改变MSE分数的情况下继续进行的epochs训练的数量。

更多信息参见 <span
class="function">fann\_get\_cascade\_candidate\_change\_fraction</span>.

层叠候选停滞周期的数量是 12.

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，返回层叠候选停滞周期的数量，错误则返回 **`false`**.

### 参见

-   <span
    class="function">fann\_set\_cascade\_candidate\_stagnation\_epochs</span>
-   <span
    class="function">fann\_get\_cascade\_candidate\_change\_fraction</span>

fann\_get\_cascade\_max\_cand\_epochs
=====================================

返回候选周期的最大值

### 说明

<span class="type">int</span> <span
class="methodname">fann\_get\_cascade\_max\_cand\_epochs</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

候选周期的最大值决定了在添加新的候选神经元之前，候选输入连接周期的最大值。

默认的最大候选周期是 150.

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，返回最大的候选周期，错误则返回**`false`** .

### 参见

-   <span class="function">fann\_set\_cascade\_max\_cand\_epochs</span>

fann\_get\_cascade\_max\_out\_epochs
====================================

返回输出周期的最大值

### 说明

<span class="type">int</span> <span
class="methodname">fann\_get\_cascade\_max\_out\_epochs</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

输出周期的最大值决定了在添加新的候选神经元之后，输出连接周期的最大值。

默认输出周期的最大值是 150.

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，则返回输出周期的最大值，错误则返回 **`false`** .

### 参见

-   <span class="function">fann\_set\_cascade\_max\_out\_epochs</span>

fann\_get\_cascade\_min\_cand\_epochs
=====================================

返回最小的候选周期

### 说明

<span class="type">int</span> <span
class="methodname">fann\_get\_cascade\_min\_cand\_epochs</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

最小候选周期表示在添加新的候选神经元之前，输入连接到被训练的候选神经元最小的周期数。

默认的最小候选周期是50.

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，返回最小候选周期，错误则返回 **`false`** .

### 参见

-   <span class="function">fann\_set\_cascade\_min\_cand\_epochs</span>

fann\_get\_cascade\_min\_out\_epochs
====================================

返回最小输出周期

### 说明

<span class="type">int</span> <span
class="methodname">fann\_get\_cascade\_min\_out\_epochs</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

最小输出周期表明在加入新的候选神经元后输出连接必须训练的最小周期。

默认的最小输出周期是50。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，返回最小的输出周期，错误则返回 **`false`** .

### 参见

-   <span class="function">fann\_set\_cascade\_min\_out\_epochs</span>

fann\_get\_cascade\_num\_candidate\_groups
==========================================

返回候选组的数量

### 说明

<span class="type">int</span> <span
class="methodname">fann\_get\_cascade\_num\_candidate\_groups</span> (
<span class="methodparam"><span class="type">resource</span>
`$ann`</span> )

候选组的数目是在训练期间使用的相同候选组的个数。

这个数字可以用来有更多的候选，而不必为候选定义新的参数。

参见 <span class="function">fann\_get\_cascade\_num\_candidates</span>
的描述。其中解释了这个参数将会生哪个成候选神经元。

默认的候选组数为2.

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，返回候选组数量，错误则返回 **`false`** .

### 参见

-   <span
    class="function">fann\_set\_cascade\_num\_candidate\_groups</span>

fann\_get\_cascade\_num\_candidates
===================================

返回训练期间使用的候选数量

### 说明

<span class="type">int</span> <span
class="methodname">fann\_get\_cascade\_num\_candidates</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

返回训练期间使用的候选数量 ( <span
class="function">fann\_get\_cascade\_activation\_functions\_count</span>,
<span
class="function">fann\_get\_cascade\_activation\_steepnesses\_count</span>
和 <span
class="function">fann\_get\_cascade\_num\_candidate\_groups</span>)的和。

实际的候选数是由 <span
class="function">fann\_get\_cascade\_activation\_functions</span> 和
<span
class="function">fann\_get\_cascade\_activation\_steepnesses</span>
数组定义的。
这些数组定义的激活功能和激活的陡度用于候选神经元。如果在激活函数数组中有两个激活函数并且陡度数组中有三个陡度，则将会有2x3=6个不同的候选神经元被训练。
这6个不同的候选神经元将会被复制到几个候选组中，这些候选组不同之处在于他们的初始权重。如果组的数量设为2，则候选神经元的数量为2x3x2=12.候选组的数量是有
<span class="function">fann\_set\_cascade\_num\_candidate\_groups</span>
函数定义的。

默认的候选神经元数量为 6x4x2 = 48

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，返回训练期间候选神经元的数量，错误则返回 **`false`** .

### 参见

-   <span
    class="function">fann\_get\_cascade\_activation\_functions</span>
-   <span
    class="function">fann\_get\_cascade\_activation\_functions\_count</span>
-   <span
    class="function">fann\_get\_cascade\_activation\_steepnesses</span>
-   <span
    class="function">fann\_get\_cascade\_activation\_steepnesses\_count</span>
-   <span
    class="function">fann\_get\_cascade\_num\_candidate\_groups</span>

fann\_get\_cascade\_output\_change\_fraction
============================================

返回级联输出变化分数

### 说明

<span class="type">float</span> <span
class="methodname">fann\_get\_cascade\_output\_change\_fraction</span> (
<span class="methodparam"><span class="type">resource</span>
`$ann`</span> )

级联输出变化分数是一个介于0到1之间的数字，决定了在<span
class="function">fann\_get\_cascade\_output\_stagnation\_epochs</span>的输出连接训练中，<span
class="function">fann\_get\_MSE</span>的值将改变多大才能保持训练不至于停滞。如果训练停滞了，
If the training stagnates, 输出连接的训练将结束，新的候选神经元将准备。

这就意味着如果在<span
class="function">fann\_get\_cascade\_output\_stagnation\_epochs</span>期间，
MSE没有被 <span
class="function">fann\_get\_cascade\_output\_change\_fraction</span>
改变, 因为训练的停滞将导致输出连接将被停止。

如果级联输出改变分数很小，输出连接将会训练的更多，如果分数很大则会训练的更少。

默认的级联输出改变分数是0.01，和MSE中的1%相等。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，返回级联输出更改分数，错误则返回 **`false`** .

### 参见

-   <span
    class="function">fann\_set\_cascade\_output\_change\_fraction</span>
-   <span class="function">fann\_get\_MSE</span>
-   <span
    class="function">fann\_get\_cascade\_output\_stagnation\_epochs</span>

fann\_get\_cascade\_output\_stagnation\_epochs
==============================================

返回级联输出停滞周期的数量

### 说明

<span class="type">int</span> <span
class="methodname">fann\_get\_cascade\_output\_stagnation\_epochs</span>
( <span class="methodparam"><span class="type">resource</span>
`$ann`</span> )

级联输出停滞周期的数量表示在<span
class="function">fann\_get\_cascade\_output\_change\_fraction</span>不改变MSE的情况下，运行训练的周期数。

更多详情参见 <span
class="function">fann\_get\_cascade\_output\_change\_fraction</span>。

级联输出停滞周期的默认值是12。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，则返回级联输出停滞周期，错误则返回 **`false`** .

### 参见

-   <span
    class="function">fann\_set\_cascade\_output\_stagnation\_epochs</span>
-   <span
    class="function">fann\_get\_cascade\_output\_change\_fraction</span>

fann\_get\_cascade\_weight\_multiplier
======================================

返回权重因子

### 说明

<span class="type">float</span> <span
class="methodname">fann\_get\_cascade\_weight\_multiplier</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

权重因子是用于在添加神经元到神经网络之前，和候选神经元权重相乘的参数。该参数的值通常介于0到1之间，用来使训练变得不那么积极。

默认权重因子是 0.4.

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，返回权重因子，错误则返回 **`false`** .

### 参见

-   <span class="function">fann\_set\_cascade\_weight\_multiplier</span>

fann\_get\_connection\_array
============================

获取网络中的连接。

### 说明

<span class="type">array</span> <span
class="methodname">fann\_get\_connection\_array</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

获取网络中的连接。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

包含网络中所有连接的数组。

fann\_get\_connection\_rate
===========================

获取当网络创建时连接的使用率。

### 说明

<span class="type">float</span> <span
class="methodname">fann\_get\_connection\_rate</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

获取当网络创建时连接的使用率。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，则返回当网络创建时连接的使用率, 错误则返回 **`false`** .

fann\_get\_errno
================

返回最后一个错误数字。

### 说明

<span class="type">int</span> <span
class="methodname">fann\_get\_errno</span> ( <span
class="methodparam"><span class="type">resource</span> `$errdat`</span>
)

返回最后一个错误数字。

### 参数

`errdat`  
Either neural network <span class="type">resource</span> or neural
network trainining data <span class="type">resource</span>.

### 返回值

成功，返回错误数字，错误则返回 **`false`** .

### 参见

-   <span class="function">fann\_reset\_errno</span>
-   <span class="function">fann\_get\_errstr</span>

fann\_get\_errstr
=================

返回最后的错误字符串。

### 说明

<span class="type">string</span> <span
class="methodname">fann\_get\_errstr</span> ( <span
class="methodparam"><span class="type">resource</span> `$errdat`</span>
)

返回最后的错误字符串。

### 参数

`errdat`  
Either neural network <span class="type">resource</span> or neural
network trainining data <span class="type">resource</span>.

### 返回值

成功，返回最后的错误字符串,，失败则返回 **`false`** 。

### 参见

-   <span class="function">fann\_reset\_errstr</span>
-   <span class="function">fann\_get\_errno</span>

fann\_get\_layer\_array
=======================

获取网络中每层的神经元数量。

### 说明

<span class="type">array</span> <span
class="methodname">fann\_get\_layer\_array</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

获取网络中每层的神经元数量。

偏差神经元不包括在内，所以层数是和 fann\_create 函数组想匹配的。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

包含每层神经元数量的数组。

fann\_get\_learning\_momentum
=============================

返回学习动量

### 说明

<span class="type">float</span> <span
class="methodname">fann\_get\_learning\_momentum</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

学习动量可用来加速 **`FANN_TRAIN_INCREMENTAL`** 训练。
一个过高的学习动量不利于训练。
动量设为0效果和没设一样。该参数的值建议在0.0到1.0之间。

默认动量是 0.

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

正确，返回学习动量，错误则返回 **`false`** .

### 参见

-   <span class="function">fann\_set\_learning\_momentum</span>
-   <span class="function">fann\_set\_training\_algorithm</span>

fann\_get\_learning\_rate
=========================

返回学习速率

### 说明

<span class="type">float</span> <span
class="methodname">fann\_get\_learning\_rate</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

学习率用来确定训练算法(**`FANN_TRAIN_INCREMENTAL`**,
**`FANN_TRAIN_BATCH`**,
**`FANN_TRAIN_QUICKPROP`**)中应该如何进行积极的训练。
不过，请注意这个函数不能用于 **`FANN_TRAIN_RPROP`**中。

默认的学习速率是 0.7。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，返回学习速率，错误则返回 **`false`** .

### 参见

-   <span class="function">fann\_set\_learning\_rate</span>
-   <span class="function">fann\_set\_training\_algorithm</span>

fann\_get\_MSE
==============

从网络中读取均方误差。

### 说明

<span class="type">float</span> <span
class="methodname">fann\_get\_MSE</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

从网络中读取均方误差。

从网络中读取均方误差。该值是在训练或或测试中被计算的，因此如果权重在最后一次计算时已经改变，有时候会有点不太对劲。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，则返回均方误差, 错误则返回 **`false`** .

### 参见

-   <span class="function">fann\_test\_data</span>

fann\_get\_network\_type
========================

获取所创建的神经网络类型。

### 说明

<span class="type">int</span> <span
class="methodname">fann\_get\_network\_type</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

获取所创建的神经网络的类型。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，则返回<a href="/fann/constants.html#fann_get_network_type%20是用来定义网络类型" class="link">网络类型</a>
常量, 错误则返回 **`false`** .

fann\_get\_num\_input
=====================

获取输入神经元的数量。

### 说明

<span class="type">int</span> <span
class="methodname">fann\_get\_num\_input</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

获取输入神经元的数量。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，则返回输入神经元的数量, 错误则返回 **`false`**

fann\_get\_num\_layers
======================

获取神经网络的层数。

### 说明

<span class="type">int</span> <span
class="methodname">fann\_get\_num\_layers</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

获取神经网络的层数。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，则返回神经网络的层数，错误则返回 **`false`** .

fann\_get\_num\_output
======================

获取输出神经元的数量。

### 说明

<span class="type">int</span> <span
class="methodname">fann\_get\_num\_output</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

获取输出神经元的数量。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，则返回输出神经元的数量, 错误则返回 **`false`** .

fann\_get\_quickprop\_decay
===========================

返回衰退值，用于在 quickprop 训练迭代时衰减权重

### 说明

<span class="type">float</span> <span
class="methodname">fann\_get\_quickprop\_decay</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

衰退值是一个小的负数，用于在 quickprop 训练迭代时衰减权重。
这是用来确保训练时权重不要太高。

默认衰退值是 -0.0001.

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，返回衰退值，错误则返回 **`false`** .

### 参见

-   <span class="function">fann\_set\_quickprop\_decay</span>

fann\_get\_quickprop\_mu
========================

返回放大系数

### 说明

<span class="type">float</span> <span
class="methodname">fann\_get\_quickprop\_mu</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

放大系数被用来增加和降低 quickprop
训练期间的步长。放大系数应该始终大于1，因为当它增加时，它会减少步长。

默认放大系数是 1.75.

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，返回放大系数，错误则返回 **`false`** .

### 参见

-   <span class="function">fann\_set\_quickprop\_mu</span>

fann\_get\_rprop\_decrease\_factor
==================================

返回 RPROP 训练期间的衰减系数

### 说明

<span class="type">float</span> <span
class="methodname">fann\_get\_rprop\_decrease\_factor</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

衰减系数的值小于1，用于在 RPROP 训练期间减少的步长。

The default decrease factor is 0.5.

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，返回衰减系数，错误则返回 **`false`** .

### 参见

-   <span class="function">fann\_set\_rprop\_decrease\_factor</span>

fann\_get\_rprop\_delta\_max
============================

返回最大步长

### 说明

<span class="type">float</span> <span
class="methodname">fann\_get\_rprop\_delta\_max</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

最大步长是正数，决定最大步长可能有多大。.

默认的最大值是 50.0.

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功,返回最大步长，错误则返回 **`false`** .

### 参见

-   <span class="function">fann\_set\_rprop\_delta\_max</span>
-   <span class="function">fann\_get\_rprop\_delta\_min</span>

fann\_get\_rprop\_delta\_min
============================

返回最小步长

### 说明

<span class="type">float</span> <span
class="methodname">fann\_get\_rprop\_delta\_min</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

最小步长是一个小的正数，决定最小步长可能有多小。.

默认的最小步长是 0.0.

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，返回最小步长，错误则返回 **`false`** .

### 参见

-   <span class="function">fann\_set\_rprop\_delta\_min</span>

fann\_get\_rprop\_delta\_zero
=============================

返回初始步长

### 说明

<span class="type">ReturnType</span> <span
class="methodname">fann\_get\_rprop\_delta\_zero</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

初始步长是确定初始步长的正数。

默认的初始步长是 0.1.

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，返回初始步长，错误则返回 **`false`** .

### 参见

-   <span class="function">fann\_set\_rprop\_delta\_zero</span>
-   <span class="function">fann\_get\_rprop\_delta\_min</span>
-   <span class="function">fann\_get\_rprop\_delta\_max</span>

fann\_get\_rprop\_increase\_factor
==================================

返回 RPROP 训练的递增系数

### 说明

<span class="type">float</span> <span
class="methodname">fann\_get\_rprop\_increase\_factor</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

递增系数是一个大于1的值，用于递增 RPROP 训练中的步长。

默认的递进系数是 1.2

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，返回递进系数，错误则返回 **`false`** .

### 参见

-   <span class="function">fann\_set\_rprop\_increase\_factor</span>

fann\_get\_sarprop\_step\_error\_shift
======================================

返回 sarprop 步值的误差偏移

### 说明

<span class="type">float</span> <span
class="methodname">fann\_get\_sarprop\_step\_error\_shift</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

返回 sarprop 步值的误差偏移。

默认的步值误差偏移是 1.385.

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，返回 sarprop 步值误差偏移，错误则返回 **`false`** .

### 参见

-   <span class="function">fann\_set\_sarprop\_step\_error\_shift</span>

fann\_get\_sarprop\_step\_error\_threshold\_factor
==================================================

返回 sarprop 算法步值的误差阈值系数

### 说明

<span class="type">float</span> <span
class="methodname">fann\_get\_sarprop\_step\_error\_threshold\_factor</span>
( <span class="methodparam"><span class="type">resource</span>
`$ann`</span> )

sarprop 算法步值的误差阈值系数。

默认的系数是 0.1.

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，返回 sarprop 算法步值的误差阈值系数，错误则返回 **`false`** .

### 参见

-   <span
    class="function">fann\_set\_sarprop\_step\_error\_threshold\_factor</span>

fann\_get\_sarprop\_temperature
===============================

返回 sarprop 算法温度

### 说明

<span class="type">float</span> <span
class="methodname">fann\_get\_sarprop\_temperature</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

返回 sarprop 算法温度。

默认温度是 0.015.

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，返回 sarprop 温度，错误则返回 **`false`** .

### 参见

-   <span class="function">fann\_set\_sarprop\_temperature</span>

fann\_get\_sarprop\_weight\_decay\_shift
========================================

返回 sarprop 算法权重衰减变化值

### 说明

<span class="type">float</span> <span
class="methodname">fann\_get\_sarprop\_weight\_decay\_shift</span> (
<span class="methodparam"><span class="type">resource</span>
`$ann`</span> )

sarprop 算法权重衰减变化值。

默认的最大值是 -6.644.

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，返回 sarprop 算法权重衰减变化值，错误则返回 **`false`** .

### 参见

-   <span
    class="function">fann\_set\_sarprop\_weight\_decay\_shift</span>

fann\_get\_total\_connections
=============================

获取整个网络中所有的连接数。

### 说明

<span class="type">int</span> <span
class="methodname">fann\_get\_total\_connections</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

获取整个网络中所有的连接数。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，则返回整个网络中所有的连接数, 错误则返回 **`false`** .

fann\_get\_total\_neurons
=========================

获取整个网络中神经元的数量。

### 说明

<span class="type">int</span> <span
class="methodname">fann\_get\_total\_neurons</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

获取整个网络中神经元的数量。
这个数量也包括偏置神经元，因此一个2-4-2的网络有2+4+2+2（偏置神经元）=10个神经元。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，则返回整个网络神经元的数量, 错误则返回 **`false`** .

fann\_get\_train\_error\_function
=================================

返回训练中使用的错误函数。

### 说明

<span class="type">int</span> <span
class="methodname">fann\_get\_train\_error\_function</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

返回训练中使用的错误函数。

有关于错误函数的详细描述，参见
<a href="/fann/constants.html#Error%20function%20used%20during%20training" class="link">error functions</a>
静态变量。

默认的错误函数是 **`FANN_ERRORFUNC_TANH`**.

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，则返回
<a href="/fann/constants.html#Error%20function%20used%20during%20training" class="link">error function</a>
静态变量, 错误则返回 **`false`** .

### 参见

-   <span class="function">fann\_set\_train\_error\_function</span>

fann\_get\_train\_stop\_function
================================

返回训练中使用的停止函数。

### 说明

<span class="type">int</span> <span
class="methodname">fann\_get\_train\_stop\_function</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

返回训练中使用的停止函数。

停止函数的详细描述，参见<a href="/fann/constants.html#Stop%20criteria%20used%20during%20training" class="link">stop functions</a>
常量。

默认的停止函数是 **`FANN_STOPFUNC_MSE`**.

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，则返回
<a href="/fann/constants.html#Stop%20criteria%20used%20during%20training" class="link">stop function</a>
常量, 错误则返回 **`false`** .

### 参见

-   <span class="function">fann\_set\_train\_stop\_function</span>

fann\_get\_training\_algorithm
==============================

返回训练算法。

### 说明

<span class="type">int</span> <span
class="methodname">fann\_get\_training\_algorithm</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> )

返回训练算法。该训练算法是被 <span
class="function">fann\_train\_on\_data</span> 和相关函数使用的。

要注意的是这个算法在<span
class="function">fann\_cascadetrain\_on\_data</span>函数中也是可以使用的,
尽管在层叠训练中只有**`FANN_TRAIN_RPROP`** 和 **`FANN_TRAIN_QUICKPROP`**
算法被允许使用。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功，返回<a href="/fann/constants.html#训练算法" class="link">训练算法</a>
常量, 错误则返回 **`false`** .

### 参见

-   <span class="function">fann\_set\_training\_algorithm</span>

fann\_init\_weights
===================

使用 Widrow 和 Nguyen 算法初始化权重。

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_init\_weights</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$train_data`</span> )

使用 Widrow 和 Nguyen 算法初始化权重。

该函数的作用和 <span
class="function">fann\_randomize\_weights</span>函数相似。
该函数将会使用 Derrick Nguyen 和 Bernard Widrow
开发的算法来设置权重用于加速训练。
该技术不是经常奏效，在某些场景下比纯粹的随机初始化来得更低效。

该算法要求获取输入数据的范围(比如
最大和最小输入)，因此接受别的参数，数据(将会在网络中训练的数据)。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`train_data`  
神经网络训练数据 <span class="type">资源</span>。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_randomize\_weights</span>
-   <span class="function">fann\_read\_train\_from\_file</span>

fann\_length\_train\_data
=========================

返回训练数据中训练模式的数量。

### 说明

<span class="type">int</span> <span
class="methodname">fann\_length\_train\_data</span> ( <span
class="methodparam"><span class="type">resource</span> `$data`</span> )

返回训练数据中训练模式的数量。 <span class="type">resource</span>.

### 参数

`data`  
神经网络训练数据 <span class="type">资源</span>。

### 返回值

成功，则返回训练数据<span
class="type">resource</span>中的元素数，错误则返回 **`false`** .

fann\_merge\_train\_data
========================

合并训练数据。

### 说明

<span class="type">resource</span> <span
class="methodname">fann\_merge\_train\_data</span> ( <span
class="methodparam"><span class="type">resource</span> `$data1`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$data2`</span> )

将 data1 和 data2 数据集合并为新的训练数据 <span
class="type">resource</span>.

### 参数

`data1`  
神经网络训练数据 <span class="type">资源</span>。

`data2`  
神经网络训练数据 <span class="type">资源</span>。

### 返回值

成功，则返回合并的训练数据 <span class="type">resource</span>,
错误则返回 **`false`** .

fann\_num\_input\_train\_data
=============================

返回训练数据中每个训练模式输入的数量。

### 说明

<span class="type">int</span> <span
class="methodname">fann\_num\_input\_train\_data</span> ( <span
class="methodparam"><span class="type">resource</span> `$data`</span> )

返回训练数据<span class="type">resource</span>中每个训练模式输入的数量。

### 参数

`data`  
神经网络训练数据 <span class="type">资源</span>。

### 返回值

成功，则返回输入数，错误则返回 **`false`** .

### 参见

-   <span class="function">fann\_length\_train\_data</span>
-   <span class="function">fann\_num\_output\_train\_data</span>

fann\_num\_output\_train\_data
==============================

返回训练数据中每个训练模式输出的数量。

### 说明

<span class="type">int</span> <span
class="methodname">fann\_num\_output\_train\_data</span> ( <span
class="methodparam"><span class="type">resource</span> `$data`</span> )

返回训练数据 <span
class="type">resource</span>中每个训练模式输出的数量。

### 参数

`data`  
神经网络训练数据 <span class="type">资源</span>。

### 返回值

成功，则返回输出数, 错误则返回 **`false`** .

### 参见

-   <span class="function">fann\_length\_train\_data</span>
-   <span class="function">fann\_num\_input\_train\_data</span>

fann\_print\_error
==================

打印错误字符串。

### 说明

<span class="type">void</span> <span
class="methodname">fann\_print\_error</span> ( <span
class="methodparam"><span class="type">string</span> `$errdat`</span> )

打印错误字符串。

### 参数

`errdat`  
Either neural network <span class="type">resource</span> or neural
network trainining data <span class="type">resource</span>.

### 返回值

无返回值。

### 参见

-   <span class="function">fann\_get\_errstr</span>

fann\_randomize\_weights
========================

给每个连接赋一个介于 min\_weight 和 max\_weight 之间的随机权重。

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_randomize\_weights</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">float</span>
`$min_weight`</span> , <span class="methodparam"><span
class="type">float</span> `$max_weight`</span> )

给每个连接赋一个介于 `min_weight` 和 `max_weight`之间的随机权重。

从一开始权重介于 -0.1 和 0.1之间。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`min_weight`  
最小权重值

`max_weight`  
最大权重值

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_init\_weights</span>

fann\_read\_train\_from\_file
=============================

读取存储训练数据的文件。

### 说明

<span class="type">resource</span> <span
class="methodname">fann\_read\_train\_from\_file</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

读取存储训练数据的文件。

### 参数

`filename`  
输入文件的格式如下:

``` txt
num_train_data num_input num_output
inputdata seperated by space
outputdata seperated by space

.
.
.

inputdata seperated by space
outputdata seperated by space
```

### 返回值

成功时返回训练数据 <span class="type">资源</span>，发生错误返回
**`false`**。

### 范例

**示例 \#1 <span class="methodname">fann\_read\_train\_from\_file</span>
函数的使用范例：**

``` php
<?php
$train_data = fann_read_train_from_file("xor.data");
if ($train_data) {
    // Do something with $train_data for XOR function
}
?>
```

xor.data 文件的内容：

``` txt
4 2 1
-1 -1
-1
-1 1
1
1 -1
1
1 1
-1
```

### 参见

-   <span class="function">fann\_train\_on\_data</span>
-   <span class="function">fann\_destroy\_train</span>
-   <span class="function">fann\_save\_train</span>

fann\_reset\_errno
==================

重置最后的错误代码。

### 说明

<span class="type">void</span> <span
class="methodname">fann\_reset\_errno</span> ( <span
class="methodparam"><span class="type">resource</span> `$errdat`</span>
)

重置最后的错误代码。

### 参数

`errdat`  
Either neural network <span class="type">resource</span> or neural
network trainining data <span class="type">resource</span>.

### 返回值

无返回值。

### 参见

-   <span class="function">fann\_get\_errno</span>
-   <span class="function">fann\_reset\_errstr</span>

fann\_reset\_errstr
===================

重置最后的错误字符串。

### 说明

<span class="type">void</span> <span
class="methodname">fann\_reset\_errstr</span> ( <span
class="methodparam"><span class="type">resource</span> `$errdat`</span>
)

重置最后的错误字符串。

### 参数

`errdat`  
Either neural network <span class="type">resource</span> or neural
network trainining data <span class="type">resource</span>.

### 返回值

无返回值。

### 参见

-   <span class="function">fann\_get\_errstr</span>
-   <span class="function">fann\_reset\_errno</span>

fann\_reset\_MSE
================

重置网络中的均方误差。

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_reset\_MSE</span> ( <span
class="methodparam"><span class="type">string</span> `$ann`</span> )

重置网络中的均方误差。

该函数也会重置失败时位的数量。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_get\_MSE</span>
-   <span class="function">fann\_get\_bit\_fail</span>
-   <span class="function">fann\_get\_bit\_fail\_limit</span>

fann\_run
=========

将通过神经网络运行输入。

### 说明

<span class="type">array</span> <span
class="methodname">fann\_run</span> ( <span class="methodparam"><span
class="type">resource</span> `$ann`</span> , <span
class="methodparam"><span class="type">array</span> `$input`</span> )

将通过神经网络运行输入，返回输出数组，数组的长度等于输出层神经元的个数。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`input`  
输入数组的值。

### 返回值

成功，返回输出数组，错误则返回 **`false`** .

fann\_save\_train
=================

将训练结构体保存至文件。

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_save\_train</span> ( <span
class="methodparam"><span class="type">resource</span> `$data`</span> ,
<span class="methodparam"><span class="type">string</span>
`$file_name`</span> )

将训练结构体保存至文件， 格式和 <span
class="function">fann\_read\_train\_from\_file</span> 函数中指定的一样。

### 参数

`data`  
神经网络训练数据 <span class="type">资源</span>。

`file_name`  
保存训练数据的文件名。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_read\_train\_from\_file</span>

fann\_save
==========

将整个网络保存至配置文件。

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_save</span> ( <span class="methodparam"><span
class="type">resource</span> `$ann`</span> , <span
class="methodparam"><span class="type">string</span>
`$configuration_file`</span> )

将整个网络保存至配置文件。

配置文件包含了神经网络的所有信息，并且能够通过 <span
class="function">fann\_create\_from\_file</span>
函数来创建一个原神经网络的精确副本以及与神经网络关联的所有参数。

这三个参数 (<span class="function">fann\_set\_callback</span>, <span
class="function">fann\_set\_error\_log</span>, <span
class="function">fann\_set\_user\_data</span>)
不保存在文件中，因为他们不能被安全地移植到不同的位置。当使用类似 <span
class="function">fann\_get\_MSE</span>
函数训练时，生成的临时参数也不会被保存起来。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`configuration_file`  
配置文件的路径。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_create\_from\_file</span>

fann\_scale\_input\_train\_data
===============================

在训练数据中缩放输入至指定范围

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_scale\_input\_train\_data</span> ( <span
class="methodparam"><span class="type">resource</span>
`$train_data`</span> , <span class="methodparam"><span
class="type">float</span> `$new_min`</span> , <span
class="methodparam"><span class="type">float</span> `$new_max`</span> )

在训练数据中缩放输入至指定范围。

### 参数

`train_data`  
神经网络训练数据 <span class="type">资源</span>。

`new_min`  
训练数据中缩放输入后新的最小值。

`new_max`  
训练数据中缩放数据后新的最大值。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_scale\_output\_train\_data</span>
-   <span class="function">fann\_scale\_train\_data</span>

fann\_scale\_input
==================

在以前计算参数的基础上，在训练之前放大输入向量中的数据

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_scale\_input</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">array</span>
`$input_vector`</span> )

在以前计算参数的基础上，在训练之前放大输入向量中的数据。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`input_vector`  
将要被缩放的输入向量。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_descale\_input</span>
-   <span class="function">fann\_scale\_output</span>

fann\_scale\_output\_train\_data
================================

在训练数据中缩放输出至指定范围

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_scale\_output\_train\_data</span> ( <span
class="methodparam"><span class="type">resource</span>
`$train_data`</span> , <span class="methodparam"><span
class="type">float</span> `$new_min`</span> , <span
class="methodparam"><span class="type">float</span> `$new_max`</span> )

在训练数据中缩放输出至指定范围。

### 参数

`train_data`  
神经网络训练数据 <span class="type">资源</span>。

`new_min`  
训练数据中缩放输出后新的最小值。

`new_max`  
训练数据中缩放输出后新的最大值。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_scale\_input\_train\_data</span>
-   <span class="function">fann\_scale\_train\_data</span>

fann\_scale\_output
===================

在以前计算参数的基础上，在训练之前放大输出向量中的数据

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_scale\_output</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">array</span>
`$output_vector`</span> )

在以前计算参数的基础上，在训练之前放大输出向量中的数据。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`output_vector`  
将要被缩放的输出向量

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_descale\_output</span>
-   <span class="function">fann\_scale\_input</span>

fann\_scale\_train\_data
========================

在训练数据中缩放输入和输出到指定的范围

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_scale\_train\_data</span> ( <span
class="methodparam"><span class="type">resource</span>
`$train_data`</span> , <span class="methodparam"><span
class="type">float</span> `$new_min`</span> , <span
class="methodparam"><span class="type">float</span> `$new_max`</span> )

在训练数据中缩放输入和输出到指定的范围。

### 参数

`train_data`  
神经网络训练数据 <span class="type">资源</span>。

`new_min`  
在训练数据中缩放输入和输出后新的最小值。

`new_max`  
在训练数据中缩放输入和输出后新的最大值。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_scale\_output\_train\_data</span>
-   <span class="function">fann\_scale\_input\_train\_data</span>

fann\_scale\_train
==================

在以前计算参数的基础上，缩放输入和输出数据

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_scale\_train</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$train_data`</span> )

在以前计算参数的基础上，缩放输入和输出数据。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`train_data`  
神经网络训练数据 <span class="type">资源</span>。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_descale\_train</span>
-   <span class="function">fann\_set\_scaling\_params</span>

fann\_set\_activation\_function\_hidden
=======================================

为所有隐藏层设置激活函数

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_activation\_function\_hidden</span> (
<span class="methodparam"><span class="type">resource</span>
`$ann`</span> , <span class="methodparam"><span class="type">int</span>
`$activation_function`</span> )

为所有隐藏层设置激活函数。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`activation_function`  
<a href="/fann/constants.html#Activation%20functions" class="link">激活函数</a>
常量。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_set\_activation\_function</span>
-   <span class="function">fann\_set\_activation\_function\_layer</span>
-   <span
    class="function">fann\_set\_activation\_function\_output</span>
-   <span class="function">fann\_set\_activation\_steepness</span>

fann\_set\_activation\_function\_layer
======================================

为已应用的层中所有的神经元设置激活函数。

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_activation\_function\_layer</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">int</span>
`$activation_function`</span> , <span class="methodparam"><span
class="type">int</span> `$layer`</span> )

为层数为 *layer* 的所有神经元设置激活函数，将输入层计为0.

在输入层中为神经元设置激活函数是不可能的。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`activation_function`  
<a href="/fann/constants.html#Activation%20functions" class="link">激活函数</a>
常量。

`layer`  
层数。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_set\_activation\_function</span>
-   <span
    class="function">fann\_set\_activation\_function\_hidden</span>
-   <span
    class="function">fann\_set\_activation\_function\_output</span>
-   <span class="function">fann\_set\_activation\_steepness</span>

fann\_set\_activation\_function\_output
=======================================

为输出层设置激活函数

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_activation\_function\_output</span> (
<span class="methodparam"><span class="type">resource</span>
`$ann`</span> , <span class="methodparam"><span class="type">int</span>
`$activation_function`</span> )

为输出层设置激活函数。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`activation_function`  
<a href="/fann/constants.html#Activation%20functions" class="link">激活函数</a>
常量。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_set\_activation\_function</span>
-   <span class="function">fann\_set\_activation\_function\_layer</span>
-   <span
    class="function">fann\_set\_activation\_function\_hidden</span>
-   <span class="function">fann\_set\_activation\_steepness</span>

fann\_set\_activation\_function
===============================

为已应用的神经元和层设置激活函数

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_activation\_function</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">int</span>
`$activation_function`</span> , <span class="methodparam"><span
class="type">int</span> `$layer`</span> , <span
class="methodparam"><span class="type">int</span> `$neuron`</span> )

为层数为 *layer*，神经经元数为 *neuron*
的神经元设置激活函数，将输入层记为0.

在输出层中的神经元设置激活函数是不可能的。

在选择激活函数时，注意激活函数有不同的范围，这个很重要哦。
**`FANN_SIGMOID`** 就是个例子。它的范围是0 -1，然而
**`FANN_SIGMOID_SYMMETRIC`** 的范围是-1 - 1， **`FANN_LINEAR`**
却是无限的。

应用的激活函数应该是<a href="/fann/constants.html#Activation%20functions" class="link">激活函数</a>常量之一。

返回值是<a href="/fann/constants.html#训练算法" class="link">激活函数</a>常量之一。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`activation_function`  
<a href="/fann/constants.html#Activation%20functions" class="link">激活函数</a>常量。

`layer`  
层数。

`neuron`  
神经元数。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_set\_activation\_function\_layer</span>
-   <span
    class="function">fann\_set\_activation\_function\_hidden</span>
-   <span
    class="function">fann\_set\_activation\_function\_output</span>
-   <span class="function">fann\_set\_activation\_steepness</span>
-   <span class="function">fann\_get\_activation\_function</span>

fann\_set\_activation\_steepness\_hidden
========================================

为所有隐藏层中所有的神经元设置激活函数陡度

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_activation\_steepness\_hidden</span> (
<span class="methodparam"><span class="type">resource</span>
`$ann`</span> , <span class="methodparam"><span
class="type">float</span> `$activation_steepness`</span> )

为所有隐藏层中所有的神经元设置激活陡度。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`activation_steepness`  
激活陡度。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_set\_activation\_steepness</span>
-   <span
    class="function">fann\_set\_activation\_steepness\_layer</span>
-   <span
    class="function">fann\_set\_activation\_steepness\_output</span>
-   <span class="function">fann\_get\_activation\_steepness</span>
-   <span class="function">fann\_set\_activation\_function</span>

fann\_set\_activation\_steepness\_layer
=======================================

为提供的层中所有的神经元设置激活陡度

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_activation\_steepness\_layer</span> (
<span class="methodparam"><span class="type">resource</span>
`$ann`</span> , <span class="methodparam"><span
class="type">float</span> `$activation_steepness`</span> , <span
class="methodparam"><span class="type">int</span> `$layer`</span> )

为层数为 *layer* 中所有的神经元设置激活陡度，将输入层计为0。

在输出层中设置激活陡度是不可能的。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`activation_steepness`  
激活陡度。

`layer`  
层数。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_set\_activation\_steepness</span>
-   <span
    class="function">fann\_set\_activation\_steepness\_hidden</span>
-   <span
    class="function">fann\_set\_activation\_steepness\_output</span>
-   <span class="function">fann\_get\_activation\_steepness</span>
-   <span class="function">fann\_set\_activation\_function</span>

fann\_set\_activation\_steepness\_output
========================================

在输出层中设置激活陡度

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_activation\_steepness\_output</span> (
<span class="methodparam"><span class="type">resource</span>
`$ann`</span> , <span class="methodparam"><span
class="type">float</span> `$activation_steepness`</span> )

在输出层中设置激活陡度。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`activation_steepness`  
激活陡度。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_set\_activation\_steepness</span>
-   <span
    class="function">fann\_set\_activation\_steepness\_layer</span>
-   <span
    class="function">fann\_set\_activation\_steepness\_hidden</span>
-   <span class="function">fann\_get\_activation\_steepness</span>
-   <span class="function">fann\_set\_activation\_function</span>

fann\_set\_activation\_steepness
================================

为提供的神经元和层设置激活陡度

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_activation\_steepness</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">float</span>
`$activation_steepness`</span> , <span class="methodparam"><span
class="type">int</span> `$layer`</span> , <span
class="methodparam"><span class="type">int</span> `$neuron`</span> )

为层数为 *layer*，神经元数为 *neuron*
的神经元设置激活陡度，输出层的层数计为0。

为输入层中的神经元设置激活陡度是不可能的。.

激活函数的陡度表示激活从最大值到最小值有多快。一个高的激活函数值也会导致一个更积极的训练。

当训练神经网络中输出值处于一个极端值(通常为0或者1，取决于激活函数)时，可以使用陡峭的激活函数(比如
1.0)。

默认激活陡度是0.5。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`activation_steepness`  
激活陡度。

`layer`  
层数。

`neuron`  
神经元数。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span
    class="function">fann\_set\_activation\_steepness\_layer</span>
-   <span
    class="function">fann\_set\_activation\_steepness\_hidden</span>
-   <span
    class="function">fann\_set\_activation\_steepness\_output</span>
-   <span class="function">fann\_get\_activation\_steepness</span>
-   <span class="function">fann\_set\_activation\_function</span>

fann\_set\_bit\_fail\_limit
===========================

设置训练期间使用的误差

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_bit\_fail\_limit</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">float</span>
`$bit_fail_limit`</span> )

设置训练期间使用的误差。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`bit_fail_limit`  
误差。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_get\_bit\_fail\_limit</span>

fann\_set\_callback
===================

设置训练期间使用的回调函数。

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_callback</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">collable</span>
`$callback`</span> )

设置训练期间使用的回调函数。 这意味着它被<span
class="function">fann\_train\_on\_data</span> 或 <span
class="function">fann\_train\_on\_file</span>调用。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`callback`  
提供的回调函数接受以下参数：

-   *ann* - 神经网络 <span class="type">resource</span>
-   *train* - 训练数据 <span class="type">resource</span> 或者 当被
    <span class="function">fann\_train\_on\_file</span> 为 **`null`**
-   *max\_epochs* - 训练将进行的最大周期数。
-   *epochs\_between\_reports* - 在调用该函数之前训练进行的最大周期数。
-   *desired\_error* - 期望的 <span
    class="function">fann\_get\_MSE</span> 或者 <span
    class="function">fann\_get\_bit\_fail</span>, 取决于<span
    class="function">fann\_set\_train\_stop\_function</span>函数选择的停止函数。
-   *epochs* - The current epoch

回调将会返回 **`true`**. 如果返回 **`false`**, 表明训练将会终止。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_train\_on\_data</span>
-   <span class="function">fann\_train\_on\_file</span>

fann\_set\_cascade\_activation\_functions
=========================================

设置级联候选激活函数的数组

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_cascade\_activation\_functions</span> (
<span class="methodparam"><span class="type">resource</span>
`$ann`</span> , <span class="methodparam"><span
class="type">array</span> `$cascade_activation_functions`</span> )

设置级联候选激活函数的数组。

想知道哪个候选神经元将会被该数组生成,参见 <span
class="function">fann\_get\_cascade\_num\_candidates</span> .

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`cascade_activation_functions`  
级联候选激活函数数组。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span
    class="function">fann\_get\_cascade\_activation\_functions\_count</span>
-   <span
    class="function">fann\_set\_cascade\_activation\_functions</span>

fann\_set\_cascade\_activation\_steepnesses
===========================================

设置级联候选激活陡度的数组。

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_cascade\_activation\_steepnesses</span> (
<span class="methodparam"><span class="type">resource</span>
`$ann`</span> , <span class="methodparam"><span
class="type">array</span> `$cascade_activation_steepnesses_count`</span>
)

设置级联候选激活陡度的数组。

想知道哪个候选神经元将会被该数组生成，参见 <span
class="function">fann\_get\_cascade\_num\_candidates</span> .

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`cascade_activation_steepnesses_count`  
级联候选激活陡度数组。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span
    class="function">fann\_get\_cascade\_activation\_steepnesses</span>
-   <span
    class="function">fann\_get\_cascade\_activation\_steepnesses\_count</span>

fann\_set\_cascade\_candidate\_change\_fraction
===============================================

设置级联候选更改分数

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_cascade\_candidate\_change\_fraction</span>
( <span class="methodparam"><span class="type">resource</span>
`$ann`</span> , <span class="methodparam"><span
class="type">float</span> `$cascade_candidate_change_fraction`</span> )

设置级联候选更改分数。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`cascade_candidate_change_fraction`  
级联候选更改分数。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span
    class="function">fann\_get\_cascade\_candidate\_change\_fraction</span>

fann\_set\_cascade\_candidate\_limit
====================================

设置候选限度

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_cascade\_candidate\_limit</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">float</span>
`$cascade_candidate_limit`</span> )

设置候选限度。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`cascade_candidate_limit`  
候选限度。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_get\_cascade\_candidate\_limit</span>

fann\_set\_cascade\_candidate\_stagnation\_epochs
=================================================

设置级联候选停止周期数

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_cascade\_candidate\_stagnation\_epochs</span>
( <span class="methodparam"><span class="type">resource</span>
`$ann`</span> , <span class="methodparam"><span class="type">int</span>
`$cascade_candidate_stagnation_epochs`</span> )

设置级联候选停止周期数。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`cascade_candidate_stagnation_epochs`  
级联候选停止周期数。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span
    class="function">fann\_get\_cascade\_candidate\_stagnation\_epochs</span>

fann\_set\_cascade\_max\_cand\_epochs
=====================================

设置最大候选周期数

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_cascade\_max\_cand\_epochs</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">int</span>
`$cascade_max_cand_epochs`</span> )

设置最大候选周期数。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`cascade_max_cand_epochs`  
设置最大候选周期数。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_get\_cascade\_max\_cand\_epochs</span>

fann\_set\_cascade\_max\_out\_epochs
====================================

设置最大输出周期

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_cascade\_max\_out\_epochs</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">int</span>
`$cascade_max_out_epochs`</span> )

设置最大输出周期。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`cascade_max_out_epochs`  
最大输出周期。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_get\_cascade\_max\_out\_epochs</span>

fann\_set\_cascade\_min\_cand\_epochs
=====================================

设置最小候选周期

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_cascade\_min\_cand\_epochs</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">int</span>
`$cascade_min_cand_epochs`</span> )

设置最小候选周期。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`cascade_min_cand_epochs`  
设置最小候选周期。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_get\_cascade\_min\_cand\_epochs</span>

fann\_set\_cascade\_min\_out\_epochs
====================================

设置最小输出周期

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_cascade\_min\_out\_epochs</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">int</span>
`$cascade_min_out_epochs`</span> )

设置最小输出周期。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`cascade_min_out_epochs`  
最小输出周期。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_get\_cascade\_min\_out\_epochs</span>

fann\_set\_cascade\_num\_candidate\_groups
==========================================

设置候选组数量

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_cascade\_num\_candidate\_groups</span> (
<span class="methodparam"><span class="type">resource</span>
`$ann`</span> , <span class="methodparam"><span class="type">int</span>
`$cascade_num_candidate_groups`</span> )

设置候选组数量。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`cascade_num_candidate_groups`  
候选组数量。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span
    class="function">fann\_get\_cascade\_num\_candidate\_groups</span>

fann\_set\_cascade\_output\_change\_fraction
============================================

设置级联输出改变分数

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_cascade\_output\_change\_fraction</span> (
<span class="methodparam"><span class="type">resource</span>
`$ann`</span> , <span class="methodparam"><span
class="type">float</span> `$cascade_output_change_fraction`</span> )

设置级联输出改变分数。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`cascade_output_change_fraction`  
级联输出改变分数。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span
    class="function">fann\_get\_cascade\_output\_change\_fraction</span>

fann\_set\_cascade\_output\_stagnation\_epochs
==============================================

设置级联输出停滞周期的值

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_cascade\_output\_stagnation\_epochs</span>
( <span class="methodparam"><span class="type">resource</span>
`$ann`</span> , <span class="methodparam"><span class="type">int</span>
`$cascade_output_stagnation_epochs`</span> )

设置级联输出停滞周期的值。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`cascade_output_stagnation_epochs`  
级联输出停滞周期的值

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span
    class="function">fann\_get\_cascade\_output\_stagnation\_epochs</span>

fann\_set\_cascade\_weight\_multiplier
======================================

设置权重因子

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_cascade\_weight\_multiplier</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">float</span>
`$cascade_weight_multiplier`</span> )

设置权重因子。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`cascade_weight_multiplier`  
权重因子。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_get\_cascade\_weight\_multiplier</span>

fann\_set\_error\_log
=====================

设置错误记录保存的位置。

### 说明

<span class="type">void</span> <span
class="methodname">fann\_set\_error\_log</span> ( <span
class="methodparam"><span class="type">resource</span> `$errdat`</span>
, <span class="methodparam"><span class="type">string</span>
`$log_file`</span> )

设置错误记录保存的位置。

### 参数

`errdat`  
Either neural network <span class="type">resource</span> or neural
network trainining data <span class="type">resource</span>.

`log_file`  
日志文件的路径。

### 返回值

无返回值。

fann\_set\_input\_scaling\_params
=================================

根据训练数据计算将来使用的输入比例参数

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_input\_scaling\_params</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$train_data`</span> , <span class="methodparam"><span
class="type">float</span> `$new_input_min`</span> , <span
class="methodparam"><span class="type">float</span>
`$new_input_max`</span> )

根据训练数据计算将来使用的输入比例参数。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`train_data`  
神经网络训练数据 <span class="type">资源</span>。

`new_input_min`  
缩放后输入数据的期望下限 (不严格遵循)

`new_input_max`  
缩放后输入数据的期望上线 (不严格遵循)

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_set\_output\_scaling\_params</span>

fann\_set\_learning\_momentum
=============================

设置学习动量。

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_learning\_momentum</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">float</span>
`$learning_momentum`</span> )

设置学习动量。

更多信息，参见 <span
class="function">fann\_get\_learning\_momentum</span>.

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`learning_momentum`  
学习动量。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_get\_learning\_momentum</span>
-   <span class="function">fann\_set\_training\_algorithm</span>

fann\_set\_learning\_rate
=========================

设置学习速率。

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_learning\_rate</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">float</span>
`$learning_rate`</span> )

设置学习速率。

更新信息，参见 <span class="function">fann\_get\_learning\_rate</span>.

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`learning_rate`  
学习速率。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_get\_learning\_rate</span>
-   <span class="function">fann\_set\_training\_algorithm</span>

fann\_set\_output\_scaling\_params
==================================

根据训练数据计算将来使用的输出缩放参数

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_output\_scaling\_params</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$train_data`</span> , <span class="methodparam"><span
class="type">float</span> `$new_output_min`</span> , <span
class="methodparam"><span class="type">float</span>
`$new_output_max`</span> )

根据训练数据计算将来使用的输出缩放参数

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`train_data`  
神经网络训练数据 <span class="type">资源</span>。

`new_output_min`  
缩放后输出数据的期望下限(不严格遵循)

`new_output_max`  
缩放后输出数据的期望上限(不严格遵循)

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_set\_input\_scaling\_params</span>

fann\_set\_quickprop\_decay
===========================

设置quickprop算法衰减因子

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_quickprop\_decay</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">float</span>
`$quickprop_decay`</span> )

设置quickprop算法衰减因子。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`quickprop_decay`  
quickprop算法衰减因子。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_get\_quickprop\_decay</span>

fann\_set\_quickprop\_mu
========================

设置 quickprop 算法放大因子

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_quickprop\_mu</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">float</span>
`$quickprop_mu`</span> )

设置 quickprop 算法放大因子。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`quickprop_mu`  
放大因子。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_get\_quickprop\_mu</span>

fann\_set\_rprop\_decrease\_factor
==================================

使用 RPROP 算法训练时，设置下降因子

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_rprop\_decrease\_factor</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">float</span>
`$rprop_decrease_factor`</span> )

使用 RPROP 算法训练时，设置下降因子。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`rprop_decrease_factor`  
下降因子。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_get\_rprop\_decrease\_factor</span>

fann\_set\_rprop\_delta\_max
============================

设置最大步长

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_rprop\_delta\_max</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">float</span>
`$rprop_delta_max`</span> )

最大步长是一个正数，决定最大步长可能有多大。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`rprop_delta_max`  
最大步长。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_get\_rprop\_delta\_max</span>
-   <span class="function">fann\_get\_rprop\_delta\_min</span>

fann\_set\_rprop\_delta\_min
============================

设置最小步长

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_rprop\_delta\_min</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">float</span>
`$rprop_delta_min`</span> )

最小步长是一个小的正数，决定最小步长可能有多小。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`rprop_delta_min`  
最小步长。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_get\_rprop\_delta\_min</span>

fann\_set\_rprop\_delta\_zero
=============================

设置初始步长

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_rprop\_delta\_zero</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">float</span>
`$rprop_delta_zero`</span> )

初始步长是确定初始步长的正数。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`rprop_delta_zero`  
初始步长。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_get\_rprop\_delta\_zero</span>
-   <span class="function">fann\_get\_rprop\_delta\_min</span>
-   <span class="function">fann\_get\_rprop\_delta\_max</span>

fann\_set\_rprop\_increase\_factor
==================================

使用 RPROP 算法训练时，设置增长因子

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_rprop\_increase\_factor</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">float</span>
`$rprop_increase_factor`</span> )

使用 RPROP 算法训练时，设置增长因子。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`rprop_increase_factor`  
增长因子。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_get\_rprop\_increase\_factor</span>

fann\_set\_sarprop\_step\_error\_shift
======================================

设置 sarprop 算法的步误差偏移量

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_sarprop\_step\_error\_shift</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">float</span>
`$sarprop_step_error_shift`</span> )

设置 sarprop 算法的步误差偏移量。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`sarprop_step_error_shift`  
sarprop 算法的步误差偏移量.

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_get\_sarprop\_step\_error\_shift</span>

fann\_set\_sarprop\_step\_error\_threshold\_factor
==================================================

设置 sarprop 算法的步误差阈值因子

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_sarprop\_step\_error\_threshold\_factor</span>
( <span class="methodparam"><span class="type">resource</span>
`$ann`</span> , <span class="methodparam"><span
class="type">float</span> `$sarprop_step_error_threshold_factor`</span>
)

设置 sarprop 算法的步误差阈值因子。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`sarprop_step_error_threshold_factor`  
sarprop 算法的步误差阈值因子。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span
    class="function">fann\_get\_sarprop\_step\_error\_threshold\_factor</span>

fann\_set\_sarprop\_temperature
===============================

设置 sarprop 算法的温度

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_sarprop\_temperature</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">float</span>
`$sarprop_temperature`</span> )

设置 sarprop 算法的温度。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`sarprop_temperature`  
sarprop 算法的温度。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_get\_sarprop\_temperature</span>

fann\_set\_sarprop\_weight\_decay\_shift
========================================

设置 sarprop 算法的权重衰减偏移值

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_sarprop\_weight\_decay\_shift</span> (
<span class="methodparam"><span class="type">resource</span>
`$ann`</span> , <span class="methodparam"><span
class="type">float</span> `$sarprop_weight_decay_shift`</span> )

设置 sarprop 算法的权重衰减偏移值。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`sarprop_weight_decay_shift`  
sarprop 算法的权重衰减偏移值。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span
    class="function">fann\_get\_sarprop\_weight\_decay\_shift</span>

fann\_set\_scaling\_params
==========================

根据训练数据计算输入和输出缩放参数以供将来使用

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_scaling\_params</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$train_data`</span> , <span class="methodparam"><span
class="type">float</span> `$new_input_min`</span> , <span
class="methodparam"><span class="type">float</span>
`$new_input_max`</span> , <span class="methodparam"><span
class="type">float</span> `$new_output_min`</span> , <span
class="methodparam"><span class="type">float</span>
`$new_output_max`</span> )

根据训练数据计算输入和输出缩放参数以供将来使用。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`train_data`  
神经网络训练数据 <span class="type">资源</span>。

`new_input_min`  
缩放后输入数据的期望下限 (不严格遵循)

`new_input_max`  
缩放后输入数据的期望上限 (不严格遵循)

`new_output_min`  
缩放后输出数据的期望下限 (不严格遵循)

`new_output_max`  
缩放后输出数据的期望上限 (不严格遵循)

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_set\_input\_scaling\_params</span>
-   <span class="function">fann\_set\_output\_scaling\_params</span>

fann\_set\_train\_error\_function
=================================

设置训练期间使用的错误函数。

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_train\_error\_function</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">int</span>
`$error_function`</span> )

设置训练期间使用的错误函数。

更多错误函数的信息，参见
<a href="/fann/constants.html#Error%20function%20used%20during%20training" class="link">error functions</a>
常量.

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`error_function`  
<a href="/fann/constants.html#Error%20function%20used%20during%20training" class="link">error function</a>
常量。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_get\_train\_error\_function</span>

fann\_set\_train\_stop\_function
================================

设置训练期间使用的停止函数。

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_train\_stop\_function</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">int</span>
`$stop_function`</span> )

设置训练期间使用的停止函数。

停止函数更多详情，参见
<a href="/fann/constants.html#Stop%20criteria%20used%20during%20training" class="link">stop functions</a>
常量。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`stop_function`  
<a href="/fann/constants.html#Stop%20criteria%20used%20during%20training" class="link">stop function</a>
常量。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_get\_train\_stop\_function</span>

fann\_set\_training\_algorithm
==============================

设置训练算法。

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_training\_algorithm</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">int</span>
`$training_algorithm`</span> )

设置训练算法。

更多信息参见 <span
class="function">fann\_get\_training\_algorithm</span>.

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`training_algorithm`  
<a href="/fann/constants.html#训练算法" class="link">Training algorithm</a>
常量

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_get\_training\_algorithm</span>

fann\_set\_weight\_array
========================

在网络中设置一个连接。

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_weight\_array</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">array</span>
`$connections`</span> )

在网络中设置一个连接。

只有权重将会被改变，连接和权重将被忽略如果它们不存在于网络中。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`connections`  
一个包含 <span class="classname">FANNConnection</span> 对象的数组。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

fann\_set\_weight
=================

在网络中设置一个连接。

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_set\_weight</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">int</span>
`$from_neuron`</span> , <span class="methodparam"><span
class="type">int</span> `$to_neuron`</span> , <span
class="methodparam"><span class="type">float</span> `$weight`</span> )

在网络中设置一个连接。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`from_neuron`  
连接开始处的神经元。

`to_neuron`  
连接结束处的神经元。

`weight`  
连接权重。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

fann\_shuffle\_train\_data
==========================

打算训练数据，使顺序随机。

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_shuffle\_train\_data</span> ( <span
class="methodparam"><span class="type">resource</span>
`$train_data`</span> )

打算训练数据，使顺序随机。
增量训练时推荐使用，但是批训练时并没有什么明显的效果。

### 参数

`train_data`  
神经网络训练数据 <span class="type">资源</span>。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

fann\_subset\_train\_data
=========================

返回一个训练数据子集的副本。

### 说明

<span class="type">resource</span> <span
class="methodname">fann\_subset\_train\_data</span> ( <span
class="methodparam"><span class="type">resource</span> `$data`</span> ,
<span class="methodparam"><span class="type">int</span> `$pos`</span> ,
<span class="methodparam"><span class="type">int</span> `$length`</span>
)

返回一个训练数据子集的副本 <span class="type">resource</span>, 从 *pos*
位置开始向前步进 *length* 个元素。

*fann\_subset\_train\_data(train\_data, 0,
fann\_length\_train\_data(train\_data))* 和 <span
class="function">fann\_duplicate\_train\_data</span>函数的效果是一样的。

### 参数

`data`  
神经网络训练数据 <span class="type">资源</span>。

`pos`  
起始位置。

`length`  
复制元素的数量。

### 返回值

成功时返回训练数据 <span class="type">资源</span>，发生错误返回
**`false`**。

### 参见

-   <span class="function">fann\_duplicate\_train\_data</span>

fann\_test\_data
================

使用训练数据来测试并且计算出 MSE

### 说明

<span class="type">float</span> <span
class="methodname">fann\_test\_data</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$data`</span> )

使用训练数据来测试并且计算出 MSE。

该函数将会更新 MSE 和 误差的值。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`data`  
神经网络训练数据 <span class="type">资源</span>。

### 返回值

成功，则更新 MSE, 错误则返回 **`false`**。

### 参见

-   <span class="function">fann\_train\_on\_data</span>
-   <span class="function">fann\_train\_epoch</span>
-   <span class="function">fann\_get\_bit\_fail</span>
-   <span class="function">fann\_get\_MSE</span>
-   <span class="function">fann\_set\_training\_algorithm</span>

fann\_test
==========

使用一组输入和一组期望的输出来测试。

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_test</span> ( <span class="methodparam"><span
class="type">resource</span> `$ann`</span> , <span
class="methodparam"><span class="type">array</span> `$input`</span> ,
<span class="methodparam"><span class="type">array</span>
`$desired_output`</span> )

使用一组输入和一组期望的输出来测试。
这个操作将会更新均方误差，但是无论如何都不会改变网络。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`input`  
输入数组。 这个数组必须和 <span
class="function">fann\_get\_num\_input</span> 一样长。

`desired_output`  
期望的输出数组。 这个数组必须和 <span
class="function">fann\_get\_num\_output</span> 一样长.

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_test\_data</span>
-   <span class="function">fann\_train</span>
-   <span class="function">fann\_get\_num\_input</span>
-   <span class="function">fann\_get\_num\_output</span>

fann\_train\_epoch
==================

使用一组训练数据训练一个周期。

### 说明

<span class="type">float</span> <span
class="methodname">fann\_train\_epoch</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$data`</span> )

使用保存在 data
中训练数据训练一个周期。一个训练周期表示所有的训练数据正好使用了一次。

这个函数将会返回在其实际计算之前或当中被计算的 MSE
错误。但是因为计算需要再次走一遍整个训练集，所有训练周期之后的不是真正的
MSE。 在训练中使用这个值是绰绰有余的。

该函数使用的是被 <span
class="function">fann\_set\_training\_algorithm</span>
函数选中的训练算法。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`data`  
神经网络训练数据 <span class="type">资源</span>。

### 返回值

成功，则返回 MSE, 错误则返回 **`false`** .

### 参见

-   <span class="function">fann\_train\_on\_data</span>
-   <span class="function">fann\_test\_data</span>
-   <span class="function">fann\_get\_MSE</span>
-   <span class="function">fann\_set\_training\_algorithm</span>

fann\_train\_on\_data
=====================

在整个数据集上训练一段时间。

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_train\_on\_data</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$data`</span> , <span class="methodparam"><span class="type">int</span>
`$max_epochs`</span> , <span class="methodparam"><span
class="type">int</span> `$epochs_between_reports`</span> , <span
class="methodparam"><span class="type">float</span>
`$desired_error`</span> )

在整个数据集上训练一段时间。

该训练使用 <span class="function">fann\_set\_training\_algorithm</span>
函数选择的算法和这些训练算法设置的参数。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`data`  
神经网络训练数据 <span class="type">资源</span>。

`max_epochs`  
训练应该继续的最大周期数。

`epochs_between_reports`  
用户函数之间的周期数。当为0时表示没有用户函数被调用。

`desired_error`  
期望的是 <span class="function">fann\_get\_MSE</span> 或 <span
class="function">fann\_get\_bit\_fail</span>的返回值, 取决于 <span
class="function">fann\_set\_train\_stop\_function</span>
选择的停止函数。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_train\_on\_file</span>
-   <span class="function">fann\_train\_epoch</span>
-   <span class="function">fann\_get\_bit\_fail</span>
-   <span class="function">fann\_get\_MSE</span>
-   <span class="function">fann\_set\_train\_stop\_function</span>
-   <span class="function">fann\_set\_training\_algorithm</span>
-   <span class="function">fann\_set\_callback</span>

fann\_train\_on\_file
=====================

在从某个文件读取的整个数据集上训练一段时间。

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_train\_on\_file</span> ( <span
class="methodparam"><span class="type">resource</span> `$ann`</span> ,
<span class="methodparam"><span class="type">string</span>
`$filename`</span> , <span class="methodparam"><span
class="type">int</span> `$max_epochs`</span> , <span
class="methodparam"><span class="type">int</span>
`$epochs_between_reports`</span> , <span class="methodparam"><span
class="type">float</span> `$desired_error`</span> )

在从某个文件读取的整个数据集上训练一段时间。

该训练使用 <span class="function">fann\_set\_training\_algorithm</span>
函数选择的算法和这些训练算法设置的参数。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`filename`  
包含训练数据的文件。

`max_epochs`  
训练应该继续的最大周期数。

`epochs_between_reports`  
用户函数之间的周期数。当为0时表示没有用户函数被调用。

`desired_error`  
期望的是 <span class="function">fann\_get\_MSE</span> 或 <span
class="function">fann\_get\_bit\_fail</span>的返回值, 取决于 <span
class="function">fann\_set\_train\_stop\_function</span>
选择的停止函数。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_train\_on\_data</span>
-   <span class="function">fann\_train\_epoch</span>
-   <span class="function">fann\_get\_bit\_fail</span>
-   <span class="function">fann\_get\_MSE</span>
-   <span class="function">fann\_set\_train\_stop\_function</span>
-   <span class="function">fann\_set\_training\_algorithm</span>
-   <span class="function">fann\_set\_callback</span>

fann\_train
===========

使用一个输入集和一个期望的输出集来迭代训练一次。

### 说明

<span class="type">bool</span> <span
class="methodname">fann\_train</span> ( <span class="methodparam"><span
class="type">resource</span> `$ann`</span> , <span
class="methodparam"><span class="type">array</span> `$input`</span> ,
<span class="methodparam"><span class="type">array</span>
`$desired_output`</span> )

使用一个输入集和一个期望的输出集来迭代训练一次。
该训练一直是递增训练，因此只会出现一个模式。

### 参数

`ann`  
神经网络 <span class="type">资源</span>。

`input`  
输入数组，这个数组的长度应该恰好和 <span
class="function">fann\_get\_num\_input</span> 一样长。

`desired_output`  
期望输出数组，这个数组的长度应该恰好和<span
class="function">fann\_get\_num\_output</span> 一样长。

### 返回值

成功时返回 **`true`**，其它情况下返回 **`false`**。

### 参见

-   <span class="function">fann\_train\_on\_data</span>
-   <span class="function">fann\_train\_epoch</span>
-   <span class="function">fann\_get\_num\_input</span>
-   <span class="function">fann\_get\_num\_output</span>

**目录**

-   [fann\_cascadetrain\_on\_data](/ref/fann.html#fann_cascadetrain_on_data)
    — 在整个数据集上训练，使用一段时间的 Cascade2 训练算法。
-   [fann\_cascadetrain\_on\_file](/ref/fann.html#fann_cascadetrain_on_file)
    — 读取文件并在整个数据集上训练，使用 Cascade2 训练算法训练一段时间。
-   [fann\_clear\_scaling\_params](/ref/fann.html#fann_clear_scaling_params)
    — 清除缩放参数
-   [fann\_copy](/ref/fann.html#fann_copy) — 创建一个 fann
    结构体的副本。
-   [fann\_create\_from\_file](/ref/fann.html#fann_create_from_file) —
    从配置文件中构建一个反向传播神经网络。
-   [fann\_create\_shortcut\_array](/ref/fann.html#fann_create_shortcut_array)
    — 创建一个含快捷连接而非全连接的标准反向传播神经网络。
-   [fann\_create\_shortcut](/ref/fann.html#fann_create_shortcut) —
    创建一个含快捷连接而非全连接的标准反向传播神经网络。
-   [fann\_create\_sparse\_array](/ref/fann.html#fann_create_sparse_array)
    —
    创建一个标准的反向传播神经网络，该网络使用一个表示每层大小的数组来构造，但是并不是全连接的。
-   [fann\_create\_sparse](/ref/fann.html#fann_create_sparse) —
    创建一个标准的反向传播神经网络，该网络不是全连接。
-   [fann\_create\_standard\_array](/ref/fann.html#fann_create_standard_array)
    —
    创建一个全连接的反向传播神经网络，该网络使用一个表示每层大小的数组来构造。
-   [fann\_create\_standard](/ref/fann.html#fann_create_standard) —
    创建标准的全连接反向传播神经网络。
-   [fann\_create\_train\_from\_callback](/ref/fann.html#fann_create_train_from_callback)
    — 从用户提供的函数创建训练数据结构。
-   [fann\_create\_train](/ref/fann.html#fann_create_train) —
    创建一个空的训练数据结构。
-   [fann\_descale\_input](/ref/fann.html#fann_descale_input) —
    在获取基于先前计算的参数之后，在输入向量中缩小数据
-   [fann\_descale\_output](/ref/fann.html#fann_descale_output) —
    在获取基于先前计算的参数之后，在输出向量中缩小数据
-   [fann\_descale\_train](/ref/fann.html#fann_descale_train) —
    基于先前计算的参数来缩小输入和输出数据
-   [fann\_destroy\_train](/ref/fann.html#fann_destroy_train) —
    销毁训练数据。
-   [fann\_destroy](/ref/fann.html#fann_destroy) —
    销毁整个网络并且适当地释放所有的关联内存。
-   [fann\_duplicate\_train\_data](/ref/fann.html#fann_duplicate_train_data)
    — 返回 fann 训练数据精确的副本。
-   [fann\_get\_activation\_function](/ref/fann.html#fann_get_activation_function)
    — 返回激励函数
-   [fann\_get\_activation\_steepness](/ref/fann.html#fann_get_activation_steepness)
    — 为提供的神经和网络层数返回激活陡度
-   [fann\_get\_bias\_array](/ref/fann.html#fann_get_bias_array) —
    获取网络中每一层的偏差数
-   [fann\_get\_bit\_fail\_limit](/ref/fann.html#fann_get_bit_fail_limit)
    — 返回训练期间使用的误差限制
-   [fann\_get\_bit\_fail](/ref/fann.html#fann_get_bit_fail) —
    失败位的数量
-   [fann\_get\_cascade\_activation\_functions\_count](/ref/fann.html#fann_get_cascade_activation_functions_count)
    — 返回级联激活函数的数量
-   [fann\_get\_cascade\_activation\_functions](/ref/fann.html#fann_get_cascade_activation_functions)
    — 返回级联激活函数
-   [fann\_get\_cascade\_activation\_steepnesses\_count](/ref/fann.html#fann_get_cascade_activation_steepnesses_count)
    — 激活陡度的数量
-   [fann\_get\_cascade\_activation\_steepnesses](/ref/fann.html#fann_get_cascade_activation_steepnesses)
    — 返回级联激活陡度
-   [fann\_get\_cascade\_candidate\_change\_fraction](/ref/fann.html#fann_get_cascade_candidate_change_fraction)
    — 返回级联候选变化分数
-   [fann\_get\_cascade\_candidate\_limit](/ref/fann.html#fann_get_cascade_candidate_limit)
    — 返回候选限度
-   [fann\_get\_cascade\_candidate\_stagnation\_epochs](/ref/fann.html#fann_get_cascade_candidate_stagnation_epochs)
    — 返回层叠候选停滞周期的数量
-   [fann\_get\_cascade\_max\_cand\_epochs](/ref/fann.html#fann_get_cascade_max_cand_epochs)
    — 返回候选周期的最大值
-   [fann\_get\_cascade\_max\_out\_epochs](/ref/fann.html#fann_get_cascade_max_out_epochs)
    — 返回输出周期的最大值
-   [fann\_get\_cascade\_min\_cand\_epochs](/ref/fann.html#fann_get_cascade_min_cand_epochs)
    — 返回最小的候选周期
-   [fann\_get\_cascade\_min\_out\_epochs](/ref/fann.html#fann_get_cascade_min_out_epochs)
    — 返回最小输出周期
-   [fann\_get\_cascade\_num\_candidate\_groups](/ref/fann.html#fann_get_cascade_num_candidate_groups)
    — 返回候选组的数量
-   [fann\_get\_cascade\_num\_candidates](/ref/fann.html#fann_get_cascade_num_candidates)
    — 返回训练期间使用的候选数量
-   [fann\_get\_cascade\_output\_change\_fraction](/ref/fann.html#fann_get_cascade_output_change_fraction)
    — 返回级联输出变化分数
-   [fann\_get\_cascade\_output\_stagnation\_epochs](/ref/fann.html#fann_get_cascade_output_stagnation_epochs)
    — 返回级联输出停滞周期的数量
-   [fann\_get\_cascade\_weight\_multiplier](/ref/fann.html#fann_get_cascade_weight_multiplier)
    — 返回权重因子
-   [fann\_get\_connection\_array](/ref/fann.html#fann_get_connection_array)
    — 获取网络中的连接。
-   [fann\_get\_connection\_rate](/ref/fann.html#fann_get_connection_rate)
    — 获取当网络创建时连接的使用率。
-   [fann\_get\_errno](/ref/fann.html#fann_get_errno) —
    返回最后一个错误数字。
-   [fann\_get\_errstr](/ref/fann.html#fann_get_errstr) —
    返回最后的错误字符串。
-   [fann\_get\_layer\_array](/ref/fann.html#fann_get_layer_array) —
    获取网络中每层的神经元数量。
-   [fann\_get\_learning\_momentum](/ref/fann.html#fann_get_learning_momentum)
    — 返回学习动量
-   [fann\_get\_learning\_rate](/ref/fann.html#fann_get_learning_rate) —
    返回学习速率
-   [fann\_get\_MSE](/ref/fann.html#fann_get_MSE) —
    从网络中读取均方误差。
-   [fann\_get\_network\_type](/ref/fann.html#fann_get_network_type) —
    获取所创建的神经网络类型。
-   [fann\_get\_num\_input](/ref/fann.html#fann_get_num_input) —
    获取输入神经元的数量。
-   [fann\_get\_num\_layers](/ref/fann.html#fann_get_num_layers) —
    获取神经网络的层数。
-   [fann\_get\_num\_output](/ref/fann.html#fann_get_num_output) —
    获取输出神经元的数量。
-   [fann\_get\_quickprop\_decay](/ref/fann.html#fann_get_quickprop_decay)
    — 返回衰退值，用于在 quickprop 训练迭代时衰减权重
-   [fann\_get\_quickprop\_mu](/ref/fann.html#fann_get_quickprop_mu) —
    返回放大系数
-   [fann\_get\_rprop\_decrease\_factor](/ref/fann.html#fann_get_rprop_decrease_factor)
    — 返回 RPROP 训练期间的衰减系数
-   [fann\_get\_rprop\_delta\_max](/ref/fann.html#fann_get_rprop_delta_max)
    — 返回最大步长
-   [fann\_get\_rprop\_delta\_min](/ref/fann.html#fann_get_rprop_delta_min)
    — 返回最小步长
-   [fann\_get\_rprop\_delta\_zero](/ref/fann.html#fann_get_rprop_delta_zero)
    — 返回初始步长
-   [fann\_get\_rprop\_increase\_factor](/ref/fann.html#fann_get_rprop_increase_factor)
    — 返回 RPROP 训练的递增系数
-   [fann\_get\_sarprop\_step\_error\_shift](/ref/fann.html#fann_get_sarprop_step_error_shift)
    — 返回 sarprop 步值的误差偏移
-   [fann\_get\_sarprop\_step\_error\_threshold\_factor](/ref/fann.html#fann_get_sarprop_step_error_threshold_factor)
    — 返回 sarprop 算法步值的误差阈值系数
-   [fann\_get\_sarprop\_temperature](/ref/fann.html#fann_get_sarprop_temperature)
    — 返回 sarprop 算法温度
-   [fann\_get\_sarprop\_weight\_decay\_shift](/ref/fann.html#fann_get_sarprop_weight_decay_shift)
    — 返回 sarprop 算法权重衰减变化值
-   [fann\_get\_total\_connections](/ref/fann.html#fann_get_total_connections)
    — 获取整个网络中所有的连接数。
-   [fann\_get\_total\_neurons](/ref/fann.html#fann_get_total_neurons) —
    获取整个网络中神经元的数量。
-   [fann\_get\_train\_error\_function](/ref/fann.html#fann_get_train_error_function)
    — 返回训练中使用的错误函数。
-   [fann\_get\_train\_stop\_function](/ref/fann.html#fann_get_train_stop_function)
    — 返回训练中使用的停止函数。
-   [fann\_get\_training\_algorithm](/ref/fann.html#fann_get_training_algorithm)
    — 返回训练算法。
-   [fann\_init\_weights](/ref/fann.html#fann_init_weights) — 使用
    Widrow 和 Nguyen 算法初始化权重。
-   [fann\_length\_train\_data](/ref/fann.html#fann_length_train_data) —
    返回训练数据中训练模式的数量。
-   [fann\_merge\_train\_data](/ref/fann.html#fann_merge_train_data) —
    合并训练数据。
-   [fann\_num\_input\_train\_data](/ref/fann.html#fann_num_input_train_data)
    — 返回训练数据中每个训练模式输入的数量。
-   [fann\_num\_output\_train\_data](/ref/fann.html#fann_num_output_train_data)
    — 返回训练数据中每个训练模式输出的数量。
-   [fann\_print\_error](/ref/fann.html#fann_print_error) —
    打印错误字符串。
-   [fann\_randomize\_weights](/ref/fann.html#fann_randomize_weights) —
    给每个连接赋一个介于 min\_weight 和 max\_weight 之间的随机权重。
-   [fann\_read\_train\_from\_file](/ref/fann.html#fann_read_train_from_file)
    — 读取存储训练数据的文件。
-   [fann\_reset\_errno](/ref/fann.html#fann_reset_errno) —
    重置最后的错误代码。
-   [fann\_reset\_errstr](/ref/fann.html#fann_reset_errstr) —
    重置最后的错误字符串。
-   [fann\_reset\_MSE](/ref/fann.html#fann_reset_MSE) —
    重置网络中的均方误差。
-   [fann\_run](/ref/fann.html#fann_run) — 将通过神经网络运行输入。
-   [fann\_save\_train](/ref/fann.html#fann_save_train) —
    将训练结构体保存至文件。
-   [fann\_save](/ref/fann.html#fann_save) — 将整个网络保存至配置文件。
-   [fann\_scale\_input\_train\_data](/ref/fann.html#fann_scale_input_train_data)
    — 在训练数据中缩放输入至指定范围
-   [fann\_scale\_input](/ref/fann.html#fann_scale_input) —
    在以前计算参数的基础上，在训练之前放大输入向量中的数据
-   [fann\_scale\_output\_train\_data](/ref/fann.html#fann_scale_output_train_data)
    — 在训练数据中缩放输出至指定范围
-   [fann\_scale\_output](/ref/fann.html#fann_scale_output) —
    在以前计算参数的基础上，在训练之前放大输出向量中的数据
-   [fann\_scale\_train\_data](/ref/fann.html#fann_scale_train_data) —
    在训练数据中缩放输入和输出到指定的范围
-   [fann\_scale\_train](/ref/fann.html#fann_scale_train) —
    在以前计算参数的基础上，缩放输入和输出数据
-   [fann\_set\_activation\_function\_hidden](/ref/fann.html#fann_set_activation_function_hidden)
    — 为所有隐藏层设置激活函数
-   [fann\_set\_activation\_function\_layer](/ref/fann.html#fann_set_activation_function_layer)
    — 为已应用的层中所有的神经元设置激活函数。
-   [fann\_set\_activation\_function\_output](/ref/fann.html#fann_set_activation_function_output)
    — 为输出层设置激活函数
-   [fann\_set\_activation\_function](/ref/fann.html#fann_set_activation_function)
    — 为已应用的神经元和层设置激活函数
-   [fann\_set\_activation\_steepness\_hidden](/ref/fann.html#fann_set_activation_steepness_hidden)
    — 为所有隐藏层中所有的神经元设置激活函数陡度
-   [fann\_set\_activation\_steepness\_layer](/ref/fann.html#fann_set_activation_steepness_layer)
    — 为提供的层中所有的神经元设置激活陡度
-   [fann\_set\_activation\_steepness\_output](/ref/fann.html#fann_set_activation_steepness_output)
    — 在输出层中设置激活陡度
-   [fann\_set\_activation\_steepness](/ref/fann.html#fann_set_activation_steepness)
    — 为提供的神经元和层设置激活陡度
-   [fann\_set\_bit\_fail\_limit](/ref/fann.html#fann_set_bit_fail_limit)
    — 设置训练期间使用的误差
-   [fann\_set\_callback](/ref/fann.html#fann_set_callback) —
    设置训练期间使用的回调函数。
-   [fann\_set\_cascade\_activation\_functions](/ref/fann.html#fann_set_cascade_activation_functions)
    — 设置级联候选激活函数的数组
-   [fann\_set\_cascade\_activation\_steepnesses](/ref/fann.html#fann_set_cascade_activation_steepnesses)
    — 设置级联候选激活陡度的数组。
-   [fann\_set\_cascade\_candidate\_change\_fraction](/ref/fann.html#fann_set_cascade_candidate_change_fraction)
    — 设置级联候选更改分数
-   [fann\_set\_cascade\_candidate\_limit](/ref/fann.html#fann_set_cascade_candidate_limit)
    — 设置候选限度
-   [fann\_set\_cascade\_candidate\_stagnation\_epochs](/ref/fann.html#fann_set_cascade_candidate_stagnation_epochs)
    — 设置级联候选停止周期数
-   [fann\_set\_cascade\_max\_cand\_epochs](/ref/fann.html#fann_set_cascade_max_cand_epochs)
    — 设置最大候选周期数
-   [fann\_set\_cascade\_max\_out\_epochs](/ref/fann.html#fann_set_cascade_max_out_epochs)
    — 设置最大输出周期
-   [fann\_set\_cascade\_min\_cand\_epochs](/ref/fann.html#fann_set_cascade_min_cand_epochs)
    — 设置最小候选周期
-   [fann\_set\_cascade\_min\_out\_epochs](/ref/fann.html#fann_set_cascade_min_out_epochs)
    — 设置最小输出周期
-   [fann\_set\_cascade\_num\_candidate\_groups](/ref/fann.html#fann_set_cascade_num_candidate_groups)
    — 设置候选组数量
-   [fann\_set\_cascade\_output\_change\_fraction](/ref/fann.html#fann_set_cascade_output_change_fraction)
    — 设置级联输出改变分数
-   [fann\_set\_cascade\_output\_stagnation\_epochs](/ref/fann.html#fann_set_cascade_output_stagnation_epochs)
    — 设置级联输出停滞周期的值
-   [fann\_set\_cascade\_weight\_multiplier](/ref/fann.html#fann_set_cascade_weight_multiplier)
    — 设置权重因子
-   [fann\_set\_error\_log](/ref/fann.html#fann_set_error_log) —
    设置错误记录保存的位置。
-   [fann\_set\_input\_scaling\_params](/ref/fann.html#fann_set_input_scaling_params)
    — 根据训练数据计算将来使用的输入比例参数
-   [fann\_set\_learning\_momentum](/ref/fann.html#fann_set_learning_momentum)
    — 设置学习动量。
-   [fann\_set\_learning\_rate](/ref/fann.html#fann_set_learning_rate) —
    设置学习速率。
-   [fann\_set\_output\_scaling\_params](/ref/fann.html#fann_set_output_scaling_params)
    — 根据训练数据计算将来使用的输出缩放参数
-   [fann\_set\_quickprop\_decay](/ref/fann.html#fann_set_quickprop_decay)
    — 设置quickprop算法衰减因子
-   [fann\_set\_quickprop\_mu](/ref/fann.html#fann_set_quickprop_mu) —
    设置 quickprop 算法放大因子
-   [fann\_set\_rprop\_decrease\_factor](/ref/fann.html#fann_set_rprop_decrease_factor)
    — 使用 RPROP 算法训练时，设置下降因子
-   [fann\_set\_rprop\_delta\_max](/ref/fann.html#fann_set_rprop_delta_max)
    — 设置最大步长
-   [fann\_set\_rprop\_delta\_min](/ref/fann.html#fann_set_rprop_delta_min)
    — 设置最小步长
-   [fann\_set\_rprop\_delta\_zero](/ref/fann.html#fann_set_rprop_delta_zero)
    — 设置初始步长
-   [fann\_set\_rprop\_increase\_factor](/ref/fann.html#fann_set_rprop_increase_factor)
    — 使用 RPROP 算法训练时，设置增长因子
-   [fann\_set\_sarprop\_step\_error\_shift](/ref/fann.html#fann_set_sarprop_step_error_shift)
    — 设置 sarprop 算法的步误差偏移量
-   [fann\_set\_sarprop\_step\_error\_threshold\_factor](/ref/fann.html#fann_set_sarprop_step_error_threshold_factor)
    — 设置 sarprop 算法的步误差阈值因子
-   [fann\_set\_sarprop\_temperature](/ref/fann.html#fann_set_sarprop_temperature)
    — 设置 sarprop 算法的温度
-   [fann\_set\_sarprop\_weight\_decay\_shift](/ref/fann.html#fann_set_sarprop_weight_decay_shift)
    — 设置 sarprop 算法的权重衰减偏移值
-   [fann\_set\_scaling\_params](/ref/fann.html#fann_set_scaling_params)
    — 根据训练数据计算输入和输出缩放参数以供将来使用
-   [fann\_set\_train\_error\_function](/ref/fann.html#fann_set_train_error_function)
    — 设置训练期间使用的错误函数。
-   [fann\_set\_train\_stop\_function](/ref/fann.html#fann_set_train_stop_function)
    — 设置训练期间使用的停止函数。
-   [fann\_set\_training\_algorithm](/ref/fann.html#fann_set_training_algorithm)
    — 设置训练算法。
-   [fann\_set\_weight\_array](/ref/fann.html#fann_set_weight_array) —
    在网络中设置一个连接。
-   [fann\_set\_weight](/ref/fann.html#fann_set_weight) —
    在网络中设置一个连接。
-   [fann\_shuffle\_train\_data](/ref/fann.html#fann_shuffle_train_data)
    — 打算训练数据，使顺序随机。
-   [fann\_subset\_train\_data](/ref/fann.html#fann_subset_train_data) —
    返回一个训练数据子集的副本。
-   [fann\_test\_data](/ref/fann.html#fann_test_data) —
    使用训练数据来测试并且计算出 MSE
-   [fann\_test](/ref/fann.html#fann_test) —
    使用一组输入和一组期望的输出来测试。
-   [fann\_train\_epoch](/ref/fann.html#fann_train_epoch) —
    使用一组训练数据训练一个周期。
-   [fann\_train\_on\_data](/ref/fann.html#fann_train_on_data) —
    在整个数据集上训练一段时间。
-   [fann\_train\_on\_file](/ref/fann.html#fann_train_on_file) —
    在从某个文件读取的整个数据集上训练一段时间。
-   [fann\_train](/ref/fann.html#fann_train) —
    使用一个输入集和一个期望的输出集来迭代训练一次。
