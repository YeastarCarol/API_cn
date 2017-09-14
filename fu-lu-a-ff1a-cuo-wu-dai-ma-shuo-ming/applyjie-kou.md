# **Apply接口**

使用API配置分机或者IVR等时，配置会自动Apply，为避免配置时频繁Apply出现Apply不生效情况，用户可在统一配置完毕后，调用此接口统一Apply一次。

**请

**

**请求参数说明：

无参数，直接发送Apply请求即可。

**响应示例：**

{"status":"Success"}

**响应参数说明：**

| **参数名称** | **类型** | **参数说明** | **参数值举例** |
| :--- | :--- | :--- | :--- |
| **&lt; status&gt;** | String | apply结果 | Success或者Failed |


