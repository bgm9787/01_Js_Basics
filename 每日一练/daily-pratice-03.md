### 每日一练

#### 1、link 标签定义

> 理解：link标签主要用来引入外部编写的css样式表
>

<link> 元素是空元素，它仅包含属性。此元素只能存在于 head 部分，不过它可出现任何次数。

<link> 标签定义文档与外部资源的关系；最常见的用途是链接样式表，link的rel属性有很多的值，不同的值代表了外部资源与本html文档的关系。以下列出常见用途：

- 连接外部的样式表，这个是最常用的 <link rel="stylesheet" type="text/css" href="*.css"/>指被link链接的css文档是本文档的样式描述文件。

- 链接一个外部的icon用于浏览器的栏目图标和收藏夹图标,地址栏最前面的小图标和收藏夹图标 <link rel="icon" href="/favicon.ico" >

- rel="alternate"可以定义另外一个版本的文档，可以是Pdf，另外一种语言，另外一种css样式，如 <link rel="alternate" href="url"  >，方便了浏览器插件（例如翻译插件，下载插件）和搜索引擎的搜索。

- rel="author license",规定一些作者和版权相关的信息。例如，

  <link rel="author license" href="url"  >,url所指向的就是这些信息所在的文档。

#### 2、页面导入样式时，使用 link 和 @import 有什么区别？

> 理解：都可以用来导入css样式表，<link>是HTML提供的标签，@import是CSS提供的
>
> ​			<link>引入的CSS样式是在加载页面时就被加载，@import引入的CSS是在页面加载完成后才被加载

- 从属关系区别
 `@import`是 CSS 提供的语法规则，只有导入样式表的作用；`link`是HTML提供的标签，不仅可以加载 CSS 文件，还可以定义 RSS、rel 连接属性等。
- 加载顺序区别
 加载页面时，`link`标签引入的 CSS 被同时加载；`@import`引入的 CSS 将在页面加载完毕后被加载。
- 兼容性区别
 `@import`是 CSS2.1 才有的语法，故只可在 IE5+ 才能识别；`link`标签作为 HTML 元素，不存在兼容性问题。
- DOM可控性区别
 可以通过 JS 操作 DOM ，插入`link`标签来改变样式；由于 DOM 方法是基于文档的，无法使用`@import`的方式插入样式。
- 权重区别(该项有争议)
 `link`引入的样式权重大于`@import`引入的样式。

#### 3、你对浏览器的理解？

> 理解：作为前端开发人员，Chrome、IE、Firefox、Safari、Opera五大浏览器需要熟悉，平常开发中使用最多的是Chrome
>

​		浏览器主要分为shell(外壳)+内核，shell是面向用户的界面，即浏览器上集成的各种丰富的功能菜单，例如菜单工具栏目等，主要是提供给用户界面操作，参数设置等等，它是调用内核来实现各种功能的，内核才是浏览器的核心。

​		

#### 4、介绍一下你对浏览器内核的理解？
> 理解：各浏览器的内核决定了浏览器如何显示网页的内容及格式信息，不同的浏览器内核对网页编写语法的解释也有不同，因此同一HTML网页在不同的内核的浏览器里的渲染（显示）效果也可能不同，所以为了更好地兼容，我们需在不同内核的浏览器进行网页的测试。
>

​		内核，是一个通俗的说法，其英文名称为“Layout engine”，翻译过来就是“排版引擎”，也被称为“页面渲染引擎”。它负责取得网页的内容（HTML、XML、图像等等）、整理信息（例如加入CSS等），以及计算网页的显示方式，然后会输出至显示器或打印机。所有网页浏览器、电子邮件客户端以及其它需要编辑、显示网络内容的应用程序都需要排版引擎。

​		早期，内核中Javascript引擎与页面渲染引擎概念模糊统一，随着对页面逻辑及交互性的需求的提高，Javascript引擎的能力不断发展升级，Javascript引擎逐渐独立化出来，内核即主要由页面渲染引擎及Javascript引擎组成，并各自独立发展升级（内核引擎倾向于指页面渲染引擎，因为历史原因习惯了）。常见的浏览器内核可以分为四种：Trient,Gecko,Presto,Webkit,代表者分别为IE,Firefox,Opera,chrome.

#### 5、常见的浏览器内核比较  
> 理解：作为程序员最常用的浏览器是Chrome，其内核是blink，谷歌中使用的javascript 解析引擎 ---- V8引擎（用C++语言编写），使js代码在浏览器端被解析；Nodejs也是借助于V8引擎 使得js代码能在运行在服务器上。。。。。。。。。


  浏览器	| 内核	| 备注
  -- | -- | --
chrome		| Chromium/Blink	| 	Blink 其实是 WebKit 的分支，大部分国产浏览器最新版都采用Blink内核进行二次开发
 firefox	| 	Gecko	| 	可惜这几年已经没落了，打开速度慢、升级频繁
IE		| Trident		| IE、猎豹安全、360极速浏览器、百度浏览器
Safari		| webkit		| 现在很多人错误地把 webkit 叫做 chrome内核（chrome 已经是 blink 内核了）
Opera		| blink		| 现在跟随 chrome 用 blink 内核

![image-20200402120722551](https://upload-images.jianshu.io/upload_images/13785765-d2002b7eadd13275.png)