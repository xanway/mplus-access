# 单点登录接口 

----------  

<h2 id="cid_0">单点登录接口1.0</h2>  

说明：用于第三方应用进行单点登录token认证，用于客户端的token认证和web端单点登录的认证。

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
      <td>mobileark.ssocheck</td>
      <td>接口定义</td>
   </tr>
   <tr>
      <td>v</td>
      <td>String</td>
      <td>1.0</td>
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
      <td>sessionId</td>
      <td>String</td>
      <td>是</td>
      <td>不限</td>
      <td>会话编号，使用token值</td>
   </tr>
   <tr>
      <td>type</td>
      <td>String</td>
      <td>是</td>
      <td>(1|2)</td>
      <td>1.终端 2、管理端</td>
   </tr>
</table>  

响应业务参数：  

<table>
   <tr>
      <td>参数</td>
      <td>类型</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>resultcode</td>
      <td>String</td>
      <td>返回码，0：成功，1：无效</td>
   </tr>
   <tr>
      <td>orginfo</td>
      <td>OrgInfo[]</td>
      <td>机构信息</td>
   </tr>
   <tr>
      <td>userinfo</td>
      <td>UserInfo</td>
      <td>用户信息</td>
   </tr>
   <tr>
      <td>role</td>
      <td>String[]</td>
      <td>用户权限</td>
   </tr>
</table>  

Role权限说明：  

<table>
   <tr>
      <td>role值</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>0000</td>
      <td>普通用户</td>
   </tr>
   <tr>
      <td>0001</td>
      <td>门户管理权限</td>
   </tr>
   <tr>
      <td>0002</td>
      <td>门户发布权限</td>
   </tr>
</table>  

OrgInfo对象说明：  

<table>
   <tr>
      <td>参数</td>
      <td>类型</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>orgCode</td>
      <td>String</td>
      <td>机构编码</td>
   </tr>
   <tr>
      <td>orgName</td>
      <td>String</td>
      <td>机构名称</td>
   </tr>
</table>  

UserInfo对象说明：  

<table>
   <tr>
      <td>参数</td>
      <td>类型</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>loginid</td>
      <td>String</td>
      <td>用户登录ID</td>
   </tr>
   <tr>
      <td>name</td>
      <td>String</td>
      <td>用户姓名</td>
   </tr>
</table>  

<h2 id="cid_1">单点登录接口1.1</h2>    

<font color="red">2.7.2版本以上支持</font>  

说明：用于第三方应用进行单点登录token认证，用于客户端的token认证和web端单点登录的认证。增加机构唯一标识字段。  

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
      <td>mobileark.ssocheck</td>
      <td>接口定义</td>
   </tr>
   <tr>
      <td>v</td>
      <td>String</td>
      <td><font color="red">1.1</font></td>
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
      <td>sessionId</td>
      <td>String</td>
      <td>是</td>
      <td>不限</td>
      <td>会话编号，使用token值</td>
   </tr>
   <tr>
      <td>type</td>
      <td>String</td>
      <td>是</td>
      <td>(1|2)</td>
      <td>1.终端 2、管理端</td>
   </tr>
</table> 

响应业务参数：  

<table>
   <tr>
      <td>参数</td>
      <td>类型</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>resultcode</td>
      <td>String</td>
      <td>返回码，0：成功，1：无效</td>
   </tr>
   <tr>
      <td>orginfo</td>
      <td>OrgInfo[]</td>
      <td>机构信息</td>
   </tr>
   <tr>
      <td>userinfo</td>
      <td>UserInfo</td>
      <td>用户信息</td>
   </tr>
   <tr>
      <td>role</td>
      <td>String[]</td>
      <td>用户权限</td>
   </tr>
</table>  

Role权限说明：  

<table>
   <tr>
      <td>role值</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>0000</td>
      <td>普通用户</td>
   </tr>
   <tr>
      <td>0001</td>
      <td>门户管理权限</td>
   </tr>
   <tr>
      <td>0002</td>
      <td>门户发布权限</td>
   </tr>
</table>  

OrgInfo对象说明：  

