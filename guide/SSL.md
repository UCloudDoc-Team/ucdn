## 证书管理

当您需要使用https加速时，需要上传证书。

进入证书管理页面，点击<code>上传证书</code>，若您需要购买证书，可点击<code>购买证书</code>跳转到<strong>USSL配置平台</strong>操作。

![2022-UCDN证书管理列表](/images/2022-UCDN证书管理列表.png)

输入<code>证书名称</code>，<code>上传授权证书(.crt文件)</code>、<code>授权私钥(.key文件)</code>、<code>CA机构证书(.crt文件)</code>。

![2022-UCDN证书上传-1](/images/2022-UCDN证书上传-1.png)

如果您的证书上传到了USSL，可以通过选择已购买上传，需要自定义证书名称，选择<strong>未过期，且证书状态是正常的</strong>证书。

![2022-UCDN证书上传-2](/images/2022-UCDN证书上传-2.png)

注：

<li /> 上传证书后，还需要到域名详情页面选择对应证书开通https加速。

<li /> 如需更换证书，请上传新的证书后到域名详情页面进行新证书的绑定。

<li /> 若需新增海外HTTPS,请知悉HTTPS请求数费用，详情见[CDN境外HTTPS请求数计费](https://docs.ucloud.cn/ucdn/charge/flowday_new?id=cdn%e5%a2%83%e5%a4%96https%e8%af%b7%e6%b1%82%e6%95%b0)

## 相关API：

| API | 描述信息 |
|:---|:---|
|[AddCertificate](api/ucdn-api/add_certificate)|添加证书|
|[DeleteCertificate](api/ucdn-api/delete_certificate)|删除证书|
|[GetCertificateV2](api/ucdn-api/get_certificate_v2)|获取证书|
