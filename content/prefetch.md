# 内容预取

内容预取是指在提交预热文件后，会将源站文件缓存到CDN上层节点上，当用户首次请求时，CDN节点会响应用户请求，无需再回源站获取。

一般在业务高峰前预热热点资源，减轻源站压力，提高请求的命中效率。

内容预取仅支持文件预取，不支持目录预取。

预取一般适用于<strong>大文件</strong>，避免因源站出口带宽较小导致的访问回源响应慢的问题。

注：

* 填写文件的完整路径，必须以http(s)://开头，如http(s)://static.ucloud.cn/packages/document.zip。 默认HTTP和HTTPS共用缓存，建议使用HTTP协议的URL进行预取。

* 每条url一行，以回车换行。一次性最多提交<strong>30</strong>条。

* 文件大的时候，预取有可能占用大量带宽，建议在不影响业务的时候进行预取。

* 如果发现预取一直显示处理中，有可能是由于路径填写不正确，填写文件的完整路径。

* 预取需要将文件分发到所有加速节点，完成的总时长取决于源站到加速节点的公网质量，一个100M的文件，预估在30分钟之内。偶然有部分小运营商和较远地区会速度较慢，请您耐心等待。

* 预取文件的过程中将从源站拉取文件，会升高您源站的带宽，导致网络访问变慢。

* 预取产生的带宽/流量，不计入计费带宽，没有控制台显示。

* <strong>单域名</strong>默认预取上限：<strong>500条/天</strong>；若需添加预取上限，请联系技术支持处理。

>加速类型为下载时，预取文件与页面加速略微不同。
>
>下载类型的加速，预取文件是主动从源站获取文件至二级服务器进行加速，需要注意：预取文件不能是图片、html、文本等能够在网页加速中进行加速的文件格式。

相关API文档：

获取预取任务状态: [DescribeNewUcdnPrefetchCacheTask](https://docs.ucloud.cn/api/ucdn-api/describe_new_ucdn_prefetch_cache_task)

提交预取任务:[PrefetchNewUcdnDomainCache](https://docs.ucloud.cn/api/ucdn-api/prefetch_new_ucdn_domain_cache)


#### 操作步骤：

![image-20200305141148288](../images/image-20200305141148288.png)

![image-20200305141201807](../images/image-20200305141201807.png)



