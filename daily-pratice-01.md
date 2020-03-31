### 每日一练

#### 1、DOCTYPE 的作用是什么？

​		DOCTYPE是document type (文档类型) 的缩写，是对文档类型进行声明，它的目的是告诉浏览器的解析器，使用哪种应该使用什么样的文档类型定义（DTD）来解析文档。

​		<!DOCTYPE>不存在或者形式不正确会导致HTML或XHTML文档以兼容（混杂）模式呈现，就是把如何渲染html页面的权利交给了浏览器，有多少种浏览器就有多少种展示方式。因此要提高浏览器兼容性就必须重视<!DOCTYPE>

#### 2、标准模式与兼容模式各有什么区别？

​		**标准模式：**又称严格模式，是指浏览器按照W3C标准来解析代码，呈现页面。

​		**兼容模式：**又称为怪异模式或者混杂模式，是指浏览器按照自己的方式来解析代码，使用一种比较宽松的向后兼容的方式来显示页面。

#### 3、HTML5 为什么只需要写 <!DOCTYPE HTML>，而不需要引入 DTD？

​		HTML4.01基于SGML，DTD 标准是SGML 的一部分，所以需要对DTD进行引用，才能告知浏览器文档所使用的文档类型。而HTMl5不基于SGML，因此不需要对DTD进行引用，但是需要doctype来规范浏览器的行为(让浏览器按照它们应该的方式来运行)。

#### 4、SGML 、 HTML 、XML 和 XHTML 的区别？

**SGML**（Standard Generalized Markup Language）是指“标准通用标记语言”，SGML的功能很强大，它的组成包括语法定义，DTD，文件实例三部分。可以支持非常多的文档结构类型，并且可以创建与特定的软硬件无关的文档，因此很容易与使用不同计算机系统的用户交换文档。和XML相比，定义的功能很强大，缺点是它不适用于Web数据描述，而且SGML软件价格非常价格昂贵。

**XML**（eXtensible Markup Language）是“可扩展标记语言”。

**HTML**(Hyper Text Mark-up Language)即“超文本标记语言”，是目前网络上应用最为广泛的语言，也是构成网页文档的主要语言。它告诉浏览器如何显示内容。

**XHTML**是扩展超文本标签语言（eXtensible HyperText Markup Language）,目标是取代HTML.

>  XML 和 HTML 是 SGML 的子集，但使用比较严格的模式。
>
> **XML** 是一种必须正确标记且格式良好的标记语言，用于描绘封装数据
>
> 而**HTML**超文本标记语言主要用于展示数据
>
>  **XHTML**是通过结合 XML 和 HTML 的长处所开发出的，它是作为 XML 被重新设计的 HTML。

由于XML语法严格，因此，**XHTML**要求

- 元素被正确嵌套
- 必须有关闭标签
- 必须小写
- 文档必须有一个根元素

以下从网上摘来一张图来说明这几着之间的关系：

<img src="/Users/baoguomei/kkb/frontEnd/images/SGML、XML、HTML、XHTML.jpg" width = "500" />

#### 5、DTD 介绍

​		在HTML5之前，网页的前面几行都有类似于这么一行:

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
```

​		DTD（Document Type Definition文档类型定义）是一组机器可读的规则，它们定义XML或HTML的特定版本中允许有什么，不允许有什么。在解析网页时，浏览器将使用这些规则检查页面的有效性并且采取相应的措施。（由DTD中定义的文档类型影响）。

​		**文档类型定义（DTD）**可定义合法的XML文档构建模块。它使用一系列合法的元素来定义文档的结构。DTD 可被成行地声明于 XML 文档中，也可作为一个外部引用。      -----------来着w3school