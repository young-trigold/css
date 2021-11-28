**目录：**

- [1. CSS 简介](#1-css-简介)
  - [1.1. CSS 历史](#11-css-历史)
  - [1.2. HTML 元素](#12-html-元素)
    - [1.2.1. 可替换性](#121-可替换性)
      - [1.2.1.1. 替换性元素](#1211-替换性元素)
      - [1.2.1.2. 非替换性元素](#1212-非替换性元素)
    - [1.2.2. 显示方式](#122-显示方式)
      - [1.2.2.1. 块级元素](#1221-块级元素)
      - [1.2.2.2. 行内元素](#1222-行内元素)
  - [1.3. 引入 CSS](#13-引入-css)
    - [1.3.1. 外部样式表](#131-外部样式表)
      - [1.3.1.1. link 元素的属性](#1311-link-元素的属性)
      - [1.3.1.2. @import](#1312-import)
    - [1.3.2. 内部样式表](#132-内部样式表)
    - [1.3.3. 行内样式](#133-行内样式)
  - [1.4. 样式表](#14-样式表)
    - [1.4.1. 样式规则](#141-样式规则)
    - [1.4.2. 厂商前缀](#142-厂商前缀)
    - [1.4.3. 空白](#143-空白)
    - [1.4.4. 注释](#144-注释)
  - [1.5. 媒体查询](#15-媒体查询)
    - [1.5.1. 媒体类型](#151-媒体类型)
    - [1.5.2. 媒体特性](#152-媒体特性)
    - [1.5.3. 媒体描述符](#153-媒体描述符)
- [2. 选择器](#2-选择器)
  - [2.1. 基本选择器](#21-基本选择器)
    - [2.1.1. 通用选择器](#211-通用选择器)
    - [2.1.2. 元素选择器](#212-元素选择器)
    - [2.1.3. 类选择器](#213-类选择器)
    - [2.1.4. id 选择器](#214-id-选择器)
    - [2.1.5. 属性选择器](#215-属性选择器)
  - [2.2. 组合选择器](#22-组合选择器)
    - [2.2.1. 后代选择器](#221-后代选择器)
    - [2.2.2. 直接后代选择器](#222-直接后代选择器)
    - [2.2.3. 兄弟选择器](#223-兄弟选择器)
    - [2.2.4. 相邻兄弟选择器](#224-相邻兄弟选择器)
  - [2.3. 伪元素选择器](#23-伪元素选择器)
    - [2.3.1. ::after](#231-after)
    - [2.3.2. ::before](#232-before)
    - [2.3.3. ::first-line](#233-first-line)
    - [2.3.4. ::first-letter](#234-first-letter)
    - [2.3.5. ::selection](#235-selection)
  - [2.4. 伪类选择器](#24-伪类选择器)
    - [2.4.1. 结构性伪类选择器](#241-结构性伪类选择器)
    - [2.4.2. UI 伪类选择器](#242-ui-伪类选择器)
    - [2.4.3. 动态伪类选择器](#243-动态伪类选择器)
    - [2.4.4. 其他伪类选择器](#244-其他伪类选择器)
  - [2.5. 并集选择器](#25-并集选择器)
- [3. 层叠与继承](#3-层叠与继承)
  - [3.1. 用户代理样式](#31-用户代理样式)
  - [3.2. 样式的层叠](#32-样式的层叠)
  - [3.3. !important](#33-important)
  - [3.4. 样式冲突](#34-样式冲突)
  - [3.5. 继承](#35-继承)
- [4. 值与单位](#4-值与单位)
  - [4.1. 关键字](#41-关键字)
    - [4.1.1. inherit](#411-inherit)
    - [4.1.2. initial](#412-initial)
    - [4.1.3. unset](#413-unset)
  - [4.2. 长度](#42-长度)
    - [4.2.1. 绝对单位](#421-绝对单位)
    - [4.2.2. 相对单位](#422-相对单位)
  - [4.3. 颜色](#43-颜色)
  - [4.4. 其他单位](#44-其他单位)
    - [4.4.1. 角度](#441-角度)
    - [4.4.2. 时间](#442-时间)
- [5. 字体](#5-字体)
  - [5.1. font-family](#51-font-family)
  - [5.2. @font-face](#52-font-face)
  - [5.3. font-weight](#53-font-weight)
  - [5.4. font-size](#54-font-size)
    - [5.4.1. 绝对大小](#541-绝对大小)
    - [5.4.2. 相对大小](#542-相对大小)
    - [5.4.3. 长度单位](#543-长度单位)
  - [5.5. font-style](#55-font-style)
  - [5.6. font-variant](#56-font-variant)
  - [5.7. font](#57-font)
- [6. 文本](#6-文本)
  - [6.1. 缩进与行内对齐](#61-缩进与行内对齐)
    - [6.1.1. text-indent](#611-text-indent)
    - [6.1.2. text-align](#612-text-align)
    - [6.1.3. text-align-last](#613-text-align-last)
  - [6.2. 块级对齐](#62-块级对齐)
    - [6.2.1. line-height](#621-line-height)
    - [6.2.2. vertical-align](#622-vertical-align)
  - [6.3. 文本间距](#63-文本间距)
    - [6.3.1. wording-spacing](#631-wording-spacing)
    - [6.3.2. letter-spacing](#632-letter-spacing)
  - [6.4. text-transform](#64-text-transform)
  - [6.5. text-decoration](#65-text-decoration)
  - [6.6. text-shadow](#66-text-shadow)
  - [6.7. 处理空白](#67-处理空白)
  - [6.8. line-break](#68-line-break)
  - [6.9. overflow-wrap](#69-overflow-wrap)
  - [6.10. writing-mode](#610-writing-mode)
  - [6.11. text-orientation](#611-text-orientation)
  - [6.12. direaction](#612-direaction)
- [7. 盒模型基础](#7-盒模型基础)
- [8. 边距](#8-边距)
- [9. 颜色，背景和渐变](#9-颜色背景和渐变)
- [10. 浮动](#10-浮动)
- [11. 定位](#11-定位)
- [12. 弹性盒子](#12-弹性盒子)
- [13. 网格](#13-网格)
- [14. 表格](#14-表格)
- [15. 列表](#15-列表)
- [16. 变换](#16-变换)
- [17. 过渡](#17-过渡)
- [18. 动画](#18-动画)
- [19. 滤镜，混合，剪切与遮罩](#19-滤镜混合剪切与遮罩)
- [20. 媒体查询](#20-媒体查询)

# 1. CSS 简介

**层叠样式表(Cascading Style Sheet, CSS)** 是一个强大的工具，能影响一个或一组文档的表现。CSS 几乎触及 Web 的每个角落，甚至很多非 Web 环境也能见到它的身影。

## 1.1. CSS 历史

1994 年，正值 Web 开始广泛流行开来，CSS 的第一个提案发布了。那时，浏览器为用户提供了各种各样的定制功能。例如，用户在 Mosaic 的表现偏好设置中可以为单个元素设定字体族，字号和颜色。而文档的编写人员却做不到这一点，文档编写人员只能把内容标记称一个个段落，标题，预格式文本，或者一些其他类型的元素。如果用户愿意，可以把以及标题设为粉红色的小字，而把六级标题设为红色的大字。

CSS 就是在这样的背景下诞生的。它的目标是提供一个简单的声明式样式语言，而且具有一定的灵活性，能为文档编写人员和用户提供等同的样式化功能。层叠样式表中的“层叠”是指样式表可以结合起来使用，而且具有优先级，文档编写人员和用户都有话语权，不过最终的决策权在用户手中。

草案制定的速度很快，到 1996 年末，CSS1 完成了。此后，刚组建的 CSS 工作组开始着手制定 CSS2，而各个浏览器则相互协作，努力实现 CSS1。单独来看，CSS 的每一部分都很简单，但把各部分放在一起就变得已成复杂。而且早期的实现有些先天不足。例如，不同浏览器对盒模型(Box Model)的实现差异尤其为人诟病。这些问题直接影响到 CSS 的名声，幸好一些聪明人提出了变通方法，让浏览器的行为保持了一致。得益于一致性的提高和高调的开发活动，几年之间，CSS 逐渐开始流行。

不过，在此之前，CSS2 规范于 1998 年初定案。随后，CSS 工作组立即投身 CSS3 的制定工作，以及 CSS2 的修订工作。与以往不同的是，CSS3 有多个模块构成，而不是单独一个臃肿的规范。XHTML 规范受此启发，也采用了模块机制。

CSS3 分成多个模块的根本原因是各模块可以独立演进，尤其是模块可以按照 W3C 的规划向前推进，而不必受其他模块拖累。事实证明，这样做是对的。截至 2012 年初，有 3 个 CSS3 模块(CSS Color Level 3，CSS Namespace，Selectors Level 3) 变成了推荐状态，而有 7 个模块处于候选状态，还有 7 个模块处在不同的草案状态。如果采用以前的机制，要等到其他部分完成才能在一份完成的规范中发布颜色，选择器和命名控件的新条款。得益于模块化，我们无需等待。

但是，这样做也有缺点，CSS3 规范不能涵盖一切。即便其他模块在某一时刻到达了 Level 3，比如说 2016 年末（然而事实是没有），Selectors Level 4 也都开始制定了。那会不会有 CSS4？CSS3 那些尚未正式发布的新特性呢？还有 Grid Layout，它甚至还没到 Level 1！

可见，我们不能指着一摞厚厚的文件说，这就是 CSS3，而应该分模块学习不同的特性。模块的灵活性有时可以弥补语义不足。

了解这些历史之后，就可以开始学习 CSS 了。在此之前，我们不得不介绍一下 CSS 中的 HTML 元素。

## 1.2. HTML 元素

CSS 依赖 HTML 元素，但并非每种元素都以同样的方式创建。例如，img 和 p 是不同类型的元素。对 CSS 而言，HTML 元素分为两种：置换元素和非置换元素。

### 1.2.1. 可替换性

#### 1.2.1.1. 替换性元素

替换性元素(replaced element)是指用来置换元素内容的部分不是由文档内容表示的。例如，img 元素，它的内容由文档之外的图像文件替换，由文档直接表示的内容是空的：

```html
<img src="img.jpg" />
```

这个元素只包含一个属性，并没有内容。

还有 input 元素，根据类型的不同会被替换为复选框或者输入框。

#### 1.2.1.2. 非替换性元素

HTML 元素大部分都是非替换性的，意思就是这种元素的内容在文档中直接表示了。例如：

```html
<p>一段文本。</p>
```

这个元素在显示时，直接显示的是 "一段文本。"。

### 1.2.2. 显示方式

除了 HTML 元素的可替换性外，CSS 还把元素分为块级和行内类型。

#### 1.2.2.1. 块级元素

HTML 元素大多数都是“块级”元素或行内元素。块级元素占据其父元素的整个水平空间，垂直空间等于其内容高度，因此创建了一个“块”。通常浏览器会在块级元素前后另起一个新行。

块级元素可以包含行内元素，也可以包含块级块级元素。

块级元素的 display 属性值为 block。

#### 1.2.2.2. 行内元素

一个行内元素只占据它对应标签的边框所包含的空间。也不会在前后另起新行。

行内元素可以包含文本和行内元素，但不能包含块级元素。

行内元素的 display 属性值为 inline。

## 1.3. 引入 CSS

在学习 CSS 之前，我们得首先在 HTML 关联 CSS，不然 CSS 就没法影响 HTML 文档。下面介绍 3 种引入 CSS 的方式。

### 1.3.1. 外部样式表

外部样式表式引入 CSS 最常用的方式。这种方式用到了 link 元素，例如：

```html
<!DOCTYPE html>
<html>
  <head>
    <title>外部样式表</title>
    <link rel="stylesheet" href="style.css" media="screen" />
  </head>
  <body></body>
</html>
```

上述例子向 HTML 文档中引入了一个 style.css 外部样式表。

外部样式表中没有任何 HTML 标签。外部样式表保存为纯文本文件，文件扩展名是 .css。

#### 1.3.1.1. link 元素的属性

link 元素的 rel 属性表示链接资源和 HTML 文档的关系，对于 CSS 文档来说，就是“stylesheet”。

link 元素的 href 属性制定了链接资源的地址。

最后的 media 属性，它的值是一个或多个媒体描述符(media descriptor)，表示什么样的媒体应该使用这个 CSS 文档。例如：

```html
<link rel="stylesheet" href="style.css" media="screen, screen" />
```

多个媒体描述符用逗号分隔。媒体描述符本书后面会详细的介绍。

link 的 type 属性现在已经不常用了，它用来指定资源的 MIME 类型，不过对于 CSS 文档，浏览器默认为 "text/css"。

#### 1.3.1.2. @import

@import 指令可以出现在 CSS 文档中，它的作用是链接另外一个 CSS 文档。例如：

```css
@import url(basic.css);
```

@import 指令必需放在 CSS 规则之前，否则不会有效。

### 1.3.2. 内部样式表

另外一种引入 CSS 的方式是通过 style 元素。例如：

```html
<!DOCTYPE html>
<html>
  <head>
    <title>内部样式表</title>
    <style>
      h1 {
        color: red;
      }

      h2 {
        color: maroon;
        background: black;
      }
    </style>
  </head>
  <body></body>
</html>
```

内部样式表的层叠优先级大于外部样式表。本书后面会详细讨论。

### 1.3.3. 行内样式

最后一种的方式是通过 HTML 元素的 style 全局属性。例如：

```html
<!DOCTYPE html>
<html>
  <head>
    <title>行内样式</title>
  </head>
  <body>
    <p style="color: red;">一段文本。</p>
  </body>
</html>
```

这种方式应用的 CSS 样式层叠优先级最高。但是这种方式使用 CSS 不好管理。

## 1.4. 样式表

样式表包含什么呢？其实是一系列 CSS 样式规则。例如：

```css
h1 {
  color: red;
}

h2 {
  color: maroon;
  background: black;
}
```

### 1.4.1. 样式规则

一个 CSS 样式规则有 2 个部分组成：选择器和声明块。选择器制定了声明块中样式的应用目标元素。声明块则由一个或多个样式声明组成。一个样式声明是一个键值对，包含属性和对应值。

例如：

```css
h1 {
  color: red;
  background-color: yellow;
}
```

这个例子中，h1 就是一个最简单的选择器（本书后面会介绍各种选择器），后面的声明块中包含了 2 条样式声明：color 和 backgroung-color。属性和值用冒号分开。每一条声明都要以分号结尾。

### 1.4.2. 厂商前缀

有时候，CSS 中的属性会包含厂商前缀(vendor prefix)。如：-o-border-image。带有厂商前缀的属性往往只是对应厂商的浏览器有，或者这些属性还在实验中。

下表列出了常用的厂商前缀：

| 浏览器            | 前缀     |
| ----------------- | -------- |
| Chrome, Safari    | -webkit- |
| Opera             | -o-      |
| Firefox           | -moz-    |
| Internet Explorer | -ms-     |

### 1.4.3. 空白

CSS 对 CSS 文档中的空白没有严格要求。一般来说，样式规则之间用换行符分隔。选择器和声明块之间用一个空格分隔。样式声明之间用换行符分隔，且缩进 2 个或是 4 个空格。

良好的空白有助于阅读。

### 1.4.4. 注释

CSS 支持注释。CSS 文档注释的风格和很多语言相似。

例如：

```css
/* 这是一个注释 */
h1 {
  color: red;
}
```

在解析时，注释会被浏览器忽略。

良好的注释风格有助于理解 CSS 文档。

## 1.5. 媒体查询

媒体查询(media query) 可以让特定的样式适用于特定的媒体。过去，实现这一机制的方式是通过 link，style 元素的 media 属性，或者在 @import 指令中指定 media。现在，媒体查询更近一步，使得开发者可以使用 @media 指令。本章只是粗略地涉及媒体查询，本书后面还会详细地讨论。

下面的例子指定了一个媒体查询:

```css
h1 {
  color: red;
}

@media screen {
  body {
    background-color: yellow;
  }
}
```

这个例子中，所有媒体的 h1 元素显示出来都是红色，但是在屏幕媒体中，body 的背景色为黄色。

一个媒体查询包含媒体类型和媒体特性的说明。

### 1.5.1. 媒体类型

下面总结了常用的媒体类型：

- all

用于所有媒体

- screen

用于屏幕

- print

用于印刷

但是往往我们还需要知道一些媒体的特性，例如屏幕的大小等等。

### 1.5.2. 媒体特性

媒体特性(Media features) 描述了 user agent、输出设备，或是浏览环境的具体特征。媒体特性表达式是完全可选的，它负责测试这些特性或特征是否存在、值为多少。每条媒体特性表达式都必须用括号括起来。

width
min-width
max-width
device-width
min-device-width
max-device-width
height
min-height
max-height
device-height
min-device-height
max-device-height
aspect-ratio
min-aspect-ratio
max-aspect-ratio
device-aspect-ratio
min-device-aspect-ratio
max-device-aspect-ratio
color
min-color
max-color
color-index
min-color-index
max-color-index
monochrome
min-monochrome
max-monochrome
resolution
min-resolution
max-resolution
orientation
scan
grid

### 1.5.3. 媒体描述符

媒体描述适用媒体类型，媒体特性以及逻辑关键词的组合。例如：

```css
@media screen and (min-wdith: 1000px) {
  /* 样式声明 */
}
```

上述例子使用了逻辑关键词 and，表示同时满足屏幕和最小宽度为 1000px 的媒体才适用。

除了 and 之外，还有 not 关键词用于反转，以及 only 关键字。

多条媒体描述可以用逗号隔开：

```css
@media (min-height: 680px), screen and (orientation: portrait) {
  /* 样式声明 */
}
```

# 2. 选择器

在前面我们知道了，一个 CSS 规则中，选择器指定了应用样式的目标元素。本章我们来详细介绍选择器。

## 2.1. 基本选择器

有些选择器使用起来非常简单，我们把这部分选择器称为 **基本选择器(basic selector)**。开发人员可使用这类选择器在文档中进行比较宽泛的选择，也可以将其看做结合多种选择器进行特殊选择的基础（本章后面会介绍复合选择器）。接下来每节介绍一种基本选择器的用法。

### 2.1.1. 通用选择器

通用选择器（\*）匹配文档中的所有元素。它是最基本的选择器，不过使用很少，因为匹配过于广泛。一般不推荐使用这个选择器，它性能很低。

### 2.1.2. 元素选择器

CSS 元素选择器(也称为类型选择器)通过 node 节点名称匹配元素. 因此,在单独使用时,寻找特定类型的元素时,元素选择器都会匹配该文档中所有此类型的元素。

下面的例子展示了元素选择器的用法。

```css
body {
  margin: 0px;
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
}
```

### 2.1.3. 类选择器

在一个 HTML 文档中，CSS 类选择器会根据元素的类属性中的内容匹配元素。类属性被定义为一个以空格分隔的列表项，在这组类名中，必须有一项与类选择器中的类名完全匹配，此条样式声明才会生效。

类选择器有 3 种基本用法：

1. **.className**

这种用法选择所有具有 className 的元素。

2. **tagName.className**

这种用法选择所有 tagName 类型的元素中含有 className 的元素。

3. **.className1.className2**

这种用法选择所有同时具有 className1 和 className2 的元素。

当然你也可以组合产生更多用法。

下面展示了了一些用例。

```css
p.center.bold {
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: bold;
}
```

### 2.1.4. id 选择器

在一个 HTML 文档中，CSS ID 选择器会根据该元素的 ID 属性中的内容匹配元素，元素 ID 属性名必须与选择器中的 ID 属性名完全匹配，此条样式声明才会生效。

id 选择器既可以单独使用也可以紧跟在一个元素选择器后面：

```css
#nav-bar {
  display: flex;
}
```

```css
div#nav-bar {
  display: flex;
}
```

### 2.1.5. 属性选择器

CSS 属性选择器通过已经存在的属性名或属性值匹配元素。

1. **[attr]**

选取有 attr 属性的元素。

```css
input[required] {
  /* 选择input中带有 required 的元素。 */
}
```

2. **[attr=value]**

选取属性为特定值的元素

```css
a[target='_blank'] {
  /* 选取 target 属性为 "_blank" 的 a 元素 */
  background-color: yellow;
}
```

3. **[attr~=value]**

[attr~=value] 选择器选取属性值包含指定词的元素。

```css
[title~='flower'] {
  border: 5px solid yellow;
}
```

上面的例子会匹配以下属性的元素：title="flower"、title="summer flower" 以及 title="flower new"，但不匹配：title="my-flower" 或 title="flowers"。

4. **[attr|=value]**

[attr|=value] 选择器用于选取指定属性以指定值开头的元素。

```css
[class|='top'] {
  background: yellow;
}
```

上例选取 class 属性以 "top" 开头的所有元素，而且值必须是完整或单独的单词，比如 class="top" 或者后跟连字符的，比如 class="top-text"。

5. **[attr^=value]**

[attr^=value] 选择器用于选取指定属性以指定值开头的元素。

```css
[class^='top'] {
  background: yellow;
}
```

上例选取 class 属性以 "top" 开头的所有元素，但值不必是完整单词！

6. **[attr$=value]**

[attre$=value] 选择器用于选取指定属性以指定值结尾的元素。

```css
[class$='wrapper'] {
  background-color: yellow;
}
```

上例选取 class 属性以 "test" 结尾的所有元素，但值不必是完整单词。

7. **[attr*=value]**

[attr*=value] 选择器选取属性值包含指定词的元素。

```css
[class*='te'] {
  background: yellow;
}
```

上例选取 class 属性包含 "te" 的所有元素，但值不必是完整单词！

## 2.2. 组合选择器

组合使用不同的选择器可以匹配更特定的元素。有的组合选择器能将目标样式应用到更多元素，有的组合选择器则会锁定更少元素，总之会让你的选择非常具体。在接下来的几节中，我会为你展示组合使用选择器的各种方法。

### 2.2.1. 后代选择器

后代组合器（通常用单个空格（ ）字符表示）组合了两个选择器，如果第二个选择器匹配的元素具有与第一个选择器匹配的祖先（父母，父母的父母，父母的父母的父母等）元素，则它们将被选择。利用后代组合器的选择器称为后代选择器。

从技术上讲，后代组合器是两个选择器之间的一个或多个 CSS 空格字符-空格字符和/或四个控制字符之一：回车，换页，换行和制表符在没有其他组合器的情况下。此外，组成组合器的空白字符可以包含任意数量的 CSS 注释。

```css
h1 em {
  color: red;
}
```

这个例子中，选择了 h1 元素中的所有 em 元素。

### 2.2.2. 直接后代选择器

如果您不希望选择任意的后代元素，而是希望缩小范围，只选择某个元素的子元素，请使用子元素选择器（Child selector）。例如，如果您希望选择只作为 h1 元素子元素的 strong 元素，可以这样写：

```css
h1 > strong {
  color: red;
}
```

这个规则会把第一个 h1 下面的两个 strong 元素变为红色，但是第二个 h1 中的 strong 不受影响：

```html
<h1>
  This is
  <strong>very</strong>
  <strong>very</strong>
  important.
</h1>
<h1>
  This is
  <em>
    really
    <strong>very</strong>
  </em>
  important.
</h1>
```

### 2.2.3. 兄弟选择器

兄弟选择符，位置无须紧邻，只须同层级，A~B 选择 A 元素之后所有同层级 B 元素。

```css
p ~ span {
  color: red;
}
```

```html
<span>This is not red.</span>
<p>Here is a paragraph.</p>
<code>Here is some code.</code>
<span>And here is a span.</span>
```

这样，只有最后一个 span 元素会被选中。

### 2.2.4. 相邻兄弟选择器

相邻兄弟选择器 (+) 介于两个选择器之间，当第二个元素紧跟在第一个元素之后，并且两个元素都是属于同一个父元素的子元素，则第二个元素将被选中。

```css
li + li {
  font-weight: bold;
}
```

```html
<div>
  <ul>
    <li>List item 1</li>
    <li>List item 2</li>
    <li>List item 3</li>
  </ul>
  <ol>
    <li>List item 1</li>
    <li>List item 2</li>
    <li>List item 3</li>
  </ol>
</div>
```

上面这个选择器只会把列表中的第二个和第三个列表项变为粗体。第一个列表项不受影响。

## 2.3. 伪元素选择器

目前为止， 我们已经学习了如何使用 HTML 文档中定义的元素选择文档内容。CSS 中还定义了伪选择器(pseudo-selector)， 它们提供了更复杂的功能，但并非直接对应 HTML 文档定义的元素。伪选择器分两种：伪元素和伪类。本节将介绍和演示伪元素选择器。顾名思义，伪元素实际上并不存在，它们是 CSS 提供的额外“福利”，为了方便你选中文档内容。

### 2.3.1. ::after

CSS 伪元素::after 用来创建一个伪元素，作为已选中元素的最后一个子元素。通常会配合 content 属性来为该元素添加装饰内容。这个虚拟元素默认是行内元素。

```css
/* Add an arrow after links */
a::after {
  content: '<-';
}
```

### 2.3.2. ::before

CSS 伪元素::before 用来创建一个伪元素，作为已选中元素的第一个一个子元素。通常会配合 content 属性来为该元素添加装饰内容。这个虚拟元素默认是行内元素。

```css
/* Add an arrow before links */
a::after {
  content: '->';
}
```

### 2.3.3. ::first-line

::first-line 选择器匹配文本块的首行。

```css
::first-line {
  background-color: grey;
  color: white;
}
```

### 2.3.4. ::first-letter

CSS 伪元素 ::first-letter 会选中某 block-level element（块级元素）第一行的第一个字母，并且文字所处的行之前没有其他内容（如图片和内联的表格） 。

```css
p::first-letter {
  font-weight: bold;
  color: red;
}
```

### 2.3.5. ::selection

::selection CSS 伪元素应用于文档中被用户高亮的部分（比如使用鼠标或其他选择设备选中的部分）。

```css
::selection {
  background-color: cyan;
}
```

只有一小部分 CSS 属性可以用于::selection 选择器：

color
background-color
cursor
caret-color
outline and its longhands
text-decoration and its associated properties
text-emphasis-color (en-US)
text-shadow

## 2.4. 伪类选择器

伪类跟伪元素一样，并不是直接针对文档元素的，而是为你基于某些共同特征选择元素提供方便。

### 2.4.1. 结构性伪类选择器

使用结构性伪类选择器能够根据元素在文档中的位置选择元素。这类选择器都有一个冒号字符前缀（:）， 例如： empty。它们可以单独使用，也可以跟其他选择器组合使用，如 p:empty。

- **:root**

:root 选择器匹配文档中的根元素。它可能是用得最少的一个伪类选择器，因为总是返回 html 元素。

```css
:root {
  background: yellow;
}
```

- **子元素伪类**

使用子元素伪类匹配直接包含在其他元素中的单个元素。

1. **:first-child**

:first-child 伪类表示在一组兄弟元素中的第一个元素。

```html
<div>
  <p>This text is selected!</p>
  <p>This text isn't selected.</p>
</div>

<div>
  <h2>This text isn't selected: it's not a `p`.</h2>
  <p>This text isn't selected.</p>
</div>
```

```css
p:first-child {
  color: lime;
  background-color: black;
  padding: 5px;
}
```

这个例子中，只会选择第一个 p 元素。

2. **:last-child**

:lst-child 伪类表示在一组兄弟元素中的最后一个元素。

```html
<ul>
  <li>此元素背景色不是lime</li>
  <li>我的也不是lime。</li>
  <li>我的才是lime！ :)</li>
</ul>
```

```css
li:last-child {
  background-color: lime;
}
```

在这个例子中，只有最后一个 li 元素被选择。

4. **:nth-child(n)**

:nth-child(n) 伪类选择器选择一组兄弟元素中顺序地第 n 个。

```html
<ul>
  <li>此元素背景色不是lime</li>
  <li>我的也不是lime。</li>
  <li>我的才是lime！ :)</li>
</ul>
```

```css
li:nth-child(2) {
  background-color: blue;
}
```

这个例子中，只有第 2 个 li 元素会被选中。

5. **:nth-last-child(n)**

这个伪类选择器和 :nth-child(n) 非常类似，只不过这个选择器的顺序是逆序。

```html
<ul>
  <li>此元素背景色不是lime</li>
  <li>我的也不是lime。</li>
  <li>我的才是lime！ :)</li>
</ul>
```

```css
li:nth-last-child(1) {
  background-color: blue;
}
```

这个例子中，最后一个 li 元素被选中。

6. **:only-child**

:only-child 匹配没有任何兄弟元素的元素。

```html
<ol>
  <li>
    First
    <ul>
      <li>This list has just one element.</li>
    </ul>
  </li>
  <li>
    Second
    <ul>
      <li>This list has three elements.</li>
      <li>This list has three elements.</li>
      <li>This list has three elements.</li>
    </ul>
  </li>
</ol>
```

```css
li li {
  list-style-type: disc;
}
li:only-child {
  color: red;
  list-style-type: square;
}
```

这个例子中 "This list has just one element." 内容的 li 元素会被选中。

7. **:only-of-type**

:only-of-type 代表了任意一个元素，这个元素没有其他相同类型的兄弟元素。

<main>
  <div>I am `div` #1.</div>
  <p>I am the only `p` among my siblings.</p>
  <div>I am `div` #2.</div>
  <div>I am `div` #3.
    <i>I am the only `i` child.</i>
    <em>I am `em` #1.</em>
    <em>I am `em` #2.</em>
  </div>
</main>

```css
main :only-of-type {
  color: red;
}
```

上面的例子中只会选中 p 元素。

6. **:nth-of-type(n)**

:nth-of-type() 这个 CSS 伪类是针对具有一组兄弟节点的标签, 用 n 来筛选出在一组兄弟节点的位置。

```html
<div>
  <div>这段不参与计数。</div>
  <p>这是第一段。</p>
  <p>这是第二段。</p>
  <div>这段不参与计数。</div>
  <p>这是第三段。</p>
  <p>这是第四段。</p>
</div>
```

```css
/* 奇数段 */
p:nth-of-type(2n + 1) {
  color: red;
}

/* 偶数段 */
p:nth-of-type(2n) {
  color: blue;
}

/* 第一段 */
p:nth-of-type(1) {
  font-weight: bold;
}
```

7. **:nth-last-of-type(n)**

:nth-last-of-type(n) 和 :nth-of-type(n) 类型，不过顺序相反。

### 2.4.2. UI 伪类选择器

1. **:enabled 和 :disabled**

有些元素有启用或者禁用状态，这些元素一般是用来收集用户输入的。:enabled 和 :disabled 选择器不会匹配没有禁用状态的元素。

2. **:checked**

使用:checked 选择器可以选中由 checked 属性或者用户勾选的单选按钮或者复选框。

3. **:valid 和 :invalid**

:valid 和:invalid 选择器分别匹配符合和不符合它们的输入验证要求的 input 元素。

4. **:required 和 :optional**

:required 选择器匹配具有 required 属性的 input 元素，这能够确保用户必需输入与 input 元素相关的值才能提交表单。:optional 选择器匹配没有 required 属性的 input 元素。

5. **:in-range 和 :out-of-range**

关于输入验证的一种具体程度更高的变体是选择值限于指定范围的 input 元素。:in-range 选择器匹配位于指定范围内的 input 元素，:out-of-range 选择器匹配位千指定范围之外的 input 元素。

### 2.4.3. 动态伪类选择器

之所以称为动态伪类选择器，是因为它们根据条件的改变匹配元素，是相对于文档的固定状态来说的。随着 JavaScript 广泛用于修改文档内容和元素状态，动态选择器和静态选择器之间的界限线越来越模糊，不过，动态伪类选择器仍然是一类比较特别的选择器。

1. **:link**

:link 选择器匹配超级链接。

2. **:visited**

:visited 选择器匹配用户已访问的超级链接。

3. **:hover**

:hover 选择器匹配用户鼠标悬停在其上的任意元素。鼠标在 HTML 页面内移动时，选中的元素样式会发生改变。

4. **:active**

:active 选择器匹配当前被用户激活的元素。浏览器依然可以自行决定如何诠释激活，但多数浏览器会在鼠标点击（在触摸屏上是手指按压）的情况下使用这个选择器。

5. **:focus**

最后一个动态伪类选择器是 :focus 选择器，它匹配当前获得焦点的元素。

### 2.4.4. 其他伪类选择器

1. **:not()**

CSS 伪类 :not() 用来匹配不符合一组选择器的元素。由于它的作用是防止特定的元素被选中，它也被称为反选伪类。

```css
/* 选择所有不是段落（p）的元素 */
:not(p) {
  color: blue;
}
```

2. **:empty**

:empty 选择器匹配没有定义任何子元素的元素。

3. **:lang()**

:lang 选择器匹配基于 lang 全局属性值的元素。如：:lang(zh-CN)。

3. **:target**

:target CSS 伪类代表一个唯一的页面元素(目标元素)，其 id 与当前 URL 片段匹配。

```css
/* 选择一个ID与当前URL片段匹配的元素*/
:target {
  border: 2px solid black;
}
```

## 2.5. 并集选择器

创建由逗号分隔的多个选择器可以将样式应用到单个选择器匹配的所有元素。

如：

```css
h1,
h2,
h3 {
}
```

# 3. 层叠与继承

要想掌握样式表，弄清样式层叠和继承这两个概念是关键。浏览器根据层叠和继承规则确定显示一个元素时各种样式属性采用的值。每个元素都有一套浏览器呈现页面时要用到的 CSS 属性。对于每一个这种属性，浏览器都需要查看一下其所有的样式来源。前面已经讲过三种定义样式的方式（行内样式、内部样式表和外部样式表），但是要知道，样式还有另外一种来源。

## 3.1. 用户代理样式

用户代理样式一般指元素尚未设置样式时浏览器应用在它身上的默认样式。这些样式因浏览器而略有差异，不过大体一致。以 a 元素（超链接）为例，想想没有特别为它定义样式时浏览器会怎样显示。下面代码所示为一个不含任何样式的简单 HTML 文档。

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <a href="http://www.google.com/">google</a>
  </body>
</html>
```

我们对浏览器应用于链接的样式早已习以为常，以至于不会留意到它的存在。用户代理样式可以通过浏览器的控制台查看。如下是 Chrome 浏览器中，上面超链接的用户代理样式：

```css
a:-webkit-any-link {
  color: -webkit-link;
  cursor: pointer;
  text-decoration: underline;
}
```

虽然不是每一个 HTML 元素都有默认的浏览器样式，但是多数元素都有。本书介绍 HTML 元素的各章都会介绍常见浏览器一般都会应用的典型默认样式。

## 3.2. 样式的层叠

明白了浏览器所要查看的所有样式来源之后， 现在可以看看浏览器要显示元素时求索一个 CSS 属性值的次序。这个次序很明确：

1. 行内样式（用元素的全局属性 style 定义的样式）；
2. 内部样式表（定义在 style 元素中的样式）；
3. 外部样式表（用 link 元素导入的样式）；
4. 浏览器样式（浏览器应用的默认样式）。

设想用户需要显示一个 a 元素。浏览器需要知道的一件事情是其文字应显示为哪种颜色。为了解决这个问题，它需要为 CSS 属性 color 找到一个值。首先它会查看所要呈现的那个元素是否具有一条设定了 color 值的行内样式。比如下面这种：

```html
<a style="color: blue;" href="http://www.google.com/">google</a>
```

如果不存在元素内嵌样式， 那么接下来浏览器会看看是否有一个 style 元素包含着作用于那个元素的样式。比如下面这种：

```html
<style>
  a {
  color: red;
  ｝
</style>
```

如果不存在这样的 style 元素，那么浏览器接下来会查看用 link 元素载入的样式表。依次类推，直到找到一个 color 属性值或查完用户定义样式。在后面一种情况下， 最终使用的将是浏览器默认样式中的值。

前述次序表中的前三个属性来源（行内样式、内部样式表和外部样式表）合称作者样式。定义在用户样式表中的样式称为用户样式。由浏览器的默认样式则称为用户代理样式（浏览器样式）。

## 3.3. !important

在样式属性值后用 !important 标记，可以改变正常的层叠次序。

例如：

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <style>
      a {
        color: blue !important;
      }
    </style>
    <title>Document</title>
  </head>
  <body>
    <a style="color: red;" href="http://www.baidu.com/">baidu</a>
  </body>
</html>
```

这样浏览器在检查样式时，内部样式表的样式就会被首先查询。因此，这个例子中，超链接文字颜色是蓝色而不是红色。

## 3.4. 样式冲突

在使用内部或外部样式表时，有时可能发生 **样式冲突**。样式冲突是指定义在内部样式表或外部样式表中的多条样式规则可能作用于同一个元素。例如：

```css
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <style>
      a{
        color:blue;
      }

      a.myClass{
        color: green;
        background-color: yellow;
      }
    </style>
    <title>Document</title>
  </head>
  <body>
    <!--蓝色文字-->
    <a href="http://www.google.com/">google</a>

    <!--蓝色文字，黄色背景-->
    <a class="myClass" href="http://www.baidu.com/">baidu</a>
  </body>
</html>
```

在这些情况下，为了判断该用哪个值，浏览器会评估两条样式的具体程度，然后选中较为特殊的那条。样式的具体程度通过统计三类特征得出：

- a: 样式的选择器中 id 值的数目；
- b: 选择器中其他属性和伪类的数目；
- c: 选择器中元素名和伪元素的数目。

在评定具体程度时要按 a-b-c 的形式（其中每一个字母依次代表上述三类特征的统计结果）生成一个数字。它不是一个三位数。如果对某个样式算出的 a 值最大，那么它就是具体程度高的那个。只有 a 值相等时浏览器才会比较 b 值，此时 b 值较大的样式具体程度更高。只有 a 值和 b 值都分别相等时浏览器才会考虑 c 值。也就是说，1-0-0 这个得分比 0-5-5 这个得分代表的具体程度更高。

本例中 a.myclass 这个选择器含有一个 class 属性，于是该样式的值为 0-1-0 (0 个 id 值+1 个其他属性+0 个元素名）。另一条样式的具体程度值为 0-0-0（因为它不包含 id 值、其他属性或元素名）。因此浏览器在呈现被归入 myclass 类的 a 元素时将使用 a.myclass 样式中设定的 color 属性值。对于所有其他 a 元素，使用的则是另一条样式中设定的值。

如果同一个样式属性出现在具体程度相当的几条样式中，那么浏览器会根据其位置的先后选择所用的值，规则是后来者居上。

例如：

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <style>
      a.myClass1 {
        color: blue;
      }

      a.myClass2 {
        color: red;
      }
    </style>
    <title>Document</title>
  </head>
  <body>
    <!--红色文字-->
    <a class="myClass1 myClass2" href="http://www.baidu.com/">baidu</a>
  </body>
</html>
```

此例 style 元素中定义的两条样式在具体程度上得分相同。因此，超链接应用了第 2 条样式。同样地，如果我们颠倒了这 2 条样式，那么超链接就会变为蓝色文字。读者不妨自行尝试。

根据样式的具体程度和定义次序确定选用的样式属性值，应该把各个属性分开考虑。本节的几个例子还定义了背景颜色属性的值。因为该值并非两个样式中都有，所以不会发生冲突，也就没有必要查找其他值。

## 3.5. 继承

如果浏览器在直接相关的样式中找不到某个属性的值，就会求助于继承机制，使用父元素的这个样式属性值。

例如：

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <style>
      p {
        color: white;
        background-color: black;
        border: 1px solid yellow;
      }
    </style>
    <title>Document</title>
  </head>
  <body>
    <p>
      I like
      <!--继承父元素 p 的前景色-->
      <span>apples</span>
      and oranges.
    </p>
  </body>
</html>
```

本例关注的是浏览器应用于 span 元素（其父元素为 p) 的样式。这个文档并没有在针对 span 元素的样式中设定 color 属性值，但是浏览器显示该元素的文字内容时却使用了前景色 white。这个值系由父元素 p 继承而来。

令人挠头的是，并非所有 CSS 属性均可继承。这方面有条经验可供参考：与元素外观（文字颜色、字体等）相关的样式会被继承；与元素在页面上的布局相关的样式不会被继承。在样式中使用 inherit 这个特别设立的值可以强行实施继承，明确指示浏览器在该属性上使用父元素样式中的值。

例如：

```css
span {
  border: inherit;
}
```

此例定义了一条用于 span 元素的样式，其 border 属性值继承自父元素。因此 apples 就会出现黄色边框。

# 4. 值与单位

本章探讨单位。单位可以影响距离，尺寸，颜色等等。单位时 CSS 的重要基础，几乎一切值都离不开它。

## 4.1. 关键字

有时，值用一个关键字表示。比如：none。

例如，下面的例子移除了链接的下划线：

```css
a:link,
a:visited {
  text-decoration: none;
}
```

属性值的关键字具体可以写什么取决于这个属性。而且不同属性同一个关键字表示的含义也不同。例如：letter-spacing 属性和 font-style 属性同样取 normal 值时，含义是不同的。

CSS3 定义了几个全局关键字，任何属性都可以使用：inherit, initial, 和 unset。

### 4.1.1. inherit

inherit 关键字把属性设置为和包含元素对应属性相同的值。换句话说，这个属性用于强制继承。

例如：

```html
<div id="toolbar">
  <a href="one.html">One</a>
  |
  <a href="two.html">Two</a>
  |
  <a href="three.html">Three</a>
</div>
```

```css
#toolbar {
  background: blue;
  color: white;
}
```

div 元素将有蓝色背景和白字，而链接将根据浏览器的用户代理样式设置。多数情况下，这里的来链接显示为蓝底蓝字，中间以白色的竖线分隔。

你可以单独编写一个规则，把这个工具栏中的链接设为白色，不过使用 inherit 是更为推荐的：

```css
#toolbar a {
  color: inherit;
}
```

使用 inherit 还能把默认不能继承的属性强制继承。例如，border 属性默认不会继承，如果想要 span 继承父元素的边框，只需使用：

```css
span {
  border: inherit;
}
```

### 4.1.2. initial

initial 关键字将属性设置为预定义的初始值，相当于重设值。例如 font-weight 的默认值为 normal。因此，font-weight: initial 的作用和 font-weight: normal 的作用一样。

这种看起来有些多余，不过有些属性没有预定义的初始值。例如：color 属性的初始值却决于用户代理样式。多数情况下，用户不会修改默认的用户代理属性值，但也有人会改。此时，initial 的作用就是将属性值设置为默认的用户代理样式。

### 4.1.3. unset

unset 关键字是 inherit 和 initial 的通用替身。对继承的属性来说，unset 的作用和 inherit 一样。对不继承的属性来说，unset 的作用和 initial 一样。

## 4.2. 长度

许多 CSS 属性要求为其设置长度值。width 属性和 font-size 属性就是这方面的例子。前者用于设置元素的宽度，后者用于设置元素内容的字号。

例如：

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <style>
      body {
        margin: 0px;
        font-size: 20px;
      }
    </style>
    <title>Document</title>
  </head>
  <body>
    一段文本
  </body>
</html>
```

设置长度值时，应让数字和单位标识符连在一起，二者之间不加空格或其他字符。上面这个例子中将 body 的外边框（margin）的长度设为 0px，将其内容的文字大小设置为 20px。CSS 规定了两种类型的长度单位，一种是绝对单位，另一种是与其他属性挂钩的相对单位。下面介绍这两种单位。

### 4.2.1. 绝对单位

绝对长度单位是固定的，用其中任何一个单位表示的长度都会显示为该尺寸。

绝对长度单位不建议在屏幕上使用，因为屏幕尺寸变化太大。然而，如果输出媒介是已知的，例如印刷品的排版，则可以使用它们。

下表列出了常见的绝对单位：

| 单位 | 描述                          |
| ---- | ----------------------------- |
| cm   | 厘米                          |
| mm   | 毫米                          |
| in   | 英寸 (1 英寸 = 96px = 2.54cm) |
| px   | CSS 像素 (1px = 1/96 英寸)    |
| pt   | 点 (1pt = 1/72 英寸)          |
| pc   | 12 点活字 (1pc = 12 pt)       |

像素（px）是相对于观看设备而言的。对于低 DPI 设备，1px 是显示器的一个设备像素（点）。对于打印机和高分辨率的屏幕，1px 意味着多个设备像素，实际上这个数字大概等于 window.devicePixelRatio。

一条样式中可以混合使用多种单位，包括混合使用绝对单位和相对单位。如果能预先知道内容的呈现方式（例如为供打印的文档设计样式）， 那么绝对单位很有用处。我设计 CSS 样式不怎么使用绝对单位。个人认为相对单位更灵活、更容易管理， 而且我也很少创作需要与现实世界度量挂钩的内容。

### 4.2.2. 相对单位

相对长度的规定和实现都比绝对长度更复杂，需要以严密、精确的语言明确定义。相对单位的测量需要依托其他类型的单位。可惜 CSS 规范的语言还没那么精确（这个问题巳经困扰 CSS 多年）。因此尽管 CSS 规定了许多既有趣又有用的相对单位，但是其中一些单位还没有得到浏览器广泛、一致的支持，用户还无法使用。下表出了主流浏览器支持的一些 CSS 相对单位。

| 单位 | 描述                                                |
| ---- | --------------------------------------------------- |
| em   | 相对于元素的字体大小（2em 表示当前字体大小的 2 倍） |
| ex   | 相对于字符“x”的高度                                 |
| ch   | 相对于数字“0”的宽度                                 |
| rem  | 相对于根元素的字体大小                              |
| lh   | 相对于元素的 line-height                            |
| vw   | 相对于视口宽度的 1%                                 |
| vh   | 相对于视口高度的 1%                                 |
| vmin | 相对于视口小尺寸的 1%                               |
| vmax | 相对于视口大尺寸的 1%                               |
| %    | 与父元素的相对值                                    |

下表中的数字指定了完全支持长度单位的第一个浏览器版本。

| 长度单位                          | Chrome | Edge | FireFox | Safari | Opera |
| --------------------------------- | ------ | ---- | ------- | ------ | ----- |
| em, ex, %, px, cm, mm, in, pt, pc | 1.0    | 3.0  | 1.0     | 1.0    | 3.5   |
| ch                                | 27.0   | 9.0  | 1.0     | 7.0    | 20.0  |
| rem                               | 4.0    | 9.0  | 3.6     | 4.1    | 11.6  |
| vh, vw                            | 20.0   | 9.0  | 19.0    | 6.0    | 20.0  |
| vmin                              | 20.0   | 12.0 | 19.0    | 6.0    | 20.0  |
| vmax                              | 26.0   | 16.0 | 19.0    | 7.0    | 20.0  |

下面我们具体看一下这些相对单位。

1. **em 与 rem**

em 单位的使用有两种情况：

- em 作为本元素的非 font-size 属性。此时，em 的大小就是本元素的字号大小。
- em 作为本元素的 font-size 属性。此时，em 的大小为父元素的字号大小。

来看下面几个例子。

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <style>
      body {
        font-size: 20px;
        height: fit-content;
        border: 1px black solid;
        margin: 1em;
      }
    </style>
    <title>Document</title>
  </head>
  <body>
    一段文本
  </body>
</html>
```

这个例子中，我们改写了 body 的 margin 属性，这个属性的用户代理样式为 8px，现在改写为 1em。显然 margin 不是 font-size，因此它的大小就是 body 字体的大小，因此，我们可以看到这里的 1em = 20 px。当我们修改了本元素的字体时，margin 也会跟着变化。

再来看一个例子：

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <style>
      body {
        font-size: 20px;
        margin: 0px;
      }

      span {
        font-size: 1em;
      }
    </style>
    <title>Document</title>
  </head>
  <body>
    <span>一段文本</span>
  </body>
</html>
```

这个例子中，span 元素最近的父元素为 body，span 元素的 font-size 属性值为 1em，因此这个大小就是父元素字号的大小：20px。

rem 则和 em 不同，它只相对于 html 元素（根元素）的字号大小。

来看这个例子：

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <style>
      html {
        font-size: 20px;
      }
      body {
        font-size: 16px;
        margin: 0px;
      }
      span {
        font-size: 1rem;
      }
    </style>
    <title>Document</title>
  </head>
  <body>
    <span>一段文本</span>
  </body>
</html>
```

在这个例子中，span 的 font-size 属性被设置为 1rem，而 html 元素的 font-size 被设置为 20px。因此，这里的 1rem = 20px。而不是 16px。

2. **vw 与 vh**

1vw 代表视口宽度的 1%。而 1vh 表示视口高度的 1%。

视口 (viewport) 代表当前可见的计算机图形区域。在 Web 浏览器术语中，通常与浏览器窗口相同，但不包括浏览器的 UI， 菜单栏等——即指你正在浏览的文档的那一部分。

文档，比如这篇文章，可能会非常长。你的 viewport 就是你现在所能见到的所有事物。值得注意的是“什么是视口区域”这个问题，页面中的一些导航菜单也包括在其中。Viewport 的大小取决于屏幕的大小，无论浏览器是否处于全屏模式，是否被用户缩放了。Viewport 外的区域，比如这个文档的 See Also 部分，可能需要滚动到其所在的区域才会出现在屏幕上。

- 在尺寸较大的设备中，在这些设备上，应用显示区域不一定是全屏的，viewport 是浏览器窗口的大小。
- 在大多数移动设备中，浏览器是全屏的，viewport 是整个屏幕的大小。
- 在全屏模式下，viewport 是设备屏幕的范围，窗口是浏览器窗口，浏览器窗口大小小于或等于视口的大小，并且文档是这个网站，文档的大小可比 viewport 长或宽。

概括地说，viewport 基本上是当前文档的可见部分。

在实测中，innerWidth 和 outerWidth 是相同的，但是 outerHeight 比 innerHeight 高 100px。这是因为 outerHeight 的测量包括浏览器框架在内，包括了地址栏和书签栏总共 100px 的高度，而浏览器没有左右边框。

innerHeight 和 innerWidth 所组成的区域通常被认为是布局视口 (layout viewport)。浏览器的框架不被认为是 viewport 的一部分。

Web 浏览器包含两个 viewport，**布局视口(layout viewport)** 和 **视觉视口(visual viewport)**。visual viewport 指当前浏览器中可见的部分，并且可以变化。当使用触屏双指缩放，当动态键盘在手机上弹出的时候，或者之前隐藏的地址栏变得可见的时候，visual viewport 缩小了，但是 layout viewport 却保持不变。

我们上面说到的固定的头部和尾部，固定在 layout viewport 的底部和顶部，所以当 visual viewport 缩小的时候,头部和尾部仍保留在视觉中。当你缩放页面时，布局视口可能不能被全部看到。如果你放大布局视口的中间部分，内容将在四个方向上扩展。如果你有一个固定的头部和底部，它们依然固定在布局视口的顶部和底部，因此它们可能会在设备屏幕的底部和顶部不可见-视觉视口。视觉视口是布局视口当前的可见部分如果你向下滚动，视觉视口的内容就会改变，并布局视口的底部就会滚动到可视区域。

视觉视口是屏幕的可视部分，不包括屏幕键盘，缩放外的区域。视觉视口比布局视口相同或者更小

对于一个包含框架，objects 或外部 svg 的页面，两者都有它们自己的 window 对象，只有最外层的 window 的视觉视口不同于布局视口。对于包含的文档，视觉视口与布局视口是相同的。

来看一个例子：

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <style>
      body {
        width: 100vw;
        height: 100vh;
        margin: 0px;
        background-color: #eeffee;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 20em;
        color: #ffeef8;
      }
    </style>
    <title>Document</title>
  </head>
  <body>
    <span>居中文字</span>
  </body>
</html>
```

这个例子中，我们将 body 的 width 设置为 100vw，高度设置为 100vh，margin 为 0px。这样 body 就占满了整个可见视口。接着我们将 body 设置为 flexbox，并居中字体。

vmin 和 vmax 和我们讲的上述单位很相似。但是也考虑到了屏幕旋转的影响。vmin 指的是可见视口中长度和宽度中较小的一个，vmax 则是较大的一个。

3. **%**

可以把一个度量单位表示为其他属性值的百分比，这正是%单位的用途。50%这个单位是相对于父元素的对应属性的大小而言的。

来看这个例子。

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <style>
      html {
        height: 100%;
        background-color: skyblue;
      }

      body {
        margin: 0px;
        width: 50%;
        height: 50%;
        background-color: blueviolet;
      }

      #target {
        width: 50%;
        height: 50%;
        background-color: aliceblue;
      }
    </style>
    <title>Document</title>
  </head>
  <body>
    <div id="target"></div>
  </body>
</html>
```

这个例子中，html，body，div 的宽度和长度都是上一个 1/2。使用百分比单位会遇到两个麻烦。一是并非所有属性都能用这个单位。二是对于能用百分比单位的属性，那个百分比挂钩的其他属性各不相同。例如，对于 font-size 属性，挂钩的是元素继承到的 font-size 值；而对于 width 属性，挂钩的则是元素的包含块的宽度。

4. **cal()**

允许将 CSS 属性值设置为算式是 CSS3 定义的一个引人关注的特性。这种灵活手段在控制能力和精确程度方面都给样式设计工作提供了帮助。calc() 此 CSS 函数允许在声明 CSS 属性值时执行一些计算。它可以用在如下场合：`<length>`、`<frequency>`, `<angle>`、`<time>`、`<percentage>`、`<number>`、或 `<integer>`。

来看这个例子。

```css
/* property: calc(expression) */
width: calc(100% - 80px);
```

此 calc()函数用一个表达式作为它的参数，用这个表达式的结果作为值。这个表达式可以是任何如下操作符的组合，采用标准操作符处理法则的简单表达式。

+: 加法。
-: 减法。
\*: 乘法，乘数中至少有一个是 `<number>`。
/: 除法，除数（/ 右面的数）必须是 `<number>`。

表达式中的运算对象可以使用任意 `<length>` 值。如果你愿意，你可以在一个表达式中混用这类值的不同单位。在需要时，你还可以使用小括号来建立计算顺序。

## 4.3. 颜色

颜色在网页中的作用非常重要。在 CSS 中设置颜色有好几种方法。最简单的办法是使用规定的颜色名称，或者设置红、绿、蓝三种颜色成分的值（十进制或十六进制）。设置颜色成分值时，十进制值以逗号分隔，十六进制值前面通常要加上一个`#`号（例如`#ffffff`，它代表白色）。你可以查看[MDN 参考](https://developer.mozilla.org/zh-CN/docs/Web/CSS/color_value)查看各种颜色代码。

**更复杂的颜色**

颜色名称和简单的十六进制数不是表示颜色的唯一方式。CSS 中还可以用一些函数选择颜色。下表逐一介绍了这些函数。

| 函数             | 说明示例                                                                              |
| ---------------- | ------------------------------------------------------------------------------------- | -------------------------------- |
| rgb(r, g, b)     | 用 RGB 模型表示颜色 color: rgb(112, 128,144)                                          |
| rgba(r, g, b, a) | 用 RGB 模型表示颜色，外加一个用于表示透明度的 a 值（0 代表全透明， 1 代表完全不透明） | color: rgba(112, 128, 144, 0.4)  |
| hsl(h, s, l)     | 用 HSL 模型（色相(hue)、饱和度(saturation)和明度(Lightness)）表示颜色                 | color: hsl(120, 100%, 22%)       |
| hsla(h, s, l, a) | 与 HSL 模式类似， 只不过增加了一个表示透明度的 a 值                                   | color: hsla(120, 100%, 22%, 0.4) |

## 4.4. 其他单位

CSS 中的单位不止有长度这一项，而是种类繁多。但是其中只有一小部分得到了广泛应用。下面要介绍的是本书用到的那些单位。

### 4.4.1. 角度

角度这种单位在旋转变换时可以用到。角度的表示方式是一个数字后跟一个单位，如 360deg。数字可以是负数，负数表示逆时针，而正数表示顺时针。

| 单位 | 说明                                                                                               |
| ---- | -------------------------------------------------------------------------------------------------- |
| deg  | 度。一个完整的圆是 360deg。例：0deg，90deg，14.23deg。                                             |
| grad | 百分度。一个完整的圆是 400grad。例：0grad，100grad，38.8grad。                                     |
| rad  | 弧度。一个完整的圆是 2π 弧度，约等于 6.2832rad。1rad 是 180/π 度。例：0rad，1.0708rad，6.2832rad。 |
| turn | 圈数。一个完整的圆是 1turn。例：0turn，0.25turn，1.2turn。                                         |

### 4.4.2. 时间

时间的单位可以在过渡中使用。时间单位包含秒（s）和毫秒（ms）。1 秒等于 1000 毫秒。

# 5. 字体

设计字体属性是样式表常见的用途之一。

## 5.1. font-family

我们熟知的字体包含多个变体：粗体，斜体等。例如，Times 字体实际上有：TimesRegular, TimesBold, TimesItalic 等。Times 的这些变体都是来自于一个字体族，而不是一种字体。

使用 font-family 可以指定字体族。例如，让一个文档使用无衬线字体，你可以这样写：

```css
body {
  font-family: sans-serif;
}
```

在一些情况，用户的电脑可能没有安装一个字体。这时，我们可以使用字体族序列指定 font-family:

```css
body {
  font-family: Georgia, serif;
}
```

这样做，如果用户电脑没有安装 Georgia，则文档就会显示 serif。

## 5.2. @font-face

@font-face 的作用是让你在设计中使用自定义的字体。这个特性首次出现在 CSS2 中。

假设你想使用的字体没有广泛安装，而是个特殊的字体。借助 @font-face，你可以定义一个专门的字体族名称，对应服务器上的一个字体文件。用户代理将下载那个文件，使用它渲染。

例如：

```css
@font-face {
  font-family: 'SwitzeraADF';
  src: url('SwitzeraADF-Regular.otf');
}
```

## 5.3. font-weight

font-weight 属性可以精确控制字重。一般来说，自重越大，字体越黑，越粗。

font-weight 属性值可以取 100 到 900 的正一百值。还可以取 normal, bold, bolder, lighter 这几个关键字。不过一般而言，还是推荐使用关键字。

## 5.4. font-size

font-size 属性用于控制字体的大小。

### 5.4.1. 绝对大小

font-size 支持的绝对大小值有：xx-small, x-small, small, medium, large, x-large, 和 xx-large。这个几个关键字没有固定的大小是相对而言的。

### 5.4.2. 相对大小

关键字 larger 和 smaller 相对简单，它们根据父元素的字号增大或减少一定比例。

百分数也可以用作字号，百分数始终根据父元素的字号计算。

em 这个相对单位和百分数相似，1em 相当于 100%。

### 5.4.3. 长度单位

font-size 可以设置为任何的长度值。

## 5.5. font-style

font-style 设置字体在 normal（常规），italic（斜体），和 oblique（倾斜体之间做选择）。

斜体和倾斜体之间的区别是，斜体是一种单独的字型，字母的构造有改动。而倾斜体只是竖直体的倾斜版本。

## 5.6. font-variant

font-variant 设置了字体的一些变形信息。

## 5.7. font

font 属性是 font-style, font-size, font-family 属性的简写。

# 6. 文本

本章讨论关于文本属性的控制。不过在此之前，我们要明白“行内”和“块级”这两个术语。文本书写的块级方向是指文本是竖直放置的，就像一个个段落那样。而行内书写方向是横向的，可能是从左至右（比如英语），也可能是从右往左（阿拉伯语）。

## 6.1. 缩进与行内对齐

### 6.1.1. text-indent

多数语言在排版时，会缩进第一段的第一行。以前，要想达到缩进效果，会在第一行的左边放一个透明的图像。CSS 为缩进文本提供了一个更好的方法：text-indent。

text-indent 属性把元素第一行文本缩进指定的长度。这个属性常用作缩进段落的第一行。

例如：

```css
p {
  text-indent: 2em;
}
```

text-indent 可以用于任何块级元素上，但不能用于行内元素或替换性元素。

### 6.1.2. text-align

text-align 可以控制元素中每行文本的对齐方式。这个属性的值可以取 start，end，left，right，center，justify。

left，right，和 center 取值从字面意思就可以看出它们的含义。left 代表各行文本靠左对齐。right 则是靠右。center 是居中对齐。

CSS3 添加了 start 和 end。这是由于一些语言，如阿拉伯语默认情况下就是从右往左书写的。新修订的 start 值表示文本与元素盒子的起始边对齐。end 表示和元素盒子的终止边对齐。

justify 值表示两端对齐。

### 6.1.3. text-align-last

有时候，你可能希望对齐最后一行。此时，你可以使用 text-align-last。它的取值和 text-align 基本一致。

## 6.2. 块级对齐

讲完行内文本对齐后，我们开始讲块级文本对齐。

### 6.2.1. line-height

line-height 可以控制文本行的高度。在讲解之前我们首先得了解行高是由什么构成的。

实际上，一个文本行的高度并不是字体的大小，而是加上了行距。一般而言，如果字体大小是 16px，那么浏览器会设置行高为 16px 的 1.2 倍，这样字的上下方就各有 (16px \* 1.2 - 16px) = 0.6px 的行距，这样文本行之间显得就不是很紧密。

如果我们设置了 line-height 为 18px，那么相当于增大了行距，假设字体大小为 16px，那么行距为：(18px - 16px)/2 = 1px。

### 6.2.2. vertical-align

vertical-align 可以控制行内元素文本竖直方向的对齐。它可以取值：baseline，sub，super，bottom，text-bottom，middle，top 和 text-top。

当 vertical-align 取 baseline（默认值）时，会使得元素的基线和父元素的基线对齐。如果目标元素没有基线，例如替换性元素，那么元素的底端和父元素的基线对齐。

当 vertical-align 取 sub 值时，元素的基线低于父元素的基线，此时我们说目标元素位于下标位置。不同的浏览器对于目标元素的下沉距离实现不同。

和 sub 类似，super 值使得目标元素位于上标位置。

当 vertical-align 取 bottom 值时，目标元素和父元素的文本行底部对齐。

和 bottom 类似，top 值使得目标元素和父元素的文本行顶部对齐。

## 6.3. 文本间距

本节来讨论单词间距和字符间距。

### 6.3.1. wording-spacing

word-spacing 属性用来指定文本的单词间距。默认值为 0。对于单词的定义，不能适用于象形文字。

### 6.3.2. letter-spacing

letter-spacing 属性用来指定文本的字符间距。默认值为 0。这个属性可以用于象形文字。

## 6.4. text-transform

text-transform 用于转换文本，可以取值：none(默认值), lowercase, uppercase, 和 captalize。

lowercase 用于将文本转为小写。uppercase 用于将文本转为大写。captalize 用于将单词的首字母大写。

## 6.5. text-decoration

text-decoration 用于装饰文本。可以取值：none(默认值), underline, overline, line-through, blink。

underline 在文本下面加上下划线，overline 在文本上面加上一条线。line-through 绘制一条穿过文本的线，也叫删除线。

## 6.6. text-shadow

text-shadow 用于给文本加上阴影。这个属性的默认值为 none。

这个属性可以多次使用，相当于给文本加上多个阴影。

下面的例子演示了一个文本阴影：

```css
p {
  text-shadow: black 5px 2px;
}
```

第一个参数表示阴影的颜色，第 2 个参数表示阴影的横向偏移，在这个例子中阴影向右边偏移了 5px，第 3 个参数表示纵向偏移。

## 6.7. 处理空白

white-space 属性用于处理 HTML 源码中的空格，换行符，制表符。

white-space 属性可以取值：normal(默认值), nowrap, pre, pre-wrap, pre-line。

## 6.8. line-break

## 6.9. overflow-wrap

## 6.10. writing-mode

## 6.11. text-orientation

## 6.12. direaction

# 7. 盒模型基础

# 8. 边距

# 9. 颜色，背景和渐变

# 10. 浮动

# 11. 定位

# 12. 弹性盒子

# 13. 网格

# 14. 表格

# 15. 列表

# 16. 变换

# 17. 过渡

# 18. 动画

# 19. 滤镜，混合，剪切与遮罩

# 20. 媒体查询
