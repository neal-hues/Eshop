# eshop

## －基于.Net平台的网上购物商城的设计与实现

### 1  系统概述
#### 1.1  设计背景
　　随着计算机技术在各行各业日益广泛和深入的应用，网络的概念早已深入人心。网络在各行各业的发展战略中占据了重要的位置，成为商家不可分割的部分。商品的宣传已不只局限于电视与报纸，网络已成为商家展示自己的另一个舞台。商家建立网站，将商家各方面的宣传与服务展现于网络中，这些在改变我们原有经营方式与经营理念的同时，也为商家带来了更高的效益。因此，对于商家来说，拥有一个属于自己的网站是至关重要的。“网上商城”实际上是运行在Web服务器中的一个Web运用程序。“网上商店”模拟一般的商店的经营模式。利用页面、脚本程序来实现“网上商城”的销售管理、库存管理。互联网技术提供的不仅仅只是供需双方间的较低的交易成本，还有较低的选择费用和更多可供选择的商品。这些特点促使商家更多地通过使用网站来实现电子商务。

#### 1.2  设计目的和思路
##### 1.2.1  设计目的
　　长期以来，大部分的销售活动，都是面对面的销售，如：店铺销售、广交会、上门推销等。这些销售活动，都会受到地域、时间、环境等方面的影响，从而给企业、公司等的销售管理带来极大的不便，而且信息的人工管理，也存在诸多缺点。而网上商城，正好能全面解决这样的问题。<br>

　　网上商城类似于现实世界当中的商店，差别是利用电子商务的各种手段，达成从买到卖的过程的虚拟商店，从而减少中间环节，消除运输成本和代理中间的差价，造就对普通消费和加大市场流通带来巨大的发展空间。

##### 1.2.2  设计思路
　　本网站主要从以下三个方面开始设计：<br>
　　1.做出网站的功能架构图，具体要实现什么的功能，各个功能模块之间有什么联系，有无子模块，子模块之间又是怎样的关系。<br>
　　2.确定网站的主题标准，网站用什么字体，主体颜色用什么，其他颜色是怎么搭配的，内容呈现的模块是怎样的等等。<br>
　　3.设计数据库，数据表的表名如何编写，各个数据表中需要多少个字段，每个字段用什么类型的比较合适，以及表和表、字段和字段之间的联系。

#### 1.3  系统需求分析
　　系统需求分析就是指在整个系统开发过程中解决“做什么”的问题，把要解决哪些问题，满足用户哪些具体的信息需求调查分析清楚。本网上商城系统的目的是鉴于互联网的优势以及对国内外相关现状的研究分析，我决定以基于Web的商城网站开发作为我的毕业设计主题。立足于设计一个在网络平台上运行的集购物、支付和配送等功能于一体的无店铺商城。<br>

　　系统能实现用户的注册功能、登录功能、商品的查询，订购等功能。该系统基本上具备一个商品销售网站应该具备的功能，该设计项目基本上体现了构建一个动态商务网站所需要的技术。<br>

　　本网站是一个电子商品销售网站，消费者可以有目的性的快速找到你所期望的产品，可以直观的浏览商品的价格、内容、生产日期是否符合需要，为现在高效率的生活带来方便。<br>

　　经过前期的深入调查和研究，总结出该平台需要完成的一些具体功能，分析如下：<br>

- 用户管理：能够完成用户基本信息录入的注册和用户基本信息的个人前台与后台管理。
- 管理员管理：能够完成管理员对网站的商品资料（添加大类、添加小类、商品添加）、商品交易（外理订单、发货查询）、会员管理、操作管理（管理员添加、管理员审查、管理员退出）的功能。
- 搜索功能：通过商品的名称，商品的分类进行搜索。
- 查询功能：能够通过查看购物车对所选商品进行确定、挑选，通过定单查询对支付费用进行确定。

#### 1.3  运行环境
- 运行环境：IIS7.5、Microsoft .NET Framework 4.5和Microsoft SQL Server 2005
- 运行条件：装有Windows7操作系统的PC
- 开发工具：Microsoft Visual Studio 2013、Adobe Dreamweaver CS6、Adobe Fireworks CS6
- 分辨率：最佳效果1920×1080像素

### 2  总体设计
#### 2.1  系统结构
##### 2.1.1  系统流程图
　　E商城的系统流程图如图2-1所示。

