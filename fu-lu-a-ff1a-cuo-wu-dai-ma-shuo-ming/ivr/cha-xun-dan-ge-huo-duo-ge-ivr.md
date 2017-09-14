# 查询单个或多个IVR

通过本接口查询单个或多个IVR的详细信息，如：IVR号码，名称，按键事件，响应超时时间。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/](https://192.168.5.150:8088/api/v1.0.0/ivr/query?token=6cad9cee6e2ad94570636e7b3690aeb2){version}[/ivr/query?token=6cad9cee6e2ad94570636e7b3690aeb2](https://192.168.5.150:8088/api/v1.0.0/ivr/query?token=6cad9cee6e2ad94570636e7b3690aeb2)

**请求示例：**

{"ivrid": "6500"}

**请求参数说明：**

1.不带参数时表示查询所有；

2.带参数表示查询单个或多个，多个时需用‘ , ’号隔开。如：{"ivrid": "6500,6501,6502"}。

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;ivrid&gt; | string | 查询单个或多个IVR | 6202 |

**响应示例：**

{"status":"Success","ivr":\[{"ivrnumber":"6500","ivrname":"6500","prompt":"\[Default\]","promptrepeat":"3","responsetimeout":"3","digittimeout":"3","dialext":"on","dialoutboundroutes":"off","dialtocheckvoicemail":"off"}\]}

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;ivrnumber&gt; | string | IVR号码 | 6500 |
| &lt;ivrname&gt; | string | IVR名称 | 6202 |
| \[prompt\] | string | IVR提示音 | \[Default\] |
| \[promptrepeat\] | string | 提示音播放次数 | 3 |
| \[responsetimeout\] | int | 响应超时时间 | 3 |
| \[digittimeout\] | int | 按键超时时间 | 5 |
| \[dialext\] | string | 允许从分机呼出 | on：开启 off：关闭 |
| \[dialoutboundroutes\] | string | 允许从呼出路由拨出 | on：开启 off：关闭 |
| \[selectedrouters\] | string | 所选择的路由 |  |
| \[dialtocheckvoicemail\] | string | 允许查阅语音留言 | on：开启 off：关闭 |

**可能出现的错误码：**10012，30001

