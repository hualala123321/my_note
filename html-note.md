# html笔记
## 简介
+ HTML指的是超文本标记语言 (Hyper Text Markup Language)。
+ HTML不是一种编程语言，而是一种标记语言 (markup language)。
+ 标记语言是一套标记标签 (markup tag)。
+ HTML 使用标记标签来描述网页。

## 元素
+ html元素以开始标签起始，以结束标签终止。
+ 元素的内容是开始标签与结束标签之间的内容。
+ 某些 HTML 元素具有空内容（empty content）。
+ 空元素在开始标签中进行关闭（以开始标签的结束而结束）。
+ 大多数 HTML 元素可拥有属性。

 
 
## 属性
+ HTML标签可以拥有属性。属性提供了有关 HTML 元素的更多的信息。
+ 属性总是以名称/值对的形式出现，比如：name="value"。
+ 属性总是在 HTML 元素的开始标签中规定。
+ 常见属性
  - id
  - class
  - title

## 注释
+ 注释中的内容不会在网页中显示。
  - 格式:  <！-- 在此处写注释 -->
  - 合理的使用注释可以帮助开发人员理解网页- 注释不能嵌套。

## 页面基础结构
```
<!DOCTYPE html>
<html>
<head>
	<meta charset="UTF-8">
	<title>网页标题</title>
</head>
<body>
	...
</body>
</html>
```

## 标签

### 常见标签
+ html标签
用于告诉浏览器这个文档中包含的信息是用HTML编写的。
+ meta标签
用于设置页面的字符集
  - 中文编码gbk gb2312  big5...
  - 全球码: unicode
  - 优化全球码: utf-8 
+ head标签
用于定义文档的头部，它是所有头部元素的容器
+ title标签
用于定义文档的标题（浏览器tab显示的内容），它是 head 部分中唯一必需的元素。
+ body标签
用来设置网页的主体，所有在页面中能看到的内容都应该编写到body标签中
+ h1~h6标签
用于定义标题,每级页面中只能有一个。h1>标签定义最大的标题。h6标签 定义最小的标题。
+ p标签
用于定义段落。浏览器会自动地在段落的前后添加空行。
+ br
换行符
+ hr
分割线

### 超级链接 
+ 使用a标签与网络上的另一个文档相连，点击链接可以从一张页面跳转到另一张页面。
+ hrft：指向一个链接
+ target：设置打开目标页面的位置
 		- self  默认
 		- blank 新窗口打开
		- parent 父类窗口
  		- top 顶级窗口


### 图片
 + src 图片路径
    - 绝对路径：网络绝对路径和本地绝对路径。
    - 相对路径：同级路径、同级文件夹下的文件、上一级/上多级文件
  + alt 图片描述
  	属性用来为图像定义一串预备的可替换的文本。在浏览器无法载入图像时，浏览器将显示这个替代性的文本。

### 字体标签
+ em和strong标签
em标签用于表示一段内容中的着重点。strong标签用于表示一个内容的重要性。
+ i和b标签
跟上面类似，不过没有实际意义。
+ sup和sub标签
	上标和下标
+ ins和del标签
	删除线

### 表格
+ 表格由 table 标签来定义。
	- tr 元素定义表格行。
	- th 元素定义表头。
	- td 元素定义表格单元。
	- colspan/rowspan 列合并/行合并。
	- < caption>表头文字< /caption>
+ 属性
	- border：单元格边框的宽度
	- width / height ：表格的宽度与高度。
	- cellspacing  / cellpadding：规定单元格之间的空白/规定单元边沿与其内容之间的空白。
	- frame：规定外侧边框的哪个部分是可见的。
	- rules：规定内侧边框的哪个部分是可见的。
	- align :  left   |   center  |  right（不赞成使用）
	- bgcolor（不赞成使用）

### 列表
+ 无序列表： ul  li
+ 有序列表： ol  li
+ 自定义列表： dl   dt   dd

### 表单
+ form元素定义 HTML 表单
+ 表单method 属性规定在提交表单时所用的 HTTP 方法（GET 或 POST）
+ fieldset 标签 -- 对表单进行分组
	- fieldset：对表单进行分组，一个表单可以有多个fieldset。
	- legend：说明每组的内容描述
+ put元素是最重要的表单元素，定义表单类型.
+ Input元素的属性：
	- readonly 属性定义只读（不能修改）
	- disabled 属性输入字段禁用 被禁用的元素是不可用、不可点击、不会被提交。
	- value 属性规定输入字段的初始值
+ input元素的 type 属性:
	- text：定义一个单行的文本字段（默认宽度为 20 个字符）
	- textarea：定义输入多行字段（文本域）
	- Password：定义密码字段
	- Button：定义可点击的按钮
	- radio：定义单选按钮
	- checkbox：定义复选框
	- Select：定义下拉列表
	- option：定义待选择的选项
	- file：定义文件选择字段和 "浏览..." 按钮，供文件上传。
	- submit：定义提交按钮
	- ....  
+ name表单特有属性，用于标识当前表单作用,用于向后台传递数据，如果需要用表单给后台提交数据 必须有name属性。name属性用于给表单(单选/多选)分组，在单选分组内会出现互斥 。复选框虽然不需要互斥 但是一组多选应该也加上相同的name属性

### 转义字符
+ 空格 &nbsp；
+ 小于号	&lt；
+ 大于号	&gt；
+ 和号 &amp；
+ 引号 &quot；
+ 撇号 &apos；(IE不支持)
（注意：;为小写）