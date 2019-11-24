---
title: "Css基础"
date: 2019-11-24T21:27:10+08:00
draft: false
---
### 一、语法
1. 样式语法
```
选择器 {
  属性名:  属性值;
  /*注释*/
}
```
2. at语法
```
@charset "UTF-8";
@import url(style.css);
@media (min-width: 100px) and (max-width: 200px) {
  语法一
}
```
#### 注意事项：
- @charset必须放在第一行
- at语法必须以分号;结尾
- 所有符号都是英文符号，区分大小写 

### 二、css调试
1. 使用vscode看颜色
2. 使用WebStorm看颜色
3. 使用开发者工具看警告
4. border调试法:
```
- 怀疑某元素有问题就给其加border
- border没出现？说明选择器错了或者语法错了
- border出现？看看边界是否符合预期
- bug解决后把border删掉
```
##### Example:
`段落p背景颜色不显示，使用border调试`
```
<style>
  p{ 
    background:black
    color:red;  
  }
</style>
<p>你好</p>
```
![](https://upload-images.jianshu.io/upload_images/16155751-061e3f88216f1e57.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![](https://upload-images.jianshu.io/upload_images/16155751-8735d36232b2aa98.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![](https://upload-images.jianshu.io/upload_images/16155751-9f7ff67bfd2f2a63.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
### 三、资料查找
- Google 关键字 MDN    `flex mdn`
![](https://upload-images.jianshu.io/upload_images/16155751-d95f83b4249314c8.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
- CSS tricks  `flex css tricks`
-  张鑫旭的博客  `flex 张鑫旭`
- [PSD素材](https://www.freepik.com/search?query=web&type=psd)
- [效果图](https://dribbble.com/)

### 四、文档流：文档内元素的流动方向
- 流动方向
inline元素从左到右，到达最右边才会换行
block元素从上到下，每一个都另起一行
inline-block元素也是从左到右
```
  <span>这是第1个span</span>
  <span>这是第2个span</span>
  <span>这是第3个span</span>
  <span>这是第4个span</span>
  <span>这是第5个span</span>
  <div>这是第1个div</div>
  <div>这是第2个div</div>
  <div>这是第3个div</div>
  <div>这是第4个div</div>
  <div>这是第5个div</div>
  <span class="ib">这是第1个inline-block元素</span>
  <span class="ib">这是第2个inline-block元素</span>
  <span class="ib">这是第3个inline-block元素</span>
  <span class="ib">这是第4个inline-block元素</span>
  <span class="ib">这是第5个inline-block元素</span>
```
![](https://upload-images.jianshu.io/upload_images/16155751-4ce28c9469dfca1b.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
- 宽度
inline宽度为内部inline元素的和，不能用width指定
block默认自动计算宽度，可用width指定
inline-block结合前两者特点，可用width
```
  <span>这是第1个span</span>
  <div>这是第1个div</div>
  <span class="ib">这是第1个inline-block元素</span>
```
![](https://upload-images.jianshu.io/upload_images/16155751-9d3a9cd3a7a902b2.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
- 高度
inline高度由line-height间接确定，与height无关
block高度由内部文档流元素决定，可以设置height
inline-block跟block相似，可以设置height

![block、inline-block](https://upload-images.jianshu.io/upload_images/16155751-5f614a0dc2b0fed0.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![inline](https://upload-images.jianshu.io/upload_images/16155751-8cb9382d1b4379cc.gif?imageMogr2/auto-orient/strip)
```
  <span>第1个span元素</span>
  <div style="width:10em;">
    第1个div元素第1个div元素第1个div元素第1个div元素
    <div style="position: absolute; background:green;">额外的Div</div>
    其他文字其他文字其他文其他文字其他文字
  </div>
  <span class="ib" style="width: 400px;">
    第1个inline-block元素第1个inline-block元素第1个inline-block元素第1个inline-block元素第1个inline-block元素第1个inline-block元素第1个inline-block元素第1个inline-block元素第1个inline-block元素
    <div>block</div>
    <span>span</span>
  </span>
```
![复杂情况](https://upload-images.jianshu.io/upload_images/16155751-00339394a8db36a4.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### 五、脱离文档流
- float
- position:absolute/fixed
```
<div class="div1">
  <div class="div2">
    <span>span元素</span>
  </div>
</div>
```
![](https://upload-images.jianshu.io/upload_images/16155751-dfd163339af65b75.gif?imageMogr2/auto-orient/strip)

### 六、overflow溢出
- 当内容的宽度或高度大于容器，会溢出，使用overflow设置是否显示滚动条
- overflow: visible;  直接显示溢出部分
- overflow: hidden; 直接隐藏溢出部分
- overflow: auto;     灵活设置滚动条
- overflow: scroll;    永远显示滚动条
```
  <div class="div1">
    主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容主要内容
    <div class="div2">hi</div>
    <span>Hello</span>
  </div>
```
![](https://upload-images.jianshu.io/upload_images/16155751-290c7be7a010b3ea.gif?imageMogr2/auto-orient/strip)

### 七、盒模型
- content-box(默认)
- border-box
```
  <div class="content-box">content box</div>
  <div class="border-box">border box</div>
```
```
.content-box{
  width: 100px;  
  margin: 25px;
  padding:15px;
  box-sizing: content-box;
  border:5px solid red;
}
.border-box{
  width: 100px;
  margin: 25px;
  padding:15px;
  box-sizing: border-box; 
  border:5px solid green;
}
```
![](https://upload-images.jianshu.io/upload_images/16155751-0bff577beecee907.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![](https://upload-images.jianshu.io/upload_images/16155751-d5f2d5bdb5820f3f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 区别
content-box 的 width 等于 `内容宽度`
border-box 的 width 等于 `内容宽度 + padding + border`

### 八、margin合并
- 相邻元素合并
```
  <h1>好好学习</h1>
  <h2>天天向上</h2>
```
```
body{
  border: 1px solid black;
}
h1{
  margin:20px 0;
  border:1px solid red;
}
h2{
  margin:30px 0;
  border:1px solid green;
}
```
![](https://upload-images.jianshu.io/upload_images/16155751-229f9d2c8cf4eb7b.gif?imageMogr2/auto-orient/strip)
注：<h1> 的`margin-bottom`与 <h2> 的`margin-top`合并
- 父子元素合并
```
  <div class="parent">
    <div class="child">子元素</div>
    <div class="child">子元素</div>
  </div>
```
```
body{
  border:1px solid black;
}
.parent{
  margin:15px;
  background:rgba(255,0,0,0.5);
}
.child{
  margin:30px;
  border:2px solid green;
}
```
![](https://upload-images.jianshu.io/upload_images/16155751-01ac60aabde765f8.gif?imageMogr2/auto-orient/strip)
- 阻止合并
##### 父子合并用`padding`、`border`、`overflow:hidden`挡住
![](https://upload-images.jianshu.io/upload_images/16155751-1dee7ecbe4ab0f59.gif?imageMogr2/auto-orient/strip)

### 九、基本单位
- 长度单位
px 像素
em 1em = 默认字体大小的倍数(比如不设置时是字体是20px，那2em 就是40px)
rem 1rem = 根元素(html 节点)字体大小的倍数
- 颜色
颜色关键字、十六进制值、RGB、HSL、RGBA & HSLA
```
  background-color: blue;
  background-color: #e0b0ff;
  background-color: rgb(224, 176, 255);
  background-color: hsl(276, 100%, 85%);
  background-color: rgb(224, 176, 255, .5);
  background-color: hsla(240, 100%, 50%, 0.5);
```

