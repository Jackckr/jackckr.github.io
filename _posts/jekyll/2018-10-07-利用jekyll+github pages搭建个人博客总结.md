---
categories: jekyll
toc: true
---
# 背景

博主一直想搭建一个可以自主管理的博客，然后去网上搜了一下后，发现GitHub pages就提供这样一种功能，能普通用户**免费**在上面进行搭站，于是就根据官方文档和各种网上资料进行自己搭站尝试。此间过程有些曲折，所以也把过程记录下来，提供给其他的朋友进行参考。

# 基础知识

要使用jekyll+github pages搭站，需要学些一个基础的知识，这样才能在使用的过程中得心应手。关于jekyll的用法，如果有不熟悉的，可以参考博主的另一篇文章[jekyll基本概念介绍和安装]({{ site.url }}/jekyll/jekyll基本概念介绍和安装)

如果看到这里的，博主就假设已经知道jekyll是个什么东西，以及会markdown等语言了。那么接下来就给大家介绍怎么利用github pages来搭建自己的博客站。

# 搭建步骤

## 第一步：物色自己喜欢的模板
github pages本身提供了一些简单的模板可以在setting中进行配置，不过可选择的太少，所以如果没有喜欢的可以去其它地方多挑几个找到自己喜欢的模板。
博主在进行搜索过程中，无意找到了一位大神的blog[Jekyll&Github Pages博客模板挑选和配置](http://cenalulu.github.io/jekyll/choose-a-template-for-your-blog/)，然后里面介绍了几个找模板的地方，这里接只接做一个搬运工，将这几个地址copy过来了
- [jekyllthemes.org](http://jekyllthemes.org/)
- [jekythemes.net](http://jekythemes.net)
- [mademistakes](https://mademistakes.com/work/jekyll-themes/) (最后博主我也是在这个大神的几个模板中挑中了现在这个模板)

## 第二步：github创建blog项目
按照官方文档[github pages](https://pages.github.com/)新建一个github pages项目，并以username.github.io格式命名新分支。

## 第三步：导入模板
导入模板有两种方式：一种是本地自己直接clone模板项目的github文件，然后放到自己项目中进行编译，还有一种是通过远程的方式，自己的项目中没有模板项目的任何文件。这两种的区别是，远程的每次build的时候需要通过去远端拉取相关资源，如果本地调试的时候，网路不好可能会导致项目启动很慢。但博主作为一个洁癖，为了使自己的项目看起来干净，所以选择了第二种方式。
如果使用第二种远端的方式，那么只需要在项目的根目录下创建一个_config.yml的文件，并将主题配置写进文件就可以了，还是以博主自己为例：
![_config文件示意图]({{ site.url }}/assets/pic/jekyll/config文件示意图.png)

然后在_config.yml文件中写入remote-theme配置信息
```yml
remote_theme           : "mmistakes/minimal-mistakes"
```
## 第四步：导入博客
如果已经有博客了，那么就将博客直接导入到_posts目录下，并按照模板以及jekyll的配置规则，进行配置就好了。

## 第五步：本地调试并推送到github中
到了这一步，那么恭喜你，你离成功就只差一步之遥了。在本地调试，布局等都符合预期后，就可以直接将项目push到github中了，然后等待github page帮你构建项目，并启动就好了。

## 第六步：欣赏自己的博客站
在github的项目setting页面，在github pages配置中，就可以看到自己的博客站域名，点击后就可以看到属于自己的博客了👏
![查看自己域名]({{ site.url }}/assets/pic/jekyll/查看博客站域名.png)