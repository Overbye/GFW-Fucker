## 1. 交互界面(UI)

### 1.1 Loon 开关 & 分流模式

<img src="https://raw.githubusercontent.com/Repcz/Tool/X/Loon/Photo/1.1.PNG" width="600">


点击 LOON 下方的 自动分流/全局直连/全局代理 可进行切换：


- 全局直连，即所有请均不使用节点访问，此时分流模式区域为蓝色
- 自动分流，由分流规则及所有策略（内置以及自定义策略）共同決定是否通过节点以及通过什么节点访问，此时分流模式区域为黄色。
- 全部代理，即所有请求均使用 「策略标签页」的 `全局策略` 选择的节点/策略访问，此时分流模式区域为红色。


### 1.2 快捷方式：「编辑」

点击「节点」可对「仪表标签页」所展示的快捷方式进行编辑

拖动右侧 `≡`，可进行排序

<img src="https://raw.githubusercontent.com/Repcz/Tool/X/Loon/Photo/1.2.PNG">


### 1.3 快捷方式：「节点」

> 此区域对应「配置标签页」-「节点」区域 - `全部节点`


点击可查看当前所有节点数目，点击「节点」或右下角图标 可查看

<img src="https://raw.githubusercontent.com/Repcz/Tool/X/Loon/Photo/1.3.PNG">

### 1.4 快捷方式：「请求记录」

点击顶部搜索栏可对 Host、URL、Rule、Rewrite、Script、UserAgent 进行搜索


- 蓝色表示当前请求状态为已完成

- 绿色表示当前请求状态为未完成

- 红色表示当前请求状态为失败


#### TCP/CONNCT


可在概述中查看请求时间、状态、目标地址、流量大小、MITM、规则、策略等信息

点击概述页右上角 `···` 可快捷添加规则

<img src="https://raw.githubusercontent.com/Repcz/Tool/X/Loon/Photo/1.4.1.PNG" width="900">


当开启`SNI辅助规则匹配`后，当请求 Host 是 IP 时，会使用 TLS证书 中的 SNI 进行规则匹配，如果匹配不到规则的话会继续用 Host 匹配

长按 SNI 可复制

<img src="https://raw.githubusercontent.com/Repcz/Tool/X/Loon/Photo/1.4.2.PNG" width="300">



当状态为失败时，会根据策略返回相应的数据(例如去广告规则使用的 REJECT 返回 HTTP 404)，或是当前请求连接失败，点击可查看概述(详情)


<img src="https://raw.githubusercontent.com/Repcz/Tool/X/Loon/Photo/1.4.3.PNG" width="900">


#### POST/GET

在客户机和服务器之间进行请求-响应时，两种最常被用到的方法是：GET 和 POST。

- GET：从指定的资源请求数据。
- POST：向指定的资源提交要被处理的数据。


当 MITM 了对应的主机名，此时POST/GET右侧会有蓝色的🔒

<img src="https://raw.githubusercontent.com/Repcz/Tool/X/Loon/Photo/1.4.4.PNG" width="600">

当使用脚本对请求进行处理时，🔒的右侧会有绿色文件夹📁图标


<img src="https://raw.githubusercontent.com/Repcz/Tool/X/Loon/Photo/1.4.5.PNG" width="600">


当使用复写规则对请求进行处理时，🔒的右侧会有紫色文件夹📁图标

<img src="https://raw.githubusercontent.com/Repcz/Tool/X/Loon/Photo/1.4.6.PNG" width="600">

#### 1.5 快捷方式：「DNS记录」

点击顶部搜索栏可对 IP、Domain、Server 进行搜索

点击可查看记录对应的 域名、DNS服务器、查询结果、查询日期、TTL、状态

`A`记录 表示 IPv4 ，`AAAA`记录 表示 IPv6

<img src="https://raw.githubusercontent.com/Repcz/Tool/X/Loon/Photo/1.5.PNG" width="900">
