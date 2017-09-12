# 配置单个IVR

通过本接口进行单个配置IVR，如：配置IVR号码，名称等等。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/v1.0.0/ivr/update?token=6cad9cee6e2ad94570636e7b3690aeb2](https://192.168.5.150:8088/api/v1.0.0/ivr/update?token=6cad9cee6e2ad94570636e7b3690aeb2)

**请求示例：**

{"ivrid": "6500","ivrnumber":"6501"}

**请求参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;ivrid&gt; | string | 要配置的IVR唯一标识（IVR号码） | 6202 |
| \[ivrnumber\] | string | 修改后的IVR号码 | 6204 |
| \[ivrname\] | string | IVR名称 | 6202，限制:!$\(\)\/\#;,\"=&lt;&gt;&'\`^%@{}\|\（空字符也不行）最大31位，不为空 |
| \[promptrepeat\] | string | 提示音播放次数 | 范围：1,2,3,4,5 |
| \[responsetimeout\] | int | 响应超时时间 | 范围：1,2,3,4,5,6,7,8,9,10 |
| \[digittimeout\] | int | 按键超时时间 | 范围：1,2,3,4,5,6,7,8,9,10 |
| \[dialext\] | string | 允许从分机呼出 | on：开启 off：关闭 |
| \[dialtocheckvoicemail\] | string | 允许查阅语音留言 | on：开启 off：关闭 |

**响应示例：**

{"status":"Success"}

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;status&gt; | string | IVR设置结果 | Success或者Failed |



