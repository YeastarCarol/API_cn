# 查询设备信息

通过此接口可查询S系列IPPBX设备的相关信息。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/v1.0.0/deviceinfo/query?token=7d20390952e15eb72b0a1df7172de65c](https://192.168.5.150:8088/api/v1.0.0/deviceinfo/query?token=7d20390952e15eb72b0a1df7172de65c)

**请求参数说明：**

无参数，直接发送查询设备信息的请求即可。

**响应示例：**

{"status":"Success","deviceinfo":{"devicename":"Yeastar S100","sn":"369364835218","hardwarever":"V1.30 0000-0000","firmwarever":"30.5.0.19","systemtime":"2017-05-24 23:25:20 UTC-8","uptime":"03:25:04","extensionstatus":"7/100"}}

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;devicename&gt; | string | 产品设备名称 | Yeastar S100 |
| &lt;sn&gt; | string | 产品序列号 | 369364835218 |
| &lt;hardwarever&gt; | string | 硬件版本号 | V1.30 0000-0000 |
| &lt;firmwarever&gt; | string | 固件版本号 | 30.5.0.19 |
| &lt;systemtime&gt; | string | 系统时间 | 2017-05-24 23:25:20 UTC-8 |
| &lt;uptime&gt; | string | 启动时间 | 03:25:04 |
| &lt;extensionstatus&gt; | string | 当前分机数/总分机数 | 7/100 |

**可能出现的错误码：**30001

