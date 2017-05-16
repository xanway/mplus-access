# 应用接口 

----------  

<h2 id="cid_0">获得应用列表1.0</h2>  

系统参数：  

<table>
   <tr>
      <td>系统参数</td>
      <td>类型</td>
      <td>值</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>method</td>
      <td>String</td>
      <td>mobileark.getmanageapplist</td>
      <td>接口定义</td>
   </tr>
   <tr>
      <td>v</td>
      <td>String</td>
      <td>1.0</td>
      <td>版本</td>
   </tr>
</table>  

业务层参数：  

<table>
   <tr>
      <td>业务参数</td>
      <td>类型</td>
      <td>是否必须</td>
      <td>字段约束</td>
      <td>说明</td>
   </tr>
   <tr>
      <td>orgUuid</td>
      <td>String</td>
      <td>是</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>机构唯一标识</td>
   </tr>
   <tr>
      <td>startPage</td>
      <td>String</td>
      <td>否</td>
      <td>\d{-1,n}</td>
      <td>分页参数-起始页，默认为1。-1表示全查，分页参数失效。</td>
   </tr>
   <tr>
      <td>limit</td>
      <td>String</td>
      <td>否</td>
      <td>\d{0,n}</td>
      <td>分页参数-页面条数，默认为10</td>
   </tr>
   <tr>
      <td>sort</td>
      <td>String</td>
      <td>否</td>
      <td>(0|1)</td>
      <td>0为升序，1为降序。默认0</td>
   </tr>
   <tr>
      <td>sortName</td>
      <td>String</td>
      <td>否</td>
      <td>(0|1|2|3)</td>
      <td>0为应用名称，1为应用类型，2为评分，3为装机数。默认0</td>
   </tr>
   <tr>
      <td>appNameSearch</td>
      <td>String</td>
      <td>否</td>
      <td>{0,20}</td>
      <td>检索字段：应用名称</td>
   </tr>
   <tr>
      <td>appTypeSearch</td>
      <td>String</td>
      <td>否</td>
      <td>(1|2|3|4|5|6)</td>
      <td>检索字段：1 ExMobi应用，2 Android应用，3 iOS应用（企业证书），4 HTML，5Web app应用，5 iOS Appstore中的应用，6所有类型。默认为6</td>
   </tr>
   <tr>
      <td>appStatusSearch</td>
      <td>String</td>
      <td>否</td>
      <td>(0|1|2|3|4)</td>
      <td>检索字段：0-下架，1-上架，2-待审核，3-拒绝发布，4所有状态。默认为4</td>
   </tr>
</table> 

响应业务参数：  

<table>
   <tr>
      <td>参数</td>
      <td>值</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>appInfos</td>
      <td>AppInfo[]</td>
      <td>应用信息列表</td>
   </tr>
   <tr>
      <td>appSize</td>
      <td>int</td>
      <td>应用总数</td>
   </tr>
</table>  

AppInfo对象说明  

<table>
   <tr>
      <td>参数</td>
      <td>值</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>appInfoUuid</td>
      <td>String</td>
      <td>应用信息唯一标识</td>
   </tr>
   <tr>
      <td>appId</td>
      <td>String</td>
      <td>应用ID，类似包名</td>
   </tr>
   <tr>
      <td>appStatus</td>
      <td>String</td>
      <td>应用状态：3-拒绝发布，2-待审核，1-上架，0-下架。默认为1</td>
   </tr>
   <tr>
      <td>appType</td>
      <td>String</td>
      <td>应用类型：1 ExMobi应用，2 Android应用，3 iOS应用（企业证书），4 HTML，5Web app应用，5 iOS Appstore中的应用</td>
   </tr>
   <tr>
      <td>appName</td>
      <td>String</td>
      <td>应用名称</td>
   </tr>
   <tr>
      <td>appVersion</td>
      <td>String</td>
      <td>应用版本</td>
   </tr>
   <tr>
      <td>belongDep</td>
      <td>String</td>
      <td>所属部门</td>
   </tr>
   <tr>
      <td>starNumber</td>
      <td>String</td>
      <td>应用得分（应用评分）</td>
   </tr>
   <tr>
      <td>isTablet</td>
      <td>String</td>
      <td>适用设备：1适用于手机，2适用于手机与平板，3适用于平板</td>
   </tr>
   <tr>
      <td>appInstallCount</td>
      <td>String</td>
      <td>装机数</td>
   </tr>
</table>  

<h2 id="cid_1">上/下架应用1.0</h2>  

<font color="red">4.3.0及以后版本支持</font>  

系统参数：  

<table>
   <tr>
      <td>系统参数</td>
      <td>类型</td>
      <td>值</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>method</td>
      <td>String</td>
      <td>mobileark.optapp</td>
      <td>接口定义</td>
   </tr>
   <tr>
      <td>v</td>
      <td>String</td>
      <td>1.0</td>
      <td>版本</td>
   </tr>
