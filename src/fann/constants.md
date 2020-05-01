预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`FANN_TRAIN_INCREMENTAL`** (<span class="type">integer</span>)  
<span class="simpara">
标准反向传播算法，每次训练匹配后权重都会更新。这意味着在每个单历元中权重会被更新很多次。因为这个原因，很多问题使用这个算法将会训练的非常快，然而其他更高级的问题的训练效果不是很好。
</span>

**`FANN_TRAIN_BATCH`** (<span class="type">integer</span>)  
<span class="simpara">
标准反向传播算法，计算均方差误差后权重值将会更新。
这意味着每个单历元只会更新一次。因为这个原因，很多问题使用这个算法会训练的很慢。但是计算出的均方差误差比增量训练的效果更好，使用这个算法某些问题将会得到更好的解决方案。
</span>

**`FANN_TRAIN_RPROP`** (<span class="type">integer</span>)  
<span class="simpara">
一个更高级的批训练算法，对于很多问题该算法还会获得很好的结果。RPROP
训练算法是自适应的，因此不需要使用 learning\_rate. 其他一些参数用来设置
RPROP 算法工作的方式，只推荐给那些知道 RPROP
算法如何工作的人来设置。RPROP 训练算法是被 Riedmiller 和 BraunSome
在1993年提出来的，实际上此处使用的是由 Igel 和 Husken 在2000年提出来的
iRPROP 训练算法，它是标准 RPROP 训练算法的一个变种。 </span>

**`FANN_TRAIN_QUICKPROP`** (<span class="type">integer</span>)  
<span class="simpara">
一个更高级的批训练算法，对于很多问题该算法还会获得很好的结果。quickprop
训练算法使用 learning\_rate 参数和其他更高级的参数，
但是只有当用户真正明白 quickprop
训练算法如何工作的时候才建议修改这些高级参数。 quickprop 训练算法是被
Fahlman 在1988年描述的。 </span>

**`FANN_TRAIN_SARPROP`** (<span class="type">integer</span>)  
<span class="simpara"> 更高级的训练算法，只在2.2版本中可用。 </span>

<!-- -->

**`FANN_LINEAR`** (<span class="type">integer</span>)  
<span class="simpara"> 线性激励函数。 </span>

**`FANN_THRESHOLD`** (<span class="type">integer</span>)  
<span class="simpara"> 阈值激励函数。 </span>

**`FANN_THRESHOLD_SYMMETRIC`** (<span class="type">integer</span>)  
<span class="simpara"> 阈值激励函数。 </span>

**`FANN_SIGMOID`** (<span class="type">integer</span>)  
<span class="simpara"> Sigmoid激励函数。 </span>

**`FANN_SIGMOID_STEPWISE`** (<span class="type">integer</span>)  
<span class="simpara"> 逐步线性逼近 Sigmoid 激励函数。 </span>

**`FANN_SIGMOID_SYMMETRIC`** (<span class="type">integer</span>)  
<span class="simpara"> 对称 Sigmoid 激励函数， 又名：tanh. </span>

**`FANN_SIGMOID_SYMMETRIC_STEPWISE`** (<span class="type">integer</span>)  
<span class="simpara"> 逐步线性逼近对称 Sigmoid 激励函数。 </span>

**`FANN_GAUSSIAN`** (<span class="type">integer</span>)  
<span class="simpara"> Gaussian (高斯) 激励函数。 </span>

**`FANN_GAUSSIAN_SYMMETRIC`** (<span class="type">integer</span>)  
<span class="simpara"> 对称 gaussian (高斯)激励函数。 </span>

**`FANN_GAUSSIAN_STEPWISE`** (<span class="type">integer</span>)  
<span class="simpara"> 逐步 gaussian (高斯)激励函数。 </span>

**`FANN_ELLIOT`** (<span class="type">integer</span>)  
<span class="simpara"> 快速(类sigmoid)激励函数，由 David Elliott
定义的。 </span>

**`FANN_ELLIOT_SYMMETRIC`** (<span class="type">integer</span>)  
<span class="simpara"> 快速(类对称sigmoid)激励函数，由 David
Elliott定义的。 </span>

**`FANN_LINEAR_PIECE`** (<span class="type">integer</span>)  
<span class="simpara"> 有界线性激励函数。 </span>

**`FANN_LINEAR_PIECE_SYMMETRIC`** (<span class="type">integer</span>)  
<span class="simpara"> 有界线性激励函数。 </span>

**`FANN_SIN_SYMMETRIC`** (<span class="type">integer</span>)  
<span class="simpara"> 周期sin(正弦)激励函数。 </span>

**`FANN_COS_SYMMETRIC`** (<span class="type">integer</span>)  
<span class="simpara"> 周期cos(余弦)激励函数。 </span>

**`FANN_SIN`** (<span class="type">integer</span>)  
<span class="simpara"> 周期sin(正弦)激励函数。 </span>

**`FANN_COS`** (<span class="type">integer</span>)  
<span class="simpara"> 周期cos(余弦)激励函数。 </span>

