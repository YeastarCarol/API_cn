# 响铃组拨打外线

通过本接口可让S系列IPPBX先呼叫外线，外线通后，转给响铃组。转至响铃组后，响铃组分机根据响铃组所设置的响铃策略响铃。

**说明：**需采用某个分机的路由权限匹配呼出路由呼出规则呼出。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/](https://192.168.5.150:8088/api/v1.0.1/ringgroup/dial_outbound?token=172970ee3f5f92fe65cd6bc17663b1f7){version}[/ringgroup/dial\_outbound?token=172970ee3f5f92fe65cd6bc17663b1f7](https://192.168.5.150:8088/api/v1.0.1/ringgroup/dial_outbound?token=172970ee3f5f92fe65cd6bc17663b1f7)

**请求示例：**

{ "ringgroupid": "6200","outto": "118396210850","fromext": "1000000"}

**请求参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;ringgroupid&gt; | int | 响铃组号码 | 6200 |
| &lt;outto&gt; | string | 要拨打的外线号码 | 118396210850 |
| &lt;fromext&gt; | string | 采用哪个分机的权限 | 1000000 |

**响应示例：**

{"status":"Success","callid":"1501145750.391"}

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;status&gt; | string | 请求结果 | Success或者Failed |
| &lt;callerid&gt; | string | 该通通话的id | 1501145750.391 |



