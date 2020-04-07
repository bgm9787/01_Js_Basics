### 每日一练

#### 1、介绍一下标准的 CSS 的盒子模型？低版本 IE 的盒子模型有什么不同的？

> CSS中的标准盒子模型：元素的宽度或高度=内容content的宽度或高度
>
> 低版本的IE盒子模型：元素的宽度 = content的宽度 + padding-left + padding-right + border-left + border-right   （高度同理）

以下为标准盒子模型和IE盒子模型对照图：

![image-20200402120722551](https://img-blog.csdn.net/20180308203902825)


![image-20200402120722551](https://img-blog.csdn.net/20180308204055254)

box-sizing属性可以为三个值之一：content-box（default），border-box，padding-box。

- content-box，border和padding不计算入width之内
- padding-box，padding计算入width内
- border-box，border和padding计算入width之内，其实就是怪异模式了~

#### 2、CSS选择符有哪些？

> 自己能想出来的有：id选择器、类选择器、标签选择器、属性选择器、通配符选择器、

>   CSS基础选择器：标签选择器（元素选择器）、类选择器、id选择器、通配符选择器、
>
>   CSS复合选择器：交集选择器、并集选择器、后代选择器、子元素选择器、伪类选择器、

#### 3、::before 和 :after 中双冒号和单冒号 有什么区别？解释一下这2个伪元素的作用。

> 单冒号是CSS3之前 对伪元素的写法，双冒号是CSS3中 伪元素的写法，为了和伪类相区分

这个两个伪元素的作用：在真正页面*元素内部*`之前`和`之后`添加新内容，可以对其使用诸如页面元素一样的css样式

#### 4、伪类与伪元素的区别

​		CSS的**伪元素**，之所以被称为伪元素，是因为他们不是真正的页面元素，html没有对应的元素，但是其所有用法和表现行为与真正的页面元素一样，可以对其使用诸如页面元素一样的css样式，表面上看上去貌似是页面的某些元素来展现，实际上是css样式展现的行为。

- **伪类**不产生新的对象，只是在DOM中一个元素的不同状态 eg: :hover :active
- **伪元素**产生新对象，但不是真实的元素，在DOM树中看不到



#### 5、CSS 中哪些属性可以继承？ 

> 字体属性：font-
> 文本属性：text-
> 颜色属性：color
> 行高：line-height

1、字体系列属性

> font-family：字体系列
> font-weight：字体的粗细
> font-size：字体的大小
> font-style：字体的风格


2、文本系列属性

> text-indent：文本缩进
> text-align：文本水平对齐
> line-height：行高
> word-spacing：单词之间的间距
> letter-spacing：中文或者字母之间的间距
> text-transform：控制文本大小写（就是uppercase、lowercase、capitalize这三个）
> color：文本颜色


3、元素可见性：

>  visibility：控制元素显示隐藏

4、列表布局属性：

> list-style：列表风格，包括list-style-type、list-style-image等

5、光标属性：

> cursor：光标显示为何种形态