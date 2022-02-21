## 日志下载

进入日志下载页面下载相关日志信息。当天的日志第二天支持下载，目前CDN日志保存3个月，也可通过API拉取。如果您需要将日志保存更长时间，建议您尽早下载日志并保存。

可按照5分钟、1小时或者天粒度下载日志

![日志下载](/images/2022-UCDN日志下载.png)

### 默认日志格式如下：

|	字段	|	名称	|	示例	|	举例	|
|------|------|------|------|
|	1	|	日期时间	|	日志记录时间	|	[2022-02-18 00:15:00]|
|	2	|	客户端IP	|	客户端ip	|	120.32.40.179	|
|	3	|	"方法 url 协议版本"	|	http请求	|	"GET /ucdntest.mp4 HTTP/1.1"	|
|	4	|	命中状态	|	命中状态,具体内容显示参考[备注1](../ucdn/guide/LOG.md#备注1)	|	TCP_HIT	|
|	5	|	响应码	|	http返回状态码	|	200	|
|	6	|	发送字节数	|	包括http头的本次请求发送的所有字节数	|	674	|
|	7	|	响应延时	|	响应延时(ms)	|	81	|
|	8	|	Host	|	http host	|	www.ucloud.cn	|
|	9	|	Referer	|	http referer	|	http://www.ucloud.cn/	|
|	10	|	username	|	http username 一般为"-" 不存在	|	-	|
|	11	|	回源方式/host	|	回源方式/回源host 预留 现在都是 NONE/-	|	NONE/-	|
|	12	|	服务器IP	|	处理该请求的服务器ip	|	27.155.93.38	|
|	13	|	源IP	|	源站ip	|	122.228.243.88	|
|	14	|	源站响应码	|	源站http响应码	|	0	|
|	15	|	客户端请求结束标记	|	客户端请求结束标记(0正常结束 1客户端提前断开)	|	0	|
|	16	|	源站请求结束标记	|	源站请求结束标记 目前都是0	|	0	|
|	17	|	User-Agent	|	http user-agent（小文件至此结束）	|	"Mozilla/5.0+AppleWebKit/537.36+(KHTML,+like+Gecko)+Language/zh_CN"	|
|	18	|	请求开始处理时间	|	请求开始处理时间 unix时间戳	|	1495186500	|
|	19	|	前端flow	|	前端flow 用来标识一个http请求的唯一标识码 类似于id	|	1513283749	|
|	20	|	range	|	http range	|	bytes=0-1	|
|	21	|	发送字节数	|	发送字节数(不包括http头)	|	2	|
|	22	|	文件大小	|	文件大小	|	8459952	|
|	23	|	缓存命中的字节数	|	缓存命中的字节数	|	674	|
|	24	|	合并回源的字节数	|	合并回源的字节数	|	0	|
|	25	|	内部错误码	|	内部错误码(开发调试用)	|	0	|
|	26	|	结束时状态	|	请求结束标志(开发调试用)	|	50	|
|	27	|	从ufile获取的字节数	|	从ufile获取的字节数 目前都是0	|	0	|
|	28	|	cache端口	|	cache端口(开发调试用)	|	40080	|
|	29	|	传输协议	|		|	HTTP	|

### 备注1

|	命中状态值	|	说明	|
|-------|------|
|	ERR_READ_ERROR	|	读错误	|
|	ERR_READ_TIMEOUT	|	访问超时	|
|	TCP_HIT	|	命中cache	|
|	TCP_IMS_HIT	|	客户端发起的If条件请求，命中cache	|
|	TCP_IMS_MISS	|	客户端发起的If条件请求，未命中	|
|	TCP_MEM_HIT	|	命中内存cache	|
|	TCP_MISS	|	未命	|
|	TCP_REFRESH_HIT	|	cache时间过期，回源检查后命中	|
|	TCP_REFRESH_MISS	|	cache时间过期，回源检查后未命中	|
|	TCP_SWAPFAIL_MISS	|	磁盘命中失败而产生回源	|
|	注：大文件现在只有TCP_MISS,TCP_HIT			|

## 相关API
| API | 描述信息 |
|:---|:---|
|[GetUcdnDomainLog](api/ucdn-api/get_ucdn_domain_log)|获取加速域名日志|
|[GetUcdnDomainLogV2](api/ucdn-api/get_ucdn_domain_log_v2)|获取域名5分钟日志|