</table>  

业务层参数：  

<table>
   <tr>
      <td>业务参数</td>
      <td>类型</td>
      <td>是否必须</td>
      <td>字段约束</td>
      <td>说明</td>
   </tr>
   <tr>
      <td>orgUuid</td>
      <td>String</td>
      <td>是</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>机构唯一标识</td>
   </tr>
   <tr>
      <td>appId</td>
      <td>String</td>
      <td>是</td>
      <td>{1,256}</td>
      <td>应用唯一标识</td>
   </tr>
   <tr>
      <td>appType</td>
      <td>String</td>
      <td>是</td>
      <td>{1|2|3|4|5}</td>
      <td>应用类型：1 ExMobi应用，2 Android应用，3 iOS应用（企业证书），4 HTML，5Web app应用，5 iOS Appstore中的应用</td>
   </tr>
   <tr>
      <td>appStatus</td>
      <td>String</td>
      <td>是</td>
      <td>(0|1)</td>
      <td>1-上架，0-下架</td>
   </tr>
</table>  

响应业务参数：    

<table>
   <tr>
      <td>参数</td>
      <td>值</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>resultCode</td>
      <td>String</td>
      <td>结果0成功</td>
   </tr>
</table>  

<h2 id="cid_2">Exmobi应用代理配置1.0</h2>  

<font color="red">4.3.0及以后版本支持</font>  

区别于页面逻辑，下架应用也可以配置。  

系统参数：  

<table>
   <tr>
      <td>系统参数</td>
      <td>类型</td>
      <td>值</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>method</td>
      <td>String</td>
      <td>mobileark.proxyapp</td>
      <td>接口定义</td>
   </tr>
   <tr>
      <td>v</td>
      <td>String</td>
      <td>1.0</td>
      <td>版本</td>
   </tr>
</table>  

业务层参数：  

<table>
   <tr>
      <td>业务参数</td>
      <td>类型</td>
      <td>是否必须</td>
      <td>字段约束</td>
      <td>说明</td>
   </tr>
   <tr>
      <td>orgUuid</td>
      <td>String</td>
      <td>是</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>机构唯一标识</td>
   </tr>
   <tr>
      <td>appId</td>
      <td>String</td>
      <td>是</td>
      <td>{1,256}</td>
      <td>应用ID</td>
   </tr>
   <tr>
      <td>ip</td>
      <td>String</td>
      <td>是</td>
      <td>{1,18}</td>
      <td>代理地址</td>
   </tr>
   <tr>
      <td>port</td>
      <td>String</td>
      <td>是</td>
      <td>1-65534</td>
      <td>代理端口</td>
   </tr>
   <tr>
      <td>name</td>
      <td>String</td>
      <td>否</td>
      <td>{0,64}</td>
      <td>代理帐号</td>
   </tr>
   <tr>
      <td>pwd</td>
      <td>String</td>
      <td>否</td>
      <td>{0,64}</td>
      <td>代理密码</td>
   </tr>
</table>  

响应业务参数：  

<table>
   <tr>
      <td>参数</td>
      <td>值</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>resultCode</td>
      <td>String</td>
      <td>结果 0 成功</td>
   </tr>
</table>  

<h2 id="cid_3">Exmobi应用域名配置1.0</h2>  

<font color="red">4.3.0及以后版本支持</font>  

区别于页面逻辑，下架应用也可以配置。  

系统参数：  

<table>
   <tr>
      <td>系统参数</td>
      <td>类型</td>
      <td>值</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>method</td>
      <td>String</td>
      <td>mobileark.dnsapp</td>
      <td>接口定义</td>
   </tr>
   <tr>
      <td>v</td>
      <td>String</td>
      <td>1.0</td>
      <td>版本</td>
   </tr>
</table>  

业务层参数：  

<table>
   <tr>
      <td>业务参数</td>
      <td>类型</td>
      <td>是否必须</td>
      <td>字段约束</td>
      <td>说明</td>
   </tr>
   <tr>
      <td>orgUuid</td>
      <td>String</td>
      <td>是</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>机构唯一标识</td>
   </tr>
   <tr>
      <td>appId</td>
      <td>String</td>
      <td>是</td>
      <td>{1,256}</td>
      <td>应用ID</td>
   </tr>
   <tr>
      <td>appDns</td>
      <td>Dns[]</td>
      <td>是</td>
      <td>{0,*}</td>
      <td>为JSON数组，[{"domainname":"21312","domainaddr":"1231"}]</td>
   </tr>
</table>  

Dns的格式为：  

<table>
   <tr>
      <td>业务参数</td>
      <td>类型</td>
      <td>是否必须</td>
      <td>字段约束</td>
      <td>说明</td>
   </tr>
   <tr>
      <td>domainname</td>
      <td>String</td>
      <td>是</td>
      <td>{1,32}</td>
      <td>域名</td>
   </tr>
   <tr>
      <td>domainaddr</td>
      <td>String</td>
      <td>是</td>
      <td>{1,256}</td>
      <td>域名地址</td>
   </tr>
