# QueryTaskInfoHistory {#concept_s5f_vyk_c2b .concept}

分页查询自己账户下的域名任务历史列表。

## 请求参数 {#section_gdr_yqm_c2b .section}

公共请求参数，详见[公共参数](intl.zh-CN/API 参考/调用方式/公共参数.md#)。

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是|操作接口名，系统规定参数，取值：QueryTaskInfoHistory。|
|PageSize|Integer|是|分页大小。|
|BeginCreateTime|Long|否|创建日期范围查询开始时间，UTC时间1970年1月1日0点距离现在的毫秒数，目前只支持按天查询。|
|EndCreateTime|Long|否|创建日期范围查询结束时间，UTC时间1970年1月1日0点距离现在的毫秒数，目前只支持按天查询。|
|CreateTimeCursor|String|否|创建日期游标。|
|TaskNoCursor|String|否|任务光标，翻页时传入对应页游标中的任务编号。|

## 返回参数 {#section_wb5_crm_c2b .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|唯一请求识别码。|
|PageSize|Integer|分页大小。|
|CurrentPageCursor|[TaskInfoHistoryCurrentPageCursorType](#table_v3m_prm_c2b)|当前页游标。|
|NextPageCursor|[TaskInfoHistoryNextPageCursorType](#table_a1s_srm_c2b)|下一页游标。|
|PrePageCursor|[TaskInfoHistoryPrePageCursorType](#table_t4m_xrm_c2b)|上一页游标。|
|Objects|[TaskInfoHistoryType](#table_nzd_bsm_c2b)|任务信息。|

|类型|名称|描述|
|:-|:-|:-|
|String|TaskType|任务类型。枚举值范围： -   CHG\_HOLDER 修改所有者信息
-   CHG\_DNS 修改DNS
-   SET\_WHOIS\_PROTECT 设置隐私保护
-   UPDATE\_ADMIN\_CONTACT 修改管理者信息
-   UPDATE\_BILLING\_CONTACT 修改付费者信息
-   UPDATE\_TECH\_CONTACT 修改技术者信息
-   SET\_UPDATE\_PROHIBITED 设置域名安全锁
-   SET\_TRANSFER\_PROHIBITED 设置域名转移锁
-   ORDER\_ACTIVATE 创建注册订单
-   ORDER\_RENEW 创建续费订单
-   ORDER\_REDEEM 创建赎回订单
-   CREATE\_DNSHOST 创建DNS host
-   UPDATE\_DNSHOST 更新DNS host
-   UPDATE\_REGISTRANT\_CONTACT修改注册联系人
-   DELETE\_DOMAIN 删除域名
-   SYNC\_DNSHOST 同步DNS host

 |
|Integer|TaskNum|任务包含域名数量。|
|String|TaskStatus|任务状态。可能值： -   WAITING\_EXECUTE 等待执行
-   EXECUTING 执行中
-   COMPLETE 执行完成

 |
|String|TaskStatusCode|任务状态码。可能值： -   1 等待执行
-   2 执行中
-   3 执行完成

 |
|String|CreateTime|任务创建时间。|
|String|CreateTimeLong|任务创建时间。|
|String|Clientip|提交任务时用户IP。|
|String|TaskNo|任务编号。|
|String|TaskTypeDescription|任务类型描述。|

|类型|名称|描述|
|:-|:-|:-|
|String|TaskType|任务类型。枚举值范围： -   CHG\_HOLDER 修改所有者信息
-   CHG\_DNS 修改DNS
-   SET\_WHOIS\_PROTECT 设置隐私保护
-   UPDATE\_ADMIN\_CONTACT 修改管理者信息
-   UPDATE\_BILLING\_CONTACT 修改付费者信息
-   UPDATE\_TECH\_CONTACT 修改技术者信息
-   SET\_UPDATE\_PROHIBITED 设置域名安全锁
-   SET\_TRANSFER\_PROHIBITED 设置域名转移锁
-   ORDER\_ACTIVATE 创建注册订单
-   ORDER\_RENEW 创建续费订单
-   ORDER\_REDEEM 创建赎回订单
-   CREATE\_DNSHOST 创建DNS host
-   UPDATE\_DNSHOST 更新DNS host
-   UPDATE\_REGISTRANT\_CONTACT 修改注册联系人
-   DELETE\_DOMAIN 删除域名
-   SYNC\_DNSHOST 同步DNS host

 |
|Integer|TaskNum|任务包含域名数量。|
|String|TaskStatus|任务状态。可能值： -   WAITING\_EXECUTE 等待执行
-   EXECUTING 执行中
-   COMPLETE 执行完成

 |
|String|TaskStatusCode|任务状态码。可能值： -   1 等待执行
-   2 执行中
-   3 执行完成

 |
|String|CreateTime|任务创建时间。|
|String|CreateTimeLong|任务创建时间。|
|String|Clientip|提交任务时用户IP。|
|String|TaskNo|任务编号。|
|String|TaskTypeDescription|任务类型描述。|

|类型|名称|描述|
|:-|:-|:-|
|String|TaskType|任务类型。枚举值范围： -   CHG\_HOLDER 修改所有者信息
-   CHG\_DNS 修改DNS
-   SET\_WHOIS\_PROTECT 设置隐私保护
-   UPDATE\_ADMIN\_CONTACT 修改管理者信息
-   UPDATE\_BILLING\_CONTACT 修改付费者信息
-   UPDATE\_TECH\_CONTACT 修改技术者信息
-   SET\_UPDATE\_PROHIBITED 设置域名安全锁
-   SET\_TRANSFER\_PROHIBITED 设置域名转移锁
-   ORDER\_ACTIVATE 创建注册订单
-   ORDER\_RENEW 创建续费订单
-   ORDER\_REDEEM 创建赎回订单
-   CREATE\_DNSHOST 创建DNS host
-   UPDATE\_DNSHOST 更新DNS host
-   UPDATE\_REGISTRANT\_CONTACT修改注册联系人
-   DELETE\_DOMAIN 删除域名
-   SYNC\_DNSHOST 同步DNS host

 |
|Integer|TaskNum|任务包含域名数量。|
|String|TaskStatus|任务状态。可能值： -   WAITING\_EXECUTE 等待执行
-   EXECUTING 执行中
-   COMPLETE 执行完成

 |
|String|TaskStatusCode|任务状态码。可能值： -   1 等待执行
-   2 执行中
-   3 执行完成

 |
|String|CreateTime|任务创建时间。|
|String|CreateTimeLong|任务创建时间。|
|String|Clientip|提交任务时用户IP。|
|String|TaskNo|任务编号。|
|String|TaskTypeDescription|任务类型描述。|

|类型|名称|描述|
|:-|:-|:-|
|String|TaskType|任务类型。枚举值范围： -   CHG\_HOLDER 修改所有者信息
-   CHG\_DNS 修改DNS
-   SET\_WHOIS\_PROTECT 设置隐私保护
-   UPDATE\_ADMIN\_CONTACT 修改管理者信息
-   UPDATE\_BILLING\_CONTACT 修改付费者信息
-   UPDATE\_TECH\_CONTACT 修改技术者信息
-   SET\_UPDATE\_PROHIBITED 设置域名安全锁
-   SET\_TRANSFER\_PROHIBITED 设置域名转移锁
-   ORDER\_ACTIVATE 创建注册订单
-   ORDER\_RENEW 创建续费订单
-   ORDER\_REDEEM 创建赎回订单
-   CREATE\_DNSHOST 创建DNS host
-   UPDATE\_DNSHOST 更新DNS host
-   UPDATE\_REGISTRANT\_CONTACT 修改注册联系人
-   DELETE\_DOMAIN 删除域名
-   SYNC\_DNSHOST同步DNS host

 |
|Integer|TaskNum|任务包含域名数量。|
|String|TaskStatus|任务状态。可能值： -   WAITING\_EXECUTE 等待执行
-   EXECUTING 执行中
-   COMPLETE 执行完成

 |
|String|TaskStatusCode|任务状态码。可能值： -   1 等待执行
-   2 执行中
-   3 执行完成

 |
|String|CreateTime|任务创建时间。|
|String|CreateTimeLong|任务创建时间。|
|String|Clientip|提交任务时用户IP。|
|String|TaskNo|任务编号。|
|String|TaskTypeDescription|任务类型描述。|

## 错误码 {#section_ytj_3sm_c2b .section}

|错误代码|描述|HTTP状态码|语义|
|:---|:-|:------|:-|
|ParameterIllegal|Parameter illegal.|400|参数错误。|
|NetworkIOError|Network IO Error.|400|网络I/O异常。|

## 示例 {#section_vxg_lsm_c2b .section}

**请求示例**

``` {#codeblock_wyi_ozt_jbe}
http://domain-intl.aliyuncs.com/?Action=QueryTaskInfoHistory
&PageSize=2
&<公共请求参数>
```

**返回示例**

-   XML示例

    ``` {#codeblock_bi9_925_a0y}
    <?xml version='1.0' encoding='UTF-8'?>
    <QueryTaskInfoHistoryResponse>
        <Objects>
            <TaskInfoHistory>
                <Clientip>127.0.0.1</Clientip>
                <TaskNo>aa634d3f-927e-4d17-9d2c-test</TaskNo>
                <CreateTime>2017-11-01 17:22:51</CreateTime>
                <TaskStatus>COMPLETE</TaskStatus>
                <TaskNum>1</TaskNum>
                <TaskStatusCode>3</TaskStatusCode>
                <TaskType>CHG_DNS</TaskType>
                <CreateTimeLong>1509528171000</CreateTimeLong>
            </TaskInfoHistory>
            <TaskInfoHistory>
                <Clientip>127.0.0.1</Clientip>
                <TaskNo>f9baa3d5-33b9-4c81-8847-test</TaskNo>
                <CreateTime>2017-11-01 17:19:47</CreateTime>
                <TaskStatus>COMPLETE</TaskStatus>
                <TaskNum>15</TaskNum>
                <TaskStatusCode>3</TaskStatusCode>
                <TaskType>CHG_DNS</TaskType>
                <CreateTimeLong>1509527987000</CreateTimeLong>
            </TaskInfoHistory>
        </Objects>
        <PageSize>2</PageSize>
        <NextPageCursor>
            <TaskNo>8f112aa1-98be-48c3-82f8-test</TaskNo>
            <CreateTime>2017-10-27 13:07:07</CreateTime>
            <CreateTimeLong>1509080827000</CreateTimeLong>
        </NextPageCursor>
        <RequestId>EB3FCCBA-CA1F-4D31-9F34-test</RequestId>
        <CurrentPageCursor>
            <Clientip>127.0.0.1</Clientip>
            <TaskNo>aa634d3f-927e-4d17-9d2c-test</TaskNo>
            <CreateTime>2017-11-01 17:22:51</CreateTime>
            <TaskStatus>COMPLETE</TaskStatus>
            <TaskNum>1</TaskNum>
            <TaskStatusCode>3</TaskStatusCode>
            <TaskType>CHG_DNS</TaskType>
            <CreateTimeLong>1509528171000</CreateTimeLong>
        </CurrentPageCursor>
    </QueryTaskInfoHistoryResponse>
    ```

-   JSON示例

    ``` {#codeblock_web_dby_1hq}
    {
      "currentPageCursor": {
        "clientip": "127.0.0.1",
        "createTime": "2017-11-01 17:22:51",
        "createTimeLong": 1509528171000,
        "taskNo": "aa634d3f-927e-4d17-9d2c-test",
        "taskNum": 1,
        "taskStatus": "COMPLETE",
        "taskStatusCode": 3,
        "taskType": "CHG_DNS"
      },
      "nextPageCursor": {
        "createTime": "2017-10-27 13:07:07",
        "createTimeLong": 1509080827000,
        "taskNo": "8f112aa1-98be-48c3-82f8-test"
      },
      "objects": [
        {
          "clientip": "127.0.0.1",
          "createTime": "2017-11-01 17:22:51",
          "createTimeLong": 1509528171000,
          "taskNo": "aa634d3f-927e-4d17-9d2c-test",
          "taskNum": 1,
          "taskStatus": "COMPLETE",
          "taskStatusCode": 3,
          "taskType": "CHG_DNS"
        },
        {
          "clientip": "127.0.0.1",
          "createTime": "2017-11-01 17:19:47",
          "createTimeLong": 1509527987000,
          "taskNo": "f9baa3d5-33b9-4c81-8847-test",
          "taskNum": 15,
          "taskStatus": "COMPLETE",
          "taskStatusCode": 3,
          "taskType": "CHG_DNS"
        }
      ],
      "pageSize": 2,
      "prePageCursor": {},
      "requestId": "6EB5D9B8-AD99-4423-9D02-test"
    }
    ```


