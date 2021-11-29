**目录：**

- [1. CSS 简介](#1-css-简介)
  - [1.1. CSS 历史](#11-css-历史)
  - [1.2. HTML 元素](#12-html-元素)
    - [1.2.1. 可替换性](#121-可替换性)
    - [1.2.2. 显示类型](#122-显示类型)
  - [1.3. 引入 CSS](#13-引入-css)
    - [1.3.1. 外部样式表](#131-外部样式表)
    - [1.3.2. 内部样式表](#132-内部样式表)
    - [1.3.3. 行内样式](#133-行内样式)
  - [1.4. CSS 处理模型](#14-css-处理模型)
  - [1.5. 样式表](#15-样式表)
    - [1.5.1. 样式规则](#151-样式规则)
    - [1.5.2. 厂商前缀](#152-厂商前缀)
    - [1.5.3. 空白](#153-空白)
    - [1.5.4. 注释](#154-注释)
  - [1.6. 媒体查询](#16-媒体查询)
    - [1.6.1. 媒体类型](#161-媒体类型)
    - [1.6.2. 媒体特性](#162-媒体特性)
    - [1.6.3. 媒体描述符](#163-媒体描述符)
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
  - [3.1. 继承](#31-继承)
  - [3.2. 层叠](#32-层叠)
    - [3.2.1. 层叠顺序](#321-层叠顺序)
    - [3.2.2. !important 规则](#322-important-规则)
    - [3.2.3. 特指度](#323-特指度)
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
    - [6.7.1. white-space](#671-white-space)
    - [6.7.2. tab-size](#672-tab-size)
  - [6.8. 换行和断字](#68-换行和断字)
    - [6.8.1. word-break](#681-word-break)
    - [6.8.2. line-break](#682-line-break)
    - [6.8.3. overflow-wrap](#683-overflow-wrap)
  - [6.9. 书写模式](#69-书写模式)
    - [6.9.1. writing-mode](#691-writing-mode)
    - [6.9.2. text-orientation](#692-text-orientation)
- [7. 盒模型](#7-盒模型)
  - [7.1. 盒模型基础](#71-盒模型基础)
    - [7.1.1. 重要概念](#711-重要概念)
    - [7.1.2. 包含盒子](#712-包含盒子)
  - [7.2. 盒子的类型和尺寸](#72-盒子的类型和尺寸)
    - [7.2.1. 改变显示类型](#721-改变显示类型)
    - [7.2.2. 改变尺寸](#722-改变尺寸)
  - [7.3. 块级盒子](#73-块级盒子)
    - [7.3.1. 横向格式化](#731-横向格式化)
      - [7.3.1.1. 1 个 auto](#7311-1-个-auto)
      - [7.3.1.2. 多个 auto](#7312-多个-auto)
    - [7.3.2. 替换性块级元素](#732-替换性块级元素)
    - [7.3.3. 纵向格式化](#733-纵向格式化)
  - [7.4. 行内盒子](#74-行内盒子)
  - [7.5. 行内块级盒子](#75-行内块级盒子)
- [8. 边距与边框](#8-边距与边框)
  - [8.1. 内边距](#81-内边距)
  - [8.2. 边框](#82-边框)
  - [8.3. 轮廓](#83-轮廓)
  - [8.4. 外边距](#84-外边距)
- [9. 颜色，背景和渐变](#9-颜色背景和渐变)
  - [9.1. 颜色](#91-颜色)
  - [9.2. 背景](#92-背景)
  - [9.3. 渐变](#93-渐变)
- [10. 浮动](#10-浮动)
  - [10.1. 浮动](#101-浮动)
  - [10.2. 清除浮动](#102-清除浮动)
  - [10.3. 浮动形状](#103-浮动形状)
- [11. 定位](#11-定位)
  - [11.1. 基本概念](#111-基本概念)
  - [11.2. 偏移属性](#112-偏移属性)
  - [11.3. 宽度和高度](#113-宽度和高度)
  - [11.4. 内容溢出](#114-内容溢出)
  - [11.5. 可见性](#115-可见性)
  - [11.6. 绝对定位](#116-绝对定位)
  - [11.7. 固定定位](#117-固定定位)
  - [11.8. 相对定位](#118-相对定位)
  - [11.9. 粘连定位](#119-粘连定位)
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

CSS 依赖 HTML 元素，但并非每种元素都以同样的方式创建。例如，img 和 p 是不同类型的元素。对 CSS 而言，HTML 元素分为两种：替换元素和非替换元素。

### 1.2.1. 可替换性

- 替换性元素

替换性元素(replaced element)是指用来替换元素内容的部分不是由文档内容表示的。例如，img 元素，它的内容由文档之外的图像文件替换，由文档直接表示的内容是空的：

```html
<img src="img.jpg" />
```

这个元素只包含一个属性，并没有内容。

还有 input 元素，根据类型的不同会被替换为复选框或者输入框。

- 非替换性元素

HTML 元素大部分都是非替换性的，意思就是这种元素的内容在文档中直接表示了。例如：

```html
<p>一段文本。</p>
```

这个元素在显示时，直接显示的是 "一段文本。"。

### 1.2.2. 显示类型

除了 HTML 元素的可替换性外，CSS 还把元素分为块级和行内类型，这是根据元素的 display 属性进行区分的，当然还有其他显式类型。

- 块级元素

HTML 元素大多数都是“块级”元素或行内元素。块级元素占据其父元素的整个水平空间，垂直空间等于其内容高度，因此创建了一个“块”。通常浏览器会在块级元素前后另起一个新行。

块级元素可以包含行内元素，也可以包含块级块级元素。

块级元素的 display 属性值为 block。

- 行内元素

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

- link 元素的属性

link 元素的 rel 属性表示链接资源和 HTML 文档的关系，对于 CSS 文档来说，就是“stylesheet”。

link 元素的 href 属性制定了链接资源的地址。

最后的 media 属性，它的值是一个或多个媒体描述符(media descriptor)，表示什么样的媒体应该使用这个 CSS 文档。例如：

```html
<link rel="stylesheet" href="style.css" media="screen, screen" />
```

多个媒体描述符用逗号分隔。媒体描述符本书后面会详细的介绍。

link 的 type 属性现在已经不常用了，它用来指定资源的 MIME 类型，不过对于 CSS 文档，浏览器默认为 "text/css"。

- @import

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

## 1.4. CSS 处理模型

本节介绍了支持 CSS 的用户代理如何工作的一个可能模型。这只是一个概念性的模型；实际的实现可能会有所不同。

在这个模型中，用户代理通过以下步骤来处理一个源。

1. 解析源文档并创建一个文档树。
2. 识别目标媒体类型。
3. 检索所有与该文档相关的、为目标媒体类型指定的样式表。
4. 通过给适用于目标媒体类型的每个属性分配一个单一的值来注释文档树的每个元素。属性是根据层叠和继承一节中描述的机制来分配数值的。部分数值的计算取决于适合于目标媒体类型的格式化算法。例如，如果目标媒体是屏幕，用户代理会应用视觉格式化模型。
5. 从注释的文档树中，生成一个格式化结构。通常，格式化结构与文档树非常相似，但也可能有很大不同，特别是当作者使用伪元素和生成的内容时。首先，格式化结构根本不需要是 "树形 "的，结构的性质取决于实现。第二，格式化结构可能包含比文档树更多或更少的信息。例如，如果文档树中的一个元素的 "display "属性的值是 "none"，那么这个元素在格式化结构中就不会产生任何信息。另一方面，一个列表元素可能会在格式化结构中产生更多的信息：列表元素的内容和列表样式信息（例如，一个子弹头图像）。请注意，CSS 用户代理在这个阶段不会改变文档树。特别是，由于样式表产生的内容不会被反馈给文档语言处理器（例如，用于重新解析）。
6. 将格式化结构转移到目标媒介（例如，打印结果、在屏幕上显示、渲染成语音等）。

## 1.5. 样式表

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

### 1.5.1. 样式规则

一个 CSS 样式规则有 2 个部分组成：选择器和声明块。选择器制定了声明块中样式的应用目标元素。声明块则由一个或多个样式声明组成。一个样式声明是一个键值对，包含属性和对应值。

例如：

```css
h1 {
  color: red;
  background-color: yellow;
}
```

这个例子中，h1 就是一个最简单的选择器（本书后面会介绍各种选择器），后面的声明块中包含了 2 条样式声明：color 和 backgroung-color。属性和值用冒号分开。每一条声明都要以分号结尾。

### 1.5.2. 厂商前缀

有时候，CSS 中的属性会包含厂商前缀(vendor prefix)。如：-o-border-image。带有厂商前缀的属性往往只是对应厂商的浏览器有，或者这些属性还在实验中。

下表列出了常用的厂商前缀：

| 浏览器            | 前缀     |
| ----------------- | -------- |
| Chrome, Safari    | -webkit- |
| Opera             | -o-      |
| Firefox           | -moz-    |
| Internet Explorer | -ms-     |

### 1.5.3. 空白

CSS 对 CSS 文档中的空白没有严格要求。一般来说，样式规则之间用换行符分隔。选择器和声明块之间用一个空格分隔。样式声明之间用换行符分隔，且缩进 2 个或是 4 个空格。

良好的空白有助于阅读。

### 1.5.4. 注释

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

## 1.6. 媒体查询

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

### 1.6.1. 媒体类型

下面总结了常用的媒体类型：

- all

用于所有媒体

- screen

用于屏幕

- print

用于印刷

但是往往我们还需要知道一些媒体的特性，例如屏幕的大小等等。

### 1.6.2. 媒体特性

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

### 1.6.3. 媒体描述符

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

要想掌握CSS，弄清样式层叠和继承这两个概念是关键。

## 3.1. 继承

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

## 3.2. 层叠

样式表可能有三个不同的来源：作者、用户和用户代理。

- **作者**。作者根据文档语言的惯例为一个源文档指定样式表。例如，在 HTML 中，样式表可能被包含在文档中或从外部链接。
- **用户**：用户可能能够为一个特定的文档指定样式信息。例如，用户可以指定一个包含样式表的文件，或者用户代理可以提供一个生成用户样式表的界面（或者表现得像它一样）。
- **用户代理**。符合要求的用户代理必须应用一个默认的样式表（或者表现得像他们一样）。一个用户代理的默认样式表应该以满足文档语言的一般表现期望的方式来表现文档语言的元素（例如，对于视觉浏览器，HTML 中的 EM 元素用斜体字来表现）。

注意，用户可以修改影响默认样式表的系统设置（例如，系统颜色）。然而，一些用户代理的实现使其无法改变默认样式表的值。

来自这三个源头的样式表在范围上会重叠，它们根据层叠进行交互。

CSS 层叠给每个样式规则分配了一个权重。当有几个规则适用时，具有最大权重的规则优先。

默认情况下，作者样式表中的规则比用户样式表中的规则具有更大的权重。然而，对于"!important"的规则，优先权是相反的。所有的用户和作者规则都比用户代理的默认样式表中的规则有更大的权重。

### 3.2.1. 层叠顺序

为了找到一个元素/属性组合，用户代理必须应用以下排列顺序：

1. 找到所有适用于有关元素和属性的声明，用于目标媒体类型。如果相关的选择器与查询元素相匹配，并且目标媒体与包含声明的所有@media规则上的媒体列表以及到达样式表的路径上的所有链接相匹配，则声明适用。
2. 根据重要性（正常或重要）和来源（作者、用户或用户代理）排序。以升序的方式排列：
   1. 用户代理声明
   2. 用户正常声明
   3. 作者正常声明
   4. 作者重要声明
   5. 用户重要声明
3. 根据选择器的特指度对具有相同重要性和来源的规则进行排序：更具体的选择器将覆盖更一般的选择器。伪元素和伪类分别被算作正常元素和类。
4. 最后，按指定的顺序排列：如果两个声明具有相同的权重、来源和特指度，则指定的后者获胜。在导入的样式表中的声明被认为是在样式表本身的任何声明之前。

除了个别声明的"!important"设置外，这个策略给予作者的样式表比读者的样式表更高的权重。用户代理必须让用户有能力关闭特定作者样式表的影响，例如通过一个下拉菜单。

### 3.2.2. !important 规则

CSS 试图在作者和用户的样式表之间建立一种权力平衡。默认情况下，作者的样式表中的规则优先于用户的样式表中的规则。

然而，为了平衡，一个"!important"的声明（分隔符"!"和关键字 "important"跟在声明后面）优先于一个普通的声明。作者和用户的样式表都可以包含"!important"声明，而用户的"!important"规则优先于作者的"!important"规则。这个 CSS 特性通过给有特殊要求的用户（大字体、颜色组合等）对表现形式的控制来提高文档的可访问性。

将一个简写属性（例如，"background"）声明为"!important"，相当于将其所有的子属性声明为"!important"。

在下面的例子中，用户的样式表中的第一条规则包含一个"!important"的声明，它覆盖了作者样式表中的相应声明。第二个声明也会因为被标记为"!important"而获胜。然而，用户样式表中的第三条规则不是"!important"的，因此将输给作者样式表中的第二条规则（它恰好在一个简写属性上设置样式）。另外，第三个作者规则将输给第二个作者规则，因为第二个规则是"!important"的。这表明"!important"声明在作者样式表中也有作用。

```css
/* 来自用户的样式表 */
p {
  text-indent: 1em !important;
}
p {
  font-style: italic !important;
}
p {
  font-size: 18pt;
}

/* 来自作者的样式表 */
p {
  text-indent: 1.5em !important;
}
p {
  font: normal 12pt sans-serif !important;
}
p {
  font-size: 24pt;
}
```

### 3.2.3. 特指度

一个选择器的特指度的计算方法如下：

- 如果声明来自一个 "style" 属性而不是一个带有选择器的规则，则计数为 1，否则为 0（=a）（在 HTML 中，一个元素的 "style" 属性的值是样式表规则。这些规则没有选择器，所以 a=1，b=0，c=0，d=0）。
- 计算选择器中 ID 属性的数量(=b)
- 计算选择器中其他属性和伪类的数量(= c)
- 计算选择器中的元素名称和伪元素的数量(= d)

特指度只基于选择器的形式。特别是，形式为"[id=p33]"的选择器被算作一个属性选择器（a=0, b=0, c=1, d=0），即使 id 属性在源文档的 DTD 中被定义为 "ID"。

将 a-b-c-d 这四个数字串联起来就得到了特指度。

一些例子：

```css
 * {}  /* a=0 b=0 c=0 d=0 -> 特指度=0,0,0,0 */
 li {}  /* a=0 b=0 c=0 d=1 --> 特指度=0,0,0,1 */
 li::first-line {} /* a=0 b=0 c=0 d=2 -> 特指度=0,0,0,2 */
 ul li {}  /* a=0 b=0 c=0 d=2 --> 特指度 = 0,0,0,2 */
 ul ol+li {}  /* a=0 b=0 c=0 d=3 --> 特指度=0,0,0,3 */
 h1 + *[rel=up]{} /* a=0 b=0 c=1 d=1 --> 特指度=0,0,1,1 */
 ul ol li.red {}  /* a=0 b=0 c=1 d=3 --> 特指度 = 0,0,1,3 */
 li.red.level {}  /* a=0 b=0 c=2 d=1 --> 特指度=0,0,2,1 */
 #x34y {}  /* a=0 b=1 c=0 d=0 --> 特指度=0,1,0,0 */
 style="" /* a=1 b=0 c=0 d=0 --> 特指度 = 1,0,0,0 */
```

```html
<head>
  <style type="text/css">
    #x97z {
      color: red;
    }
  </style>
</head>
<body>
  <p id="x97z" style="color: green"></p>
</body>
```

在上面的例子中，P 元素的颜色将是绿色。由于层叠规则，"style" 属性中的声明将优先于 STYLE 元素中的声明，因为它具有更高的特指度。

# 4. 值与单位

本章探讨单位。单位可以影响距离，尺寸，颜色等等。单位是 CSS 的重要基础，几乎一切值都离不开它。

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

### 6.7.1. white-space

white-space 属性用于处理 HTML 源码中的空格，换行符，制表符。

white-space 属性可以取值：normal(默认值), nowrap, pre, pre-wrap, pre-line。

normal 值表示 HTML 文档中，文本之间连续的空格默认会被合并为 1 个：

```html
<p>有 很多 空格 的 文 本。</p>
```

这个 p 元素实际上和下面的是相同的：

```html
<p>有 很多 空格 的文 本。</p>
```

然而，我们可以设置 white-space 为 pre，这样连续的空格不会被忽略。但不仅如此，回车符，制表符也会得到保留。

nowrap 禁止元素中的文本换行，除非使用了 br 元素。

pre-wrap 和 pre-line 是 CSS2.1 引入的，设为 pre-wrap 时，文本中的空白可以保留，但文本将换行。pre-line 则是合并连续空白，但是保留换行。

下表进行了总结：

| 值       | 空白 | 换行符 | 自动换行 |
| -------- | ---- | ------ | -------- |
| normal   | 合并 | 忽略   | 允许     |
| nowrap   | 合并 | 忽略   | 禁止     |
| pre-line | 合并 | 保留   | 允许     |
| pre-wrap | 保留 | 保留   | 允许     |
| pre      | 保留 | 保留   | 禁止     |

### 6.7.2. tab-size

既然 white-space 取某些值时空白保留下来，那么制表符就会被保留下来。但一个制表符等于多少个空格呢？tab-size 属性就派上了用场。

默认情况下，一个制表符相当于 8 个连续的空格。不过，可以使用 tab-size 属性改变。

## 6.8. 换行和断字

### 6.8.1. word-break

word-break 属性用于控制文本换行。可以取值：normal, break-all, keep-all。

默认值 normal 的意思是文本在单词之间换行。如果使用 break-all，换行可以出现在任意字符之间。keep-all 禁止在字符之间换行。

### 6.8.2. line-break

line-break 适用于中文，日文以及韩文语言的换行。这个属性可以取值：auto，loose，normal，和 strict。

### 6.8.3. overflow-wrap

overflow-wrap 用于文本行超出容器时的处理。可以取值：normal 和 break-word。当取 normal 时，按照单词之间换行。使用 break-word 时可以在单词内部换行。

## 6.9. 书写模式

英语是从左向右从上到下排列的，然而其他语言并不都是这样。

### 6.9.1. writing-mode

writing-mode 可以指定书写模式。可以取值：horizontal-tb（默认值），vertical-rl，vertical-lr。

默认值 horizontal-tb 表示行内方向为横向，块级方向为从上到下。后 2 个值得行内方向时纵向，块级方向分别为从右到左和从
左到右。

### 6.9.2. text-orientation

选定书写模式后，可能还想改变文本行中字符的方向。这就要用到 text-orientation。可以取值：mixed（默认），upright，sideways。

当书写模式取值 vertical-lr 时，中英文的字符方向并不统一，这是因为 text-orientation 默认取值 mixed。当取值 sideways 时，2 种字符都是一个方向向侧边。而 upright 则是从上到下的方向。

# 7. 盒模型

本章全面阐述 CSS 视觉渲染理论。

## 7.1. 盒模型基础

对于任何 HTML 元素，CSS 都会在逻辑上生成一个对元素层层包围的盒子。这个盒子从中心到外围依次是：内容区，内边距，边框，外边距。内边距，边框，外边距都有针对每一条边的属性，例如：border-bottom, margin-left, padding-right 等等。
默认情况下，内容区的背景出现在内边距范围内。外边距始终是不可见的。

### 7.1.1. 重要概念

下面简要说明一下要讨论的不同显示方式的盒子，以及一些术语。

- 常规流动

常规流动是指 HTML 元素从上往下，从左往右的布局方式。除非元素浮动，定位，放入弹性盒子或采用网格布局了，不然 HTML 元素都采用常规流动。

- 块级盒子

块级盒子是指块级元素生成的盒子。块级盒子在常规流动下，前后都会换行，因此是纵向排列的。常见的生成 块级盒子的 HTML 元素有：div，p，h1-h6。

- 行内盒子

行内盒子是指行内元素生成的盒子。这种盒子在常规流动下前后不换行。常用的生成 行内盒子的 HTML 元素有：span, strong。

- 行内块级盒子

这种盒子外部特征像行内盒子，内部像块级盒子。这种盒子的行为和替换性元素相似。

### 7.1.2. 包含盒子

还有一种盒子需要深入说明：包含盒子。

每个元素的盒子相对上都有其包含盒子，包含盒子也叫元素盒子的布局上下文。

在采用常规流动方式渲染的文本中，包含盒子一般是元素的父元素，而且 display 属性为 block。

## 7.2. 盒子的类型和尺寸

HTML 元素几乎都有 display 属性。可以取值：none, inline, block, flex, grid, table 等一系列值。

### 7.2.1. 改变显示类型

假设 nav 元素中有一系列链接，而我们相纵向布局，为此我们可以将 a 元素的 display 属性改为 block。

```html
<nav>
  <a href="http://www.google.com/">google</a>
  <a href="http://www.baidu.com/">baidu</a>
  <a href="http://www.github.com/">github</a>
  <a href="http://www.stackoverflow.com/">stackoverflow</a>
</nav>
```

### 7.2.2. 改变尺寸

默认情况下生成 块级盒子的元素的大小(width，或者 height)等于内容区的大小。这是由于 box-sizing 默认为 content-box。

在这种情况下，我们给元素设置的大小只是给内容区设置的。如果加上内边距的话，总的可见区域的大小就是内边距和内容区大小的合并。因此比较麻烦。

我们通常设置 box-sizing 为 border-box，这表示你给元素设置的大小等于内容区，内边距和边框的大小的合并，因此我们就不用时刻关注一个元素的内边距。

```css
* {
  box-sizing: border-box;
}
```

## 7.3. 块级盒子

### 7.3.1. 横向格式化

横向格式化比较复杂。

常规流动下，块级盒子的整个宽度等于包含盒子的宽度。

假设，box-sizing 为 border-box。现在 1 个 div 元素中有 2 个 p 元素。div 元素的宽度为 30em，那么每个 p 元素的 width 属性值和外边距之和就等于 30em。

横向格式化属性有 7 个：除了 width 属性之外。还有内边距，边框，外边距对应的横向属性。

这 7 个属性的值加在一起等于包含盒子的宽度。而这一宽度通常为块级元素父元素的 width 值（块级元素的父元素几乎都是块级元素）。

#### 7.3.1.1. 1 个 auto

在这 7 个属性中，只有 3 个属性的值能设置为 auto：width, margin-left, margin-right。剩下的几个值要么使用默认值 0，要么使用具体的值。

如果把这 3 个属性都设置为具体的值，用 CSS 术语来说就是过约束了，在这种情况下，margin-right 将被设置为 auto，即补全值。

例如，给定 box-sizing 为 border-box，p 元素的父元素 width 为 500px，且给定 p 的 width, margin-left, margin-right 都为 100px，那么实际情况可能不是我们所想的那样。实际上，p 的 margin-left 属性和 width 属性不会改变，而 margin-right 会被设置为 auto，即补全值 300px。

在这 3 个属性中，如果 1 个属性被设为 auto，其他属性被设为具体的值，那么这个 auto 值就会被计算为补全的宽度值。

例如，如果左右外边距都设为具体的值，且 width 设置为 auto 或者不设置，那么 width 就是补全值。上个例子中，margin-left 和 margin-right 设置为 100px，那么 width 就是 300px。

#### 7.3.1.2. 多个 auto

如果左右边距都设置为 auto，width 设置为具体的值，那么这种情况显示效果就是：可见区域（内容区+内边距+边框）居中显示，其长度就是设置的具体值，而左右外边距的宽度相等，其值是补全值的一半。

例如，width 被设置为 300px，那么 margin-left 和 margin-right 都是 100px。

在常规流动下，这种方式可以使得元素可见区域在父元素盒子中居中显示。

如果一个边距被设置为具体值，另一个边距被设置为 auto，且 width 也被设置为 auto，那么在这种情况下，被设置为 auto 的那个外边距的宽度为 0，width 值就是补全值。

如果三个属性都被设置为 auto 呢？答案是外边距被设置为 0，width 为补全值，即父元素的宽度。实际上这和默认情况是一样的：外边距和 width 都没有显式声明，那么 块级盒子的 width 值就是父元素的宽度。

### 7.3.2. 替换性块级元素

到目前为止，我们都在讨论常规流动下非替换性元素生成的 块级盒子的横向格式化。对于替换性元素生成的 块级盒子处理就要简答一些。前面所讲的规则都成立，不过有个例外是 width 为 auto 时，元素的 width 等于替换内容自身的宽度。

不过，我们可以显式指定这个 width 值，就会覆盖默认的替换性内容宽度。当我们明确设置 width 值时，其 height 会根据比例放缩，单独设置 height 也是一样的。除非我们将 width 和 height 都明确设置。

### 7.3.3. 纵向格式化

块级盒子的纵向格式化与横向格式化类似，但也有一些不同。元素的默认 height 值是元素内容的高度，而不是像 width 是其父元素的 width 值。

与横向格式化一样，纵向格式化也涉及 7 个属性。这 7 个属性中能设置为 auto 的属性和横向格式化类似：margin-top, margin-bottom, height。

在 margin-top 和 margin-bottom 都设置为 auto，且 height 为具体值的情况下，和横向格式化不同，marign-top 和 margin-bottom 都将设置为 0。

纵向格式化还有一点不同的是，纵向的外边距会发生折叠。

例如：

```css
ul > li {
  margin-top: 10px;
  margin-bottom: 15px;
}
```

这个例子中，每个项目列表都有 10px 的上外边距和 15px 的下外边距，然而多个列表项目之间的边距不是 25px，而是 15px。这是因为，相邻的外边距在纵轴上折叠的，较小的外边距被较大的覆盖了。

## 7.4. 行内盒子

除了块级元素之外，行内元素是最为常见的。常见的非替换性行内元素有：em, a。替换性元素：img。

## 7.5. 行内块级盒子

# 8. 边距与边框

## 8.1. 内边距

## 8.2. 边框

## 8.3. 轮廓

## 8.4. 外边距

# 9. 颜色，背景和渐变

## 9.1. 颜色

## 9.2. 背景

## 9.3. 渐变

# 10. 浮动

## 10.1. 浮动

## 10.2. 清除浮动

## 10.3. 浮动形状

# 11. 定位

## 11.1. 基本概念

## 11.2. 偏移属性

## 11.3. 宽度和高度

## 11.4. 内容溢出

## 11.5. 可见性

## 11.6. 绝对定位

## 11.7. 固定定位

## 11.8. 相对定位

## 11.9. 粘连定位

# 12. 弹性盒子

# 13. 网格

# 14. 表格

# 15. 列表

# 16. 变换

# 17. 过渡

# 18. 动画

# 19. 滤镜，混合，剪切与遮罩

# 20. 媒体查询
