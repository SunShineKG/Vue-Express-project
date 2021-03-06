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
 
 
 ## 线上地址

服务器是阿里云的最低配 1核 1G 1M带宽，并且好多性能优化还没来记得做，并且图片是直接从我服务器上加载的，没有放到OSS上，所以资源加载速度可能有点慢。

http://106.15.224.110:3001   测试账号  admin  密码 123123

