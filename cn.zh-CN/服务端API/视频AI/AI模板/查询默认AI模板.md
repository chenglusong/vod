# 查询默认AI模板

查询默认AI模板。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=vod&api=GetDefaultAITemplate&type=RPC&version=2017-03-21)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|GetDefaultAITemplate|系统规定参数，取值：**GetDefaultAITemplate**。 |
|TemplateType|String|是|AIMediaAudit|模板类型，取值：**AIMediaAudit\(智能审核\)**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|A017F1DE-3DC3-4441-\*\*\*\*-37E81113C10F|请求ID。 |
|TemplateInfo|Struct| |AI模板信息。 |
|CreationTime|String|2020-07-08T06:50:45Z|创建时间。 |
|IsDefault|String|Default|是否默认。取值：**Default**\(是\)，**NotDefault**\(否\)。 |
|ModifyTime|String|2020-07-08T07:05:49Z|修改时间。 |
|Source|String|Custom|模板来源：

 -   System：系统
-   Custom：自定义 |
|TemplateConfig|String|\{"AuditRange":\["text-title","video"\],"AuditContent":\["screen"\],"AuditItem":\["terrorism","porn"\],"AuditAutoBlock":"yes"\}|模板详细配置。JSON字符串，详见[AITemplateConfig](~~89863#title-vd3-499-o36~~)。 |
|TemplateId|String|1706a0063dd733f6a823e83\*\*\*\*5879e|模板ID。 |
|TemplateName|String|DemoAITemplate|模板名称。 |
|TemplateType|String|AIMediaAudit|模板类型。 |

**说明：** 下述请求示例中的“公共请求参数”详情，参见[公共参数说明文档](~~44432~~)。

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=GetDefaultAITemplate
&TemplateType=AIMediaAudit
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<GetDefaultAITemplateResponse>
  <TemplateInfo>
        <IsDefault>Default</IsDefault>
        <ModifyTime>2020-07-08T07:05:49Z</ModifyTime>
        <CreationTime>2020-07-08T06:50:45Z</CreationTime>
        <TemplateName>DemoAITemplate</TemplateName>
        <TemplateConfig>
              <AuditRange>text-title</AuditRange>
              <AuditRange>video</AuditRange>
              <AuditContent>screen</AuditContent>
              <AuditItem>terrorism</AuditItem>
              <AuditItem>porn</AuditItem>
              <AuditAutoBlock>yes</AuditAutoBlock>
        </TemplateConfig>
        <TemplateType>AIMediaAudit</TemplateType>
        <Source>Custom</Source>
        <TemplateId>1706a0063dd733f6a823e83****5879e</TemplateId>
  </TemplateInfo>
  <RequestId>A017F1DE-3DC3-4441-****-37E81113C10F</RequestId>
</GetDefaultAITemplateResponse>
```

`JSON` 格式

```
{
	"TemplateInfo": {
		"IsDefault": "Default",
		"ModifyTime": "2020-07-08T07:05:49Z",
		"CreationTime": "2020-07-08T06:50:45Z",
		"TemplateName": "DemoAITemplate",
		"TemplateConfig": {
			"AuditRange": [
				"text-title",
				"video"
			],
			"AuditContent": [
				"screen"
			],
			"AuditItem": [
				"terrorism",
				"porn"
			],
			"AuditAutoBlock": "yes"
		},
		"TemplateType": "AIMediaAudit",
		"Source": "Custom",
		"TemplateId": "1706a0063dd733f6a823e83****5879e"
	},
	"RequestId": "A017F1DE-3DC3-4441-****-37E81113C10F"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/vod)查看更多错误码。

## SDK示例

建议使用 [服务端SDK](~~101789~~) 来调用API，此API各语言调用的示例代码，请参考如下：

-   [Java](~~100692#GetDefaultAITemplate~~)
-   [Python](~~101181#GetDefaultAITemplate~~)
-   [PHP](~~101159#GetDefaultAITemplate~~)
-   [.NET](~~100844#GetDefaultAITemplate~~)
-   [Node.js](~~101564#GetDefaultAITemplate~~)
-   [Go](~~101575#GetDefaultAITemplate~~)
-   [C/C++](~~102987#GetDefaultAITemplate~~)

