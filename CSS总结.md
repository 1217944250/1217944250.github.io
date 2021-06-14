# CSS总结

------



## 简介

- CSS 指层叠样式表 (**C**ascading **S**tyle **S**heets)

- 样式定义**如何显示** HTML 元素

- 样式通常存储在**样式表**中

- **外部样式表**可以极大提高工作效率

- 外部样式表通常存储在 **CSS 文件**中

- 多个样式定义可**层叠**为一个

  样式表定义如何显示 HTML 元素，就像 HTML 中的字体标签和颜色属性所起的作用那样。样式通常保存在外部的 .css 文件中。我们只需要编辑一个简单的 CSS 文档就可以改变所有页面的布局和外观。



## CSS基本教程

CSS 规则由两个主要的部分构成：选择器，以及一条或多条声明:

![img](https://www.runoob.com/wp-content/uploads/2013/07/632877C9-2462-41D6-BD0E-F7317E4C42AC.jpg)

选择器通常是您需要改变样式的 HTML 元素。

每条声明由一个属性和一个值组成。

属性（property）是您希望设置的样式属性（style attribute）。每个属性有一个值。属性和值被冒号分开。

例：CSS声明总是以分号(;)结束，声明总以大括号({})括起来:

```
p {color:bule;text-align:center;}
```

#### id和class选择器

如果你要在HTML元素中设置CSS样式，你需要在元素中设置"id" 和 "class"选择器。

id 选择器可以为标有特定 id 的 HTML 元素指定特定的样式。

HTML元素以id属性来设置id选择器,CSS 中 id 选择器以 "#" 来定义。

以下的样式规则应用于元素属性 id="para1":

(**注: ID属性不要以数字开头，数字开头的ID在 Mozilla/Firefox 浏览器中不起作用。**)

例：

```
#text1
{
    text-align:center;
    color:bule;
}
```

class 选择器用于描述一组元素的样式，class 选择器有别于id选择器，class可以在多个元素中使用。

例:

```
.center {text-align:center;}
```

## 生效CSS

当读到一个样式表时，浏览器会根据它来格式化 HTML 文档。

插入样式表的方法有三种:

- 外部样式表(External style sheet)
- 内部样式表(Internal style sheet)
- 内联样式(Inline style)

#### 外部样式表

当样式需要应用于很多页面时，外部样式表将是理想的选择。在使用外部样式表的情况下，你可以通过改变一个文件来改变整个站点的外观。每个页面使用 &lt;link&gt; 标签链接到样式表。 &lt;link&gt; 标签在（文档的）头部：

```
<head>
<link rel="stylesheet" type="text/css" href="firststyle.css">
</head>
```

浏览器会从文件 mystyle.css 中读到样式声明，并根据它来格式文档。

外部样式表可以在任何文本编辑器中进行编辑。文件不能包含任何的 html 标签。样式表应该以 .css 扩展名进行保存。下面是一个样式表文件的例子：

```
hr {color:sienna;}
p {margin-left:20px;}
body {background-image:url("/images/back40.gif");}
```

#### 内部样式表

当单个文档需要特殊的样式时，就应该使用内部样式表。你可以使用 <style> 标签在文档头部定义内部样式表，就像这样:

```
<head>
<style>
hr {color:sienna;}
p {margin-left:20px;}
body {background-image:url("images/back40.gif");}
</style>
</head>
```

#### 内联样式

由于要将表现和内容混杂在一起，内联样式会损失掉样式表的许多优势。请慎用这种方法，例如当样式仅需要在一个元素上应用一次时。

要使用内联样式，你需要在相关的标签内使用样式（style）属性。Style 属性可以包含任何 CSS 属性。本例展示如何改变段落的颜色和左外边距：

例:

```
<p style="color:sienna;margin-left:20px">这是一个段落。</p>
```



## CSS基础属性

#### Backgrounds(背景)

CSS 背景属性

| Property              | 描述                                         |
| :-------------------- | :------------------------------------------- |
| background            | 简写属性，作用是将背景属性设置在一个声明中。 |
| background-attachment | 背景图像是否固定或者随着页面的其余部分滚动。 |
| background-color      | 设置元素的背景颜色。                         |
| background-image      | 把图像设置为背景。                           |
| background-position   | 设置背景图像的起始位置。                     |
| background-repeat     | 设置背景图像是否及如何重复。                 |

#### Text(文本)

CSS文本属性

| 属性            | 描述                     |
| :-------------- | :----------------------- |
| color           | 设置文本颜色             |
| direction       | 设置文本方向。           |
| letter-spacing  | 设置字符间距             |
| line-height     | 设置行高                 |
| text-align      | 对齐元素中的文本         |
| text-decoration | 向文本添加修饰           |
| text-indent     | 缩进元素中文本的首行     |
| text-shadow     | 设置文本阴影             |
| text-transform  | 控制元素中的字母         |
| unicode-bidi    | 设置或返回文本是否被重写 |
| vertical-align  | 设置元素的垂直对齐       |
| white-space     | 设置元素中空白的处理方式 |
| word-spacing    | 设置字间距               |

### Fonts(字体)

CSS字体属性

| Property     | 描述                                 |
| :----------- | :----------------------------------- |
| font         | 在一个声明中设置所有的字体属性       |
| font-family  | 指定文本的字体系列                   |
| font-size    | 指定文本的字体大小                   |
| font-style   | 指定文本的字体样式                   |
| font-variant | 以小型大写字体或者正常字体显示文本。 |
| font-weight  | 指定字体的粗细。                     |

## Link(链接)

链接的样式，可以用任何CSS属性（如颜色，字体，背景等）。

特别的链接，可以有不同的样式，这取决于他们是什么状态。

这四个链接状态是：

- a:link - 正常，未访问过的链接
- a:visited - 用户已访问过的链接
- a:hover - 当用户鼠标放在链接上时
- a:active - 链接被点击的那一刻

## list(列表)

CSS列表属性

| 属性                | 描述                                               |
| :------------------ | :------------------------------------------------- |
| list-style          | 简写属性。用于把所有用于列表的属性设置于一个声明中 |
| list-style-image    | 将图像设置为列表项标志。                           |
| list-style-position | 设置列表中列表项标志的位置。                       |
| list-style-type     | 设置列表项标志的类型。                             |

## Table(表格)

指定CSS表格边框，使用border属性。

border-collapse 属性设置表格的边框是否被折叠成一个单一的边框或隔开：

Width和height属性定义表格的宽度和高度。

text-align属性设置水平对齐方式，向左，右，或中心

如果在表的内容中控制空格之间的边框，应使用td和th元素的填充属性

## Dimension(尺寸)

CSS 尺寸 (Dimension)属性

| 属性        | 描述                 |
| :---------- | :------------------- |
| height      | 设置元素的高度。     |
| line-height | 设置行高。           |
| max-height  | 设置元素的最大高度。 |
| max-width   | 设置元素的最大宽度。 |
| min-height  | 设置元素的最小高度。 |
| min-width   | 设置元素的最小宽度。 |
| width       | 设置元素的宽度。     |

## Border(边框)

CSS 边框属性

| 属性                | 描述                                                         |
| :------------------ | :----------------------------------------------------------- |
| border              | 简写属性，用于把针对四个边的属性设置在一个声明。             |
| border-style        | 用于设置元素所有边框的样式，或者单独地为各边设置边框样式。   |
| border-width        | 简写属性，用于为元素的所有边框设置宽度，或者单独地为各边边框设置宽度。 |
| border-color        | 简写属性，设置元素的所有边框中可见部分的颜色，或为 4 个边分别设置颜色。 |
| border-bottom       | 简写属性，用于把下边框的所有属性设置到一个声明中。           |
| border-bottom-color | 设置元素的下边框的颜色。                                     |
| border-bottom-style | 设置元素的下边框的样式。                                     |
| border-bottom-width | 设置元素的下边框的宽度。                                     |
| border-left         | 简写属性，用于把左边框的所有属性设置到一个声明中。           |
| border-left-color   | 设置元素的左边框的颜色。                                     |
| border-left-style   | 设置元素的左边框的样式。                                     |
| border-left-width   | 设置元素的左边框的宽度。                                     |
| border-right        | 简写属性，用于把右边框的所有属性设置到一个声明中。           |
| border-right-color  | 设置元素的右边框的颜色。                                     |
| border-right-style  | 设置元素的右边框的样式。                                     |
| border-right-width  | 设置元素的右边框的宽度。                                     |
| border-top          | 简写属性，用于把上边框的所有属性设置到一个声明中。           |
| border-top-color    | 设置元素的上边框的颜色。                                     |
| border-top-style    | 设置元素的上边框的样式。                                     |
| border-top-width    | 设置元素的上边框的宽度。                                     |

## margin(边距)

CSS边距属性

| 属性          | 描述                                       |
| :------------ | :----------------------------------------- |
| margin        | 简写属性。在一个声明中设置所有外边距属性。 |
| margin-bottom | 设置元素的下外边距。                       |
| margin-left   | 设置元素的左外边距。                       |
| margin-right  | 设置元素的右外边距。                       |
| margin-top    | 设置元素的上外边距。                       |

## Position(定位)

position 属性指定了元素的定位类型。

position 属性的五个值：

- **static HTML** 元素的默认值，即没有定位，遵循正常的文档流对象。

  静态定位的元素不会受到 top, bottom, left, right影响。

- **relative** 元素的位置相对于浏览器窗口是固定位置。

  即使窗口是滚动的它也不会移动：

- **fixed** 相对定位元素的定位是相对其正常位置。

- **absolute**绝对定位的元素的位置相对于最近的已定位父元素，如果元素没有已定位的父元素，那么它的位置相对于&lt;html&gt;:

- **sticky** 粘性定位的元素是依赖于用户的滚动，在 **position:relative** 与 **position:fixed** 定位之间切换。

## Float(浮动)

CSS 的 Float（浮动），会使元素向左或向右移动，其周围的元素也会重新排列。

Float（浮动），往往是用于图像，但它在布局时一样非常有用。

CSS" 列中的数字表示不同的 CSS 版本（CSS1 或 CSS2）定义了该属性。

| 属性  | 描述                               | 值                           |
| :---- | :--------------------------------- | :--------------------------- |
| clear | 指定不允许元素周围有浮动元素。     | left right both none inherit |
| float | 指定一个盒子（元素）是否可以浮动。 | left right none inherit      |

## 对齐

#### 元素居中对齐

要水平居中对齐一个元素(如 <div>), 可以使用 **margin: auto;**。

设置到元素的宽度将防止它溢出到容器的边缘。

元素通过指定宽度，并将两边的空外边距平均分配：

#### 文本居中对齐

如果仅仅是为了文本在元素内居中对齐，可以使用 **text-align: center;**

#### 图片居中对齐

要让图片居中对齐, 可以使用 **margin: auto;** 并将它放到 **块** 元素中:

#### 左右对齐 - 使用定位方式

我们可以使用 **position: absolute;** 属性来对齐元素:

#### 垂直居中对齐 - 使用 padding

CSS 中有很多方式可以实现垂直居中对齐。 一个简单的方式就是头部顶部使用 **padding**:

## Box Model(盒子)

CSS盒模型本质上是一个盒子，封装周围的HTML元素，它包括：边距，边框，填充，和实际内容。

盒模型允许我们在其它元素和周围元素边框之间的空间放置元素。

下面的图片说明了盒子模型(Box Model)：


![CSS box-model](https://www.runoob.com/images/box-model.gif)

不同部分的说明：

- **Margin(外边距)** - 清除边框外的区域，外边距是透明的。
- **Border(边框)** - 围绕在内边距和内容外的边框。
- **Padding(内边距)** - 清除内容周围的区域，内边距是透明的。
- **Content(内容)** - 盒子的内容，显示文本和图像。

## 组合选择符

CSS组合选择符包括各种简单选择符的组合方式。

在 CSS3 中包含了四种组合方式:

- 后代选择器(以空格   分隔)

  例:以下实例选取所有p 元素插入到div 元素中: 

  ```
  div p
  {
    background-color:yellow;
  }
  ```

- 子元素选择器(以大于 **>** 号分隔）

  例:与后代选择器相比，子元素选择器（Child selectors）只能选择作为某元素子元素的元素。

  ```
  div>p
  {
    background-color:yellow;
  }
  ```

  

- 相邻兄弟选择器（以加号 **+** 分隔）

  例:相邻兄弟选择器（Adjacent sibling selector）可选择紧接在另一元素后的元素，且二者有相同父元素。

  如果需要选择紧接在另一个元素后的元素，而且二者有相同的父元素，可以使用相邻兄弟选择器（Adjacent sibling selector）

  ```
  div+p
  {
    background-color:yellow;
  }
  ```

  

- 普通兄弟选择器（以波浪号 **～** 分隔）

  例:后续兄弟选择器选取所有指定元素之后的相邻兄弟元素。

  ```
  div~p
  {
    background-color:yellow;
  }
  ```

## 伪元素和伪类

伪类（pseudo-class）或伪元素（pseudo-element）用于定义元素的某种特定的状态或位置等。
比如我们可能有这样的需求：

- 鼠标移到某元素上变换背景颜色
- 超链接访问前后访问后样式不同
- 离开必须填写的输入框时出现红色的外框进行警示
- 保证段落的第一行加粗，其它正常
- ...

CSS伪类/元素

| 选择器            | 示例           | 示例说明                                             |
| :---------------- | :------------- | :--------------------------------------------------- |
| :link             | a:link         | 选择所有未访问链接                                   |
| :visited          | a:visited      | 选择所有访问过的链接                                 |
| :active           | a:active       | 选择正在活动链接                                     |
| :hover            | a:hover        | 把鼠标放在链接上的状态                               |
| :focus            | input:focus    | 选择元素输入后具有焦点                               |
| :first-letter     | p:first-letter | 选择每个&lt;p&gt; 元素的第一个字母                   |
| :first-line       | p:first-line   | 选择每个&lt;p&gt;元素的第一行                        |
| :first-child      | p:first-child  | 选择器匹配属于任意元素的第一个子元素的 &lt;p&gt;元素 |
| :before           | p:before       | 在每个&lt;p&gt;元素之前插入内容                      |
| :after            | p:after        | 在每个&lt;p&gt;元素之后插入内容                      |
| :lang(*language*) | p:lang(it)     | 为&lt;p&gt;元素的lang属性选择一个开始值              |

------

## 最后的总结

css就像是做web网页见面的化妆师，他与JS，HTML更多不同的是，它做的更加细致，要做好一个令人赏心悦目的网页需要个人的一点美术功底。同时学好css需要更多的细心以及注意更多的细节！