# 概述

UCloudCDN控制台【域名管理】页面下，您将会看到账户计费方式、流量消耗剩余明细，加速域名基本信息展示、加速域名配置等。本文将有助您了解并使用UCloud CDN产品。

## 功能概述

![2022-Ucdn域名管理](../images/2022-UCDN域名管理.png)

| 功能项             | 说明                                                         |
| ------------------ | ------------------------------------------------------------ |
| 添加加速           | 新增需要加速的域名  |
| 域名基本信息和操作 | 域名基本信息，包含CNAME域名，源站信息，加速类型等。<br />基本操作包含开启加速、停止加速、删除加速等。|
| 域名配置信息       | 包含回源配置，缓存配置等，可自主进行操作修改配置。           |

如下将会针对每个模块进行逐一的介绍说明。

## 相关API
| API | 描述信息 |
|:---|:---|
|[GetUcdnDomainInfoList](https://docs.ucloud.cn/api/ucdn-api/get_ucdn_domain_info_list)|获取域名基本信息|
|[GetUcdnDomainConfig](https://docs.ucloud.cn/api/ucdn-api/get_ucdn_domain_config)|批量获取加速域名配置|
