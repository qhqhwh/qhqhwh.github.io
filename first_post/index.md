# 期末作业



# 期末作业
## 1.在Linux下，安装git
sudo yum install git

<image src="/1.jpeg">

## 2.使用git管理大作业相关的代码、配置文件等，要求有能反映大作业过程的git提交记录
### (1)先用git init创建一个仓库
git init

<image src="/2.jpeg">

### (2)编写客户端和服务端文件
Vim client.c

Vim service.c
### (3)然后创建代码文件的提交记录
Git add client.c

Git commit -m ‘客户端’

Git add service.c

Git commit -m ‘服务端’

<image src="/3.jpeg">

## 3.在Linux下，利用 socket 技术编写程序，包含客户端和服务端

## 4.实现客户端和服务端之间相互联系
服务端:

<image src="/4.jpeg">

客户端:

<image src="/5.jpeg">

## 5.利用hugo创建静态网站(新建虚拟机Ubuntu)
### (1)配置好Hugo相关环境
sudo apt-get install snap

sudo apt-get install hugo

sudo apt-get install git

### (2)使用Hugo，创建静态网站文件夹,在文件夹中创建md文件，使用Markdown语法编写网站内容
hugo new site mysite

git clone [https://github.com/dillonzq/LoveIt.git(Hugo主题链接)](https://hugoloveit.com/zh-cn/theme-documentation-basics/)

hugo new posts/first_post.md

<image src="/6.jpeg">

### (3)使用Hugo，生成静态网站，部署到Web服务器
hugo serve --bulidDrafts

<image src="/7.jpeg">

## 6.在托管平台github pages上部署静态网站，使其可以公网访问
### (1)在平台中，创建仓库,生成网址链接
hugo --theme=LoveIt --baseUrl="https://qhqhwh.github.io/" --buildDrafts

<image src="/8.jpeg">

### (2)使用git在网址文件夹中创建一个空的仓库，推入静态网站文件夹中的内容并与github我们所创建的仓库进行连接
git init

git add .

git commit -m "first push"

git remote add origin https://github.com/qhqhwh/qhqhwh.github.io.git

git push -u origin master

