# 订货管理端

> 这个系统分为两个端，一个是这个订货管理端，还有一个供应商端，正在做，过段时间会发出来


## 技术栈

> vue2.0 + vue-router + vuex + axios + express + mongodb + mongoose


## 功能简介

1.物料管理

  （1）"订货管理端"采购商可以对物料添加无限级分类
  （2）"订货管理端"采购商需要先发布需要采购的物料，下采购单的时候直接选择。

2.采购单管理（定向招标）

  （1）"订货管理端"发布采购单流程：选择需要采购的物料 => 指定供应商 =>  完善信息 => 发布
  （2）"供应商端"对于指定的供应商会收到这里发布的采购单，并对采购单进行报价
  （3）"订货管理端"收到供应商的报价后，经比价后自行选择中标供应商，并生成订单
  （4）"订货管理端"生成订单后，当前采购单自动移除，订单为待发货状态

3.招标管理（全局招标）

  （1）"订货管理端"采购商发布全局招标，对于"供应商端"系统中的所有用户都可以进行报价，即使不是自己的供应商
  （2）"供应商端"中的所有用户都可以收到这条招标信息，并可以对其进行报价
  （3）"订货管理端"收到供应商的报价后，经比价后自行选择中标供应商，并生成订单
  （4）"订货管理端"生成订单后，当前招标信息自动移除，订单为待发货状态

4.订单管理

  （1）"订货管理端"订单状态分为待发货、待收货、已发货三个状态，对于待收货订单可以进行确认收货，对于已发货订单，即订单完成，可删除订单

5.供应商管理

 （1）"订货管理端"可以对供应商进行自定义分类，对于分类有修改、删除等功能
 （2）对于"供应商端"中的供应商入驻，这里我目前只提供一种方式，就是"订货管理端"中的采购商新增供应商的时候绑定对应关系，并为此供应商分配登录账号

## 部分项目截图

![image](https://github.com/SunShineKG/SRM/blob/master/gif/login.gif)

![image](https://github.com/SunShineKG/SRM/blob/master/gif/materiel.gif)

![image](https://github.com/SunShineKG/SRM/blob/master/gif/supplierClassfication.gif)

![image](https://github.com/SunShineKG/SRM/blob/master/gif/supplierList.gif)

## 补充说明

  这个系统只是我闲来无事做着玩的，对于业务和功能欠缺很多，老铁们随便看看就好，我起初是想做个SRM系统的，然后我整体做了个架构，发现功能块太多太多了，
  然后并没有那么充裕的时间去做，就随手做了这个简易的订货的小系统。

  欢迎大牛们帮我指出问题，刚接触的小白们看到代码不懂的地方也可以随时联系我，一块学习提高， Q:173169254
