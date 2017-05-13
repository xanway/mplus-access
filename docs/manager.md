# 管理员接口 

----------  

<h2 id="cid_0">获得管理员列表接口1.0</h2>  

说明：此接口返回机构管理员和部门管理员，区别字段为管理员类别字段。返回的所管机构/部门编码字段有所区别。详见字段说明。  

可以根据机构唯一标识获得该机构的管理员和机构下的部门管理员。  

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
      <td>mobileark.getmanagers</td>
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
      <td>orgUuid</td>
      <td>String</td>
      <td>否</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>机构唯一标识。默认查询所有机构</td>
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
      <td>mngUuid</td>
      <td>String</td>
      <td>管理员唯一标识（对应获得管理员接口参数adminUuid）</td>
   </tr>
   <tr>
      <td>loginId</td>
      <td>String</td>
      <td>管理员帐号</td>
   </tr>
   <tr>
      <td>mngName</td>
      <td>String</td>
      <td>管理员名称</td>
   </tr>
   <tr>
      <td>roleName</td>
      <td>String</td>
      <td>管理员角色</td>
   </tr>
   <tr>
      <td>mngType</td>
      <td>String</td>
      <td>管理员类别，1机构管理员，2部门管理员；当为2时，且管理全机构部门，返回scopeUuid值为-1。</td>
   </tr>
   <tr>
      <td>orgUuid</td>
      <td>String</td>
      <td>机构唯一标识，当mngType=1时，值为-1，否则为机构唯一标识。</td>
   </tr>
   <tr>
      <td>locked</td>
      <td>String</td>
      <td>管理员状态，被锁定后，无法登录系统；0未锁定，1为锁定</td>
   </tr>
   <tr>
      <td>scopeSize</td>
      <td>String</td>
      <td>管理机构数</td>
   </tr>
   <tr>
      <td>scopeList</td>
      <td>Scope[]</td>
      <td>管理机构列表</td>
   </tr>
</table>  

Scope对象说明：  

<table>
   <tr>
      <td>参数</td>
      <td>值</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>scopeUuid</td>
      <td>String</td>
      <td>机构/部门唯一标识</td>
   </tr>
   <tr>
      <td>scopeCode</td>
      <td>String</td>
      <td>机构/部门，当mngType=1时，为机构编码。</td>
   </tr>
   <tr>
      <td>scopeName</td>
      <td>String</td>
      <td>机构/部门名称</td>
   </tr>
</table>  

<h2 id="cid_1">获得管理员列表接口1.1</h2>    

<font color="red">4.2版本以上支持</font>  

说明：此接口返回机构管理员和部门管理员，区别字段为管理员类别字段。返回的所管机构/部门编码字段有所区别。详见字段说明。  

可以根据机构唯一标识获得该机构的管理员和机构下的部门管理员。  

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
      <td>mobileark.getmanagers</td>
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
      <td>否</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>机构唯一标识。默认查询所有机构</td>
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
      <td>mngUuid</td>
      <td>String</td>
      <td>管理员唯一标识</td>
   </tr>
   <tr>
      <td>userUuid</td>
      <td>String</td>
      <td>用户唯一标识（当mngType=2时，对应用户的标识，升级上来的版本可能为空字符串）（注 mos使用）</td>
   </tr>
   <tr>
      <td>loginId</td>
      <td>String</td>
      <td>管理员帐号</td>
   </tr>
   <tr>
      <td>mngName</td>
      <td>String</td>
      <td>管理员名称</td>
   </tr>
   <tr>
      <td>roleName</td>
      <td>String</td>
      <td>管理员角色</td>
   </tr>
   <tr>
      <td>mngType</td>
      <td>String</td>
      <td>管理员类别，1机构管理员，2部门管理员；当为2时，且管理全机构部门，返回scopeUuid值为-1。</td>
   </tr>
   <tr>
      <td>orgUuid</td>
      <td>String</td>
      <td>机构唯一标识，当mngType=1时，值为-1，否则为机构唯一标识。</td>
   </tr>
   <tr>
      <td>locked</td>
      <td>String</td>
      <td>管理员状态，被锁定后，无法登录系统；0未锁定，1为锁定</td>
   </tr>
   <tr>
      <td>scopeSize</td>
      <td>String</td>
      <td>管理机构数</td>
   </tr>
   <tr>
      <td>scopeList</td>
      <td>Scope[]</td>
      <td>管理机构列表</td>
   </tr>
</table>  

Scope对象说明：  

<table>
   <tr>
      <td>参数</td>
      <td>值</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>scopeUuid</td>
      <td>String</td>
      <td>机构/部门唯一标识</td>
   </tr>
   <tr>
      <td>scopeCode</td>
      <td>String</td>
      <td>机构/部门，当mngType=1时，为机构编码。</td>
   </tr>
   <tr>
      <td>scopeName</td>
      <td>String</td>
      <td>机构/部门名称</td>
   </tr>
</table>  

<h2 id="cid_2">获得管理员接口1.0</h2>    

<font color="red">4.0版本以上支持</font>  

说明：此接口返回机构管理员和部门管理员，区别字段为管理员类别字段。返回的所管机构/部门编码字段有所区别，详见说明。  

可以根据机构唯一标识获得该机构的管理员和机构下的部门管理员。  

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
      <td>mobileark.getadmin</td>
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
      <td>adminUuid</td>
      <td>String</td>
      <td>是</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>管理员唯一标识。默认查询所有机构</td>
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
      <td>mngUuid</td>
      <td>String</td>
      <td>管理员唯一标识</td>
   </tr>
   <tr>
      <td>loginId</td>
      <td>String</td>
      <td>管理员帐号</td>
   </tr>
   <tr>
      <td>mngName</td>
      <td>String</td>
      <td>管理员名称</td>
   </tr>
   <tr>
      <td>roleName</td>
      <td>String</td>
      <td>管理员角色</td>
   </tr>
   <tr>
      <td>mngType</td>
      <td>String</td>
      <td>管理员类别，1机构管理员，2部门管理员</td>
   </tr>
   <tr>
      <td>orgUuid</td>
      <td>String</td>
      <td>机构唯一标识，当mngType=1时，值为-1，否则为机构唯一标识。</td>
   </tr>
   <tr>
      <td>locked</td>
      <td>String</td>
      <td>管理员状态，被锁定后，无法登录系统；0未锁定，1为锁定</td>
   </tr>
   <tr>
      <td>scopeSize</td>
      <td>String</td>
      <td>管理机构/部门数</td>
   </tr>
   <tr>
      <td>scopeList</td>
      <td>Scope[]</td>
      <td>管理机构/部门列表</td>
   </tr>
</table>  

Scope对象说明：  

<table>
   <tr>
      <td>参数</td>
      <td>值</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>scopeUuid</td>
      <td>String</td>
      <td>机构/部门唯一标识</td>
   </tr>
   <tr>
      <td>scopeCode</td>
      <td>String</td>
      <td>机构/部门编码，当mngType=1时，为机构编码。</td>
   </tr>
   <tr>
      <td>scopeName</td>
      <td>String</td>
      <td>机构/部门名称</td>
   </tr>
</table>