<table>
   <tr>
      <td>参数</td>
      <td>类型</td>
      <td>描述</td>
   </tr>
	<tr>
      <td><font color="red">orguuid</font></td>
      <td>String</td>
      <td>机构唯一标识</td>
   </tr>
   <tr>
      <td>orgCode</td>
      <td>String</td>
      <td>机构编码</td>
   </tr>
   <tr>
      <td>orgName</td>
      <td>String</td>
      <td>机构名称</td>
   </tr>
</table>  

UserInfo对象说明：  

<table>
   <tr>
      <td>参数</td>
      <td>类型</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>loginid</td>
      <td>String</td>
      <td>用户登录ID</td>
   </tr>
   <tr>
      <td>name</td>
      <td>String</td>
      <td>用户姓名</td>
   </tr>
</table>  

<h2 id="cid_2">单点登录接口1.2</h2>    

<font color="red">2.7.2版本以上支持</font>  

说明：用于第三方应用进行单点登录token认证，用于客户端的token认证和web端单点登录的认证。增加机构唯一标识字段。  

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
      <td>mobileark.ssocheck</td>
      <td>接口定义</td>
   </tr>
   <tr>
      <td>v</td>
      <td>String</td>
      <td><font color="red">1.2</font></td>
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
      <td>sessionId</td>
      <td>String</td>
      <td>是</td>
      <td>不限</td>
      <td>会话编号，使用token值</td>
   </tr>
   <tr>
      <td>type</td>
      <td>String</td>
      <td>是</td>
      <td>(1|2)</td>
      <td>1.终端 2、管理端</td>
   </tr>
</table> 

响应业务参数：  

<table>
   <tr>
      <td>参数</td>
      <td>类型</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>resultcode</td>
      <td>String</td>
      <td>返回码，0：成功，1：无效</td>
   </tr>
	<tr>
      <td><font color="red">msg</font></td>
      <td>String</td>
      <td>状态说明</td>
   </tr>
   <tr>
      <td>orginfo</td>
      <td>OrgInfo[]</td>
      <td>机构信息</td>
   </tr>
   <tr>
      <td>userinfo</td>
      <td>UserInfo</td>
      <td>用户信息</td>
   </tr>
   <tr>
      <td>role</td>
      <td>String[]</td>
      <td>用户权限</td>
   </tr>
</table>  

Role权限说明：  

<table>
   <tr>
      <td>role值</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>0000</td>
      <td>普通用户</td>
   </tr>
   <tr>
      <td>0001</td>
      <td>门户管理权限</td>
   </tr>
   <tr>
      <td>0002</td>
      <td>门户发布权限</td>
   </tr>
</table>  

OrgInfo对象说明：  

<table>
   <tr>
      <td>参数</td>
      <td>类型</td>
      <td>描述</td>
   </tr>
	<tr>
      <td><font color="red">orguuid</font></td>
      <td>String</td>
      <td>机构唯一标识</td>
   </tr>
   <tr>
      <td>orgCode</td>
      <td>String</td>
      <td>机构编码</td>
   </tr>
   <tr>
      <td>orgName</td>
      <td>String</td>
      <td>机构名称</td>
   </tr>
</table>  

UserInfo对象说明：  

<table>
   <tr>
      <td>参数</td>
      <td>类型</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>loginid</td>
      <td>String</td>
      <td>用户登录ID</td>
   </tr>
   <tr>
      <td>name</td>
      <td>String</td>
      <td>用户姓名</td>
   </tr>
<tr>
      <td><font color="red">phoneNumber</font></td>
      <td>String</td>
      <td>手机号码</td>
   </tr>
<tr>
      <td><font color="red">emailAddress</font></td>
      <td>String</td>
      <td>邮箱</td>
   </tr>
</table>  

<h2 id="cid_3">单点登录接口1.3</h2>    

<font color="red">4.6.1版本以上支持</font>  

