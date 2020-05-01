Other Changes
-------------

### 放宽了保留词限制

现在允许全局保留词用于类/接口/Trait 中的属性、常量和方法名。
在引入新关键词时，此变更减少了对向后兼容的破坏，避免了 API 命名的限制。

使用流畅的接口实现内部 DSL 时，这非常有用：

``` php
<?php
// 以前不能用  'new'、'private' 和 'for'
Project::new('Project Name')->private()->for('purpose here')->with('username here');
?>
```

唯一的限制是： *class*关键词不能用于常量名，否则会和 类名解析语法冲突
(*ClassName::class*)。

### 移除 date.timezone 警告

调用任意 date- 开头或者其他基于时间的函数时， 未设置 `date.timezone` INI
设置的情况下， 之前会产生警告。 现在移除了警告（`date.timezone`
默认仍然是 UTC）
