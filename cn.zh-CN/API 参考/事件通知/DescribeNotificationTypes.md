# DescribeNotificationTypes {#concept_71117_zh .concept}

查询弹性伸缩事件及资源变化通知类型（`DescribeNotificationTypes`）。

## 请求参数 { .section}

|名称|类型|是否必选|描述|
|:-|:-|:---|:-|
|Action|String|是|系统规定参数。取值：DescribeNotificationTypes。|

## 返回参数 { .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|请求 ID。|
|NotificationTypes|Array of [NotificationTypeSet](#hxfour)|弹性伸缩事件及资源变化通知类型列表。|

## NotificationTypeSet {#hxfour .section}

|名称|类型|描述|
|:-|:-|:-|
|NotificationType|String|弹性伸缩事件及资源变化通知类型。可能值：-   AUTOSCALING:SCALE\_OUT\_SUCCESS：成功的弹性扩张活动
-   AUTOSCALING:SCALE\_IN\_SUCCESS：成功的弹性收缩活动
-   AUTOSCALING:SCALE\_OUT\_ERROR：失败的弹性扩张活动
-   AUTOSCALING:SCALE\_IN\_ERROR：失败的弹性收缩活动
-   AUTOSCALING:SCALE\_REJECT：拒绝弹性伸缩活动
-   AUTOSCALING:SCALE\_OUT\_START：开始扩张活动
-   AUTOSCALING:SCALE\_IN\_START：开始收缩活动
-   AUTOSCALING:SCHEDULE\_TASK\_EXPIRING：定时任务到期

|

## 示例 { .section}

请求示例

```
http://ess.aliyuncs.com/?Action=DescribeNotificationTypes
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeNotificationTypesResponse>
    <RequestId>21F638C3-7054-4C1E-A143-A74C20F507A3</RequestId>
    <NotificationTypes>
        <NotificationType>AUTOSCALING:SCALE_OUT_SUCCESS</NotificationType>
        <NotificationType>AUTOSCALING:SCALE_IN_SUCCESS</NotificationType>
        <NotificationType>AUTOSCALING:SCALE_OUT_ERROR</NotificationType>
        <NotificationType>AUTOSCALING:SCALE_IN_ERROR</NotificationType>
        <NotificationType>AUTOSCALING:SCALE_REJECT</NotificationType>
    </NotificationTypes>
</DescribeNotificationTypesResponse>
```

`JSON` 格式

```
{
    "notificationTypes": [
        "AUTOSCALING:SCALE_OUT_SUCCESS",
        "AUTOSCALING:SCALE_IN_SUCCESS",
        "AUTOSCALING:SCALE_OUT_ERROR",
        "AUTOSCALING:SCALE_IN_ERROR",
        "AUTOSCALING:SCALE_REJECT"
    ],
    "requestId": "21F638C3-7054-4C1E-A143-A74C20F507A3"
}
```

