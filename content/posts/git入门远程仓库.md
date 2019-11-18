---
title: "Git入门———远程仓库"
date: 2019-11-17T20:39:12+08:00
draft: false
---

### 1. 新建仓库
![](https://upload-images.jianshu.io/upload_images/16155751-033320f7150e94fb.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
`Repository name：填写仓库名称`

### 2. 上传代码
![](https://upload-images.jianshu.io/upload_images/16155751-7a9ffd6205261278.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![](https://upload-images.jianshu.io/upload_images/16155751-2749894abc0f8785.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![](https://upload-images.jianshu.io/upload_images/16155751-f802919cc1432115.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

```
  git remote add origin git@xxxxxxx   在本地添加远程仓库地址
  git push -u origin master           推送本地master到远程origin的master分支
```
![上传完毕](https://upload-images.jianshu.io/upload_images/16155751-2c24c7737cdac071.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
### 3. 下载代码
![](https://upload-images.jianshu.io/upload_images/16155751-45989ea943be5484.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![](https://upload-images.jianshu.io/upload_images/16155751-49f6c11074b13565.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

```
git clone git@?/xxx.git      下载代码
git clone https://github.com/?/xxx.git
注： 下载别人代码使用https地址
     下载自己代码https、ssh均可
```
![](https://upload-images.jianshu.io/upload_images/16155751-f11a69e5705e3432.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
### 4. 上传到两个远程仓库
![](https://upload-images.jianshu.io/upload_images/16155751-1915736f5824bbb3.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

```
    第二个仓库上传时使用如下代码：
        git remote add origin2 git@xxx.git
        git push -u origin2 master
```
![效果图](https://upload-images.jianshu.io/upload_images/16155751-e07756988dd15ace.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### 5. git高级操作
#### 使用bash alias简化命令

```
touch ~/.bashrc
echo 'alias ga="git add"'>> ~/.bashrc
echo 'alias gc="git commit -v"'>> ~/.bashrc
echo 'alias gl="git pull"'>> ~/.bashrc
echo 'alias gp="git push"'>> ~/.bashrc
echo 'alias gco="git checkout"'>> ~/.bashrc
echo 'alias gst="git status -sb"'>> ~/.bashrc
echo 'alias glog="git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit -- | less"' >> ~/.bashrc
```

`ga、gc、gl、gp、gco、gst、glog`

```
git rebase -i XXX       美化历史命令
git stash               临时隐藏代码
git stash pop           显示临时隐藏代码
```