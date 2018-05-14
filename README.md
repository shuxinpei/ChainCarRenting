# ChainCarRenting
HackPKU 2018 Project


创意来源
-----------------

背景
----------------
1. 真正意义上的共享经济
2. 信用机制
3. 责任机制 
4. 物联网
5. 更加方便的租借服务
6. AR

汽车共享，开车人对车辆暂时拥有使用权。但是存在的问题是需要一个公司对车辆进行协调，保险以及停放的问题。本质上还是租赁服务。<br>
一边是需求方，一边是供给方，双方互相之间存在正或者负的外部性，然后通过平台交易解决信息不对称。<br>
在本次Hack中我们以汽车作为突破点进行开发。<br>
1.由于租赁服务中存在种种不安全的因素，例如交互双方的信息需要通过第三方进行传输，可以被第三方获取，或者第三方可以使用信息进行非法活动。<br>
2.同时汽车租赁不同于其他租赁，存在一定风险，需要引入问责以及信任机制。最后结合一系列提高交互的手段提供XXXX平台来保障这一些租赁交易。

解决的问题
--------------------
1.数据中转第三方的去除：<br>
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;直接在区块链中寻找得到合适的车辆信息，选择合适服务。<br>
2.选择车辆：<br>
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;使用AR技术<br>
3.开锁权限与密钥：<br>
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
	2.1 直接转移权限到租车者，除了租车者以外没有人拥有使用权限<br>
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
	2.2租车者通过对车进行充值从而获得权限，通过判断余额，自动进行权限转移。为车辆提供者提供了便捷，节省了时间。<br>
4.问责机制与信用机制：<br>
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
	3.1在租赁之前生成法律协议，上传至网络中，带有双方签名后才可继续交易。协议具有不可篡改的特性，为问责提供保障,为信任考察提供依据。<br>

用户使用流程（实际展示,iOS端AR选择车辆，web前端车主确认申请同时法律协议签字，iOS端获得秘钥以后获得开启与关闭车门的权限(使用树莓派代替车门展示)）
--------------------
租者：
---------------

1.租者浏览区块链得到租车信息，通过使用AR技术查看车子的外形，满意以后确认选择车辆。<br>
2.生成法律协议，租车者确认签名，同时请求发送到供车者，供车者签署协议，协议上传至网络，以供认证之用。<br>
3.签署法律协议以后，车主确认租赁车辆给租者，租者开始拥有对汽车进行转入钱的权限。当钱足够的时候，开启车门的权限转移至租者。<br>
4.租者拥有权限以后，车子更新秘钥，将新的秘钥发给租者。<br>
5.租者可以使用秘钥进行开启车锁（树莓派）
5.每天将车子中的余额转移至车主，当余额不足的时候，权限转移至车主，生成新的秘钥给车主。

供车者：
-----------------
1.签署法律协议
2.接受申请



使用的技术：
-----------------
ios->ARKit

后端->Koa

树莓派->Raspberry Pi + Flask

前端 layui vue

使用的API
-----------------

纸贵BaaS





未来展望
-----------------

在链上进行推荐算法实现

增加隐私保护

