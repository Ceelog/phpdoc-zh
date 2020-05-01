处理 XForms
===========

<a href="http://www.w3.org/MarkUp/Forms/" class="link external">» XForms</a>
定义了一种传统 web
表单的变种，它可以用于更多的平台和浏览器，甚至非传统的媒体例如 PDF
文档。

XFroms
的第一个关键区别是表单怎样发送到客户端。<a href="http://www.w3.org/MarkUp/Forms/2003/xforms-for-html-authors.html" class="link external">» XForms for HTML Authors</a>
包含有怎样创建 XForms 的详细说明。本节只看一个简单例子。

**示例 \#1 一个简单的 XForms 搜索表单**

``` html
<h:html xmlns:h="http://www.w3.org/1999/xhtml"
        xmlns="http://www.w3.org/2002/xforms">
<h:head>
 <h:title>Search</h:title>
 <model>
  <submission action="http://example.com/search"
              method="post" xml:id="s"/>
 </model>
</h:head>
<h:body>
 <h:p>
  <input ref="q"><label>Find</label></input>
  <submit submission="s"><label>Go</label></submit>
 </h:p>
</h:body>
</h:html>
```

上面的表单显示一个文本输入框（命名为
`q`）和一个提交按钮。当点击提交按钮，表单将被发送到 *action*
所指示的页面。

下面是从 web 应用端的角度看上去的区别。在普通的 HTML
表单中，数据发送格式是 *application/x-www-form-urlencoded*，在 XForms
的世界中，该信息是以 XML 格式数据发送的。

如果选择使用 XForms，那么数据为 XML，这种情况下，在
`$HTTP_RAW_POST_DATA` 中包含了由浏览器产生的 XML
文档，可以将其传递给所偏好的 XSLT 引擎或者文档解析器。

如果对格式不感兴趣，只想让数据进入到传统的 `$_POST`
变量中，可以指示客户端浏览器将其以 *application/x-www-form-urlencoded*
格式发送，只要将 `method` 属性改成 *urlencoded-post* 即可。

**示例 \#2 使用 XForm 来产生 `$_POST`**

``` html
<h:html xmlns:h="http://www.w3.org/1999/xhtml"
        xmlns="http://www.w3.org/2002/xforms">
<h:head>
 <h:title>Search</h:title>
 <model>
  <submission action="http://example.com/search"
              method="urlencoded-post" xml:id="s"/>
 </model>
</h:head>
<h:body>
 <h:p>
  <input ref="q"><label>Find</label></input>
  <submit submission="s"><label>Go</label></submit>
 </h:p>
</h:body>
</h:html>
```

> **Note**: <span class="simpara"> 在写本文档时，许多浏览器还不支持
> XForms。如果上面例子失败请检查自己的浏览器版本。 </span>