说明：用于第三方应用进行单点登录token认证，用于客户端的token认证和web端单点登录的认证。增加用户唯一标识字段，修改机构响应值参数。  

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
      <td>mobileark.ssocheck</td>
      <td>接口定义</td>
   </tr>
   <tr>
      <td>v</td>
      <td>String</td>
      <td>1.3</td>
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
      <td>sessionId</td>
      <td>String</td>
      <td>是</td>
      <td>不限</td>
      <td>会话编号，使用token值</td>
   </tr>
   <tr>
      <td>type</td>
      <td>String</td>
      <td>是</td>
      <td>(1|2)</td>
      <td>1.终端 2、管理端</td>
   </tr>
</table>  

响应业务参数：  

<table>
   <tr>
      <td>参数</td>
      <td>类型</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>resultCode</td>
      <td>String</td>
      <td>返回码，0：成功，1：无效</td>
   </tr>
   <tr>
      <td>msg</td>
      <td>String</td>
      <td>状态说明</td>
   </tr>
   <tr>
      <td>orgInfo</td>
      <td>OrgInfo[]</td>
      <td>机构信息</td>
   </tr>
   <tr>
      <td>userInfo</td>
      <td>UserInfo</td>
      <td>用户信息</td>
   </tr>
   <tr>
      <td>role</td>
      <td>String[]</td>
      <td>用户权限</td>
   </tr>
</table>  

Role权限说明：  

<table>
   <tr>
      <td>role值</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>0000</td>
      <td>普通用户</td>
   </tr>
   <tr>
      <td>0001</td>
      <td>门户管理权限</td>
   </tr>
   <tr>
      <td>0002</td>
      <td>门户发布权限</td>
   </tr>
</table>  

OrgInfo对象说明：  

<table>
   <tr>
      <td>参数</td>
      <td>类型</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>orgUuid</td>
      <td>String</td>
      <td>机构唯一标识</td>
   </tr>
   <tr>
      <td>orgCode</td>
      <td>String</td>
      <td>机构编码</td>
   </tr>
   <tr>
      <td>orgName</td>
      <td>String</td>
      <td>机构名称</td>
   </tr>
</table>  

UserInfo对象说明：  

<table>
   <tr>
      <td>参数</td>
      <td>类型</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>loginId</td>
      <td>String</td>
      <td>用户登录ID</td>
   </tr>
   <tr>
      <td>userName</td>
      <td>String</td>
      <td>用户姓名</td>
   </tr>
   <tr>
      <td>phoneNumber</td>
      <td>String</td>
      <td>手机号码</td>
   </tr>
   <tr>
      <td>emailAddress</td>
      <td>String</td>
      <td>邮箱</td>
   </tr>
   <tr>
      <td><font color="red">userUuid</font></td>
      <td>String</td>
      <td>用户唯一标识</td>
   </tr>
</table>  

<h2 id="cid_4">单点登录接口1.4</h2>    

<font color="red">5.0.0版本以上支持</font>  

说明：用于第三方应用进行单点登录token认证，用于客户端的token认证和web端单点登录的认证。  

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
      <td>mobileark.ssocheck</td>
      <td>接口定义</td>
   </tr>
   <tr>
      <td>v</td>
      <td>String</td>
      <td><font color="red">1.4</font></td>
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
      <td>sessionId</td>
      <td>String</td>
      <td>是</td>
      <td>不限</td>
      <td>会话编号，使用token值</td>
   </tr>
   <tr>
      <td>type</td>
      <td>String</td>
      <td>是</td>
      <td>(1|2)</td>
      <td>1.终端 2、管理端</td>
   </tr>
   <tr>
      <td>appId</td>
      <td>String</td>
      <td>是</td>
      <td>不限</td>
      <td>应用ID（不校验正确性）</td>
   </tr>
   <tr>
      <td>appType</td>
      <td>String</td>
      <td>是</td>
      <td>不限</td>
      <td>应用类型（不校验正确性）应用类型：1 ExMobi应用，2 Android应用，3 iOS应用（企业证书），4 HTML，5Web app应用，6 iOS Appstore中的应用；圈子appType为99</td>
   </tr>
</table>  

响应业务参数：  

