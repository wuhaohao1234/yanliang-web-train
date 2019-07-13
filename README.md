# 阎良Web培训

第一天上午完成的内容

## 文件扩展名与文件编码

文件扩展名:.html或者.htm

文件编码:UTF-8

## html页面结构

```
<!Doctype html>
<html>
    <head>
        <title>网页标题</title>
        <meta charset="UTF-8">
    </head>
    <body>
        网页内容
    </body>
</html>
```

网页介绍:

网页是由标签加关键字加内容组成

双标签:

`<关键字></关键字>`

单标签

`<关键字/>`

`<!Doctype html>` 声明这是一个html5页面

head标签里面的内容是给计算机看的

body标签里面的内容是给人看的

### head标签内容

meta标签: 作用:网页的说明，meta标签里面有个属性，这里只列举一个:

```
charset="UTF-8" 
```

说明这是一个以UTF-8为编码的网页(常见的编码为GB2312,ASCII)

title标签:网页标题

### body标签里面的内容

#### h1~h6的标题

```

<h1>我是标题一</h1>
<h2>我是标题二</h2>
<h3>我是标题三</h3>
<h4>我是标题四</h4>
<h5>我是标题五</h5>
<h6>我是标题六</h6>
```

注意没有h7标题,原因：设计电脑的人为保护使用电脑的人的眼睛，避免字体太小导致眼睛近视,所以没有h7

#### p段落

```
<p>我是段落我是段落我是段落我是段落我是段落我是段落我是段落我是段落我是段落我是段落我是段落我是段落我是段落</p>
```

#### 列表

列表分为有序列表ol

无序列表ul

中间是li

```
    <ul>
        <li>我是无序列表</li>
        <li>我是无序列表</li>
        <li>我是无序列表</li>
        <li>我是无序列表</li>
        <li>我是无序列表</li>
        <li>我是无序列表</li>
        <li>我是无序列表</li>
        <li>我是无序列表</li>
        <li>我是无序列表</li>
    </ul>
```

```
    <ol>
        <li>我是有序列表</li>
        <li>我是有序列表</li>
        <li>我是有序列表</li>
        <li>我是有序列表</li>
        <li>我是有序列表</li>
        <li>我是有序列表</li>
        <li>我是有序列表</li>
        <li>我是有序列表</li>
        <li>我是有序列表</li>
    </ol>
```

#### 超链接

a标签

```
<a href="http://www.baidu.com" target="_blank" >百度</a>
```

### 图片

```
<img src="https://www.baidu.com/img/baidu_resultlogo@2.png" alt="百度">
```

### 路径

相对路径

../上一级目录/文件

./当前目录文件

./当前文件夹/文件

绝对路径

基本不用

#### 学习css最好的2个标签

div标签

span标签

因为是最典型的两个标签，无任何样式

### css文件

#### 为网页添加样式的三种方法

##### 行内样式

```
<div style="color: red;" >我是红色</div>
```

link标签导入

新建css文件,以.css文件结尾的文件

一般写法:

```
元素{
    属性名:属性值
}
```

实例

```
h1 {
    color: red;
}
```

常用的属性:

width : 宽度
height : 高度
color : 字体颜色
background-color : 背景颜色
font-size: 字体大小，采用px单位
opacity: 透明度 0 到1
background-image: 背景图片 url('文件路径')
margin: 外边距
padding: 内边距
border: 边框
text-decoration: 有无下划线
text-align: 字体像哪里对齐

left,right,center

style标签
在head内新建一个style标签，里面写css内容
行内样式

```
<div style="color: red;" >我是红色</div>
```

#### 盒模型:

行内元素与块级元素

行内元素特征:

像文本一样，不可设置宽度与高度，大小由内容自动撑开,一行不够则自动换行，可设置字体颜色，背景颜色,不可设置margin-top与margin-bottom,可设置

块极元素特征:

默认独占一行，可设置宽高，可设置margin,padding,border(边框)

做项目中会用到的行内元素:

a标签，img标签,span标签

会用到的块级标签

div,h1~h6,ul,li,p

第一天晚自习完成的内容

#### 浮动与定位

##### 浮动

float:left,right

分别为向左浮动与向右浮动

重点:脱离原来的文档流,会向最靠左与最靠右浮动,会覆盖普通文档流元素里面的内容

##### 定位

position

分别有3个在项目中会用到

realtive:相对定位

相对原来的位置定位，可设置left,top,right,bottom

特点:不会占位

absolute: 绝对定位

相对于它父级元素为relative的位置相对定位,如果父级不是，则依次往上找,如果找不到，则相对于整个页面定位

fixed

固定定位,与absolute相似，但是是针对整个页面进行定位

### 布局中的2个bug

高度塌陷

当一个元素设置为浮动或者绝对定位元素时候,这个元素的父元素的高度会消失(不会被子元素撑开)

解决办法:父元素设置高度或者
设置overflow:hidden属性

边距传递

当子元素设置margin的时候会让父元素也继承自子元素的margin

边距重合


子元素

----------------------------------------------------------------------------------------------------

第二天完成的内容

### css动画

transform

旋转角度

`transform: rotate(角度deg);`

缩放比

`transform: scale(x轴倍数,y轴倍数);`

位移

`transform: translate(x轴位移,y轴位移);`

倾斜角度

`transform: skew(x轴倾斜,y轴倾斜);`

x轴倾斜角度

`transform: rotateX(120deg);`

y轴倾斜角度

`transform: rotateY(120deg);`

动画时间

transition

```
div {
    width: 100px;
    height: 100px;
    background: #f00;
    transition: width 2s;
}

div:hover {
    width: 300px;
    height: 100px;
}
```

animation

```
<!DOCTYPE html>
<html>

<head>
    <meta charset="utf-8">
    <title>菜鸟教程(runoob.com)</title>
    <style>
        div {
            width: 100px;
            height: 100px;
            background: red;
            animation: myfirst 5s;
        }

        @keyframes myfirst {
            0% {
                background: red;
            }

            25% {
                background: yellow;
            }

            50% {
                background: blue;
            }

            100% {
                background: green;
            }
        }
    </style>
</head>

<body>

    <div></div>

    <p><b>注释：</b>当动画完成时，会变回初始的样式。</p>


    <p><b>注意:</b> 该实例在 Internet Explorer 9 及更早 IE 版本是无效的。</p>

</body>

</html>
```

