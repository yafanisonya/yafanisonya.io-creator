---
title: "Git入门本地仓库"
date: 2019-11-17T19:01:56+08:00
draft: false
---

### 1. 配置 git
`git 六行配置`
![](https://upload-images.jianshu.io/upload_images/16155751-72729a60473bfd7e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

```
  git config --global user.name 你的英文名
  git config --global user.email 你的邮箱
  git config --global push.default simple
  git config --global core.quotepath false
  git config --global core.editor "code --wait"
  git config --global core.autocrlf input
```

### 2. 创建目录

![](https://upload-images.jianshu.io/upload_images/16155751-7f21fcdbb6a83d90.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

```
  git init  创建.git 目录
  git status -sb 查看代码在缓存区状态（？未添加 ， A 已添加）
             -sb 显示总结和分支

```

### 3. 添加文件

![](https://upload-images.jianshu.io/upload_images/16155751-4846cd611464942f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

```
git add 将文件添加到暂存区
```

### 4. 提交代码

![](https://upload-images.jianshu.io/upload_images/16155751-34b4b0bbb95231de.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![commit -v](https://upload-images.jianshu.io/upload_images/16155751-a5eab528635a604a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![commit -m](https://upload-images.jianshu.io/upload_images/16155751-d529650ce7917777.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

```
  git commit -m "注释"   将暂存区内容正式提交到本地仓库
  git commit -v          显示差异信息和更多有意义的信息
```

### 5. 查看历史
![](https://upload-images.jianshu.io/upload_images/16155751-6d3ffe7769c035c6.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

```
git log                查看变更历史
```

### 6. 代码回滚
![](https://upload-images.jianshu.io/upload_images/16155751-313bf160e72cdb22.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![](https://upload-images.jianshu.io/upload_images/16155751-310bde25116983c6.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

```
  git reset --hard XXXXXX  回到之前的提交，切换版本
  git reflog   查看所有历史
```

### 7. 忽略提交
![](https://upload-images.jianshu.io/upload_images/16155751-f7bd39b4dde00fad.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

```
  创建.gitignore文件，将忽略的文件添加至.gitignore
  .gitignore文件描述不提交的内容
```

### 8. 新建分支
![](https://upload-images.jianshu.io/upload_images/16155751-0bfd5d1563f50308.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

```
  git branch newdev 创建newdev分支
  git branch 显示分支
```

### 9. 切换分支
![](https://upload-images.jianshu.io/upload_images/16155751-c95b1d8fa6143e96.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

```
  git checkout newdev  切换到newdev分支
```

### 10. 合并分支
![](https://upload-images.jianshu.io/upload_images/16155751-429adc7da4862de4.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![](https://upload-images.jianshu.io/upload_images/16155751-7b9d5d8b2baa7620.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

```
git merge newdev 将newdev分支内容合并到当前分支
git branch -d newdev 删除newdev分支
```

#### 合并分支冲突解决办法

![](https://upload-images.jianshu.io/upload_images/16155751-3871bb11d4b42447.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![](https://upload-images.jianshu.io/upload_images/16155751-da81380fbd0a47eb.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)