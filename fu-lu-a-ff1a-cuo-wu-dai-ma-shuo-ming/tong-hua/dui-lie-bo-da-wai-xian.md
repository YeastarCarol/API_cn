# 队列拨打外线

通过本接口可使S系列IPPBX先呼叫外线，外线通后，转给队列。转至队列后，队列坐席根据队列所设置的坐席响铃策略响铃。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/v1.0.1/queue/dial\_outbound?token=25e9c77a705e6da650082dc1409fb68e](https://192.168.5.150:8088/api/v1.0.1/queue/dial_outbound?token=25e9c77a705e6da650082dc1409fb68e)

**请求示例：**

{ "queueid": "6700","outto": "118396210850","fromext": "1000000"}

**请求参数说明：**

| **参数名称** | **类型** | **参数说明** | **参数值举例** |
| :--- | :--- | :--- | :--- |
| **&lt; queueid&gt;** | String | 队列号码 | 6200 |
| **&lt;outto&gt;** | String | 外线号码 | 18045924562 |
| **&lt;fromext&gt;** | String | 采用哪个分机的权限 | 1000 |

**响应示例：**

{"status":"Success","callid":"1501126620.23"}

**响应参数说明：**

| **参数名称** | **类型** | **参数说明** | **参数值举例** |
| :--- | :--- | :--- | :--- |
| **&lt; Status&gt;** | String | 请求结果 | Success或者Failed |
| **&lt;callerid&gt;** | String | 通话唯一标识符 |  |



