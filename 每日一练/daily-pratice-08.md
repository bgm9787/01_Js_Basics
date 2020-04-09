### 每日一练

#### 1、position 的值 relative 和 absolute 定位原点是？

> relative：相对定位，相对于自身左上角进行定位
>
> absolute：绝对定位，相对于其上一个定位的父级元素，若父级元素没有定位，依次往上，直找到HTML元素也没有定位，则以浏览器为定位原点。

相对定位是将元素相对于它在标准流中的位置进行定位。

#### 2、CSS3 有哪些新特性？（根据项目回答）

> 小米官网项目中，用到了伪类选择器、圆角、阴影、背景图片等特性。

整理：

- CSS3中新增选择器（伪类选择器、伪元素选择器、属性选择器）
- 背景属性，设置多背景、背景缩放等
- CSS3的盒子模型 通过box-sizing指定
- CSS3的过渡属性transition
- 2D、3D变形属性 transform   调整元素转换变形的原点 transform-origin
- 移动属性 改变元素的位置 translate(X, Y)
- 缩放属性 scale(x, y)
- 旋转属性 rotate(deg)
- 倾斜属性 skew(deg, deg)
- 动画 animation
- flex布局
- 。。。。。。

#### 3、请解释一下 CSS3 的 Flexbox（弹性盒布局模型），以及适用场景？

> Flex 布局，弹性模型，用来为盒状模型提供最大的灵活性。可以简便、完整、响应式地实现各种页面布局

http://www.ruanyifeng.com/blog/2015/07/flex-grammar.html  详细训练！

#### 4、用纯 CSS 创建一个三角形的原理是什么？

> 主要利用标准盒子模型的特性，其宽度=内容的宽度，不包括边框的宽度。
>
> 由此利用border属性，宽高为0时，设置border四条边均有一定的宽度，设置其余三条边框颜色均为透明transparent，另一条为某颜色 即可实现，
>
> div {
>
> ​      width: 0px;
>
> ​      height: 0px;
>
> ​      border: 100px solid transparent;
>
> ​      border-bottom-color: #aaa;
>
> ​    }



#### 5、一个满屏品字布局如何设计?

主要通过百分比进行布局，上半部分通过margin: 0 auto; 水平居中，下半部分通过百分比+ 浮动完成 实现代码如下


```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        html,body{width:100%;height:100%}
        .first{height:48%;}
        .up{
            width:50%;
            height:96%;
            margin:0 auto;
            border:2px solid red;
        }
        .second{
            height:48%;
            position:relative;
            
        }
        .left{
            float:left;
            width:48%;
            height:100%;
            border:2px solid red;
        }
        .right{
            float:right;
            width:48%;
            height:100%;
            border:2px solid red;
        }
    </style>
</head>
<body>
    <div class="first">
        <div class="up"></div>
    </div>
    <div class="second">
        <div class="left"></div>
        <div class="right"></div>
    </div>
    
</body>
</html>
```


`	

