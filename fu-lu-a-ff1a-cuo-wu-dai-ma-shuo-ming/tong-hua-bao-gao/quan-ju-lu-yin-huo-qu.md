# 全局录音获取

通过本接口可获取IPPBX中的全局录音文件。

**获取方法如下：**

通过CDR事件中的“recording”参数获取到全局录音文件名称，再通过获取到的名称从IPPBX获取有关该文件的一个随机串，再通过该随机串组合成下载播放该录音文件请求。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/v1.0.1/recording/get\_random?token=3efd4cd64e0d06e84a98230601428106](https://192.168.5.150:8088/api/v1.0.1/recording/get_random?token=3efd4cd64e0d06e84a98230601428106)

**请求示例：**

{"recording":"20170901181806-1504261084.7-1001-1003-Internal.wav"}

**请求参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;recording&gt; | string | 全局录音文件名称 | hello001 |

**响应示例：**

{"status":"Success","recording":"20170901181806-1504261084.7-1001-1003-Internal.wav","random":"120732c546381fb020f17fba676b0ea0"}

**响应参数：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;status&gt; | string | 配置结果 | Success或者Failed |
| &lt;recording&gt; | string | 全局录音文件名称 | hello001 |
| &lt;random&gt; | string | 有关全局录音文件的一个随机串。用户需要使用这个随机串组合成下载播放该录音文件请求 |  |

**Random组合方式示例：**

https://192.168.5.150:8088/api/v1.0.1/recording/download?recording=20170724103619-1500860177.268-2000-2001-Internal.wav&random=7e60c59d187783f06ccc03621c4ad736&token=75c5891b32203d0615f9e3753a7cb779

