# 服务型应用接口 

----------  

<h2 id="cid_0">上/下架服务1.0</h2>  

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
      <td>mobileark.optserviceapp</td>
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
      <td>serviceId</td>
      <td>String</td>
      <td>是</td>
      <td>{1,256}</td>
      <td>服务ID</td>
   </tr>
   <tr>
      <td>serviceType</td>
      <td>stirng</td>
      <td>是</td>
      <td>{1}</td>
      <td>服务类型</td>
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

<h2 id="cid_1">服务（Exmobi）应用代理配置1.0</h2>  

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
      <td>mobileark.proxyserviceapp</td>
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

<h2 id="cid_2">服务（Exmobi）应用域名配置1.0</h2>  

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
      <td>mobileark.dnsserviceapp</td>
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

<h2 id="cid_3">服务访问码配置1.0</h2>  

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
      <td>mobileark.cfgserviceapp</td>
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
      <td>serviceIds</td>
      <td>String[]</td>
      <td>是</td>
      <td>{0,256}</td>
      <td>应用服务ID数组</td>
   </tr>
   <tr>
      <td>keyType</td>
      <td>String</td>
      <td>是</td>
      <td>(1|2)</td>
      <td>1正式 2试用</td>
   </tr>
   <tr>
      <td>appId</td>
      <td>String</td>
      <td>否</td>
      <td>{0,256}</td>
      <td>Exmobi应用appId;当keyType=1,必须填写appId,否则可为空。</td>
   </tr>
   <tr>
      <td>accessKey</td>
      <td>String</td>
      <td>否</td>
      <td>[a-zA-Z0-9_-]{0,36}</td>
      <td>服务访问码，需要使用时，必填。可以为空，和系统页面一致，自动生成。</td>
   </tr>
   <tr>
      <td>pwdValidity</td>
      <td>String</td>
      <td>是</td>
      <td>0-3650</td>
      <td>有效天数，keyType=2当值为0时默认为30天。keyType=1 默认当0时为3650，否则为指定有效天数。</td>
   </tr>
   <tr>
      <td>isDelay</td>
      <td>String</td>
      <td>否</td>
      <td>(1|2)</td>
      <td>是否延期标识。默认为1，表示新增或者修改有效期，从创建日期开始计算有效期；当为2时，表示延期，从过期时间开始计算有效期。</td>
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
      <td>accessKey</td>
      <td>String</td>
      <td>访问码</td>
   </tr>
   <tr>
      <td>resultCode</td>
      <td>String</td>
      <td>结果0成功</td>
   </tr>
</table>  