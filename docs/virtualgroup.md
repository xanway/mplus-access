# 虚拟组接口 

----------  

<h2 id="cid_0">新增虚拟组（集合）1.0</h2>  

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
      <td>mobileark.addvirtualgroup</td>
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
      <td>vgroupUnitName</td>
      <td>String</td>
      <td>是</td>
      <td>{1,10}</td>
      <td>虚拟组集合名称</td>
   </tr>
   <tr>
      <td>multiType</td>
      <td>String</td>
      <td>否</td>
      <td>(1|2)</td>
      <td>选择类型，1多选，2单选，默认为1。</td>
   </tr>
   <tr>
      <td>vgroupNames</td>
      <td>String[]</td>
      <td>否</td>
      <td>{1,10}</td>
      <td>虚拟组名称，一个或多个值，约束为单个值约束；多个值用逗号隔开</td>
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

<h2 id="cid_1">新增虚拟组（集合）1.1</h2>  

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
      <td>mobileark.addvirtualgroup</td>
      <td>接口定义</td>
   </tr>
   <tr>
      <td>v</td>
      <td>String</td>
      <td>1.1</td>
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
      <td>depUuid</td>
      <td>String</td>
      <td>否</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>部门唯一标识，虚拟组集合所属部门</td>
   </tr>
   <tr>
      <td>vgroupUnitName</td>
      <td>String</td>
      <td>是</td>
      <td>{1,10}</td>
      <td>虚拟组集合名称</td>
   </tr>
   <tr>
      <td>multiType</td>
      <td>String</td>
      <td>否</td>
      <td>(1|2)</td>
      <td>选择类型，1多选，2单选，默认为1。</td>
   </tr>
   <tr>
      <td>vgroupNames</td>
      <td>String[]</td>
      <td>否</td>
      <td>{1,10}</td>
      <td>虚拟组名称，一个或多个值，约束为单个值约束；多个值用逗号隔开</td>
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

<h2 id="cid_2">删除虚拟组（集合）1.0</h2>  

<font color="red">3.2及以后版本支持</font>  

说明：删除虚拟组集合时，将级联删除虚拟组集合下的虚拟组。  

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
      <td>mobileark.delvirtualgroup</td>
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
      <td>virtualUuid</td>
      <td>String</td>
      <td>是</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>虚拟组(集合) 唯一标识</td>
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

<h2 id="cid_3">修改虚拟组（集合）1.0</h2>  

说明：vgroupUuid和vgroupName应成对出现。如果增加虚拟组，对应vgroupUuids值应为为default；如果删除虚拟组，请掉用删除接口。  

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
      <td>mobileark.modifyvirtualgroup</td>
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
      <td>vgroupUnitUuid</td>
      <td>String</td>
      <td>是</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>虚拟组集合唯一标识</td>
   </tr>
   <tr>
      <td>vgroupUnitName</td>
      <td>String</td>
      <td>否</td>
      <td>{1,10}</td>
      <td>虚拟组集合名称，如果不传或者空字符，则保持原值。</td>
   </tr>
   <tr>
      <td>multiType</td>
      <td>String</td>
      <td>否</td>
      <td>(1|2)</td>
      <td>选择类型，1是，2否</td>
   </tr>
   <tr>
      <td>vgroupUuids</td>
      <td>String[]</td>
      <td>否</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>虚拟组唯一标识，约束为单个值约束；多个值用逗号隔开</td>
   </tr>
   <tr>
      <td>vgroupNames</td>
      <td>String[]</td>
      <td>否</td>
      <td>{1,10}</td>
      <td>虚拟组名称集合，约束为单个值约束；多个值用逗号隔开</td>
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

<h2 id="cid_4">获取虚拟组（集合）树1.0</h2>  

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
      <td>mobileark.getvirtualgroup</td>
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
</table>  

响应业务参数：  

<table>
   <tr>
      <td>参数</td>
      <td>值</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>virGroups</td>
      <td>VirGroup[]</td>
      <td>虚拟组(集合)唯一标识</td>
   </tr>
</table>  

VirGroup响应业务参数：  

<table>
   <tr>
      <td>参数</td>
      <td>值</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>virtualUuid</td>
      <td>String</td>
      <td>虚拟组(集合)唯一标识</td>
   </tr>
   <tr>
      <td>virtualName</td>
      <td>String</td>
      <td>虚拟组(集合)名称</td>
   </tr>
   <tr>
      <td>parentUuid</td>
      <td>String</td>
      <td>虚拟组(集合)的父节点，虚拟组集合的父节点为-1，虚拟组的父节点为虚拟组集合</td>
   </tr>
   <tr>
      <td>isMultiple</td>
      <td>String</td>
      <td>选择类型，1多选，2单选。只有为集合时才有意义。</td>
   </tr>
</table>  

<h2 id="cid_5">获取虚拟组（集合）树1.1</h2>  

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
      <td>mobileark.getvirtualgroup</td>
      <td>接口定义</td>
   </tr>
   <tr>
      <td>v</td>
      <td>String</td>
      <td>1.1</td>
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
</table>  

响应业务参数：  

<table>
   <tr>
      <td>参数</td>
      <td>值</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>virGroups</td>
      <td>VirGroup[]</td>
      <td>虚拟组(集合)唯一标识</td>
   </tr>
   <tr>
      <td>defaultDepUuid</td>
      <td>String</td>
      <td>未分组部门标识</td>
   </tr>
</table>  

VirGroup响应业务参数：  

<table>
   <tr>
      <td>参数</td>
      <td>值</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>virtualUuid</td>
      <td>String</td>
      <td>虚拟组(集合)唯一标识</td>
   </tr>
   <tr>
      <td>virtualName</td>
      <td>String</td>
      <td>虚拟组(集合)名称</td>
   </tr>
   <tr>
      <td>parentUuid</td>
      <td>String</td>
      <td>虚拟组(集合)的父节点，虚拟组集合的父节点为-1，虚拟组的父节点为虚拟组集合</td>
   </tr>
   <tr>
      <td>isMultiple</td>
      <td>String</td>
      <td>选择类型，1多选，2单选。只有为集合时才有意义。</td>
   </tr>
</table>  

<h2 id="cid_6">获取虚拟组成员1.0</h2>  

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
      <td>mobileark.getvirtualgroupusers</td>
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
      <td>virtualUuid</td>
      <td>String</td>
      <td>是</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>虚拟组唯一标识</td>
   </tr>
   <tr>
      <td>userNameSearch</td>
      <td>String</td>
      <td>否</td>
      <td>[0,48]</td>
      <td>用户名匹配查询字段,用户过滤虚拟组中的用户</td>
   </tr>
   <tr>
      <td>startPage</td>
      <td>String</td>
      <td>否</td>
      <td>\d{-1,n}</td>
      <td>分页参数-起始页，默认值为1。</td>
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
      <td>userInfos</td>
      <td>UserInfo[]</td>
      <td>成员信息列表</td>
   </tr>
   <tr>
      <td>userSize</td>
      <td>int</td>
      <td>成员总数</td>
   </tr>
</table>  

UserInfo响应业务参数：  

<table>
   <tr>
      <td>参数</td>
      <td>值</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>userName</td>
      <td>String</td>
      <td>用户名</td>
   </tr>
   <tr>
      <td>userUuid</td>
      <td>String</td>
      <td>用户唯一标识</td>
   </tr>
</table>  
