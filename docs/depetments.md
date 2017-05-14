# 部门接口 

----------  

<h2 id="cid_0">获得未分组部门1.0</h2>  

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
      <td>mobileark.getdefaultdep</td>
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
      <td>是</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>机构唯一标识</td>
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
      <td>depUuid</td>
      <td>String</td>
      <td>部门唯一标识</td>
   </tr>
   <tr>
      <td>depName</td>
      <td>String</td>
      <td>部门名称</td>
   </tr>
</table>  

<h2 id="cid_1">获得组织架构1.0</h2>  

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
      <td>mobileark.getdepartments</td>
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
      <td>是</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>机构唯一标识</td>
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
      <td>departmentInfos</td>
      <td>DepartmentTree[]</td>
      <td>部门列表</td>
   </tr>
</table>  

DepartmentTree对象说明：  

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
      <td>total</td>
      <td>String</td>
      <td>部门及子部门成员总数</td>
   </tr>
</table>  

<h2 id="cid_2">获得组织架构1.1</h2>  

<font color="red">2.9.2及以后版本支持</font>  

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
      <td>mobileark.getdepartments</td>
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
</table>  

响应业务参数：  

<table>
   <tr>
      <td>参数</td>
      <td>类型</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>departmentInfos</td>
      <td>DepartmentTree[]</td>
      <td>部门列表</td>
   </tr>
</table>  

DepartmentTree对象说明：  

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
      <td>total</td>
      <td>String</td>
      <td>部门及子部门成员总数</td>
   </tr>
</table>  

<h2 id="cid_3">获得组织架构1.2</h2>  

<font color="red">3.0.0及以后版本支持</font>  

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
      <td>mobileark.getdepartments</td>
      <td>接口定义</td>
   </tr>
   <tr>
      <td>v</td>
      <td>String</td>
      <td>1.2</td>
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
</table>  

响应业务参数：  

<table>
   <tr>
      <td>参数</td>
      <td>类型</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>departmentInfos</td>
      <td>DepartmentTree[]</td>
      <td>部门列表</td>
   </tr>
</table>  

DepartmentTree对象说明：  

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
      <td>total</td>
      <td>String</td>
      <td>部门及子部门成员总数</td>
   </tr>
</table>  

<h2 id="cid_4">获得组织架构1.3</h2>  

<font color="red">3.1.0及以后版本支持</font>  

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
      <td>mobileark.getdepartments</td>
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
      <td>类型</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>departmentInfos</td>
      <td>DepartmentTree[]</td>
      <td>部门列表</td>
   </tr>
</table>  

DepartmentTree对象说明：  

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
      <td>total</td>
      <td>String</td>
      <td>部门及子部门成员总数</td>
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
      <td>depOrder</td>
      <td>String</td>
      <td>部门序列，4位表示层级，如0006001000800044</td>
   </tr>
</table>  

<h2 id="cid_5">新增部门1.0</h2>  

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
      <td>mobileark.adddepartment</td>
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
      <td>是</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>机构唯一标识</td>
   </tr>
   <tr>
      <td>parentDepUuid</td>
      <td>String</td>
      <td>否</td>
      <td>[a-zA-Z0-9_-]{0,36}</td>
      <td>上级部门唯一标识，不填默认为机构下一级子部门。</td>
   </tr>
   <tr>
      <td>depName</td>
      <td>String</td>
      <td>是</td>
      <td>{1,40}</td>
      <td>部门名称，非空字符串。</td>
   </tr>
   <tr>
      <td>memo</td>
      <td>String</td>
      <td>否</td>
      <td>{0,200}</td>
      <td>部门描述，默认为空。</td>
   </tr>
   <tr>
      <td>email</td>
      <td>String</td>
      <td>否</td>
      <td>{0,64}</td>
      <td>邮箱地址，默认为空。</td>
   </tr>
   <tr>
      <td>weight</td>
      <td>String</td>
      <td>否</td>
      <td>{1,99999999}</td>
      <td>部门权重，默认为99999999</td>
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
      <td>depUuid</td>
      <td>String</td>
      <td>部门唯一标识</td>
   </tr>
