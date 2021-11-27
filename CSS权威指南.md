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
  - [3.1. 层叠](#31-层叠)
  - [3.2. 继承](#32-继承)
- [4. 值与单位](#4-值与单位)
  - [4.1. 关键字，字符串和其他文本值](#41-关键字字符串和其他文本值)
  - [4.2. 数值](#42-数值)
  - [4.3. 距离](#43-距离)
  - [4.4. 计算值](#44-计算值)
  - [4.5. 属性值](#45-属性值)
  - [4.6. 颜色](#46-颜色)
  - [4.7. 角度](#47-角度)
  - [4.8. 时间和频率](#48-时间和频率)
  - [4.9. 位置](#49-位置)
  - [4.10. 自定义值](#410-自定义值)
- [5. 字体](#5-字体)
  - [5.1. 字体族](#51-字体族)
  - [5.2. 5.2.](#52-52)

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

## 3.1. 层叠

## 3.2. 继承

# 4. 值与单位

## 4.1. 关键字，字符串和其他文本值

## 4.2. 数值

## 4.3. 距离

## 4.4. 计算值

## 4.5. 属性值

## 4.6. 颜色

## 4.7. 角度

## 4.8. 时间和频率

## 4.9. 位置

## 4.10. 自定义值

# 5. 字体

## 5.1. 字体族

## 5.2. 5.2.
