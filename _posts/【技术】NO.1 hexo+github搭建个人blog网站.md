---
title: 【技术】NO.1用hexo++github 搭建个人blog网站
categories:
- 财务
tags: 
- 技术
---

# 搭建环境

## 需下载安装的软件
1.node
暂时无法在飞书文档外展示此内容
2.git
暂时无法在飞书文档外展示此内容
执行如下代码，进行本地环境运行。
npm install hexo-cli -g
hexo init blog
cd blog
npm install
hexo server
# push远程仓库
首先在github建立新的仓库，作为你的blog文件托管，命名需要以username.github.io命名。 http://username.github.io ，这网址就是你的博客地址，需要把里面的username替换为你的GitHub账户名。执行以下操作：
git config --global user.name "你的GitHub用户名"
git config --global user.email "你的GitHub注册邮箱"
生成ssh密钥文件：
ssh-keygen -t rsa -C "你的GitHub注册邮箱"
然后直接三个回车即可，默认不需要设置密码
然后找到生成的.ssh的文件夹中的id_rsa.pub密钥，将内容全部复制
添加进入github中的ssh key。
配置成功后
Hexo g
Hexo s
Hexo d 
完成推送和部署。
# 写作发布
Hexo博客系统的写作方式很简单，通过Markdown语法来写作。只需要在目录post中新建md文件，就可以开始自己的写作了。
# 几个小建议
1.对于不是技术咖，单纯只是喜欢写作，那就保持写作的纯粹性。不要去想着向许多牛逼大神，把网站整得花里胡哨，不是说这样不好，而是对于技术小白，要实现这一切，会投入许多时间成本和学习成本。应为blog本质还是写作，如果一味追求网站的好看和酷炫功能，那就离原本写作初心愈来愈远。
2.对于本地源数据，虽然有仓库托管，但为了确保数据的稳定，最后在网盘备份一下，遇到特殊情况，可以用网盘恢复，然后安装下环境，便可以继续使用了。
# 报错参考
问题1：
Please make sure you have the correct access rights
and the repository exists.
https://blog.csdn.net/jingtingfengguo/article/details/51892864
# 参考文档
HEXO 文档
# 联系我
如果你按照以上方法配置不成功，或者出现各种问题，那么可以联系我帮助你解决。当然由于时间与机会成本，需要你请我喝一两杯星巴克作为补偿！

方法1：如果你有些担心，可进入闲鱼，拍下此链接，再来加我私人微信，确认解决完你想要解决的问题后，再进行确认收货，保证你的资金安全。
【闲鱼】https://m.tb.cn/h.fxYXIH8?tk=XOAQ2JAPk0w CZ0001 「我在闲鱼发布了【远程帮忙搭建github+hexo博客，让你拥有自己的写作空】」
点击链接直接打开
方法2：如果你足够信任我，那请加图片里的微信号，直接联系我，并备注说明来意。按两杯星巴克的价钱转账给我之后，我会一天之内，回复你，并解决你的问题。
