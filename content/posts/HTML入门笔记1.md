---
title: "HTML入门笔记1"
date: 2019-11-19T20:24:05+08:00
draft: false
---
### 1. HTML 起手式

`新建demo-->新建html--><!DOCTYPE html>`
![](https://upload-images.jianshu.io/upload_images/16155751-df06494fb93fad90.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
### 2. 全局属性
- [style](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/style) 元素CSS样式声明
```
<style>
      style{display:block;}
      #xxx{
       color:green;
      }
  </style>
```
![](https://upload-images.jianshu.io/upload_images/16155751-7336227b2062b399.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

`使得style可见，前提需将style放入body中`
- [class](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/class)  类名列表
```
  <style>
   [class="hder"]{
     color:red;
   }
   .hder{
     color:green;
   }
  </style>
<header class="hder">这是我的html笔记</header>
```
`如果class有多个属性，则[class="属性"]需写入全部属性才可匹配对应的class，使用 .属性方式写入class的某一个属性即可匹配class`
- [contenteditable](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/contenteditable)   元素是否可被用户编辑
![](https://upload-images.jianshu.io/upload_images/16155751-03a1374b63098e2e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- [hidden](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/hidden) 隐藏元素
![](https://upload-images.jianshu.io/upload_images/16155751-d9f330ba0b981f02.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- [id](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/id
) 唯一标识符
![翻车现场](https://upload-images.jianshu.io/upload_images/16155751-9d061d0ca79d7208.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

`不到万不得已不使用id，id不报错`

- [tabindex](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/tabindex) 整数属性，指示元素是否可以获取输入焦点（可聚焦），是否应该参与顺序键盘导航
`正值通过顺序键盘导航进行聚焦和访问,0 表示最后访问，-1表示不可通过键盘导航到达`
- [title](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/title) 表示与其所属元素相关信息的文本
![](https://upload-images.jianshu.io/upload_images/16155751-8f54fc0542dbdf8f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### 3.章节标签
| 章节                                                                                                                                                                                                                                                                                                                                                                                        |                                        |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------- |
| [`<section>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/section "HTML Section 元素 (<section>) 表示文档中的一个区域（或节），比如，内容中的一个专题组，一般来说会有包含一个标题（heading）。一般通过是否包含一个标题 (<h1>-<h6> element) 作为子节点 来 辨识每一个<section>。")                                                                                              | 定义文档中的一个章节                   |
| [`<h1>,<h2>,<h3>,<h4>,<h5>,<h6>`](https://developer.mozilla.org/zh-CN/docs/HTML/Element/Heading_Elements)                                                                                                                                                                                                                                                                                   | 六层文档标题，`<h1>` 最大`,<h6>` 最小  |
| [`<article>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/article "<article>元素表示文档、页面、应用或网站中的独立结构，其意在成为可独立分配的或可复用的结构，如在发布中，它可能是论坛帖子、杂志或新闻文章、博客、用户提交的评论、交互式组件，或者其他独立的内容项目。")                                                                                                      | 可以独立于内容其余部分的完整独立内容块 |
| [`<p>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/p "HTML <p>元素（或者说 HTML 段落元素）表示文本的一个段落。该元素通常表现为一整块与相邻文本分离的文本，或以垂直的空白隔离或以首行缩进。另外，<p> 是块级元素。")                                                                                                                                                           | 定义一个段落                           |
| [`<header>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/header "HTML <header> 元素用于展示介绍性内容，通常包含一组介绍性的或是辅助导航的实用元素。它可能包含一些标题元素，但也可能包含其他元素，比如 Logo、搜索框、作者名称，等等。")                                                                                                                                        | 定义页面或章节的头部                   |
| [`<footer>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/footer "HTML <footer> 元素表示最近一个章节内容或者根节点（sectioning root ）元素的页脚。一个页脚通常包含该章节作者、版权数据或者与文档相关的链接等信息。")                                                                                                                                                           | 定义页面或章节的尾部                   |
| [`<main>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/main "HTML <main>元素呈现了文档<body>或应用的主体部分。主体部分由与文档直接相关，或者扩展于文档的中心主题、应用的主要功能部分的内容组成。这部分内容在文档中应当是独一无二的，不包含任何在一系列文档中重复的内容，比如侧边栏，导航栏链接，版权信息，网站logo，搜索框（除非搜索框作为文档的主要功能）。")                | 定义文档中主要或重要的内容。           |
| [`<aside>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/aside "<aside> 元素表示一个和其余页面内容几乎无关的部分，被认为是独立于该内容的一部分并且可以被单独的拆分出来而不会使整体受影响。其通常表现为侧边栏或者嵌入内容。他们通常包含在工具条，例如来自词汇表的定义。也可能有其他类型的信息，例如相关的广告、笔者的传记、web 应用程序、个人资料信息，或在博客上的相关链接。") | 定义和页面内容关联度较低的内容         |
| [`<div>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/div "HTML <div> 元素 (或 HTML 文档分区元素) 是一个通用型的流内容容器，它在语义上不代表任何特定类型的内容，它可以被用来对其它元素进行分组，一般用于样式化相关的需求（使用 class 或 id 特性) 或者对具有相同特性的一组元素进行分组 (比如 lang)，它应该在没有任何其它语义元素可用时才使用 (比如 <article> 或 <nav>) 。")    | 代表一个通用的容器                     |
### 4.内容标签
| 内容标签                                                                                                                                                                                                                                                                                                                                                                       |                                              |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------- |
| [`<ol>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/ol "HTML <ol> 元素 表示多个有序列表项，通常渲染为有带编号的列表。")                                                                                                                                                                                                                                         | 定义一个有序列表                             |
| [`<ul>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/ul "The HTML <ul> 元素 ( 或 HTML 无序列表元素） 代表多项的无序列表，即无数值排序项的集合，且它们在列表中的顺序是没有意义的。通常情况下，无序列表项的头部可以是几种形式，如一个点，一个圆形或方形。头部的风格并不是在页面的HTML描述定义, 但在其相关的CSS 可以用 list-style-type 属性。")                     | 定义一个无序列表                             |
| [`<li>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/li "HTML <li> 元素 (或者 HTML 列表条目元素) 用于表示列表里的条目。它必须被包含在一个父元素里：一个有顺序的列表(<ol>)，一个无顺序的列表(<ul>)，或者一个菜单 (<menu>)。在菜单或者无顺序的列表里，列表条目通常用点排列显示。在有顺序的列表里，列表条目通常是在左边有按升序排列计数的显示，例如数字或者字母。") | 定义列表中的一个列表项                       |
| [`<dl>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/dl "HTML <dl> 元素 （或 HTML 描述列表元素）是一个包含术语定义以及描述的列表，通常用于展示词汇表或者元数据 (键-值对列表)。")                                                                                                                                                                                 | 定义一个定义列表（一系列术语和其定义）       |
| [`<dt>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/dt "HTML <dt> 元素 （或 HTML 术语定义元素）用于在一个定义列表中声明一个术语。该元素仅能作为 <dl> 的子元素出现。通常在该元素后面会跟着 <dd> 元素， 然而，多个连续出现的 <dt> 元素都将由出现在它们后面的第一个 <dd> 元素定义。")                                                                              | 代表一个由下一个 `<dd>` 定义的术语           |
| [`<dd>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/dd "HTML <dd> 元素（HTML 描述元素）用来指明一个描述列表  (<dl>) 元素中一个术语的描述。这个元素只能作为描述列表元素的子元素出现，并且必须跟着一个 <dt> 元素。")                                                                                                                                              | 代表出现在它之前术语的定义                   |
| [`<pre>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/pre "HTML <pre> 元素表示预定义格式文本。在该元素中的文本通常按照原文件中的编排，以等宽字体的形式展现出来，文本中的空白符（比如空格和换行符）都会显示出来。(紧跟在 <pre> 开始标签后的换行符也会被省略)")                                                                                                    | 代表其内容已经预先排版过，格式应当保留       |
| [`<hr>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/hr "HTML <hr> 元素表示段落级元素之间的主题转换（例如，一个故事中的场景的改变，或一个章节的主题的改变）。在HTML的早期版本中，它是一个水平线。现在它仍能在可视化浏览器中表现为水平线，但目前被定义为语义上的，而不是表现层面上。")                                                                            | 代表章节、文章或其他长内容中段落之间的分隔符 |
| [`<br>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/br "HTML <br> 元素在文本中生成一个换行（回车）符号。此元素在写诗和地址时很有用，这些地方的换行都非常重要。")                                                                                                                                                                                                | 代表换行                                     |
| [`<a>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/a "HTML <a> 元素  (或锚元素) 可以创建一个到其他网页、文件、同一页面内的位置、电子邮件地址或任何其他URL的超链接。")                                                                                                                                                                                           | 代表一个链接到其他资源的*超链接*             |
| [`<em>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/em "HTML 着重元素 (<em>) 标记出需要用户着重阅读的内容， <em> 元素是可以嵌套的，嵌套层次越深，则其包含的内容被认定为越需要着重阅读。")                                                                                                                                                                       | 代表*强调* 文字                              |
| [`<strong>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/strong "Strong 元素 (<strong>)表示文本十分重要，一般用粗体显示。")                                                                                                                                                                                                                                      | 代表*特别重要* 文字                          |
| [`<code>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/code "HTML <code> 元素呈现一段计算机代码. 默认情况下, 它以浏览器的默认等宽字体显示.")                                                                                                                                                                                                                     | 代表*计算机代码*                             |
| [`<q>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/q "HTML引用标签 (<q>)表示一个封闭的并且是短的行内引用的文本. 这个标签是用来引用短的文本，所以请不要引入换行符; 对于长的文本的引用请使用 <blockquote> 替代.")                                                                                                                                                 | 代表内联的*引用*                             |
| [`<blockquote>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/blockquote "HTML <blockquote> 元素（或者 HTML 块级引用元素），代表其中的文字是引用内容。通常在渲染时，这部分的内容会有一定的缩进（注 中说明了如何更改）。若引文来源于网络，则可以将原内容的出处 URL 地址设置到 cite 特性上，若要以文本的形式告知读者引文的出处时，可以通过 <cite> 元素。")          | 代表引用自其他来源的内容                     |
```
        <pre>
          <code>
            var a = 1
            console.log(a)
          </code>
          <hr>
          <p>
            控制风险的<em>最好办法</em>是<strong>深入思考</strong>
          </p>
          <pre>
          <ul>
            <li> 查理·芒格说过：<q>我相信人类快乐的秘诀在于不要把目标定得太高。</q></li>
            <li> 沃伦·巴菲特说过：<blockquote>在错误的道路上，奔跑也没有用</blockquote></li>
          </ul>
        </pre>

```
![](https://upload-images.jianshu.io/upload_images/16155751-be4593e60b145e5f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

