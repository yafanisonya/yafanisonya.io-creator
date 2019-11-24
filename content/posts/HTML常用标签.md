---
title: "HTML常用标签"
date: 2019-11-24T21:17:16+08:00
draft: false
---
### 一、a 标签
- 属性
`href、target、download、rel=noopener`
```html
  <a href=" "></a>
```
1. href的取值
- 网址
```html
  <a href="https://fanison.info"></a>
  <a href="http://fanison.info"></a>
  <a href="//fanison.info"></a>
```
- 路径
```html
  <a href="./posts/index.html"></a>
```
- 伪协议
```html
  <a href="javascript:;">Click</a>
  <a href="javascript:alert(1);">js伪代码</a>
  <a href="mailto:yafanison@gmail.com">发邮件给我</a>
  <a href="tel:18312345678">Call Me</a>
```
![](https://upload-images.jianshu.io/upload_images/16155751-10fbc98c1ca9e80e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![](https://upload-images.jianshu.io/upload_images/16155751-aa5ce9e0aa32a111.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![](https://upload-images.jianshu.io/upload_images/16155751-a3fee4457ecae572.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
- id
```
  <a href="#id">Call Me</a>
```
2. target的取值
```html
  <a href="http://fanison.info" target="_blank">新窗口打开</a>
  <a href="http://fanison.info" target="_self">当前页面加载</a>
```
`_parent: 加载响应到当前浏览上下文的父浏览上下文`
`_top:加载响应进入顶层浏览上下文`
3. download：下载页面

### 二、 tabel 标签
```html
  <table>
    <thead>
      <tr>
        <th>姓名</th>
        <th>性别</th>        
      </tr>
    </thead>  
    <tbody>
      <tr>
        <td>小米</td>
        <td>男</td>
      </tr>
      <tr>
        <td>苹果</td>
        <td>女</td>
      </tr>
    </tbody>
    <tfoot>
      <tr>
        <td>x</td>
        <td>y</td>
      </tr>
    </tfoot>
  </table>
```
![](https://upload-images.jianshu.io/upload_images/16155751-17887503e3dc1ed0.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
- **`border-collapse`** 用来决定表格的边框是分开的还是合并的。在分隔模式下，相邻的单元格都拥有独立的边框。在合并模式下，相邻单元格共享边框。
- **`border-spacing`** 属性指定相邻单元格边框之间的距离
```css
    table{
      width:300px;
      border-spacing:5px;
      border-collapse: collapse;
    }
    th,td{
      border:1px solid red;
    }
```
![](https://upload-images.jianshu.io/upload_images/16155751-7f6e5de27cbacb22.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
- **`table-layout`** CSS属性定义了用于布局表格单元格，行和列的算法
```css
    table{
      table-layout: auto;
     /* table-layout: fixed;*/
     }
```
![](https://upload-images.jianshu.io/upload_images/16155751-4b42fd334bb0e593.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### 三、 img标签
- 作用：发出get请求，展示图片
- 属性： **`alt、height、width、src`**
```html
  <img class="pic" src="https://www.baidu.com/img/bd_logo1.png" alt="百度logo">
```
```
    img{
      max-width:100%;
    }
```
- **`max-width:100%;`** 实现响应式 
- **`height、width`** 最好设置一项，另一项自适应；两项都设置可能会出现图片变形现象
- 事件：**`onload、onerror`**
```
  <script>
    pic.onload = function(){
      console.log("success")
    }
    pic.onerror = function(){
      console.log("failed")
    }
  </script>
```
![](https://upload-images.jianshu.io/upload_images/16155751-fdb9be4afeccdb2c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### 四、form表单
- 作用：发送get或post请求，然后刷新页面
```    
 <form action="users？zzz=3" method="post">
   <label>用户名<input type="text" name="姓名"></label>
   <label>密码<input type="password" name="密码"></label>          
   <input type="submit" value="提交">
 </form>
```
-  `action`：处理form信息的程序所在的URL
-  `method`：
    `post`: 表单数据会包含在表单体内然后发送给服务器.
   `get`: 表单数据会附加在 `action` 属性的URI中，并以 '?' 作为分隔符, 然后这样得到的 URI 再发送给服务器.。
- `autocomplete`：指示 input 元素是否能够拥有一个默认值
  off：浏览器不会自动补全输入。
  on：浏览器能够根据用户之前在表单里输入的值自动补全
- `target`:指示在提交表单之后，在哪里显示收到的回复
    _self、_blank、_parent、_top、iframename
*注意事项*：
一般不监听<input>的click事件
form标签中的input要有name属性
form里要放一个`type=submit`才能触发submit事件

### 五、 input标签	
`text、password、color、file、checkbox、radio、button、submit`
- checkbox:复选框
`Tips:label标签的for属性与input标签的id属性搭配使用，可实现点击文字勾选`
- radio:单选(给多个选项设定同一name属性) 
`Tips:如果 input 不加 name属性，那么在表单提交时，input 的值就不会出现在请求里`
```html
  <input type="text">    <input type="password">  
  <input type="color">
  <input type="file"><input type="file" multiple>

  <input type="checkbox" name="fruit" id="xxx"><label for="xxx">橘子</label>
  <input type="checkbox" name="fruit" id="yyy"><label for="yyy">苹果</label>

  <label><input name="answer" type="radio" value="Yes">对</label>
  <label><input name="answer" type="radio" value="No">错</label>
```
![](https://upload-images.jianshu.io/upload_images/16155751-d5f3b2127bffacce.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

<hr>

### 六、 其他标签
#### - label标签: `label标签将input标签包围效果等同于属性绑定`
```html
  <label>用户名<input type="text" name="姓名"></label>
  <label>密码<input type="password" name="密码"></label>
```               
![](https://upload-images.jianshu.io/upload_images/16155751-23ef156d460e9d60.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


#### - select标签
```  
  <select name="group" multiple>
    <option value="">-</option>
    <option value="1">第一组</option>
    <option value="2" disabled>第二组</option>
    <option value="3" selected>第三组</option>
  </select>
```
*补充*：
- `multiple`属性可实现多选（按ctrl或shift）
- `required`属性规定select的值不能为空(布尔值)
- `<option>`
 `disabled`不可选
 `selected`默认选择
![](https://upload-images.jianshu.io/upload_images/16155751-692bfa36e783cf63.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

#### - textarea标签
```	
<textarea name="textarea" >Write something here</textarea>
<textarea name="textarea" style="resize:none; width:100px; height:50px; ">Write something here</textarea>
```	
#### - button标签
 ```       
<button>提交</button>
<input type="submit" value="提交">	
<button type="submit">提交 </button>      三种提交
```
*补充*：
* `type`按钮的类型：
`submit`：将表单数据提交给服务器
`reset`：将所有控件重置为其初始值
`button`：没有默认行为
- `button标签type默认为submit`
- <button>和<input type="button"> 的区别:
在button 元素内部，可以放置内容，比如文本或图像
#### - 可替换元素
典型的可替换元素有：
*   [`<iframe>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/iframe "HTML内联框架元素 <iframe> 表示嵌套的浏览上下文，有效地将另一个HTML页面嵌入到当前页面中。")
*   [`<video>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/video "HTML <video> 元素 用于在HTML或者XHTML文档中嵌入媒体播放器，用于支持文档内的视频播放。")
*   [`<embed>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/embed "HTML <embed> 元素将外部内容嵌入文档中的指定位置。此内容由外部应用程序或其他交互式内容源（如浏览器插件）提供。")
*   [`<img>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/img "HTML Image 元素（ <img> ）代表文档中的一个图像。")
