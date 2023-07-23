---
title: 复式记账Beancount初识（一）
categories:
- 个人成长
tags: 
- 财务管理
---

![from unsplash](https://images.unsplash.com/photo-1688993536536-df108751b415?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHwzNHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=500&q=60)



记账的习惯，我也是大学毕业之后逐渐养成的。用过“猫猫记账”、“随手记”、“钱迹”。

这些记账软件的优势：方便、快捷、界面简单。比如“钱迹”，我现在依旧在用，但它们共同的问题是：只能记录收支情况。

当然，对于很多人来说，记录收支就够了，甚至很多人根本就没有记账的习惯，所以为什么要记账，还要用这么复杂的方法呢？

每个人都有自己答案，而我只是喜欢折腾，也认为复式记账的方式，能够更好梳理自己资产情况，辅助我做更正确的交易抉择。

 ### 复式记账

  > **复式记账会记录每笔交易的资金流动，各账户变化「有正有负，正负相等」。这便是复式记账的基本原理，称之为「会计恒等式」**  

可能大家还是不理解，我让AI写了个例子：
  
  假设小明经营着一家小型企业，他决定购买一台新的电脑。我们来看看在复式记账和普通记账下，这个场景的差别。  
  
	1. 普通记账：  
在普通记账系统中，小明只会记录资金的流入和流出。他只会记录购买电脑的支出，而没有详细记录电脑在企业资产中的价值。  
  
示例记录：

- 日期：7月1日
- 交易类别：支出
- 支出金额：5000元
- 备注：购买新电脑
  
  普通记账系统只能告诉小明他花了多少钱购买电脑，但无法提供有关电脑是企业资产的更多信息。  
  
2. 复式记账： 
    
在复式记账系统中，小明将用借贷原则记录每笔交易的影响。他会同时记录电脑的支出以及电脑在企业资产中的增值。  
  
示例记录：

- 日期：7月1日
- 交易类别：支出
- 支出金额：5000元
- 借方科目：电脑
- 贷方科目：现金
- 备注：购买新电脑
  
  这种记录方式明确显示了借方科目（电脑）的增加和贷方科目（现金）的减少，以及电脑作为企业资产的价值。这样，小明可以更好地跟踪企业的资产和负债情况。  
  
  通过这个场景的例子，可以看出复式记账相较于普通记账的优势。复式记账能够提供更详细和准确的财务信息，帮助企业主们更好地了解和管理企业的财务状况。  

  > 把自己作为一家公司  

  我们将自己比作一家公司，我们的负债与收入是对公司的投入，花销是我们的成本，而资产就是我们的产出。

  >（资产+花销）-（收入+负债）=权益
  
  权益就是这个过程中，我们得到的净利润，它会随着我们等式左边的变化，而变化。

而我们理想目标，就是使收入与负债为0，我们的花销完全由资产所产生的权益所覆盖时，我们就财务自由了。（如下图）

  ![](https://raw.githubusercontent.com/wllilerjimw/-My-photo/master/20230716120203.png)


  ### Beancount

 > *__一种允许用户在文本文件中定义金融交易记录，通过在内存中读取数据，可以生成各种报告以及提供网页界面的复式记账计算机语言__*  

Beacount是什么？简单来说，就是实现上面**复式记账**的工具。它具有以下特点：
  - 本地存储：保障数据隐私安全，可以用vscode+github的方式，进行编辑和远程数据备份。

 - 纯文本记录，源文件可阅读修改，并且搭配Fava，生成网页预览。资产负债表、损益表、账户相关信息，都能一目了然。
  
 ![](https://raw.githubusercontent.com/wllilerjimw/-My-photo/master/20230716120440.png)

		
### beancount 配置

 首先确保计算机已经安装了python环境，然后在终端执行以下命令。

	  ```
	  pip install beancount
	  pip install fava
	  ```
 安装完毕之后，就可以建立自己的账本目录，开始记账了！

 ![](https://raw.githubusercontent.com/wllilerjimw/-My-photo/master/20230716120648.png)

 这是我的账本目录，其中main.bean是账本主文件，可以在这里面设置参数，并用include命令，关联其他账本。

 ![](https://raw.githubusercontent.com/wllilerjimw/-My-photo/master/20230716120736.png)
  
 使用`fava main.bean` 命令，就可以得到浏览界面地址。

 ![](https://raw.githubusercontent.com/wllilerjimw/-My-photo/master/20230716120824.png)

 在浏览器打开，便能得到如下界面，可以在这里面，更方便看到账户资产情况，以及相应汇总数据。

 ![](https://raw.githubusercontent.com/wllilerjimw/-My-photo/master/20230716121017.png)

  accounts.bean就是账户界面，在这里面进行开户,开户的语法格式：

 >	  ``` 开启日期 open 账户名 货币类型 ```

![](https://raw.githubusercontent.com/wllilerjimw/-My-photo/master/20230716121201.png)

  
  documents里就是具体的账本文件，记录你的交易记录。
	
---

  以上是becount复式记账的基本认识，后续文章，我会再具体介绍，如何记录一些复杂账目，以及如何初始化资产等内容。

  参考文章
  
  [[@使用 Beancount 管理家庭财务]] https://www.bmpi.dev/self/beancount-my-accounting-tool-v2/

 [[@复式借贷记账法 Beancount (0) - 先导]]https://yishanhe.net/beancount-tutorial-0/