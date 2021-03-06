# DescribeCluster {#concept_gcm_ydb_kfb .concept}

查询集群的基本信息，包括：付费、ECS 机器概况、E-MapReduce 服务列表等。

## 请求参数 {#section_u3c_m2b_kfb .section}

|参数|类型|是否必须|示例值|描述|
|--|--|----|---|--|
|Id|String|是|C-E331B8AC12BF5DB4|集群 ID|
|RegionId|String|是|cn-hangzhou|区域|
|AccessKeyId|String|否|LTAI8ljWyu7y\*\*\*\*|AccessKeyId|

## 返回参数 {#section_vdw_lv4_dgb .section}

|字段|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|14E9C045-9B8D-4D1E-8D23-FC0027B6D947|请求 ID|
|ClusterInfo| | |集群详情|
|Id|String|C-E331B8AC12BF5DB4|集群 ID|
|RegionId|String|cn-hangzhou|区域|
|ZoneId|String|cn-hangzhou-b|可用区 ID|
|Name|String|cluster\_name|集群名|
|RelateClusterId|String|C-D7958B72E59BAB88|针对 gateway， 关联的主集群 ID|
|GatewayClusterIds|String|C-D7958B72E59BAB88|包含的 gateway 集群 Id|
|CreateType|String|MANUAL|集群创建的方式|
|StartTime|Long|1543804234000|集群启动时间（时间戳）|
|ExpiredTime|Long|1544076205000|包年包月集群的过期时间|
|StopTime|Long|1543804234000|集群停止时间|
|LogEnable|Boolean|true|是否打开集群 OSS日志|
|LogPath|String|oss://bucketname/path|集群 OSS 日志路径|
|UserId|String|125046002175\*\*\*\*|用户 ID|
|Status|String|IDLE|集群状态|
|HighAvailabilityEnable|Boolean|true|是否高可用集群|
|LocalMetaDb|Boolean|true|是否使用 Hive 本地元数据库|
|ChargeType|String|PostPaid|付费方式|
|DepositType|String|HALF\_MANAGED|集群托管方式|
|Period|Integer|36|包年包月时长\(天\)|
|RunningTime|Integer|1102|已经运行的时间\(秒数\)|
|MasterNodeTotal|Integer|2|Master 节点总数|
|MasterNodeInService|Integer|2|使用中的 Master 节点数|
|CoreNodeTotal|Integer|3|Core 节点总数|
|CoreNodeInService|Integer|3|使用中的 Core 节点数|
|TaskNodeTotal|Integer|2|Task 节点总数|
|TaskNodeInService|Integer|2|使用中的 Task 节点数|
|ShowSoftwareInterface|Boolean|true|是否展示快捷链接页面|
|CreateResource|String|ECM\_EMR|集群标记，无需关注|
|VpcId|String|vpc-bp1l4urd87xlh7i4bju4h|VPC ID|
|VSwitchId|String|vsw-bp11qjbyggil4pow064fg|虚拟交换机 ID|
|NetType|String|vpc|集群网络类型|
|UserDefinedEmrEcsRole|String|AliyunEmrEcsDefaultRole|使用的 EMR 权限名|
|IoOptimized|Boolean|true|是否 IO 优化|
|InstanceGeneration|String|ecs-3|ECS 分代|
|ImageId|String|m-bp118knl07yk88y8s6cj|创建集群使用的镜像 ID|
|SecurityGroupId|String|sg-bp1bvompzxgx7q0lg7oy|安全组 ID|
|SecurityGroupName|String|emr-default-securitygroup|安全组名|
|BootstrapFailed|Boolean|false|引导操作执行结果|
|Configurations|String|\[\]|无需填写|
|EasEnable|Boolean|true|是否高安全集群|
|AutoScalingEnable|Boolean|false|是否开启弹性扩容|
|AutoScalingAllowed|Boolean|false|允许弹性扩容|
|AutoScalingSpotWithLimitAllowed|Boolean|false|是否允许使用弹性伸缩竞价实例|
|ResizeDiskEnable|Boolean|true|是否允许扩容磁盘|
|GatewayClusterInfoList| | |Gateway 集群概况信息|
|ClusterId|String|C-D7958B72E59BAB88|Gateway集群 ID|
|ClusterName|String|gateway-name|Gateway 集群名|
|HostGroupList| | |集群机器组列表|
|HostGroupId|String|G-9D08642FB8CE8CFE|机器组 ID|
|HostGroupName|String|主实例组|机器组名称|
|HostGroupType|String|CORE|机器组角色|
|HostGroupSubType|String|0|保留字段|
|HostGroupChangeType|String|PostPaid|机器组的付费类型|
|hostGroupChangeStatus|String|0|保留字段|
|ChargeType|String|PostPaid|付费类型|
|Period|String|30|包年包月时间（天）|
|NodeCount|Integer|4|机器组节点数|
|InstanceType|String|ecs.n4.2xlarge|机器组实例类型|
|CpuCore|Integer|16|CPU 核心数|
|MemoryCapacity|Integer|16|内存大小|
|DiskType|String|CLOUD\_SSD|数据盘磁盘类型|
|DiskCapacity|Integer|120|数据盘容量|
|DiskCount|Integer|4|数据盘数量|
|BandWidth|String|10|带宽|
|LockType|String|0|保留字段|
|LockReason|String|0|保留字段|
|Nodes| | |机器节点|
|ZoneId|String|cn-hangzhou-e|可用区|
|InstanceId|String|i-bp1ftve3lzvpm16hp7lo|ECS 实例 ID|
|Status|String|NORMAL|状态|
|PubIp|String|47.99.162.57|公网 IP|
|InnerIp|String|192.168.128.236|内网 IP|
|ExpiredTime|String|2099-12-31T15:59Z|超时时间|
|CreateTime|String|1543804242000|创建时间|
|EmrExpiredTime|String|2099-12-31T15:59Z|EMR 超时时间|
|DaemonInfos| | |保留字段|
|Name|String|0|保留字段|
|DiskInfos| | |磁盘信息|
|Device|String|/dev/xvdb|磁盘设备信息|
|DiskName|String1|disk1|磁盘名|
|DiskId|String|d-bp15vg2nr3x2t0f37ko9|磁盘 ID|
|Type|String|data|磁盘类型|
|Size|Integer|80|磁盘容量（G）|
|BootstrapActionList| | |引导操作列表|
|Name|String|action\_name|引导操作的名字|
|Path|String|oss://bucket/path|引导操作脚本路径|
|Arg|String|--a|引导操作的参数|
|RelateClusterInfo| | |针对 gateway, 关联的主集群信息|
|ClusterId|String|C-D7958B72E59BAB88|关联集群 ID|
|ClusterName|String|main|关联集群名称|
|FailReason| | |集群创建失败的原因|
|ErrorCode|String|InvalidImageId.NotFound|创建失败错误码|
|ErrorMsg|String|The specified ImageId does not exist.|创建失败错误信息|
|RequestId|String|B8DC3A91-3953-4444-92BB-DBC29C47EC1A|创建集群请求 ID|
|SoftwareInfo| | |服务列表|
|EmrVer|String|EMR-3.16.0|EMR 版本号|
|ClusterType|String|HADOOP|集群类型|
|Softwares| | |服务列表|
|DisplayName|String|Hive|服务名称|
|Name|String|HIVE|服务内部名称|
|OnlyDisplay|Boolean|false|是否展现|
|StartTpe|Integer|1|启动类型|
|Version|String|2.3.3|服务版本|
|AccessInfo| | |集群连接信息|
|ZKLinks| | |ZooKeeper 连接信息|
|Link|String|emr-worker-1,emr-header-2,emr-header-1|ZooKeeper 连接地址|
|Port|String|2181|ZooKeeper 连接端口|