<!-- -->

**`FANN_ERRORFUNC_LINEAR`** (<span class="type">integer</span>)  
<span class="simpara"> 标准线性误差函数。 </span>

**`FANN_ERRORFUNC_TANH`** (<span class="type">integer</span>)  
<span class="simpara"> Tanh 误差函数，
通常更好但是要求更低的学习率。该误差函数当有目标输出时将会和期望值有很大的不同，然而没有目标输出时只有很小不同。此激励函数在层叠训练和增量训练。
</span>

<!-- -->

**`FANN_STOPFUNC_MSE`** (<span class="type">integer</span>)  
<span class="simpara"> 停止准则是均方误差(MSE)值。 </span>

**`FANN_STOPFUNC_BIT`** (<span class="type">integer</span>)  
<span class="simpara">
停止准则是失败时的比特位数。比特位数意味着输出神经元的个数超过了失败时的比特位数
(参考 fann\_get\_bit\_fail\_limit, fann\_set\_bit\_fail\_limit).
位数在所有的训练数据中都会被计数，所以这个数组将会比训练数据的数量更高。
</span>

<!-- -->

**`FANN_NETTYPE_LAYER`** (<span class="type">integer</span>)  
<span class="simpara"> 每一层只能连接下一层。 </span>

**`FANN_NETTYPE_SHORTCUT`** (<span class="type">integer</span>)  
<span class="simpara"> 每一层与所有以下层有连接。 </span>

<!-- -->

**`FANN_E_NO_ERROR`** (<span class="type">integer</span>)  
<span class="simpara"> 无误差。 </span>

**`FANN_E_CANT_OPEN_CONFIG_R`** (<span class="type">integer</span>)  
<span class="simpara"> 无法打开读取配置文件。 </span>

**`FANN_E_CANT_OPEN_CONFIG_W`** (<span class="type">integer</span>)  
<span class="simpara"> 无法打开写入配置文件。 </span>

**`FANN_E_WRONG_CONFIG_VERSION`** (<span class="type">integer</span>)  
<span class="simpara"> 配置文件的错误版本。 </span>

**`FANN_E_CANT_READ_CONFIG`** (<span class="type">integer</span>)  
<span class="simpara"> 从配置文件读取信息的错误。 </span>

**`FANN_E_CANT_READ_NEURON`** (<span class="type">integer</span>)  
<span class="simpara"> 从配置文件读取神经元信息的错误。 </span>

**`FANN_E_CANT_READ_CONNECTIONS`** (<span class="type">integer</span>)  
<span class="simpara"> 从配置文件读取连接的错误。 </span>

**`FANN_E_WRONG_NUM_CONNECTIONS`** (<span class="type">integer</span>)  
<span class="simpara"> 连接数和期望的值不相等。 </span>

**`FANN_E_CANT_OPEN_TD_W`** (<span class="type">integer</span>)  
<span class="simpara"> 无法打开训练数据文件写入内容。 </span>

**`FANN_E_CANT_OPEN_TD_R`** (<span class="type">integer</span>)  
<span class="simpara"> 无法打开训练数据文件读取内容。 </span>

**`FANN_E_CANT_READ_TD`** (<span class="type">integer</span>)  
<span class="simpara"> 从文件读取训练数据错误。 </span>

**`FANN_E_CANT_ALLOCATE_MEM`** (<span class="type">integer</span>)  
<span class="simpara"> 无法分配内存。 </span>

**`FANN_E_CANT_TRAIN_ACTIVATION`** (<span class="type">integer</span>)  
<span class="simpara"> 无法使用已选的激励函数训练。 </span>

**`FANN_E_CANT_USE_ACTIVATION`** (<span class="type">integer</span>)  
<span class="simpara"> 无法使用已选的激励函数。 </span>

**`FANN_E_TRAIN_DATA_MISMATCH`** (<span class="type">integer</span>)  
<span class="simpara"> 两个 fann\_train\_data
结构体之间存在不可调和的差异。 </span>

**`FANN_E_CANT_USE_TRAIN_ALG`** (<span class="type">integer</span>)  
<span class="simpara"> 不能使用已选的训练算法。 </span>

**`FANN_E_TRAIN_DATA_SUBSET`** (<span class="type">integer</span>)  
<span class="simpara"> 尝试获取不在训练集内的子集。 </span>

**`FANN_E_INDEX_OUT_OF_BOUND`** (<span class="type">integer</span>)  
<span class="simpara"> 索引超出了界限。 </span>

**`FANN_E_SCALE_NOT_PRESENT`** (<span class="type">integer</span>)  
<span class="simpara"> 标定参数不存在。 </span>

**`FANN_E_INPUT_NO_MATCH`** (<span class="type">integer</span>)  
<span class="simpara"> 在人工神经网络和数据中的输入神经元个数不匹配。
</span>

**`FANN_E_OUTPUT_NO_MATCH`** (<span class="type">integer</span>)  
<span class="simpara"> 在人工神经网络和数据中的输出神经元个数不匹配。
</span>
