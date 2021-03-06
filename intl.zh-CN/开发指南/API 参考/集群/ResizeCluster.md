# ResizeCluster {#concept_klf_nfb_kfb .concept}

根据配置扩容集群参数以及示例

## 请求参数 {#section_p5v_ffb_kfb .section}

|参数|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|ClusterId|String|是|C-D7958B72E59BAB88|集群 ID|
|RegionId|String|是|cn-hangzhou|区域ID|
|AccessKeyId|String|否|LTAI8ljWyu7y\*\*\*\*|AccessKeyId|
|HostGroup.N.AutoRenew|Boolean|否|false|针对包年包月，是否自动续费|
|HostGroup.N.ChargeType|String|否|PostPaid|机器组的机器付费类型|
|HostGroup.N.ClusterId|String|否|C-D7958B72E59BAB88|扩容集群 ID|
|HostGroup.N.Comment|String|否|0|保留字段|
|HostGroup.N.CreateType|String|否|0|保留字段|
|HostGroup.N.DiskCapacity|Integer|否|120|机器组的数据盘容量|
|HostGroup.N.DiskCount|Integer|否|4|机器组的数据盘数量|
|HostGroup.N.DiskType|String|否|CLOUD\_SSD|数据盘类型|
|HostGroup.N.HostGroupId|String|否|G-48E83B43E97111BE|待扩容的机器组 ID|
|HostGroup.N.HostGroupName|String|否|任务实例组|机器组名称|
|HostGroup.N.HostGroupType|String|否|TASK|机器组类型|
|HostGroup.N.HostKeyPairName|String|否|test-pair|机器组的密钥对名称，目前只针对 gateway 生效|
|HostGroup.N.HostPassword|String|否|pwd|机器组机器的密码，目前只针对 gateway 生效|
|HostGroup.N.InstanceType|String|否|ecs.mn4.2xlarge|机器组机器类型|
|HostGroup.N.NodeCount|Integer|否|1|机器组节点数|
|HostGroup.N.Period|Integer|否|30|机器组的包年包月时间（天）|
|HostGroup.N.SysDiskCapacity|Integer|否|120|系统盘容量|
|HostGroup.N.SysDiskType|String|否|SSD\_CLOUD|系统盘类型|
|HostGroup.N.VswitchId|Integer|否|0|虚拟交换机 ID|
|VswitchId|String|否|vsw-bp10tvjyc77psy0z5h0ni|虚拟交换机|

## 返回参数 {#section_vdw_lv4_dgb .section}

|字段|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|BF4FBAC6-B03E-4BFB-B6DB-EB53C34F2E22|请求 ID|
|ClusterId|String|C-D7958B72E59BAB88|集群 ID|

## 示例 {#section_ydw_lv4_dgb .section}

-   请求示例

    ```
    /?ClusterId=C-D7958B72E59BAB88
    &RegionId=cn-hangzhou
    &AccessKeyId=LTAI8ljWyu7y****
    &VswitchId=vsw-bp10tvjyc77psy0z5h0ni
    &HostGroup.1.AutoRenew=
    &HostGroup.1.ChargeType=PostPaid
    &HostGroup.1.ClusterId=
    &HostGroup.1.Comment=
    &HostGroup.1.CreateType=
    &HostGroup.1.DiskCapacity=120
    &HostGroup.1.DiskCount=4
    &HostGroup.1.DiskType=CLOUD_SSD
    &HostGroup.1.HostGroupId=
    &HostGroup.1.HostGroupName=任务实例组
    &HostGroup.1.HostGroupType=TASK
    &HostGroup.1.HostKeyPairName=
    &HostGroup.1.HostPassword=
    &HostGroup.1.InstanceType=ecs.mn4.2xlarge
    &HostGroup.1.1odeCount=1
    &HostGroup.1.Period=30
    &HostGroup.1.SysDiskCapacity=
    &HostGroup.1.SysDiskType=
    &HostGroup.1.VswitchId=
    &<公共请求参数>
    ```

-   正常返回示例

    JSON 格式

    ```
    {
    	"ClusterId":"C-D7958B72E59BAB88",
    	"RequestId":"BF4FBAC6-B03E-4BFB-B6DB-EB53C34F2E22"
    }
    ```

-   异常返回示例

    JSON 格式

    ```
    {
    	"code":"RAM.Permission.NotAllow",
    	"message":"It is not allow to execute this operation,please use RAM to authorize!",
    	"requestId":"9AEDC439-1F63-491D-B8C6-9737C372BF3A",
    	"successResponse":false
    }
    ```


## 错误码 {#section_a2w_lv4_dgb .section}

[查看本产品错误码](https://error-center.alibabacloud.com/status/product/Emr)

