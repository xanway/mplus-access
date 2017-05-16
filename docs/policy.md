# 可见性策略接口

----------  

<h2 id="cid_0">获得可见性策略列表1.0</h2>  

<font color="red">4.2及以后版本支持</font>  

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
      <td>mobileark.getpolicylist</td>
      <td>接口定义</td>
   </tr>
   <tr>
      <td>v</td>
      <td>String</td>
      <td>1.0</td>
      <td>接口版本</td>
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
      <td>\d{1,n}</td>
      <td>分页参数-起始页，默认值为1</td>
   </tr>
   <tr>
      <td>limit</td>
      <td>String</td>
      <td>否</td>
      <td>\d{0,n}</td>
      <td>分页参数-页面条数，默认为10</td>
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
      <td>policyBeans</td>
      <td>VisiblePolicyBean[]</td>
      <td>策略信息列表</td>
   </tr>
   <tr>
      <td>policySize</td>
      <td>int</td>
      <td>策略总数</td>
   </tr>
</table>  

VisiblePolicyBean对象说明：  

<table>
   <tr>
      <td>参数</td>
      <td>值</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>policyUuid</td>
      <td>String</td>
      <td>策略唯一标识</td>
   </tr>
   <tr>
      <td>policyName</td>
      <td>String</td>
      <td>策略名</td>
   </tr>
   <tr>
      <td>createTime</td>
      <td>String</td>
      <td>创建时间</td>
   </tr>
   <tr>
      <td>createTimeLongs</td>
      <td>long</td>
      <td>创建时间</td>
   </tr>
   <tr>
      <td>updateTime</td>
      <td>String</td>
      <td>更新时间</td>
   </tr>
   <tr>
      <td>updateTimeLongs</td>
      <td>long</td>
      <td>更新时间</td>
   </tr>
</table>  

<h2 id="cid_1">获得可见性策略详情1.0</h2>  

<font color="red">4.2及以后版本支持</font>  

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
      <td>mobileark.getpolicydetail</td>
      <td>接口定义</td>
   </tr>
   <tr>
      <td>v</td>
      <td>String</td>
      <td>1.0</td>
      <td>接口版本</td>
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
      <td>policyUuid</td>
      <td>String</td>
      <td>是</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>策略唯一标识</td>
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
      <td>policyUuid</td>
      <td>String</td>
      <td>策略唯一标识</td>
   </tr>
   <tr>
      <td>policyName</td>
      <td>String</td>
      <td>策略名</td>
   </tr>
   <tr>
      <td>isOrg</td>
      <td>int</td>
      <td>策略归属：1机构策略  0部门策略</td>
   </tr>
   <tr>
      <td>ownDepUuid</td>
      <td>String</td>
      <td>策略归属机构/部门标识</td>
   </tr>
   <tr>
      <td>isDefault</td>
      <td>int</td>
      <td>默认策略 0非 1是</td>
   </tr>
   <tr>
      <td>contactsPolicy</td>
      <td>int</td>
      <td>联系人策略(1仅机构、2仅好友、3机构和好友)</td>
   </tr>
   <tr>
      <td>friendPolicy</td>
      <td>int</td>
      <td>好友策略(1：全部可搜 2：非可见可搜)</td>
   </tr>
   <tr>
      <td>frameworkPolicy</td>
      <td>int</td>
      <td>组织架构策略(1：全部门可见 2：本部门可见 3自定义：指定部门可见)</td>
   </tr>
   <tr>
      <td>createTime</td>
      <td>String</td>
      <td>创建时间</td>
   </tr>
   <tr>
      <td>createTimeLongs</td>
      <td>long</td>
      <td>创建时间</td>
   </tr>
   <tr>
      <td>updateTime</td>
      <td>String</td>
      <td>更新时间</td>
   </tr>
   <tr>
      <td>updateTimeLongs</td>
      <td>long</td>
      <td>更新时间</td>
   </tr>
   <tr>
      <td>defaultDepUuid</td>
      <td>String</td>
      <td>默认部门标识</td>
   </tr>
   <tr>
      <td>assignDepUuid</td>
      <td>String[]</td>
      <td>分配的部门集合</td>
   </tr>
   <tr>
      <td>assignGroupUuid</td>
      <td>String[]</td>
      <td>分配的虚拟组集合</td>
   </tr>
   <tr>
      <td>assignUserUuid</td>
      <td>String[]</td>
      <td>分配的用户集合</td>
   </tr>
   <tr>
      <td>customDepUuid</td>
      <td>String[]</td>
      <td>指定部门集合（组织架构策略3有效）</td>
   </tr>
</table>