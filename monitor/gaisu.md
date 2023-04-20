# 概述

UCloudCDN提供实时监控功能，在控制台<strong>实时监控</strong>页面下，您将会看到静态加速和全站加速对应的带宽、请求数、命中率、状态码及回源带宽和回源状态码等数据。本文将有助您了解并查询UCDN的监控数据。

目前分为静态加速和全站加速两个子项分别查询。

## 监控项概述

| 监控项     | 说明                                                         |
| ---------- | ------------------------------------------------------------ |
|  剩余流量/日带宽峰值  |  若您选择的计费方式为<strong>预付费流量包</strong>，则显示<strong>剩余流量</strong>，剩余流量=所购流量包总流量-已使用流量；若您选择的计费方式为<strong>日峰值带宽后付费</strong>，则显示为<strong>当日带宽峰值</strong>。若您的计费模式为<strong>月付带宽</strong>，则显示当日峰值带宽。若计费方式为<strong>月付流量</strong>，则显示当月使用流量。 |
|   当前计费模式    |   可选择预付费流量包或者日峰值后付费进行计费（<strong>二选一</strong>），若选择日峰值后付费，则已购买的流量包不会再使用；若需要使用月付费，请与客户经理联系，修改为月付时，当前计费模式显示为：按月后付费。  |
| 带宽/流量  | 展示用户在当前时间粒度产生的<strong>下行带宽</strong>，计费按照下行带宽进行收费。</b>系统默认展示最近一天的监控情况，也可根据需求选择查询的时间粒度，支持最长查询时间跨度为31天，最久支持查询最近半年的数据；</b>若使用高级筛选，可根据分运营商或者分地区进行查看，最长支持查询31天的数据。        |
| 请求数/回源请求数     | 请求数监控，可以分析某一时段的用户请求量。  |
| 命中率   | 命中率监控，包括流量命中率和请求数命中率，通过命中率可以分析出CDN节点响应用户请求的情况。 |
| 状态码/回源状态码 | 状态码监控，可查看域名状态码情况，支持显示1XX\2XX\3XX\4XX\5XX状态码。 |

### 支持查询的时间粒度

| 时间粒度 | 单次查询最大时间跨度 | 最大查询时间范围 |
| ------- |------- |-------|
|1分钟|3天|一年|
|5分钟|30天|一年|
|1小时|30天|一年|
|1天|32天|一年|



## 相关API文档
|API文档|相关描述信息|
|------|------|
|[GetUcdnDomain95BandwidthV2](api/ucdn-api/get_ucdn_domain95_bandwidth_v2)|获取域名九五峰值带宽数据【新】|
|[GetUcdnDomainBandwidthV2](api/ucdn-api/get_ucdn_domain_bandwidth_v2)|获取域名带宽数据【新】|
|[GetUcdnDomainHitRate](api/ucdn-api/get_ucdn_domain_hit_rate)|获取域名命中率【新】|
|[GetUcdnDomainHttpCodeV2](api/ucdn-api/get_ucdn_domain_http_code_v2)|获取域名状态码信息【新】|
|[GetUcdnDomainOriginHttpCode](api/ucdn-api/get_ucdn_domain_origin_http_code)|获取域名源站状态码监控|
|[GetUcdnDomainOriginHttpCodeDetail](api/ucdn-api/get_ucdn_domain_origin_http_code_detail)|获取域名源站详细状态码监控|
|[GetUcdnDomainOriginRequestNum](api/ucdn-api/get_ucdn_domain_origin_request_num)|获取域名回源请求数【新】|
|[GetUcdnPassBandwidthV2](api/ucdn-api/get_ucdn_pass_bandwidth_v2)|获取回源带宽数据（按时间分类）【新】|
|[GetUcdnProIspBandwidthV2](api/ucdn-api/get_ucdn_pro_isp_bandwidth_v2)|按省份运营商获取域名带宽数据【新】|
|[GetUcdnProIspRequestNumV2](api/ucdn-api/get_ucdn_pro_isp_request_num_v2)|按省份运营商获取域名请求数【新】|
|[GetUcdnTrafficV2](api/ucdn-api/get_ucdn_traffic_v2)|获取账户总流量信息【新】|
