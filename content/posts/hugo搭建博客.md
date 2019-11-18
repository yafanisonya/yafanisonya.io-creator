---
title: "Hugo搭建博客"
date: 2019-11-17T21:04:49+08:00
draft: false
---
![](https://upload-images.jianshu.io/upload_images/16155751-c956bde8ee2c8e16.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
[hugo官网搭建过程](https://gohugo.io/getting-started/quick-start/)
#### 1. 安装hugo
______
#### 2. Create a New Site
```
hugo new site yafanisonya.io-creator
```
![](https://upload-images.jianshu.io/upload_images/16155751-3ca7d718d977926e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
______
#### 3. Add a Theme
```
  cd yafanisonya.io-creator/
  git init
  git submodule add https://github.com/budparr/gohugo-theme-ananke.git themes/ananke
  echo 'theme = "ananke"' >> config.toml
```
![](https://upload-images.jianshu.io/upload_images/16155751-501039de7a41cacc.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
______
#### 4.  Add Some Content
```
  hugo new posts/my-first-post.md
```
![](https://upload-images.jianshu.io/upload_images/16155751-836cc24b30c51f8c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![](https://upload-images.jianshu.io/upload_images/16155751-0d62a31b71b132eb.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
`将draft值改为false，否则为草稿状态`
______
#### 5.  Start the Hugo server
```
 hugo server -D
```
![](https://upload-images.jianshu.io/upload_images/16155751-6883ffdca42f3789.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![](https://upload-images.jianshu.io/upload_images/16155751-aca2a580277c186e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
______
#### 6. Customize the Theme
![](https://upload-images.jianshu.io/upload_images/16155751-ba0111ada6b0f6fa.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
______
#### 7.  Build static pages
```
  hugo -D
```
![](https://upload-images.jianshu.io/upload_images/16155751-fef3357e447aa567.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
______
#### 8. 本地推送至github
`在/d/github/yafanisonya.io-creator中创建.gitignore文件，将/public写入，使得public自成仓库`
```
  cd public/
  git init
  git add .
  git commit -v
```
`在github新建仓库，仓库名为 用户名.github.io`
![](https://upload-images.jianshu.io/upload_images/16155751-de1bf08a19407895.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
```
  git remote add origin git@github.com:yafanisonya/yafanisonya.github.io.git
  git push -u origin master
```
![](https://upload-images.jianshu.io/upload_images/16155751-6bef117c3ac509bb.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![](https://upload-images.jianshu.io/upload_images/16155751-254af368e24f1c7b.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
`在yafanisonya.github.io仓库中设置GitHub Pages-->Source-->master`
![](https://upload-images.jianshu.io/upload_images/16155751-b783f0c73e4fcf59.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
## 最终效果：
![](https://upload-images.jianshu.io/upload_images/16155751-83c3b91495b7e02d.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
______
## hugo更新博客方法：

#### ①：新建博客
```
  hugo new posts/my-first-post.md
```
![](https://upload-images.jianshu.io/upload_images/16155751-0581c5fd735f537d.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
`然后编辑博客内容`
#### ②：hugo
![](https://upload-images.jianshu.io/upload_images/16155751-73a2cec915ac136a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
#### ③：推送
![](https://upload-images.jianshu.io/upload_images/16155751-96be171c5cfc1d0a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
```
    cd public/
    git add .
    git commit -v
    git push
```
![](https://upload-images.jianshu.io/upload_images/16155751-616eb245c25e2e94.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![更新成功](https://upload-images.jianshu.io/upload_images/16155751-16619dc8462ef32e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

