# 高级设置

关于CDN的更多配置，您可以通过本文您可以了解如何配置及相关的注意事项等。

部分配置为非标支持配置，如需配置请联系技术支持。

|功能|是否支持|
|----|------|
|[强制跳转](../ucdn/domain/config/more?id=%e5%bc%ba%e5%88%b6%e8%b7%b3%e8%bd%ac)|支持|
|[自定义回源Header头](../ucdn/domain/config/more?id=%e8%87%aa%e5%ae%9a%e4%b9%89%e5%9b%9e%e6%ba%90header%e5%a4%b4)|支持|
|[自定义响应Header头](../ucdn/domain/config/more?id=%e8%87%aa%e5%ae%9a%e4%b9%89%e5%93%8d%e5%ba%94header%e5%a4%b4)|支持|
|[全站加速-QUIC](../ucdn/domain/config/more?id=quic)|支持|
|[全站加速Websocket](../ucdn/domain/config/more?id=websocket)|支持|
|[IPv6](../ucdn/domain/config/more?id=%e5%8d%8f%e8%ae%ae%e7%b1%bb)|支持|
|[range回源](../ucdn/domain/config/more?id=%e5%9b%9e%e6%ba%90%e7%b1%bb)|支持|
|[UA黑白名单](../ucdn/domain/config/more?id=%e8%ae%bf%e9%97%ae%e6%8e%a7%e5%88%b6%e7%b1%bb)|支持|
|[时间戳防盗链](../ucdn/domain/config/more?id=%e8%ae%bf%e9%97%ae%e6%8e%a7%e5%88%b6%e7%b1%bb)|支持|
|[带宽封顶](../ucdn/domain/config/more?id=%e8%ae%bf%e9%97%ae%e6%8e%a7%e5%88%b6%e7%b1%bb)|支持|
|[单链接限速](../ucdn/domain/config/more?id=%e8%ae%bf%e9%97%ae%e6%8e%a7%e5%88%b6%e7%b1%bb)|支持|
|[IP访问频次限制](../ucdn/domain/config/more?id=%e8%ae%bf%e9%97%ae%e6%8e%a7%e5%88%b6%e7%b1%bb)|支持|
|[Http2.0](../ucdn/domain/config/more?id=https%e7%9b%b8%e5%85%b3)|支持|
|[HTTPS强制跳转](../ucdn/domain/config/more?id=https%e7%9b%b8%e5%85%b3)|支持|
|[OCSP](../ucdn/domain/config/more?id=https%e7%9b%b8%e5%85%b3)|支持|
|[智能压缩](../ucdn/domain/config/more?id=%e5%85%b6%e4%bb%96%e9%85%8d%e7%bd%ae)|支持|

## 强制跳转

您可以通过设置强制跳转，将用户的请求强制重定向为HTTPS

> 执行该操作前，请您确保对应域名已成功配置HTTPS证书。
>

## 自定义回源Header头

通过配置回源HTTPHeader头，您可以设定回源头部信息。通过设置参数和对应值的方式来实现HTTPHeader头的设置。

| 参数       | 说明                                       |
| ---------- | ------------------------------------------ |
| 自定义参数 | 根据您的业务实际需求，进行参数和值的设定。 |

## 自定义响应Header头

通过配置响应HTTPHeader头，您可以实现跨域访问、设定或指定头部信息包含在HTTP响应头中。通过设置参数和对应值的方式来实现HTTPHeader头的设置。

常见的HTTP响应头参数如下说明：

| 参数                          | 说明                                                         |
| ----------------------------- | ------------------------------------------------------------ |
| Access-Control-Allow-Origin   | 指定允许的跨域请求的来源。<br />当设置为“*”，允许被所有域请求。 |
| Access-Control-Allow-Methods  | 指定允许的跨域请求方法。<br />一般的方法有POST, GET, OPTIONS等。 |
| Access-Control-Max-Age        | 指定客户端程序对特定资源的预取请求返回结果的缓存时间。       |
| Access-Control-Expose-Headers | 指定允许的跨域请求的字段。<br />像Cache-Control、Content-Language、Content-Type等 |
| 自定义参数                    | 您也可以自定义参数。                                         |

## 操作步骤

1.进入UCDN产品控制台【域名管理】页面，选择需要配置的域名。

![image-20191211151200171](../../images/image-20191211151200171.png)

2.进入域名配置详情页面，选择【域名配置】—【基础设置】—【高级设置】，进行相关配置。

![image-20191219165503664](../../images/image-20191219165503664.png)

3.开启强制跳转、添加回源header头，添加响应header头。

