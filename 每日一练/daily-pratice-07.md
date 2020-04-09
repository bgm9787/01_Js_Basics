### 每日一练

#### 1、CSS 优先级算法如何计算？

> 即：样式的权重问题，!important  >  行内样式  >  id选择器  >  类、伪类、属性选择器  > 标签选择器

CSS优先级通过CSS Specificity规定的公式来计算，sepcificity用一个四位的数字串来表示，更像四个级别，值从左到右，左边的最大，一级大于一级，数位之间没有进制，级别之间不可超越。

| 继承或者*的贡献值    | 0,0,0,0 |
| -- | -- |
| 元素和伪元素的贡献值 | 0,0,0,1 |
| 属性选择器、类选择器、伪类的贡献值 | 0,0,1,0 |
| ID选择器的贡献值 | 0,1,0,0 |
| 行内样式 的贡献值 | 1,0,0,0 |
| !important 的贡献值 | 无穷大 |

**注意：**数位之间没有进制。

#### 2、关于伪类 LVHA 的解释?

`:link,:visited,:hover,:active`这4个伪类  

link表示链接在正常情况下（即页面刚加载完成时）显示的颜色。

visited表示链接被点击后显示的颜色。

hover表示鼠标悬停时显示的颜色。

active表示当所指元素处于激活状态（鼠标在元素上按下还没有松开）时所显示的颜色。

focus表示元素获得光标焦点时使用的颜色，主要用于文本框输入文字时使用（鼠标松开时显示的颜色）。

> 未移入a标签链接时：link
> 移入a标签链接时：link、hover
> 点击a标签链接时：link、hover、active
> 点击后未移入a标签连接时：link、visited
> 点击后移入a标签连接时：link、visited、hover
> 点击后再次点击a标签连接时：link、visited、hover、active



#### 3、CSS3 新增伪类有那些？

> 伪类： :before :after :nth-child(n) :nth-of-type(n)  :nth-last-child(n) :first-line :first-letter

>- :root 选择文档的根元素，等同于 html 元素
>- :empty 选择没有子元素的元素
>- :target 选取当前活动的目标元素
>- :not(selector) 选择除 selector 元素意外的元素
>- :enabled 选择可用的表单元素
>- :disabled 选择禁用的表单元素
>- :checked 选择被选中的表单元素
>- :after 在元素内部最前添加内容
>- :before 在元素内部最后添加内容
>- :nth-child(n) 匹配父元素下指定子元素，在所有子元素中排序第n
>- :nth-last-child(n) 匹配父元素下指定子元素，在所有子元素中排序第n，从后向前数
>- :nth-child(odd)
>- :nth-child(even)
>- :nth-child(3n+1)
>- :first-child
>- :last-child
>- :only-child
>- :nth-of-type(n) 匹配父元素下指定子元素，在同类子元素中排序第n
>- :nth-last-of-type(n) 匹配父元素下指定子元素，在同类子元素中排序第n，从后向前数
>- :nth-of-type(odd)
>- :nth-of-type(even)
>- :nth-of-type(3n+1)
>- :first-of-type
>- :last-of-type
>- :only-of-type
>- ::selection 选择被用户选取的元素部分
>- :first-line 选择元素中的第一行
>- :first-letter 选择元素中的第一个字符

#### 4、如何居中 div ？

> margin: 0 auto;
>
> 通过定位：子绝父相，子元素设置position：absolute; top:50%; left: 50%; margin: -50% 0 0 -50%;
>
> 通过CSS3的transform + 子绝父相:  子元素设置position：absolute; top:50%; left: 50%; transform:translate(-50%, -50%)
>
> 通过flex布局：设置父元素：display: flex; justify-content: center;  align-items: center;
>
> 

#### 5、display 有哪些值？说明他们的作用。

> display的值常用的有： inline、inline-block、block、flex。。。。
>
> 常用的有：
> none：此元素不显示。
> block：将元素显示为块级元素，前后会带换行符。
> inline:默认值，元素会被显示为内联元素，前后没有换行符。
> inline-block:行内块级元素。

![image-20200402120722551](https://img-blog.csdn.net/20170426182153457?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc2ppbnNh/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)













​		

![image-20200407121729509](/Users/baoguomei/Library/Application Support/typora-user-images/image-20200407121729509.png)