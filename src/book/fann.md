FANN (快速人工神经网络)
=======================

**目录**

-   [简介](/intro/fann.html)
-   [安装／配置](/fann/setup.html)
    -   [需求](/fann/setup.html#需求)
    -   [安装](/fann/setup.html#安装)
    -   [运行时配置](/fann/setup.html#运行时配置)
    -   [资源类型](/fann/setup.html#资源类型)
-   [预定义常量](/fann/constants.html)
-   [范例](/fann/examples.html)
    -   [XOR (异或)训练](/fann/examples.html#XOR%20(异或)训练)
-   [Fann 函数](/ref/fann.html)
    -   [fann\_cascadetrain\_on\_data](/ref/fann.html#fann_cascadetrain_on_data)
        — 在整个数据集上训练，使用一段时间的 Cascade2 训练算法。
    -   [fann\_cascadetrain\_on\_file](/ref/fann.html#fann_cascadetrain_on_file)
        — 读取文件并在整个数据集上训练，使用 Cascade2
        训练算法训练一段时间。
    -   [fann\_clear\_scaling\_params](/ref/fann.html#fann_clear_scaling_params)
        — 清除缩放参数
    -   [fann\_copy](/ref/fann.html#fann_copy) — 创建一个 fann
        结构体的副本。
    -   [fann\_create\_from\_file](/ref/fann.html#fann_create_from_file)
        — 从配置文件中构建一个反向传播神经网络。
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
    -   [fann\_get\_learning\_rate](/ref/fann.html#fann_get_learning_rate)
        — 返回学习速率
    -   [fann\_get\_MSE](/ref/fann.html#fann_get_MSE) —
        从网络中读取均方误差。
    -   [fann\_get\_network\_type](/ref/fann.html#fann_get_network_type)
        — 获取所创建的神经网络类型。
    -   [fann\_get\_num\_input](/ref/fann.html#fann_get_num_input) —
        获取输入神经元的数量。
    -   [fann\_get\_num\_layers](/ref/fann.html#fann_get_num_layers) —
        获取神经网络的层数。
    -   [fann\_get\_num\_output](/ref/fann.html#fann_get_num_output) —
        获取输出神经元的数量。
    -   [fann\_get\_quickprop\_decay](/ref/fann.html#fann_get_quickprop_decay)
        — 返回衰退值，用于在 quickprop 训练迭代时衰减权重
    -   [fann\_get\_quickprop\_mu](/ref/fann.html#fann_get_quickprop_mu)
        — 返回放大系数
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
    -   [fann\_get\_total\_neurons](/ref/fann.html#fann_get_total_neurons)
        — 获取整个网络中神经元的数量。
    -   [fann\_get\_train\_error\_function](/ref/fann.html#fann_get_train_error_function)
        — 返回训练中使用的错误函数。
    -   [fann\_get\_train\_stop\_function](/ref/fann.html#fann_get_train_stop_function)
        — 返回训练中使用的停止函数。
    -   [fann\_get\_training\_algorithm](/ref/fann.html#fann_get_training_algorithm)
        — 返回训练算法。
    -   [fann\_init\_weights](/ref/fann.html#fann_init_weights) — 使用
        Widrow 和 Nguyen 算法初始化权重。
    -   [fann\_length\_train\_data](/ref/fann.html#fann_length_train_data)
        — 返回训练数据中训练模式的数量。
    -   [fann\_merge\_train\_data](/ref/fann.html#fann_merge_train_data)
        — 合并训练数据。
    -   [fann\_num\_input\_train\_data](/ref/fann.html#fann_num_input_train_data)
        — 返回训练数据中每个训练模式输入的数量。
    -   [fann\_num\_output\_train\_data](/ref/fann.html#fann_num_output_train_data)
        — 返回训练数据中每个训练模式输出的数量。
    -   [fann\_print\_error](/ref/fann.html#fann_print_error) —
        打印错误字符串。
    -   [fann\_randomize\_weights](/ref/fann.html#fann_randomize_weights)
        — 给每个连接赋一个介于 min\_weight 和 max\_weight
        之间的随机权重。
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
    -   [fann\_save](/ref/fann.html#fann_save) —
        将整个网络保存至配置文件。
    -   [fann\_scale\_input\_train\_data](/ref/fann.html#fann_scale_input_train_data)
        — 在训练数据中缩放输入至指定范围
    -   [fann\_scale\_input](/ref/fann.html#fann_scale_input) —
        在以前计算参数的基础上，在训练之前放大输入向量中的数据
    -   [fann\_scale\_output\_train\_data](/ref/fann.html#fann_scale_output_train_data)
        — 在训练数据中缩放输出至指定范围
    -   [fann\_scale\_output](/ref/fann.html#fann_scale_output) —
        在以前计算参数的基础上，在训练之前放大输出向量中的数据
    -   [fann\_scale\_train\_data](/ref/fann.html#fann_scale_train_data)
        — 在训练数据中缩放输入和输出到指定的范围
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
    -   [fann\_set\_learning\_rate](/ref/fann.html#fann_set_learning_rate)
        — 设置学习速率。
    -   [fann\_set\_output\_scaling\_params](/ref/fann.html#fann_set_output_scaling_params)
        — 根据训练数据计算将来使用的输出缩放参数
    -   [fann\_set\_quickprop\_decay](/ref/fann.html#fann_set_quickprop_decay)
        — 设置quickprop算法衰减因子
    -   [fann\_set\_quickprop\_mu](/ref/fann.html#fann_set_quickprop_mu)
        — 设置 quickprop 算法放大因子
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
    -   [fann\_set\_weight\_array](/ref/fann.html#fann_set_weight_array)
        — 在网络中设置一个连接。
    -   [fann\_set\_weight](/ref/fann.html#fann_set_weight) —
        在网络中设置一个连接。
    -   [fann\_shuffle\_train\_data](/ref/fann.html#fann_shuffle_train_data)
        — 打算训练数据，使顺序随机。
    -   [fann\_subset\_train\_data](/ref/fann.html#fann_subset_train_data)
        — 返回一个训练数据子集的副本。
    -   [fann\_test\_data](/ref/fann.html#fann_test_data) —
        使用训练数据来测试并且计算出 MSE .
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
-   [FANNConnection](/class/fannconnection.html) — FANNConnection 类
    -   [FANNConnection::\_\_construct](/class/fannconnection.html#FANNConnection::__construct)
        — 连接构造器
    -   [FANNConnection::getFromNeuron](/class/fannconnection.html#FANNConnection::getFromNeuron)
        — 返回开始连接的神经元。
    -   [FANNConnection::getToNeuron](/class/fannconnection.html#FANNConnection::getToNeuron)
        — 返回终止神经元的位置。
    -   [FANNConnection::getWeight](/class/fannconnection.html#FANNConnection::getWeight)
        — 返回连接权重。
    -   [FANNConnection::setWeight](/class/fannconnection.html#FANNConnection::setWeight)
        — 设置连接权重。

简介
----

<span class="classname">FANNConnection</span> 被用于神经网络的连接。
该类的对象一般在<span
class="function">fann\_get\_connection\_array</span> 和 <span
class="function">fann\_set\_weight\_array</span>函数中被使用。

类摘要
------

**FANNConnection**

<span class="ooclass"> class **FANNConnection** </span> {

/\* 属性 \*/

<span class="modifier">public</span> `$from_neuron` ;

<span class="modifier">public</span> `$to_neuron` ;

<span class="modifier">public</span> `$weight` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">int</span> `$from_neuron`</span>
, <span class="methodparam"><span class="type">int</span>
`$to_neuron`</span> , <span class="methodparam"><span
class="type">float</span> `$weight`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getFromNeuron</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getToNeuron</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getWeight</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setWeight</span> ( <span
class="methodparam"><span class="type">float</span> `$weight`</span> )

}

属性
----

`from_neuron`  
开始连接的神经元。

`to_neuron`  
结束连接的神经元。

`weight`  
连接的权重。

FANNConnection::\_\_construct
=============================

连接构造器

### 说明

<span class="modifier">public</span> <span
class="methodname">FANNConnection::\_\_construct</span> ( <span
class="methodparam"><span class="type">int</span> `$from_neuron`</span>
, <span class="methodparam"><span class="type">int</span>
`$to_neuron`</span> , <span class="methodparam"><span
class="type">float</span> `$weight`</span> )

创建一个新的连接并且初始化它的参数。一旦连接被初始化，只有其权重能被修改。

### 参数

`from_neuron`  
开始连接的神经元。

`to_neuron`  
结束连接的神经元。

`weight`  
连接的权重。

FANNConnection::getFromNeuron
=============================

返回开始连接的神经元。

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">FANNConnection::getFromNeuron</span> ( <span
class="methodparam">void</span> )

返回开始连接的神经元。

### 参数

此函数没有参数。

### 返回值

开始连接的神经元。

FANNConnection::getToNeuron
===========================

返回终止神经元的位置。

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">FANNConnection::getToNeuron</span> ( <span
class="methodparam">void</span> )

返回终止神经元的位置。

### 参数

此函数没有参数。

### 返回值

终止神经元的位置。

FANNConnection::getWeight
=========================

返回连接权重。

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">FANNConnection::getWeight</span> ( <span
class="methodparam">void</span> )

返回连接权重。

### 参数

此函数没有参数。

### 返回值

连接权重。

FANNConnection::setWeight
=========================

设置连接权重。

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">FANNConnection::setWeight</span> ( <span
class="methodparam"><span class="type">float</span> `$weight`</span> )

设置连接权重。

该方法不同于 <span class="function">fann\_set\_weight</span> 方法.
该方法不会网络中的权重值。只有当调用了 <span
class="function">fann\_set\_weight\_array</span>
方法后网络中的权重值才会更改。

### 参数

`weight`  
连接权重。

### 返回值

成功时返回 **`TRUE`**，其它情况下返回 **`FALSE`**。
