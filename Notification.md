# 【UCDN】关于境外HTTPS证书托管费策略调整的通知-20240415

为配合境外UCDN业务推进计划，产品目前针对CDN境外HTTPS服务所收取的证书托管费用作出以下调整：

具体内容如下：

## 一、取消收取境外HTTPS证书托管费，调整为收取境外HTTPS请求数费用。
费用调整概述：

* 取消境外HTTPS证书托管费：自2024年4月1日起，对于2024年4月1日之后部署证书的服务，将不再收取境外HTTPS证书托管费；

* 新增境外HTTPS请求数费用：自2024年5月1日起，将按照境外HTTPS请求数来收费；

* 若您有使用CDN境外HTTPS加速服务，该计费项将发生改变，烦请各位用户关注。

### 原计费方案：
|计费项目|计费单位|单价|
|:---:|:--------:|:--------:|
|境外HTTPS证书托管费|	元/月/张|	600|



账单对应收费项：

![企业微信截图_17127491723525](https://github.com/UCloudDoc-Team/ucdn/assets/89777962/e729cc5f-9542-411b-b0ea-4d38e913f25b)


### 现替换方案:

境外HTTPS请求数费用：

计费规则：

1.计费项: 境外HTTPS请求数

2.付费方式：日后付/月付。

3.计费周期：按日计费，每日中午12:00后结算前一天的境外HTTPS请求数，匹配对应价格，生成订单；按月计费，于次月1日收取本月所产生的境外HTTPS请求数费用。

4.计算方法：客户在当日统计的境外HTTPS请求数为29988次，则用户的账户扣费金额应为 2*0.05=0.1元。

|区域|协议|单价|单位|计费名称|
|:-----:|:-----:|:-----:|:-----:|:-----:|
|境外|	https|	0.05	|元/万次 |境外静态HTTPS请求数|

备注：客户境外HTTPS请求数在一个计费周期内不足一万次请求，则不收取费用。。


> 费用调整举例：例如客户境外证书是在3月15日部署的，会收取3.15-4.15的费用。4.15-4.30时间内不收取费用，5月1日起按照客户实际请求数进行收费。



## 二、客户控制台调整
自2024年4月15日起，开放境外HTTPS用户自助配置，用户可以自助部署/更新境外HTTPS配置，届时将同步更新产品文档，配置示例如下：

您可直接在域名配置页面，基本信息下对境内.境外HTTPS证书进行部署，选择开启/关闭之后，点击确定，配置即开始下发，全网下发时间大约需要10-15分钟，如在使用过程中遇到其他问题，请联系技术支持。
![image](https://github.com/UCloudDoc-Team/ucdn/assets/89777962/cda1e7f2-e75e-43fa-8e5e-f8447ed31cf1)

![image](https://github.com/UCloudDoc-Team/ucdn/assets/89777962/c3009fd3-78e2-473c-add7-5cc16f8d5c0e)

