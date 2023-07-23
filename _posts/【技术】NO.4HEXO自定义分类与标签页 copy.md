---
title: 【技术】NO.4 Hexo自定义分类与标签页
categories:
- 财务
tags: 
- 技术
---
在搭建HEXO+Github博客过程中，我们的分类与标签页，一般都是由安装的主题默认配置好的。但有时候默认或者我们喜欢的主题没有配置分类与标签页面，这就需要我们自己进行配置了。下面就用几个简单可复制的方式，来帮助大家自定义配置自己的分类与标签页面，更好管理自己的内容文章。
步骤一： 检查layout目录
找到自己博客配置主题下的layout文件夹，检查里面的ejs文件。如果里面没有分类与标签页，则需要自行配置。
![20221211182654](https://raw.githubusercontent.com/wllilerjimw/-My-photo/master/20221211182654.png)
![20221211182736](https://raw.githubusercontent.com/wllilerjimw/-My-photo/master/20221211182736.png)

步骤二：配置分类页
在layout目录下新建categories.ejs文件夹，打开后，写入以下代码。
![20221211182826](https://raw.githubusercontent.com/wllilerjimw/-My-photo/master/20221211182826.png)
然后来到你的source目录下，新建categories文件夹，里面新建index.md文件，并写入以下代码。
![20221211182910](https://raw.githubusercontent.com/wllilerjimw/-My-photo/master/20221211182910.png)
步骤三：配置标签页
也如配置分类页一样，先在layout新建tags.ejs文件,并写入以下代码。
![20221211183726](https://raw.githubusercontent.com/wllilerjimw/-My-photo/master/20221211183726.png)
然后再到source目录下，新建tags文件夹，里面新建index.md文件，并写入以下代码
![20221211194517](https://raw.githubusercontent.com/wllilerjimw/-My-photo/master/20221211194517.png)
步骤四：推送
输入命令，进行推送，查看是否报错，没有的话，，就是推送成功。访问自己网页，查看效果。
![20221211194541](https://raw.githubusercontent.com/wllilerjimw/-My-photo/master/20221211194541.png)
![20221211194601](https://raw.githubusercontent.com/wllilerjimw/-My-photo/master/20221211194601.png)
![20221211194619](https://raw.githubusercontent.com/wllilerjimw/-My-photo/master/20221211194619.png)
步骤五：文档中如何写
在写作过程中，需按照以下格式来写自己的分类与标签。
![20221211194639](https://raw.githubusercontent.com/wllilerjimw/-My-photo/master/20221211194639.png)
参考文档
1. linlif.github.io
2. blog.csdn.net
3. 编写自己的HEXO 主题 easyhexo.com