</table>  

<h2 id="cid_6">删除部门1.0</h2>  

说明：此删除是级联删除子部门、部门成员、设备等信息  

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
      <td>mobileark.deldepartment</td>
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
      <td>是</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>机构唯一标识</td>
   </tr>
   <tr>
      <td>depUuid</td>
      <td>String</td>
      <td>是</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>部门唯一标识  </td>
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

<h2 id="cid_7">修改部门1.0</h2>  

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
      <td>mobileark.modifydepartment</td>
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
      <td>是</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>机构唯一标识</td>
   </tr>
   <tr>
      <td>depUuid</td>
      <td>String</td>
      <td>是</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>部门唯一标识</td>
   </tr>
   <tr>
      <td>depName</td>
      <td>String</td>
      <td>是</td>
      <td>{1,40}</td>
      <td>部门名称，非空字符串。</td>
   </tr>
   <tr>
      <td>memo</td>
      <td>String</td>
      <td>否</td>
      <td>{0,200}</td>
      <td>部门描述。 </td>
   </tr>
   <tr>
      <td>email</td>
      <td>String</td>
      <td>否</td>
      <td>{0,64}</td>
      <td>邮箱地址。</td>
   </tr>
   <tr>
      <td>weight</td>
      <td>String</td>
      <td>否</td>
      <td>{1,99999999}</td>
      <td>部门权重，空值或者不传值，为默认值99999999。</td>
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

<h2 id="cid_8">修改部门1.4</h2>  

<font color="red">3.5及以后版本支持</font>  

说明：修改部门的同时修改部门的归属

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
      <td>mobileark.modifydepartment</td>
      <td>接口定义</td>
   </tr>
   <tr>
      <td>v</td>
      <td>String</td>
      <td>1.4</td>
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
      <td>parentDepUuid</td>
      <td>String</td>
      <td>是</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>上级部门唯一标识，不填默认为机构下一级子部门。</td>
   </tr>
   <tr>
      <td>depUuid</td>
      <td>String</td>
      <td>是</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>部门唯一标识</td>
   </tr>
   <tr>
      <td>depName</td>
      <td>String</td>
      <td>是</td>
      <td>{1,40}</td>
      <td>部门名称，非空字符串。</td>
   </tr>
   <tr>
      <td>memo</td>
      <td>String</td>
      <td>否</td>
      <td>{0,200}</td>
      <td>部门描述。 </td>
   </tr>
   <tr>
      <td>email</td>
      <td>String</td>
      <td>否</td>
      <td>{0,64}</td>
      <td>邮箱地址。</td>
   </tr>
   <tr>
      <td>weight</td>
      <td>String</td>
      <td>否</td>
      <td>{1,99999999}</td>
      <td>部门权重，空值或者不传值，为默认值99999999。</td>
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

<h2 id="cid_9">移动部门1.0</h2>  

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
      <td>mobileark.movedepartment</td>
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
      <td>是</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>机构唯一标识</td>
   </tr>
   <tr>
      <td>depUuid</td>
      <td>String</td>
      <td>是</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>部门唯一标识</td>
   </tr>
   <tr>
      <td>depParentUuid</td>
      <td>String</td>
      <td>是</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>目标部门唯一标识</td>
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

<h2 id="cid_10">部门可见性授权1.0</h2>  

<font color="red">3.1.0及以后版本支持</font>  

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
      <td>mobileark.getdepartmentmode</td>
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
      <td>是</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>机构唯一标识</td>
   </tr>
   <tr>
      <td>depUuids</td>
      <td>String[]</td>
      <td>是</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>一个或多个部门唯一标识，约束为单个值约束；多个值用逗号隔开。</td>
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
      <td>modeList</td>
      <td>ModePojo[]</td>
      <td>部门标识</td>
   </tr>