</table>  

响应业务参数：  

<table>
   <tr>
      <td>参数</td>
      <td>值</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>resultCode</td>
      <td>String</td>
      <td>结果 0 成功</td>
   </tr>
</table>  

<h2 id="cid_4">应用授权部门1.1</h2>  

* 应用重复授权（多个）部门时，如果已存在授权关系，后台直接更新，不提示“已授权无法重复授权”信息；
* 取消应用授权（多个）部门时，如果不存在授权关系，不提示“应用未授权此部门，无法取消授权”信息；  

系统参数：  

<table>
   <tr>
      <td>系统参数</td>
      <td>类型</td>
      <td>值</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>method</td>
      <td>String</td>
      <td>mobileark.optappauth</td>
      <td>接口定义</td>
   </tr>
   <tr>
      <td>v</td>
      <td>String</td>
      <td>1.1</td>
      <td>版本定义</td>
   </tr>
</table>  

业务层参数：  

<table>
   <tr>
      <td>业务参数</td>
      <td>类型</td>
      <td>是否必须</td>
      <td>字段约束</td>
      <td>说明</td>
   </tr>
   <tr>
      <td>orgUuid</td>
      <td>String</td>
      <td>是</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>机构唯一标识</td>
   </tr>
   <tr>
      <td>depUuids</td>
      <td>String[]</td>
      <td>否</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>一个或多个部门唯一标识，约束为单个值约束；多个值用逗号隔开。默认值为orgUuid</td>
   </tr>
   <tr>
      <td>appId</td>
      <td>String</td>
      <td>是</td>
      <td>{1,256}</td>
      <td>应用唯一标识</td>
   </tr>
   <tr>
      <td>appType</td>
      <td>String</td>
      <td>是</td>
      <td>1，2，3，4，5，6</td>
      <td>应用类型：1 ExMobi应用，2 Android应用，3 iOS应用（企业证书），4 HTML5，5 iOS Appstore中的应用，6 Web app应用</td>
   </tr>
   <tr>
      <td>opType</td>
      <td>String</td>
      <td>是</td>
      <td>(0|1|2)</td>
      <td>0授权应用禁止安装，1授权应用允许安装，2取消应用授权</td>
   </tr>
</table>  

响应业务参数：  

<table>
   <tr>
      <td>参数</td>
      <td>值</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>resultCode</td>
      <td>String</td>
      <td>结果 0 成功</td>
   </tr>
</table>  

<h2 id="cid_5">应用授权虚拟组1.1</h2>  

只能对虚拟组授权，不能对虚拟组集合授权。  

* 应用重复授权（多个）虚拟组时，如果已存在授权关系，后台直接更新，不提示“已授权无法重复授权”信息；
* 取消应用授权（多个）虚拟组时，如果不存在授权关系，不提示“应用未授权此虚拟组，无法取消授权”信息；

系统参数：  

<table>
   <tr>
      <td>系统参数</td>
      <td>类型</td>
      <td>值</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>method</td>
      <td>String</td>
      <td>mobileark.optappvgroupauth</td>
      <td>接口定义</td>
   </tr>
   <tr>
      <td>v</td>
      <td>String</td>
      <td>1.1</td>
      <td>版本定义</td>
   </tr>
</table>  

业务层参数：  

<table>
   <tr>
      <td>业务参数</td>
      <td>类型</td>
      <td>是否必须</td>
      <td>字段约束</td>
      <td>说明</td>
   </tr>
   <tr>
      <td>orgUuid</td>
      <td>String</td>
      <td>是</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>机构唯一标识</td>
   </tr>
   <tr>
      <td>vgroupUuids</td>
      <td>String[]</td>
      <td>是</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>一个或多个虚拟组唯一标识，约束为单个值约束；多个值用逗号隔开</td>
   </tr>
   <tr>
      <td>appId</td>
      <td>String</td>
      <td>是</td>
      <td>{1,256}</td>
      <td>应用唯一标识</td>
   </tr>
   <tr>
      <td>appType</td>
      <td>String</td>
      <td>是</td>
      <td>1，2，3，4，5，6</td>
      <td>应用类型：1 ExMobi应用，2 Android应用，3 iOS应用（企业证书），4 HTML，5 iOS Appstore中的应用，6Web app应用</td>
   </tr>
   <tr>
      <td>opType</td>
      <td>String</td>
      <td>是</td>
      <td>(0|1|2)</td>
      <td>0授权应用禁止安装，1授权应用允许安装，2取消应用授权</td>
   </tr>
</table>  

响应业务参数：  

<table>
   <tr>
      <td>参数</td>
      <td>值</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>resultCode</td>
      <td>String</td>
      <td>结果 0 成功</td>
   </tr>
</table>  