<table>
   <tr>
      <td>参数</td>
      <td>类型</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>resultCode</td>
      <td>String</td>
      <td>返回码，0：成功，1：无效</td>
   </tr>
   <tr>
      <td>msg</td>
      <td>String</td>
      <td>状态说明</td>
   </tr>
   <tr>
      <td>orgInfo</td>
      <td>OrgInfo[]</td>
      <td>机构信息</td>
   </tr>
   <tr>
      <td>userInfo</td>
      <td>UserInfo</td>
      <td>用户信息</td>
   </tr>
   <tr>
      <td>userType</td>
      <td>String</td>
      <td>用户类型（0-普通用户，1-应用管理员）</td>
   </tr>
   <tr>
      <td>appUserDepScope</td>
      <td>String</td>
      <td>管理部门范围类型（0-部门范围，1-机构范围）</td>
   </tr>
   <tr>
      <td>appUserDeps</td>
      <td>DepartmentBean[]</td>
      <td>管理的部门信息（appUserDepScope=1时，为空；管理范围是所属机构级部门，如果机构级部门为空，取机构信息）</td>
   </tr>
   <tr>
      <td>userDep</td>
      <td>DepartmentBean</td>
      <td>所属部门信息</td>
   </tr>
   <tr>
      <td>userOrgDep</td>
      <td>DepartmentBean</td>
      <td>所属的机构级部门信息，机构时为空</td>
   </tr>
   <tr>
      <td>role</td>
      <td>String[]</td>
      <td>用户权限</td>
   </tr>
</table>  

Role权限说明：  

<table>
   <tr>
      <td>role值</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>0000</td>
      <td>普通用户</td>
   </tr>
   <tr>
      <td>0001</td>
      <td>门户管理权限</td>
   </tr>
   <tr>
      <td>0002</td>
      <td>门户发布权限</td>
   </tr>
</table>  

OrgInfo对象说明：  

<table>
   <tr>
      <td>参数</td>
      <td>类型</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>orgUuid String</td>
		<td>String</td>
      <td>机构唯一标识</td>
   </tr>
   <tr>
      <td>orgCode </td>
      <td>String</td>
      <td>机构编码</td>
   </tr>
   <tr>
      <td>orgName</td>
      <td>String</td>
      <td>机构名称</td>
   </tr>
</table>  

UserInfo对象说明：  

<table>
   <tr>
      <td>参数</td>
      <td>类型</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>loginId</td>
      <td>String</td>
      <td>用户登录ID</td>
   </tr>
   <tr>
      <td>userName</td>
      <td>String</td>
      <td>用户姓名</td>
   </tr>
   <tr>
      <td>phoneNumber</td>
      <td>String</td>
      <td>手机号码</td>
   </tr>
   <tr>
      <td>emailAddress</td>
      <td>String</td>
      <td>邮箱</td>
   </tr>
   <tr>
      <td><font color="red">userUuid</font></td>
      <td>String</td>
      <td>用户唯一标识</td>
   </tr>
</table>  

DepartmentBean对象说明：  

<table>
   <tr>
      <td>参数</td>
      <td>值</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>depUuid</td>
      <td>String</td>
      <td>部门唯一标识</td>
   </tr>
   <tr>
      <td>depName</td>
      <td>String</td>
      <td>部门名称</td>
   </tr>
   <tr>
      <td>parentId</td>
      <td>String</td>
      <td>上级部门唯一标识</td>
   </tr>
   <tr>
      <td>email</td>
      <td>String</td>
      <td>部门邮箱地址</td>
   </tr>
   <tr>
      <td>depWeight</td>
      <td>Integer</td>
      <td>部门权重，默认99999999</td>
   </tr>
   <tr>
      <td>updateTime</td>
      <td>long</td>
      <td>修改时间</td>
   </tr>
   <tr>
      <td>mode</td>
      <td>Integer</td>
      <td>授权方式（0：继承，1：独立授权）</td>
   </tr>
   <tr>
      <td>total</td>
      <td>String</td>
      <td>部门及子部门成员总数-废弃保留值为0</td>
   </tr>
   <tr>
      <td><font color="red">depOrder</font></td>
      <td><font color="red">String</font></td>
      <td><font color="red">部门序列，4位表示层级，如0006001000800044</font></td>
   </tr>
</table>


<h2 id="cid_5">普通登录接口1.0</h2>    

<font color="red">2.7.2版本以上支持</font>  

