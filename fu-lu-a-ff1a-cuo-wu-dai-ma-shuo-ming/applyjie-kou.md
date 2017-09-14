# 应用（Apply）**接口**

使用API配置分机或者IVR等时，配置成功后会自动应用。为避免使用API配置时频繁应用出现应用不生效情况，用户可在统一配置完毕后，调用此接口统一应用一次。

**请求方式：**POST**  
请求地址：**[https://192.168.5.150:8088/api/{version}/apply?token=4444ed5e207395035e4ec29a6bf09ece](https://192.168.5.150:8088/api/{version}/apply?token=4444ed5e207395035e4ec29a6bf09ece)

**请求参数说明：    **

无参数，直接发送Apply请求即可。

**响应示例：**

{"status":"Success"}

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;status&gt; | string | apply结果 | Success或者Failed |