![](https://raw.githubusercontent.com/neal-hues/Eshop/master/shot/sys-cart-eshop.png)

**<p align="center">图2-1 系统流程图</p>**

##### 2.1.2  模块结构图
　　E商城的模块功能结构图如图2-2所示。

![](https://raw.githubusercontent.com/neal-hues/Eshop/master/shot/mod-cart-eshop.png)

**<p align="center">图2-2 模块功能结构图</p>**

#### 2.2  模块功能设计
##### 2.2.1  会员系统
　　会员系统中首先包括会员的注册、会员的登录，用户可以在非登录的状态下正常访问本网站，并浏览商品，但是如果会员想要将商品加入购物车或者购买，就必须登录本网站，如果没有会员资格，需要注册才可以，注册采用简单的注册方式。会员登陆后，可以把商品加入购物车，然后到个人中心结算，在个人中心会员可以设置个人基本资料、上传头像、修改密码，并且能管理购物车信息、订单信息、收货地址以及查看评价记录。

##### 2.2.2  管理员系统
　　管理员系统就是所谓的后台系统，需要具有管理员权限的账户才能登陆，管理员权限只能由管理员赋予，此账户和普通的会员账户是不相同的，能对整个网站进行全面的管理，具体的可以包括以下的管理：

1. 综合设置：导航栏分类管理，轮播图片管理，广告图片管理；
1. 接口设置：支付接口设置，帮助信息管理，搜索关键词管理；
1. 安全管理：网站管理员，修改口令，安全退出；
1. 产品管理：产品分类管理，各个产品信息管理，所有产品查询；
1. 订单管理：订单管理，所有订单查询；
1. 会员管理：会员信息管理，会员查询；
1. 留言评论：所有留言信息，所有评论信息，已处理的留言，已处理的评论。

##### 2.2.3  购物系统
　　购物系统是本网站的重要部分，其中在布局上参考了一些有名的购物网站如京东、淘宝、天猫等，网站的主色调采用的颜色值是#E4393C，次色调主要是#F7F7F7，字体是使用系统默认的字体，字体大小为12px。购物的流程是，先将中意的商品放入购物车中，然后才能到个人中心去结算，生成订单信息，操作之前还需要保持登录状态。<br>
　　会员在浏览商品的过程中，可以把自己有意的商品暂存到购物车中，并且很方便可以在购物车中，浏览自己最新加入的商品，进行查看和删除的操作。会员在查找商品的时候，系统会把标题和所搜关键字相关的所有商品检索出来，做分页处理后供会员浏览。会员也可以通过销量、价格和浏览量进行二次检索缩小的查询范围。
##### 2.2.4  留言评价
　　会员可以在购买商品之前，通过留言咨询和查看商品的评价记录等手段，对商品的信息和购买流程更加了解，而管理人员则可以在后台系统中处理会员的留言，管理商品的评价记录，必要时关闭或删除恶意信息。

### 3  运行设计
#### 3.1  用户界面
##### 3.1.1  e商城网站首页
　　如图3-1所示，是网站的首页，采用现在比较流行的购物网站的布局，把电子产品分为了8个大类，分为是电脑配件、手机配件、数码影音、家用电器、办公打印、网络产品、服务产品，首页的下部分主要是热品推荐和最新的各类商品。

![](https://raw.githubusercontent.com/neal-hues/Eshop/master/shot/3-1-eshop.png)

**<p align="center">图3-1 商城网站首页</p>**

##### 3.1.2  搜索详情页
　　如图3-2所示，是搜索商品的详情页，用户通过在搜索栏或是分类导航类中搜索查询，都能到达该页，如搜索“主机”。此页会把搜索到的商品经过分页处理后，展现给出来，并且可以增加销量、价格和浏览量的条件来缩小搜索的范围。会员可以在此界面把有意购买的商品暂存到购物车。

![](https://raw.githubusercontent.com/neal-hues/Eshop/master/shot/3-2-eshop.png)

**<p align="center">图3-2 搜索详情页</p>**

##### 3.1.3  商品详情页
　　商品的详情页包含的内容较多，除了商品的一些基本信息外，还有大量的介绍商品的图片，用户对此商品的评价和售后保障等。会员可以在此界面把有意购买的商品暂存到购物车，数量可以自己设定，如图3-3所示。

![](https://raw.githubusercontent.com/neal-hues/Eshop/master/shot/3-3-eshop.png)

**<p align="center">图3-3 商品详情页</p>**

##### 3.1.4  会员注册
　　这个是用户注册部分，非本网站会员可以注册成为我们的会员，如图3-4所示。

![](https://raw.githubusercontent.com/neal-hues/Eshop/master/shot/3-4-eshop.png)

**<p align="center">图3-4 用户注册</p>**

##### 3.1.5  会员登录
　　这个是用户登录部分，会员可以通过登录进入个人中心，如图3-5所示。

![](https://raw.githubusercontent.com/neal-hues/Eshop/master/shot/3-5-eshop.png)

**<p align="center">图3-5 用户登录</p>**

##### 3.1.6  个人中心
　　在个人中心，会员可以编辑自己的基本资料、设置自己的头像、修改密码，并且能管理购物车的商品，支付订单，管理订单，修改收货地址以及查看商品的评价记录等等，如图3-6所示。

![](https://raw.githubusercontent.com/neal-hues/Eshop/master/shot/3-6-eshop.png)

**<p align="center">图3-6 个人中心</p>**

##### 3.1.7  管理员登录
　　如图3-7所示，是管理员后台登录界面。

![](https://raw.githubusercontent.com/neal-hues/Eshop/master/shot/3-7-eshop.png)

**<p align="center">图3-7 管理员登录</p>**

##### 3.1.8  后台管理系统
　　后台主界面显示了管理员的登录名和登录次数信息，如图3-8所示。

![](https://raw.githubusercontent.com/neal-hues/Eshop/master/shot/3-8-eshop.png)

**<p align="center">图3-8 后台管理系统</p>**

##### 3.1.9  综合设置
　　后台的综合设置里主要是控制整个网站的界面显示和信息，如图3-9所示。

![](https://raw.githubusercontent.com/neal-hues/Eshop/master/shot/3-9-eshop.png)

**<p align="center">图3-9 综合设置</p>**

##### 3.1.10  产品管理
　　这个功能区中，主要是产品分类，各个产品的信息以及订单的管理查询，如图3-10所示。

![](https://raw.githubusercontent.com/neal-hues/Eshop/master/shot/3-10-eshop.png)

**<p align="center">图3-10 产品管理</p>**

##### 3.1.11  会员管理
　　如图3-11所示，主要是对会员信息的一些操作和管理。

![](https://raw.githubusercontent.com/neal-hues/Eshop/master/shot/3-11-eshop.png)

**<p align="center">图3-11 会员管理</p>**

##### 3.1.12  留言评论管理
　　这个功能区是处理会员的商品评价记录和留言咨询，如图3-12所示。

![](https://raw.githubusercontent.com/neal-hues/Eshop/master/shot/3-12-eshop.png)

**<p align="center">图3-12 留言评论管理</p>**


> PS：网站还有部分功能未实现，如支付接口和物流信息等等。
