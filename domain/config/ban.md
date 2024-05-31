# 组合封禁策略使用说明文档

> 功能说明：针对客户遇到的攻击，提供console平台配置给客户配置组合封禁策略，包括（不限于）针对IP、referer、UA等响应头参数进行限制。

> 配置可提交多个策略，策略最多支持20条，可调整策略优先级，优先级自上而下；

> 每条策略支持单选或者多选匹配规则，规则包括IP、Referer、User-Agent、URL、method;

> 每条策略需客户提交的内容不一致，具体填写规则和示例如下:

逻辑补充：等于：黑名单，不等于：白名单

备注：每次策略配置完成之后，需点击下发配置才会部署配置，预计下发完成时间10分钟。
![image](https://github.com/UCloudDoc-Team/ucdn/assets/89777962/9daa452e-2ea2-49da-9708-fca68347d580)



|匹配规则(多选)	|逻辑(单选）|	参数|	参数限制	|参数示例  |
|----|----|----|----|----|
|IP   	|等于/不等于	  	|客户填写，按回车符隔开  	|	500条  	|	1.1.1.1 <br />   1.2.3.0/24  	|
|User-Agent	  	|等于/不等于	  	|客户填写，按回车符隔开，模糊匹配	  	|100条  	|Chrome/122.0.0.0 Safari/537.36
|Referer  	|	等于/不等于  	|	客户填写，按回车符隔开  	|	100条  	|	*.aaa.ucloud.com  <br /> aaa.ucloud.com.cn	|
|URL  	|	等于/不等于	  	|客户填写，按回车符隔开  	|	100条  	|	http://.www.ttt1.com/1.txt <br /> ^https?:// [^/] +/dir1/dir2/(dir3_1|dir3_2).html$  	|
|method	  	|等于/不等于	  	|GET(默认)/POST  	| 二选一	  	|	GET  	|

配置示例

<strong>IP封禁：</strong>
![image](https://github.com/UCloudDoc-Team/ucdn/assets/89777962/e42a00ef-f0da-4b9c-a4c6-57b20060e540)


<strong> IP+UA+Referer封禁:</strong>
![image](https://github.com/UCloudDoc-Team/ucdn/assets/89777962/b2172d33-8181-4980-978a-7b73c45629d6)

<strong>策略顺序调整</strong>
![image](https://github.com/UCloudDoc-Team/ucdn/assets/89777962/b1b382b0-683f-4b16-8e4b-99d62ec37a4d)


