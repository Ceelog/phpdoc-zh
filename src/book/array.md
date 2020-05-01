数组
====

**目录**

-   [简介](/intro/array.html)
-   [安装／配置](/array/setup.html)
    -   [需求](/array/setup.html#需求)
    -   [安装](/array/setup.html#安装)
    -   [运行时配置](/array/setup.html#运行时配置)
    -   [资源类型](/array/setup.html#资源类型)
-   [预定义常量](/array/constants.html)
-   [对数组进行排序](/array/sorting.html)
-   [数组 函数](/ref/array.html)
    -   [array\_change\_key\_case](/ref/array.html#array_change_key_case)
        — 将数组中的所有键名修改为全大写或小写
    -   [array\_chunk](/ref/array.html#array_chunk) —
        将一个数组分割成多个
    -   [array\_column](/ref/array.html#array_column) —
        返回数组中指定的一列
    -   [array\_combine](/ref/array.html#array_combine) —
        创建一个数组，用一个数组的值作为其键名，另一个数组的值作为其值
    -   [array\_count\_values](/ref/array.html#array_count_values) —
        统计数组中所有的值
    -   [array\_diff\_assoc](/ref/array.html#array_diff_assoc) —
        带索引检查计算数组的差集
    -   [array\_diff\_key](/ref/array.html#array_diff_key) —
        使用键名比较计算数组的差集
    -   [array\_diff\_uassoc](/ref/array.html#array_diff_uassoc) —
        用用户提供的回调函数做索引检查来计算数组的差集
    -   [array\_diff\_ukey](/ref/array.html#array_diff_ukey) —
        用回调函数对键名比较计算数组的差集
    -   [array\_diff](/ref/array.html#array_diff) — 计算数组的差集
    -   [array\_fill\_keys](/ref/array.html#array_fill_keys) —
        使用指定的键和值填充数组
    -   [array\_fill](/ref/array.html#array_fill) — 用给定的值填充数组
    -   [array\_filter](/ref/array.html#array_filter) —
        用回调函数过滤数组中的单元
    -   [array\_flip](/ref/array.html#array_flip) — 交换数组中的键和值
    -   [array\_intersect\_assoc](/ref/array.html#array_intersect_assoc)
        — 带索引检查计算数组的交集
    -   [array\_intersect\_key](/ref/array.html#array_intersect_key) —
        使用键名比较计算数组的交集
    -   [array\_intersect\_uassoc](/ref/array.html#array_intersect_uassoc)
        — 带索引检查计算数组的交集，用回调函数比较索引
    -   [array\_intersect\_ukey](/ref/array.html#array_intersect_ukey) —
        用回调函数比较键名来计算数组的交集
    -   [array\_intersect](/ref/array.html#array_intersect) —
        计算数组的交集
    -   [array\_key\_exists](/ref/array.html#array_key_exists) —
        检查数组里是否有指定的键名或索引
    -   [array\_key\_first](/ref/array.html#array_key_first) — Gets the
        first key of an array
    -   [array\_key\_last](/ref/array.html#array_key_last) — Gets the
        last key of an array
    -   [array\_keys](/ref/array.html#array_keys) —
        返回数组中部分的或所有的键名
    -   [array\_map](/ref/array.html#array_map) —
        为数组的每个元素应用回调函数
    -   [array\_merge\_recursive](/ref/array.html#array_merge_recursive)
        — 递归地合并一个或多个数组
    -   [array\_merge](/ref/array.html#array_merge) — 合并一个或多个数组
    -   [array\_multisort](/ref/array.html#array_multisort) —
        对多个数组或多维数组进行排序
    -   [array\_pad](/ref/array.html#array_pad) —
        以指定长度将一个值填充进数组
    -   [array\_pop](/ref/array.html#array_pop) —
        弹出数组最后一个单元（出栈）
    -   [array\_product](/ref/array.html#array_product) —
        计算数组中所有值的乘积
    -   [array\_push](/ref/array.html#array_push) —
        将一个或多个单元压入数组的末尾（入栈）
    -   [array\_rand](/ref/array.html#array_rand) —
        从数组中随机取出一个或多个单元
    -   [array\_reduce](/ref/array.html#array_reduce) —
        用回调函数迭代地将数组简化为单一的值
    -   [array\_replace\_recursive](/ref/array.html#array_replace_recursive)
        — 使用传递的数组递归替换第一个数组的元素
    -   [array\_replace](/ref/array.html#array_replace) —
        使用传递的数组替换第一个数组的元素
    -   [array\_reverse](/ref/array.html#array_reverse) —
        返回单元顺序相反的数组
    -   [array\_search](/ref/array.html#array_search) —
        在数组中搜索给定的值，如果成功则返回首个相应的键名
    -   [array\_shift](/ref/array.html#array_shift) —
        将数组开头的单元移出数组
    -   [array\_slice](/ref/array.html#array_slice) — 从数组中取出一段
    -   [array\_splice](/ref/array.html#array_splice) —
        去掉数组中的某一部分并用其它值取代
    -   [array\_sum](/ref/array.html#array_sum) — 对数组中所有值求和
    -   [array\_udiff\_assoc](/ref/array.html#array_udiff_assoc) —
        带索引检查计算数组的差集，用回调函数比较数据
    -   [array\_udiff\_uassoc](/ref/array.html#array_udiff_uassoc) —
        带索引检查计算数组的差集，用回调函数比较数据和索引
    -   [array\_udiff](/ref/array.html#array_udiff) —
        用回调函数比较数据来计算数组的差集
    -   [array\_uintersect\_assoc](/ref/array.html#array_uintersect_assoc)
        — 带索引检查计算数组的交集，用回调函数比较数据
    -   [array\_uintersect\_uassoc](/ref/array.html#array_uintersect_uassoc)
        — 带索引检查计算数组的交集，用单独的回调函数比较数据和索引
    -   [array\_uintersect](/ref/array.html#array_uintersect) —
        计算数组的交集，用回调函数比较数据
    -   [array\_unique](/ref/array.html#array_unique) —
        移除数组中重复的值
    -   [array\_unshift](/ref/array.html#array_unshift) —
        在数组开头插入一个或多个单元
    -   [array\_values](/ref/array.html#array_values) —
        返回数组中所有的值
    -   [array\_walk\_recursive](/ref/array.html#array_walk_recursive) —
        对数组中的每个成员递归地应用用户函数
    -   [array\_walk](/ref/array.html#array_walk) —
        使用用户自定义函数对数组中的每个元素做回调处理
    -   [array](/ref/array.html#array) — 新建一个数组
    -   [arsort](/ref/array.html#arsort) —
        对数组进行逆向排序并保持索引关系
    -   [asort](/ref/array.html#asort) — 对数组进行排序并保持索引关系
    -   [compact](/ref/array.html#compact) —
        建立一个数组，包括变量名和它们的值
    -   [count](/ref/array.html#count) —
        计算数组中的单元数目，或对象中的属性个数
    -   [current](/ref/array.html#current) — 返回数组中的当前单元
    -   [each](/ref/array.html#each) —
        返回数组中当前的键／值对并将数组指针向前移动一步
    -   [end](/ref/array.html#end) — 将数组的内部指针指向最后一个单元
    -   [extract](/ref/array.html#extract) —
        从数组中将变量导入到当前的符号表
    -   [in\_array](/ref/array.html#in_array) — 检查数组中是否存在某个值
    -   [key\_exists](/ref/array.html#key_exists) — 别名
        array\_key\_exists
    -   [key](/ref/array.html#key) — 从关联数组中取得键名
    -   [krsort](/ref/array.html#krsort) — 对数组按照键名逆向排序
    -   [ksort](/ref/array.html#ksort) — 对数组按照键名排序
    -   [list](/ref/array.html#list) — 把数组中的值赋给一组变量
    -   [natcasesort](/ref/array.html#natcasesort) —
        用“自然排序”算法对数组进行不区分大小写字母的排序
    -   [natsort](/ref/array.html#natsort) — 用“自然排序”算法对数组排序
    -   [next](/ref/array.html#next) — 将数组中的内部指针向前移动一位
    -   [pos](/ref/array.html#pos) — current 的别名
    -   [prev](/ref/array.html#prev) — 将数组的内部指针倒回一位
    -   [range](/ref/array.html#range) —
        根据范围创建数组，包含指定的元素
    -   [reset](/ref/array.html#reset) — 将数组的内部指针指向第一个单元
    -   [rsort](/ref/array.html#rsort) — 对数组逆向排序
    -   [shuffle](/ref/array.html#shuffle) — 打乱数组
    -   [sizeof](/ref/array.html#sizeof) — count 的别名
    -   [sort](/ref/array.html#sort) — 对数组排序
    -   [uasort](/ref/array.html#uasort) —
        使用用户自定义的比较函数对数组中的值进行排序并保持索引关联
    -   [uksort](/ref/array.html#uksort) —
        使用用户自定义的比较函数对数组中的键名进行排序
    -   [usort](/ref/array.html#usort) —
        使用用户自定义的比较函数对数组中的值进行排序
