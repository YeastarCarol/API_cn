# 响铃组拨打外线

通过本接口可让S系列IPPBX先呼叫外线，外线通后，转给响铃组。转至响铃组后，响铃组分机根据响铃组所设置的响铃策略响铃。

**请求方式：**POST

**请求地址：**https://192.168.5.150:8088/api/v1.0.1/ringgroup/dial\_outbound?token=172970ee3f5f92fe65cd6bc17663b1f7

**请求示例：**

{ "ringgroupid": "6200","outto": "118396210850","fromext": "1000000"}

**请求参数说明：**

| **参数名称** | **类型** | **参数说明** | **参数值举例** |
| :--- | :--- | :--- | :--- |
| **&lt; ringgroupid&gt;** | String | 响铃组号码 | 6400 |
| **&lt;outto&gt;** | String | 外线号码 | 18045924562 |
| **&lt;fromext&gt;** | String | 采用哪个分机的权限 | 1000 |

**响应示例：**

{"status":"Success","callid":"1501145750.391"}

**响应参数说明：**

| **参数名称** | **类型** | **参数说明** | **参数值举例** |
| :--- | :--- | :--- | :--- |
| **&lt; Status&gt;** | String | 请求结果 | Success或者Failed |
| **&lt;callerid&gt;** | String | 通话唯一标识符 |  |