说明：用于应用登录认证。<font color="red">（3.1.0以后版本支持机构编码和登录帐号不区分大小写）</font>  

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
      <td>mobileark.userlogin</td>
      <td>接口定义</td>
   </tr>
   <tr>
      <td>v</td>
      <td>String</td>
      <td>1.0</td>
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
      <td>orgCode</td>
      <td>String</td>
      <td>是</td>
      <td>{1,20}</td>
      <td>机构编码，<font color="red">不区分大小写</font></td>
   </tr>
   <tr>
      <td>loginId</td>
      <td>String</td>
      <td>是</td>
      <td>{1,36}</td>
      <td>登录帐号，<font color="red">不区分大小写</font></td>
   </tr>
   <tr>
      <td>pwd</td>
      <td>String</td>
      <td>是</td>
      <td>{6,64}</td>
      <td>密码,使用AES加密</td>
   </tr>
   <tr>
      <td>type</td>
      <td>String</td>
      <td>是</td>
      <td>(0|1)</td>
      <td>0表示普通成员，1表示管理员，默认为0</td>
   </tr>
</table>  

响应业务参数：登录成功后，提供成员属性（loginId,username,phoneNumber,emailAddress）  

<table>
   <tr>
      <td>参数</td>
      <td>类型</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>resultCode</td>
      <td>String</td>
      <td>返回码，0：成功，1：无效</td>
   </tr>
   <tr>
      <td>msg</td>
      <td>String</td>
      <td>状态信息</td>
   </tr>
   <tr>
      <td>loginId</td>
      <td>String</td>
      <td>登录帐号</td>
   </tr>
   <tr>
      <td>userName</td>
      <td>String</td>
      <td>用户昵称</td>
   </tr>
   <tr>
      <td>phoneNumber</td>
      <td>String</td>
      <td>手机号码</td>
   </tr>
   <tr>
      <td>emailAddress</td>
      <td>String</td>
      <td>电子邮件</td>
   </tr>
</table>  

<h2 id="cid_6">普通登录接口1.1</h2>    

<font color="red">3.3.0版本以上支持</font>  

说明：用于应用登录认证。（支持机构编码和登录帐号不区分大小写）  

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
      <td>mobileark.userlogin</td>
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
      <td>orgCode</td>
      <td>String</td>
      <td>是</td>
      <td>\w{1,20}</td>
      <td>机构编码，<font color="red">不区分大小写</font></td>
   </tr>
   <tr>
      <td>loginId</td>
      <td>String</td>
      <td>是</td>
      <td>{1,36}</td>
      <td>登录帐号，<font color="red">不区分大小写</font></td>
   </tr>
   <tr>
      <td>pwd</td>
      <td>String</td>
      <td>是</td>
      <td>{6,64}</td>
      <td>密码,使用AES加密</td>
   </tr>
   <tr>
      <td>type</td>
      <td>String</td>
      <td>否</td>
      <td>(0|1)</td>
      <td>0表示普通成员，1表示管理员，默认为0</td>
   </tr>
</table>  

响应业务参数：登录成功后，提供成员属性（loginId,username,phoneNumber,emailAddress）  

<table>
   <tr>
      <td>参数</td>
      <td>类型</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>resultCode</td>
      <td>String</td>
      <td>返回码，0：成功，1：无效</td>
   </tr>
   <tr>
      <td>msg</td>
      <td>String</td>
      <td>状态信息</td>
   </tr>
   <tr>
      <td>loginId</td>
      <td>String</td>
      <td>登录帐号</td>
   </tr>
   <tr>
      <td>userName</td>
      <td>String</td>
      <td>用户昵称</td>
   </tr>
   <tr>
      <td>phoneNumber</td>
      <td>String</td>
      <td>手机号码</td>
   </tr>
   <tr>
      <td>emailAddress</td>
      <td>String</td>
      <td>电子邮件</td>
   </tr>
   <tr>
      <td>userUuid</td>
      <td>String</td>
      <td>用户标识</td>
   </tr>
   <tr>
      <td>orgUuid</td>
      <td>String</td>
      <td>机构标识</td>
   </tr>
</table>  