</table>  

ModePojo对象属性如下：  

<table>
   <tr>
      <td>参数</td>
      <td>值</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>depUuid</td>
      <td>String</td>
      <td>部门标识，与请求参数一致</td>
   </tr>
   <tr>
      <td>mode</td>
      <td>Int</td>
      <td>0为继承，1为独立授权；</td>
   </tr>
   <tr>
      <td>modeOrg</td>
      <td>Int</td>
      <td>是否授权给全机构0否1是</td>
   </tr>
   <tr>
      <td>modeUserUuids</td>
      <td>String[]</td>
      <td>独立授权的用户标识</td>
   </tr>
   <tr>
      <td>modeDepUuids</td>
      <td>String[]</td>
      <td>独立授权的部门标识</td>
   </tr>
</table>   

<h2 id="cid_11">部门可见性授权1.1</h2>  

<font color="red">3.3.0及以后版本支持</font>  

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
      <td>mobileark.getdepartmentmode</td>
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
      <td>是</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>一个或多个部门唯一标识，约束为单个值约束；多个值用逗号隔开。</td>
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
      <td>modeList</td>
      <td>ModePojo[]</td>
      <td>部门标识</td>
   </tr>
   <tr>
      <td>defaultDepUuid</td>
      <td>String</td>
      <td>未分组部门标识</td>
   </tr>
</table>  

ModePojo对象属性如下：  

<table>
   <tr>
      <td>参数</td>
      <td>值</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>depUuid</td>
      <td>String</td>
      <td>部门标识，与请求参数一致</td>
   </tr>
   <tr>
      <td>mode</td>
      <td>Int</td>
      <td>0为继承，1为独立授权；</td>
   </tr>
   <tr>
      <td>modeOrg</td>
      <td>Int</td>
      <td>是否授权给全机构0否1是</td>
   </tr>
   <tr>
      <td>modeUserUuids</td>
      <td>String[]</td>
      <td>独立授权的用户标识</td>
   </tr>
   <tr>
      <td>modeDepUuids</td>
      <td>String[]</td>
      <td>独立授权的部门标识</td>
   </tr>
</table>   

<h2 id="cid_12">部门可见性授权1.2</h2>  

<font color="red">4.0.0及以后版本支持</font>  

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
      <td>mobileark.getdepartmentmode</td>
      <td>接口定义</td>
   </tr>
   <tr>
      <td>v</td>
      <td>String</td>
      <td>1.2</td>
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
      <td>是</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>一个或多个部门唯一标识，约束为单个值约束；多个值用逗号隔开。</td>
   </tr>
   <tr>
      <td>type</td>
      <td>String</td>
      <td>否</td>
      <td>（0|1）</td>
      <td>当为0时，根据depUuids逐个获取；当为1时，获取全部。默认为0。</td>
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
      <td>modeList</td>
      <td>ModePojo[]</td>
      <td>部门标识</td>
   </tr>
   <tr>
      <td>defaultDepUuid</td>
      <td>String</td>
      <td>未分组部门标识</td>
   </tr>
</table>  

ModePojo对象属性如下：  

<table>
   <tr>
      <td>参数</td>
      <td>值</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>depUuid</td>
      <td>String</td>
      <td>部门标识，与请求参数一致</td>
   </tr>
   <tr>
      <td>mode</td>
      <td>Int</td>
      <td>0为继承，1为独立授权；</td>
   </tr>
   <tr>
      <td>modeOrg</td>
      <td>Int</td>
      <td>是否授权给全机构0否1是</td>
   </tr>
   <tr>
      <td>modeUserUuids</td>
      <td>String[]</td>
      <td>独立授权的用户标识</td>
   </tr>
   <tr>
      <td>modeDepUuids</td>
      <td>String[]</td>
      <td>独立授权的部门标识</td>
   </tr>
</table>   