>配置修改完成后一定要点击**确认配置**后，才能成功修改配置。
>
>![2022-域名配置-确认配置](../../images/2022-域名配置-确认配置.png)

开启强制跳转

![image-20191220102409939](../../images/image-20191220102409939.png)

添加响应Header头![image-20191219165518918](../../images/image-20191219165518918.png)

添加回源Header头

![image-20191219165531832](../../images/image-20191219165531832.png)


## 全站加速特殊配置

### Quic

Quic协议实现低延时传输，适用于弱网环境，若您的业务用户场景需要保持网络流畅性，可选择使用Quic协议。

Quic协议服务为增值服务，需针对请求数进行收费，费用详情请参考[全站加速-请求数](https://docs.ucloud.cn/ucdn/charge/flowday_new?id=%e5%85%a8%e7%ab%99%e5%8a%a0%e9%80%9f-%e8%af%b7%e6%b1%82%e6%95%b0)

开启方式：联系客户经理非标开启。

开启完成后，您可以在对应域名配置下查看服务开启状态。

![image](https://user-images.githubusercontent.com/89777962/233562214-fc604bf9-9871-41e4-8af6-b48bb1724edd.png)

### WebSocket

WebSocket能保持实时通信，不需要一直通过向服务端发出请求来保持链接。当您的服务需要主动推送信息到客户端，且针对实时通信要求较高，建议您选择开启WebSocket服务。

Websocket服务为增值业务收费，费用详情参考 [全站加速WebSocket月流量计费](https://docs.ucloud.cn/ucdn/charge/month?id=%e5%85%a8%e7%ab%99%e5%8a%a0%e9%80%9fwebsocket%e6%9c%88%e6%b5%81%e9%87%8f%e8%ae%a1%e8%b4%b9)

开启方式：联系客户经理非标开启。

开启完成后，您可以在对应域名配置下查看服务开启状态。

![image](https://user-images.githubusercontent.com/89777962/233562150-ff331a8a-2b6f-47ba-a7fc-0382e11d239c.png)


## 更多非标配置

当您需要针对域名配置更多策略，但控制台自助无法满足，需联系客户经理或者技术支持进行非标配置；

下面举例支持的部分非标配置，若以下配置未能满足您的需求，也可联系客户经理或者技术支持进行非标评估并配置。

配置时间与需求复杂度相关，正常情况下需求可在工作日当天完成，非工作日会延期交付。

### 协议类

* IPv6:目前支持IPv6协议加速，不支持IPv6协议回源.

### 回源类

* range回源 ：分段回源，默认关闭分段回源，要求源站支持Range头；启用该配置后，CDN会向源站发起Range请求（默认是回源请求整个文件），从而提高 CDN 内容获取效率；开启分片回源可能会影响回源。


### 访问控制类

* UA黑白名单：对用户请求的User-Agent头进行限制，仅允许/禁止指定 User-Agent 的请求访问CDN域名。

* 时间戳防盗链：可参考[时间戳防盗链](https://docs.ucloud.cn/ucdn/domain/config/control?id=md5%e9%98%b2%e7%9b%97%e9%93%be),若有其他防盗链策略也可评估确认支持情况。

* 带宽封顶：通过对域名进行带宽峰值限制，来控制成本或者防止攻击影响线上服务，一般来说限制策略有：
  
  A.设置带宽峰值阈值为XXX (Mbps)，对于超过阈值之后的请求进行单链接限速Y（MB/s），这种限制并不能将峰值完全限制在XXX值，会根据单链接限速的大小和请求数进行累计
  
  B.设置带宽峰值阈值为XXX (Mbps)，对于超过阈值之后的请求进行403封禁。
  
* 单链接限速：针对单次请求限速XX MB/S (也可以设置KB/s,B/s;GB/s以上不建议设置，限速效果不明显)。

* IP访问频次限制：针对单IP在单位时间内，限制访问次数，超过则设置一个时间段内返回403。配置策略为：域名/指定目录/URL在X分钟内收到ip的访问超过X次，则在接下来的X秒/分钟/小时内，达到阈值的IP再次访问该域名或者目录或者URL就会被拒绝（403）。

### HTTPS相关

* HTTP/2 设置

* HTTPS强制跳转：HTTP请求跳转到HTTPS

* OCSP配置：可提升客户端HTTPS请求时TLS的握手效率，减少用户访问时间。

### 其他配置

* 智能压缩：对静态文件进行Gzip压缩，以减少请求产生的下行流量，且加快文件传输速率，客户端在请求时需要携带Accept-Encoding来进行压缩请求。
