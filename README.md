# [首页查询更多项目](https://github.com/GraduationProject-ssm) 包安装运行


# 10963ssm企业公寓后勤管理系统

![picture](https://raw.githubusercontent.com/GraduationProject-springboot/.github/main/img/wx.png)

### 点击播放视频 ▼
[![Watch the video](https://i.sstatic.net/Vp2cE.png)](https://www.bilibili.com/video/BV1Sh44eDEx6?p=62)


# 系统概述
进过系统的分析后，就开始记性系统的设计，系统设计包含总体设计和详细设计。总体设计只是一个大体的设计，经过了总体设计，我们能够划分出系统的一些东西，例如文件、文档、数据等。而且我们通过总体设计，大致可以划分出了程序的模块，以及功能。但是只是一个初步的分类，并没有真正的实现。

整体设计，只是一个初步设计，而且，对于一个项目，我们可以进行多个整体设计，通过对比，包括性能的对比、成本的对比、效益的对比，来最终确定一个最优的设计方案，选择优秀的整体设计可以降低开发成本，增加公司效益，从这一点来讲，整体设计还是非常重要的。

后勤管理系统工作原理图如图4-1所示：

![](/md/blog.012.png)

图4-1 系统工作原理图
## 4.2 系统结构设计
系统架构图属于系统设计阶段，系统架构图只是这个阶段一个产物，系统的总体架构决定了整个系统的模式，是系统的基础。后勤管理系统的整体结构设计如图4-2所示。

![](/md/blog.013.png)

图4-2 系统结构图
## 4.3数据库设计
数据库是计算机信息系统的基础。目前，电脑系统的关键与核心部分就是数据库。数据库开发的优劣对整个系统的质量和速度有着直接影响。
### 4.3.1 数据库设计原则
数据库的概念结构设计采用实体—联系（E-R）模型设计方法。E-R模型法的组成元素有：实体、属性、联系，E-R模型用E-R图表示，是提示员工工作环境中所涉及的事物，属性则是对实体特性的描述。在系统设计当中数据库起着决定性的因素。下面设计出这几个关键实体的实体—关系图。
### 4.3.2 数据库实体
数据模型中的实体（Entity），也称为实例，对应现实世界中可区别于其他对象的“事件”或“事物”。例如，公司中的每个员工，家里中的每个家具。

本系统的E-R图如下图所示：

1、员工信息实体图如图4-3所示：

![](/md/blog.014.png)

图4-3员工信息实体图

2、公寓信息实体图如图4-4所示：

![](/md/blog.015.png)

`       `图4-4公寓信息实体图

3、订单信息实体图如图4-5所示：

![](/md/blog.016.png)

`     `图4-5订单信息实体图
### 4.3.3 数据库表设计
数据库的表信息属于设计的一部分，下面介绍数据库中的各个表的详细信息。

表4-1 allusers表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|int|11|NOT NULL|
|username|varchar|50|` `default NULL|
|pwd|varchar|50|` `default NULL|
|cx|varchar|50|` `default NULL|


`  `表4-2 gongyuxinxi表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|int|11|NOT NULL|
|addtime|varchar|50|default NULL|
|gongyubianhao|varchar|50|default NULL|
|gongyumingcheng|varchar|50|default NULL|
|gongyuhuxing|varchar|50|default NULL|
|tupian|varchar|50|default NULL|
|gongyusheshi|varchar|50|default NULL|
|weizhi|varchar|50|default NULL|
|mianji|varchar|50|default NULL|
|gongyuxiangqing|varchar|50|default NULL|
|fabushijian|varchar|50|default NULL|

表4-3：yuangong表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|` `int|11|NOT NULL |
|addtime|varchar|50|default NULL|
|gonghao|varchar|50|default NULL|
|mima|varchar|50|default NULL|
|xingming|varchar|50|default NULL|
|`      `xingbie|varchar|50|default NULL|
|nianling|varchar|50|default NULL|
|`      `shouji|varchar|50|default NULL|
|`     `shenfenzheng|varchar|50|default NULL|
|tupian|varchar|50|default NULL|
|jifen|varchar|50|default NULL|


表4-4：yuangongjifen表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|` `int|11|NOT NULL |
|addtime|varchar|50|default NULL|
|gonghao|varchar|50|default NULL|
|xingming|varchar|50|default NULL|
|shouji|varchar|50|default NULL|
|jifen|varchar|50|default NULL|
|dengjiriqi|varchar|50|default NULL|

表4-5：gongyuhuxing表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|` `int|11|NOT NULL |
|addtime|varchar|50|default NULL|
|huxing|varchar|50|default NULL|

#########
# 5系统界面实现
## 5.1 管理员登录
管理员输入个人的用户名、密码和角色登录系统，这时候系统的数据库就会在进行查找相关的信息，如果我们输入的用户名、密码和角色不正确，数据库就会提示出错误的信息提示，同时会提示管理员重新输入自己的用户名、密码、角色，直到账号密码输入成功后，会提登录成功的信息。网站管理员登录效果图如图5-1所示：

![](/md/blog.017.png)     
图5-1管理员登录界面

## 5.2  管理员功能模块     
### 5.2.1 个人信息
管理员对个人信息进行填写用户名并进行详情、删除、修改等操作。程序成效图如下图5-2所示:

![](/md/blog.018.png)

图5-2个人信息界面图
### 5.2.2员工管理
管理员对员工管理进行查看工号、姓名、性别、年龄、手机、身份证、图片、积分等信息并可以进行详情、删除、修改操作。程序效果图如下图5-3所示：

![](/md/blog.019.png)

图5-3员工管理界面
### 5.2.3 公寓户型管理
管理员对公寓户型管理进行查看户型等信息并可以进行详情、删除、修改操作。程序效果图如下图5-4所示：

![](/md/blog.020.png) 

图5-4公寓户型管理界面

### 5.2.4公寓信息管理
管理员对公寓信息管理进行查看公寓编号、公寓名称、公寓户型、图片、公寓设施、位置、面积、发布时间、积分等进行详情、删除、修改操作。程序效果图如下图5-5所示：

![](/md/blog.021.png)

图5-5公寓信息管理界面
### 5.2.5员工积分管理
管理员对员工积分管理进行查看工号、姓名、手机、积分、登记日期等信息并可以进行详情、删除、修改操作。程序效果图如下图5-6所示：

![](/md/blog.022.png) 

图5-6员工积分管理界面
### 5.2.6通知公告
管理员对通知公告进行查看标题、简介、图片等信息并可以进行详情、删除、修改操作。程序效果图如下图5-7所示：

![](/md/blog.023.png) 

图5-7通知公告界面


### 5.2.7订单管理
管理员对订单管理进行查看订单编号、商品名称、商品图片、购买数量、价格/积分、折扣价格、总价格/总积分、折扣总价格、支付类型、状态、地址等信息并可以进行详情、删除、修改操作。程序效果图如下图5-8所示：

![](/md/blog.024.png) 

图5-8订单管理界面




## 5.3 前台首页功能模块
前台首页详情页面查看首页、公寓信息、通知公告、个人中心、后台管理、在线客服等功能操作。程序效果图如下图5-9所示：

![](/md/blog.025.png)

图5-9前台首页功能界面
## 5.3.1员工注册、员工登录
员工在线填写工号、密码、姓名、年龄、手机、身份证等信息进行注册、登录操作。程序效果图如下图5-10所示：

![](/md/blog.026.png)

![](/md/blog.027.png)

图5-10员工登录、员工注册界面
## 5.3.2个人中心
员工进入个人中心可以填写工号、密码、姓名、性别、年龄、手机、身份证、图片、积分等信息，并可以进行更新信息、退出登录操作。程序效果图如下图5-11所示：

![](/md/blog.028.png)


图5-11个人中心界面
## 5.3.3公寓信息
员工进入公寓信息可以查看公寓编号、公寓名称、公寓户型、图片、公寓设施、位置、面积、发布时间、点击次数等信息进行积分兑换、点我收藏操作。程序效果图如下图5-12所示：

![](/md/blog.029.png)

图5-12公寓信息界面

## 5.4 员工功能模块

员工进入后勤管理系统可以查看首页、个人中心、员工积分管理、我的收藏管理等功能。程序效果图如下图5-13所示：

![](/md/blog.030.png)

图5-13员工功能界面
## 5.4.1员工积分管理
员工进入员工积分管理可以查看工号、姓名、手机、积分、登记日期并可以进行详情、删除等操作。程序效果图如下图5-14所示：

![](/md/blog.031.png)

图5-14员工积分管理界面