## 示例 {#section_ydw_lv4_dgb .section}

-   请求示例

    ```
    /?Id=C-E331B8AC12BF5DB4
    &RegionId=cn-hangzhou
    &AccessKeyId=LTAI8ljWyu7y****
    &<公共请求参数>
    ```

-   正常返回示例

    JSON 格式

    ```
    {
    	"code":"200",
    	"data":{
    		"ClusterInfo":{
    			"AutoScalingAllowed":true,
    			"AutoScalingEnable":false,
    			"AutoScalingSpotWithLimitAllowed":true,
    			"BootstrapActionList":{
    				"BootstrapAction":[]
    			},
    			"BootstrapFailed":false,
    			"ChargeType":"PostPaid",
    			"Configurations":"",
    			"CoreNodeInService":2,
    			"CoreNodeTotal":2,
    			"CreateResource":"ECM_EMR",
    			"CreateType":"MANUAL",
    			"EasEnable":true,
    			"GatewayClusterInfoList":{
    				"GatewayClusterInfo":[]
    			},
    			"HighAvailabilityEnable":true,
    			"HostGroupList":{
    				"HostGroup":[
    					{
    						"ChargeType":"PostPaid",
    						"CpuCore":8,
    						"DiskCapacity":80,
    						"DiskCount":1,
    						"DiskType":"CLOUD_SSD",
    						"HostGroupId":"G-79AA94922DFBE2E2",
    						"HostGroupName":"主实例组",
    						"HostGroupType":"MASTER",
    						"InstanceType":"ecs.n4.2xlarge",
    						"MemoryCapacity":16,
    						"NodeCount":2,
    						"Nodes":{
    							"Node":[
    								{
    									"CreateTime":"1543804242000",
    									"DaemonInfos":{
    										"DaemonInfo":[]
    									},
    									"DiskInfos":{
    										"DiskInfo":[
    											{
    												"Device":"/dev/xvdb",
    												"DiskId":"d-bp15vg2nr3x2t0f37ko9",
    												"Size":80,
    												"Type":"data"
    											},
    											{
    												"Device":"/dev/xvda",
    												"DiskId":"d-bp16c7qipsxtrq97mybg",
    												"Size":120,
    												"Type":"system"
    											}
    										]
    									},
    									"EmrExpiredTime":"null",
    									"ExpiredTime":"2099-12-31T15:59Z",
    									"InnerIp":"192.168.128.235",
    									"InstanceId":"i-bp16c7qipsxtrq99ixt2",
    									"PubIp":"47.97.214.105",
    									"Status":"NORMAL",
    									"ZoneId":"cn-hangzhou-b"
    								},
    								{
    									"CreateTime":"1543804242000",
    									"DaemonInfos":{
    										"DaemonInfo":[]
    									},
    									"DiskInfos":{
    										"DiskInfo":[
    											{
    												"Device":"/dev/xvdb",
    												"DiskId":"d-bp1568nnv4ev81672qe6",
    												"Size":80,
    												"Type":"data"
    											},
    											{
    												"Device":"/dev/xvda",
    												"DiskId":"d-bp16z8pr0y2vgfkghuba",
    												"Size":120,
    												"Type":"system"
    											}
    										]
    									},
    									"EmrExpiredTime":"null",
    									"ExpiredTime":"2099-12-31T15:59Z",
    									"InnerIp":"192.168.128.236",
    									"InstanceId":"i-bp1ftve3lzvpm16hp7lo",
    									"PubIp":"47.99.162.57",
    									"Status":"NORMAL",
    									"ZoneId":"cn-hangzhou-b"
    								}
    							]
    						}
    					},
    					{
    						"ChargeType":"PostPaid",
    						"CpuCore":8,
    						"DiskCapacity":80,
    						"DiskCount":4,
    						"DiskType":"CLOUD_SSD",
    						"HostGroupId":"G-9D08642FB8CE8CFE",
    						"HostGroupName":"核心实例组",
    						"HostGroupType":"CORE",
    						"InstanceType":"ecs.n4.2xlarge",
    						"MemoryCapacity":16,
    						"NodeCount":2,
    						"Nodes":{
    							"Node":[
    								{
    									"CreateTime":"1543804244000",
    									"DaemonInfos":{
    										"DaemonInfo":[]
    									},
    									"DiskInfos":{
    										"DiskInfo":[
    											{
    												"Device":"/dev/xvde",
    												"DiskId":"d-bp1568nnv4ev81672qe5",
    												"Size":80,
    												"Type":"data"
    											},
    											{
    												"Device":"/dev/xvdd",
    												"DiskId":"d-bp1967p3xp86y3wiudgq",
    												"Size":80,
    												"Type":"data"
    											},
    											{
    												"Device":"/dev/xvdc",
    												"DiskId":"d-bp11qsh4zwrwup8jm9rr",
    												"Size":80,
    												"Type":"data"
    											},
    											{
    												"Device":"/dev/xvdb",
    												"DiskId":"d-bp1d1juyl8z8aeuza9co",
    												"Size":80,
    												"Type":"data"
    											},
    											{
    												"Device":"/dev/xvda",
    												"DiskId":"d-bp1ftve3lzvpm16i37y1",
    												"Size":80,
    												"Type":"system"
    											}
    										]
    									},
    									"EmrExpiredTime":"null",
    									"ExpiredTime":"2099-12-31T15:59Z",
    									"InnerIp":"192.168.128.237",
    									"InstanceId":"i-bp1gyhphkjplgljrsw5f",
    									"PubIp":"",
    									"Status":"NORMAL",
    									"ZoneId":"cn-hangzhou-b"
    								},
    								{
    									"CreateTime":"1543804247000",
    									"DaemonInfos":{
    										"DaemonInfo":[]
    									},
    									"DiskInfos":{
    										"DiskInfo":[
    											{
    												"Device":"/dev/xvde",
    												"DiskId":"d-bp12zhcmd96101qhz8ko",
    												"Size":80,
    												"Type":"data"
    											},
    											{
    												"Device":"/dev/xvdd",
    												"DiskId":"d-bp13rttoh3l1gj84gcas",
    												"Size":80,
    												"Type":"data"
    											},
    											{
    												"Device":"/dev/xvdc",
    												"DiskId":"d-bp1cnruigppe54k6fx18",
    												"Size":80,
    												"Type":"data"
    											},
    											{
    												"Device":"/dev/xvdb",
    												"DiskId":"d-bp1967p3xp86y3wiudgr",
    												"Size":80,
    												"Type":"data"
    											},
    											{
    												"Device":"/dev/xvda",
    												"DiskId":"d-bp1ik6bdp8fpsr8zsebj",
    												"Size":80,
    												"Type":"system"
    											}
    										]
    									},
    									"EmrExpiredTime":"null",
    									"ExpiredTime":"2099-12-31T15:59Z",
    									"InnerIp":"192.168.128.238",
    									"InstanceId":"i-bp1ftve3lzvpm16hp7lp",
    									"PubIp":"",
    									"Status":"NORMAL",
    									"ZoneId":"cn-hangzhou-b"
    								}
    							]
    						}
    					}
    				]
    			},
    			"Id":"C-E331B8AC12BF5DB4",
    			"ImageId":"m-bp118knl07yk88y8s6cj",
    			"IoOptimized":true,
    			"LocalMetaDb":true,
    			"MasterNodeInService":2,
    			"MasterNodeTotal":0,
    			"Name":"df-test-safe",
    			"NetType":"vpc",
    			"RegionId":"cn-hangzhou",
    			"ResizeDiskEnable":true,
    			"RunningTime":1102,
    			"SecurityGroupId":"sg-bp1bvompzxgx7q0lg7oy",
    			"SecurityGroupName":"emr-default-securitygroup",
    			"ShowSoftwareInterface":false,
    			"SoftwareInfo":{
    				"ClusterType":"HADOOP",
    				"EmrVer":"EMR-3.16.0_pre",
    				"Softwares":{
    					"Software":[
    						{
    							"DisplayName":"HDFS",
    							"Name":"HDFS",
    							"OnlyDisplay":false,
    							"StartTpe":1,
    							"Version":"2.7.2-1.3.2"
    						},
    						{
    							"DisplayName":"YARN",
    							"Name":"YARN",
    							"OnlyDisplay":false,
    							"StartTpe":1,
    							"Version":"2.7.2-1.3.2"
    						},
    						{
    							"DisplayName":"Hive",
    							"Name":"HIVE",
    							"OnlyDisplay":false,
    							"StartTpe":1,
    							"Version":"2.3.3-1.0.3"
    						},
    						{
    							"DisplayName":"Ganglia",
    							"Name":"GANGLIA",
    							"OnlyDisplay":false,
    							"StartTpe":1,
    							"Version":"3.7.2"
    						},
    						{
    							"DisplayName":"Zookeeper",
    							"Name":"ZOOKEEPER",
    							"OnlyDisplay":false,
    							"StartTpe":1,
    							"Version":"3.4.13"
    						},
    						{
    							"DisplayName":"Spark",
    							"Name":"SPARK",
    							"OnlyDisplay":false,
    							"StartTpe":1,
    							"Version":"2.3.2-1.0.1"
    						},
    						{
    							"DisplayName":"HBase",
    							"Name":"HBASE",
    							"OnlyDisplay":false,
    							"StartTpe":1,
    							"Version":"1.1.1-1.0.2"
    						},
    						{
    							"DisplayName":"HUE",
    							"Name":"HUE",
    							"OnlyDisplay":false,
    							"StartTpe":1,
    							"Version":"4.1.0"
    						},
    						{
    							"DisplayName":"Zeppelin",
    							"Name":"ZEPPELIN",
    							"OnlyDisplay":false,
    							"StartTpe":1,
    							"Version":"0.8.0"
    						},
    						{
    							"DisplayName":"Tez",
    							"Name":"TEZ",
    							"OnlyDisplay":false,
    							"StartTpe":1,
    							"Version":"0.9.1-1.0.2"
    						},
    						{
    							"DisplayName":"Presto",
    							"Name":"PRESTO",
    							"OnlyDisplay":false,
    							"StartTpe":1,
    							"Version":"0.208"
    						},
    						{
    							"DisplayName":"Sqoop",
    							"Name":"SQOOP",
    							"OnlyDisplay":false,
    							"StartTpe":1,
    							"Version":"1.4.7-1.0.0"
    						},
    						{
    							"DisplayName":"Pig",
    							"Name":"PIG",
    							"OnlyDisplay":false,
    							"StartTpe":1,
    							"Version":"0.14.0"
    						},
    						{
    							"DisplayName":"ApacheDS",
    							"Name":"APACHEDS",
    							"OnlyDisplay":false,
    							"StartTpe":1,
    							"Version":"2.0.0"
    						},
    						{
    							"DisplayName":"HAS",
    							"Name":"HAS",
    							"OnlyDisplay":false,
    							"StartTpe":1,
    							"Version":"1.1.1"
    						},
    						{
    							"DisplayName":"Knox",
    							"Name":"KNOX",
    							"OnlyDisplay":false,
    							"StartTpe":1,
    							"Version":"0.13.0-0.0.3"
    						}
    					]
    				}
    			},
    			"StartTime":1543804234000,
    			"Status":"IDLE",
    			"TaskNodeInService":0,
    			"TaskNodeTotal":0,
    			"UserDefinedEmrEcsRole":"AliyunEmrEcsDefaultRole",
    			"UserId":125046002175****,
    			"VSwitchId":"vsw-bp11qjbyggil4pow064fg",
    			"VpcId":"vpc-bp1l4urd87xlh7i4bju4h",
    			"ZoneId":"cn-hangzhou-b"
    		},
    		"RequestId":"14E9C045-9B8D-4D1E-8D23-FC0027B6D947"
    	},
    	"requestId":"14E9C045-9B8D-4D1E-8D23-FC0027B6D947",
    	"successResponse":true
    }
    ```

-   异常返回示例

    JSON 格式

    ```
    {
    	"code":"ClusterId.NotFound",
    	"message":"ClusterId [null] does not exist.",
    	"requestId":"93EC4B6D-76D2-4CB1-847D-C7A5E5E0206A",
    	"successResponse":false
    }
    ```


## 错误码 {#section_a2w_lv4_dgb .section}

[查看本产品错误码](https://error-center.alibabacloud.com/status/product/Emr)

