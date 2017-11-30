---
layout: post
title:  "Complete the blog!"
date:   2017-10-13 09:24:38 +0800
img: "a.jpg"
---

Today, I almost complete the whole frame of my blog.


### **安装Jekyll**

参考链接

[安装Jekyll](http://www.jianshu.com/p/1093b55659180)

按照里面的步骤我遇到一个问题：jekyll new 的时候提示

  > could not load bundler, bundler install skip.

解决方法:
  gem install  bundler

### **开始写博客啦**

Jekyll官网文档看一遍 
[Jekyll官网文档](https://jekyllrb.com)

有个中文版，但是里面有很多东西没有，可以两个一起对照着看
[Jekyll中文版](http://jekyll.com.cn/)

### **优化**

  界面优化

  主题jekyll theme，参考
  [jekyll theme](http://jekyllthemes.org/)

  我的模板参考 [flexible-jekyll](http://artemsheludko.pw/flexible-jekyll/)


### **分页**

分页的时候，疑惑了好久，文档也写得不是很清楚的样子，老是提示

  Pagination: Pagination is enabled, but I couldn't find an index.html page to use as the pagination template. Skipping pagination.

  >Pagination works when called from within the HTML file, named index.html

也就是说需要有分页功能的那个页面必须叫做index.html,这个页面不能有 permalink

然后_congif.yml里面的 paginate_path 怎么设置呢。这个没什么关系，只要和分页的上一页下一页链接对应就好。

比如说我设置

  paginate_path: "blog/page/:num"

那么下一页的链接就要写成
  ```
  <a  href="\{\{ site.baseurl \}\}/blog/page/\{\{ paginator.previous_page \}\}/">
  ```

还有一个

  >:num is the pagination page number, starting with 2

所以第一页是不能通过

 ```
    <a  href="\{\{ site.baseurl \}\}/blog/page/\{\{ paginator.previous_page \}\}/">
```
  

来获取



### **其他**

layout 必须是_layout文件夹里面的文件

site.pages 还包括了blog/page/2,blog/page/3等等所有page

permalink: /about ,href="{{ site.baseurl }}/about"就可以链接得到

_config.yml修改完需要重新启动 jekyll serve

