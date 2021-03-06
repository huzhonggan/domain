# QueryDomainList {#concept_pky_ryk_c2b .concept}

QueryDomainList：分页查询自己账户下的域名列表。

## 请求参数 {#section_zcp_r3m_c2b .section}

公共请求参数，详见[公共参数](intl.zh-CN/API 参考/调用方式/公共参数.md#)。

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是|操作接口名，系统规定参数，取值：QueryDomainList。|
|PageNum|Integer|是|分页页码。|
|PageSize|Integer|是|分页大小。|
|OrderKeyType|String|否|排序字段，枚举值范围：RegistrationDate 根据注册时间排序；ExpirationDate 根据到期时间排序。不传此参数默认入库时间排序。|
|OrderByType|String|否|排序顺序，枚举值范围：ASC 升序；DESC 倒序。不传此参数默认为DESC。|
|StartRegistrationDate|Long|否|注册日期范围查询开始时间，UTC时间1970年1月1日0点距离现在的毫秒数，目前只支持按天查询。|
|EndRegistrationDate|Long|否|注册日期范围查询结束时间，UTC时间1970年1月1日0点距离现在的毫秒数，目前只支持按天查询。|
|StartExpirationDate|Long|否|到期日期范围查询开始时间，UTC时间1970年1月1日0点距离现在的毫秒数，目前只支持按天查询。|
|EndExpirationDate|Long|否|到期日期范围查询结束时间，UTC时间1970年1月1日0点距离现在的毫秒数，目前只支持按天查询。|
|Lang|String|否|语言，枚举值范围：en 英文；zh 中文。不传此参数默认en。|
|DomainName|String|否|域名搜索。|
|ProductDomainType|String|否|域名类型，枚举值范围：New gTLD；gTLD；ccTLD。|
|QueryType|String|否|列表查询类型，枚举值范围：1 急需续费类别；2 急需赎回列表。|

## 返回参数 {#section_dfj_djm_c2b .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|唯一请求识别码。|
|TotalItemNum|Integer|域名总数。|
|CurrentPageNum|Integer|当前页码。|
|TotalPageNum|Integer|总页数。|
|PageSize|Integer|分页大小。|
|PrePage|Boolean|是否有上一页。|
|NextPage|Boolean|是否有下一页。|
|Data|[DomainInfoType](#table_kt3_3jm_c2b)|域名列表。|

|名称|类型|描述|
|:-|:-|:-|
|DomainName|String|域名。|
|InstanceId|String|实例编号。|
|RegistrationDate|String|注册时间。|
|RegistrationDateLong|Long|注册时长，UTC时间1970年1月1日0点距离注册时间的毫秒数。|
|ExpirationDate|String|域名到期日期。|
|ExpirationDateLong|Long|域名到期时长，UTC时间1970年1月1日0点距离域名到期日的毫秒数。|
|DomainStatus|String|域名状态。枚举值范围：1 急需续费；2 急需赎回；3 正常|
|DomainType|String|域名类型。枚举值范围：New gTLD；gTLD；ccTLD|
|Premium|Boolean|是否是溢价域名。|
|ProductId|String|产品ID。|

## 错误码 {#section_upg_rjm_c2b .section}

|错误代码|描述|HTTP状态码|语义|
|:---|:-|:------|:-|
|ParameterIllegal|Parameter illegal.|400|参数错误。|
|NetworkIOError|Network IO Error.|400|网络I/O异常。|

## 示例 {#section_vts_wjm_c2b .section}

**请求示例**

``` {#codeblock_4q6_x4v_o2z}
http://domain-intl.aliyuncs.com/?Action=QueryDomainList
&PageNum=1&PageSize=10
&<公共请求参数>
```

**返回示例**

-   XML示例

    ``` {#codeblock_b4y_99y_zaj}
    <?xml version='1.0' encoding='UTF-8'?>
    <QueryDomainListResponse>
        <Data>
            <Domain>
                <ExpirationDate>Nov 02,2019 04:00:45</expirationDate>
                <InstanceId>ST20151102120031118</SaleId>
                <RegistrationDate>Nov 02,2017 04:00:45</registrationDate>
                <DomainName>test.com</DomainName>
                <DomainType>gTLD</domainType>
            </Domain>
        </Data>
        <TotalItemNum>1</TotalItemNum>
        <PageSize>5</PageSize>
        <CurrentPageNum>0</CurrentPageNum>
        <RequestId>B7AB5469-5E38-4AA9-A920-C65B7A9C8E6E</RequestId>
        <PrePage>false</PrePage>
        <TotalPageNum>1</TotalPageNum>
        <NextPage>false</NextPage>
    </QueryDomainListResponse>
    ```

-   JSON示例

    ``` {#codeblock_fin_is1_opk}
    {
      "Data": {
        "Domain": [
          {
            "ExpirationDate": "Nov 02,2019 04:00:45",
            "InstanceId": "ST2015110212003800001928",
            "RegistrationDate": "Nov 02,2017 04:00:45",
            "DomainName": "fds234sdf.net",
            "DomainType": "gTLD"
          }
        ]
      },
      "TotalItemNum": 1,
      "PageSize": 5,
      "CurrentPageNum": 0,
      "RequestId": "77F90DA6-89AB-4074-80F3-E595CB57DF98",
      "PrePage": false,
      "TotalPageNum": 1,
      "NextPage": false
    }
    ```


