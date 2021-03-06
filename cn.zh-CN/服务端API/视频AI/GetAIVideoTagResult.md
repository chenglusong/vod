# GetAIVideoTagResult {#doc_api_vod_GetAIVideoTagResult .reference}

调用GetAIVideoTagResult获取多模态内容理解结果。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=vod&api=GetAIVideoTagResult&type=RPC&version=2017-03-21)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|GetAIVideoTagResult|系统规定参数，取值：**GetAIVideoTagResult**。

 |
|MediaId|String|是|88c6ca184c0e47098a5b665exxxxx|视频ID。

 |
|AccessKeyId|String|否|your\_accesskey\_id|您的AccessKey ID。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|25818875-5F78-4A13-BEF6-D7393xxxxxx|请求ID。

 |
|VideoTagResult| | |结果数据。

 |
|Category| | |视频分类的集合。

 |
|Tag|String|美容|标签。

 |
|Keyword| | |关键词标签的集合。

 |
|Tag|String|气垫|标签。

 |
|Times| |\["3260","4000","5000","8410","12000","13000","14000"\]|时间点的集合。单位：毫秒。

 |
|Location| | |地点标签的集合。

 |
|Tag|String|亚洲|标签。

 |
|Times| |\["8410"\]|时间点的集合。单位：毫秒。

 |
|Person| | |人物标签的集合。

 |
|FaceUrl|String|http://example.test.com/aivideotag/663E7B7A-7E45-4CDD-AA92-D92A42XXXXX/Index\_00016.jpg|人脸URL。

 **说明：** 只有人物标签结果会返回该字段。

 |
|Tag|String|莉莉·柯林斯|标签。

 |
|Times| |\["10760"\]|时间点的集合。单位：毫秒。

 |
|Time| | |时间标签的集合。

 |
|Tag|String|毫秒|标签。

 |
|Times| |\["3260","4000","5000","8410","12000","13000","14000"\]|时间点的集合。单位：毫秒。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=GetAIVideoTagResult
&MediaId=88c6ca184c0e47098a5b665exxxxx
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<GetAIVideoTagResultResponse>
  <RequestId>25818875-5F78-4A13-BEF6-D7393xxxxxx</RequestId>
	  <VideoTagResult>
		    <Category>
			      <Tag>美容</Tag>
		    </Category>
		    <Keyword>
			      <Times>3260</Times>
			      <Times>4000</Times>
			      <Times>5000</Times>
			      <Times>8410</Times>
			      <Times>10000</Times>
			      <Times>12000</Times>
			      <Times>13000</Times>
			      <Times>14000</Times>
			      <Times>15000</Times>
			      <Tag>气垫</Tag>
		    </Keyword>
		    <Keyword>
			      <Times>3260</Times>
			      <Times>4000</Times>
			      <Times>5000</Times>
			      <Times>8410</Times>
			      <Times>12000</Times>
			      <Times>13000</Times>
			      <Times>14000</Times>
			      <Tag>兰蔻</Tag>
		    </Keyword>
		    <Keyword>
			      <Times>4000</Times>
			      <Times>5000</Times>
			      <Times>12000</Times>
			      <Times>13000</Times>
			      <Times>14000</Times>
			      <Times>15000</Times>
			      <Tag>CC霜</Tag>
		    </Keyword>
		    <Person>
			      <Times>10760</Times>
			      <Tag>莉莉·柯林斯</Tag>
			      <FaceUrl>http://example.test.com/aivideotag/663E7B7A-7E45-4CDD-AA92-D92A42XXXXX/Index_00016.jpg</FaceUrl>
		    </Person>
		    <Location>
			      <Times>8410</Times>
			      <Tag>亚洲</Tag>
		    </Location>
	  </VideoTagResult>
</GetAIVideoTagResultResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"25818875-5F78-4A13-BEF6-D7393xxxxxx",
	"VideoTagResult":{
		"Category":[
			{
				"Tag":"美容"
			}
		],
		"Keyword":[
			{
				"Tag":"气垫",
				"Times":[
					"3260",
					"4000",
					"5000",
					"8410",
					"10000",
					"12000",
					"13000",
					"14000",
					"15000"
				]
			},
			{
				"Tag":"兰蔻",
				"Times":[
					"3260",
					"4000",
					"5000",
					"8410",
					"12000",
					"13000",
					"14000"
				]
			},
			{
				"Tag":"CC霜",
				"Times":[
					"4000",
					"5000",
					"12000",
					"13000",
					"14000",
					"15000"
				]
			}
		],
		"Location":[
			{
				"Tag":"亚洲",
				"Times":[
					"8410"
				]
			}
		],
		"Person":[
			{
				"FaceUrl":"http://example.test.com/aivideotag/663E7B7A-7E45-4CDD-AA92-D92A42XXXXX/Index_00016.jpg",
				"Tag":"莉莉·柯林斯",
				"Times":[
					"10760"
				]
			}
		]
	}
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/vod)查看更多错误码。

