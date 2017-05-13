# 推送接口 

----------  

<h2 id="cid_0">IM推送接口1.0</h2>  

<font color="red">4.4.0及以后版本支持</font>

说明：用于推送IM消息接口。 

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
      <td>mobileark.impush</td>
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
      <td>ecid</td>
      <td>String</td>
      <td>是</td>
      <td>{1,20}</td>
      <td>机构标识(编码) ，不区分大小写</td>
   </tr>
   <tr>
      <td>imSender</td>
      <td>String</td>
      <td>是</td>
      <td>{1,36}</td>
      <td>发送者帐号im_loginid；如果通讯类型配置rtc类型，则不再需要im_作为前缀。</td>
   </tr>
   <tr>
      <td>imSenderName</td>
      <td>String</td>
      <td>是</td>
      <td>{1,48}</td>
      <td>发送者昵称</td>
   </tr>
   <tr>
      <td>imReceiver</td>
      <td>String[]</td>
      <td>是</td>
      <td>{1,36}</td>
      <td>接收者帐号im_${loginid}，每次最多100人 5分钟只能发3次</td>
   </tr>
   <tr>
      <td>content</td>
      <td>String</td>
      <td>是</td>
      <td>{1,1000}</td>
      <td>消息内容，如果通讯类型配置rtc类型，则不应超过2048字节。</td>
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
      <td>返回码，0：成功，1：失败 </td>
   </tr>
   <tr>
      <td>resultMsg</td>
      <td>String</td>
      <td>提示信息</td>
   </tr>
</table>  

<h2 id="cid_1">系统推送接口1.0</h2>  

<font color="red">4.4.0及以后版本支持</font>  

说明：用于批量推送系统消息接口。

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
      <td>mobileark.syspush</td>
      <td>接口定义</td>
   </tr>
   <tr>
      <td>v</td>
      <td>String</td>
      <td>1.0</td>
      <td>版本定义</td>
   </tr>
</table>

业务层参数列表：loginIds和depUuids必须存在一个  

<table>
   <tr>
      <td>业务参数</td>
      <td>类型</td>
      <td>是否必须</td>
      <td>字段约束</td>
      <td>说明</td>
   </tr>
   <tr>
      <td>ecid</td>
      <td>String</td>
      <td>是</td>
      <td>{1,20}</td>
      <td>机构标识(编码) ，不区分大小写</td>
   </tr>
   <tr>
      <td>loginIds</td>
      <td>String[]</td>
      <td>是</td>
      <td>{1,36}</td>
      <td>登录帐号，非空字符串，不区分大小写，当按depUuid发送时，可填空。</td>
   </tr>
   <tr>
      <td>depUuids</td>
      <td>String[]</td>
      <td>是</td>
      <td>{1,36}</td>
      <td>部门标识，当选择按loginid发送时，可填空。</td>
   </tr>
   <tr>
      <td>title</td>
      <td>String</td>
      <td>是</td>
      <td>{1,40}</td>
      <td>通知标题</td>
   </tr>
   <tr>
      <td>content</td>
      <td>String</td>
      <td>是</td>
      <td>{1,500}</td>
      <td>通知内容</td>
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
      <td>结果 1：成功 2：部分成功 3：全部失败</td>
   </tr>
   <tr>
      <td>failloginid</td>
      <td>String[]</td>
      <td>失败的用户列表</td>
   </tr>
   <tr>
      <td>faildepid</td>
      <td>String[]</td>
      <td>失败的部门列表</td>
   </tr>
</table>  

<h2 id="cid_2">系统推送接口1.1</h2>  

<font color="red">4.5.0及以后版本支持</font>  

说明：用于批量推送系统消息接口。 

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
      <td>mobileark.syspush</td>
      <td>接口定义</td>
   </tr>
   <tr>
      <td>v</td>
      <td>String</td>
      <td>1.1</td>
      <td>版本定义</td>
   </tr>
</table>

业务层参数列表：loginIds和depUuids必须存在一个  

<table>
   <tr>
      <td>业务参数</td>
      <td>类型</td>
      <td>是否必须</td>
      <td>字段约束</td>
      <td>说明</td>
   </tr>
   <tr>
      <td>ecid</td>
      <td>String</td>
      <td>是</td>
      <td>{1,20}</td>
      <td>机构标识(编码) ，不区分大小写</td>
   </tr>
	<tr>
      <td>type</td>
      <td>String</td>
      <td>否</td>
      <td>1|13</td>
      <td>值为1或者13。1为系统消息，13为提示消息，默认为1</td>
   </tr>
   <tr>
      <td>loginIds</td>
      <td>String[]</td>
      <td>是</td>
      <td>{1,36}</td>
      <td>登录帐号，非空字符串，不区分大小写，当按depUuid发送时，可填空。</td>
   </tr>
   <tr>
      <td>depUuids</td>
      <td>String[]</td>
      <td>是</td>
      <td>{1,36}</td>
      <td>部门标识，当选择按loginid发送时，可填空。</td>
   </tr>
   <tr>
      <td>title</td>
      <td>String</td>
      <td>是</td>
      <td>{1,40}</td>
      <td>通知标题</td>
   </tr>
   <tr>
      <td>content</td>
      <td>String</td>
      <td>是</td>
      <td>{1,500}</td>
      <td>通知内容，当type=1时，此字段有效。当type=13时，content不为空时有效，为空时使用titile值。</td>
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
      <td>结果 1：成功 2：部分成功 3：全部失败</td>
   </tr>
   <tr>
      <td>failloginid</td>
      <td>String[]</td>
      <td>失败的用户列表</td>
   </tr>
   <tr>
      <td>faildepid</td>
      <td>String[]</td>
      <td>失败的部门列表</td>
   </tr>
</table>  

<h2 id="cid_3">系统推送接口1.2</h2>  

<font color="red">4.6.0及以后版本支持</font>  

说明：用于批量推送系统消息接口。 

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
      <td>mobileark.syspush</td>
      <td>接口定义</td>
   </tr>
   <tr>
      <td>v</td>
      <td>String</td>
      <td>1.2</td>
	<td>版本定义</td>
   </tr>
</table>

业务层参数列表：当type=1或者13时：loginIds和depUuids必须存在一个；当type=16时，loginIds和depUuids都为空时，表示全机构。 

<table>
   <tr>
      <td>业务参数</td>
      <td>类型</td>
      <td>是否必须</td>
      <td>字段约束</td>
      <td>说明</td>
   </tr>
   <tr>
      <td>ecid</td>
      <td>String</td>
      <td>是</td>
      <td>{1,20}</td>
      <td>机构标识(编码) ，不区分大小写</td>
   </tr>
	<tr>
      <td>type</td>
      <td>String</td>
      <td>否</td>
      <td>1|13|16</td>
      <td>值为1、13、16。1为系统消息，13为提示消息，16为订阅号推送，默认为1</td>
   </tr>
   <tr>
      <td>loginIds</td>
      <td>String[]</td>
      <td>是</td>
      <td>{1,36}</td>
      <td>登录帐号，非空字符串，不区分大小写，当按depUuid发送时，可填空。</td>
   </tr>
   <tr>
      <td>depUuids</td>
      <td>String[]</td>
      <td>是</td>
      <td>{1,36}</td>
      <td>部门标识，当选择按loginid发送时，可填空。</td>
   </tr>
   <tr>
      <td>title</td>
      <td>String</td>
      <td>是</td>
      <td>{1,40}</td>
      <td>通知标题</td>
   </tr>
   <tr>
      <td>content</td>
      <td>String</td>
      <td>是</td>
      <td>{1,500}</td>
      <td>通知内容，当type=1时，此字段有效。当type=13时，content不为空时有效，为空时使用titile值。</td>
   </tr>
<tr>
      <td>param</td>
      <td>String</td>
      <td>否</td>
      <td>{0,500}</td>
      <td>推送参数，当type=16时，有效。json格式字符串，{"key1":"val1","key2":"val2"}</td>
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
      <td>结果 1：成功 2：部分成功 3：全部失败</td>
   </tr>
   <tr>
      <td>failloginid</td>
      <td>String[]</td>
      <td>失败的用户列表</td>
   </tr>
   <tr>
      <td>faildepid</td>
      <td>String[]</td>
      <td>失败的部门列表</td>
   </tr>
</table>  

<h2 id="cid_4">系统推送接口1.3</h2>  

<font color="red">4.7.0及以后版本支持</font>  

说明：用于批量推送系统消息接口。 

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
      <td>mobileark.syspush</td>
      <td>接口定义</td>
   </tr>
   <tr>
      <td>v</td>
      <td>String</td>
      <td>1.3</td>
	<td>版本定义</td>
   </tr>
</table>

业务层参数列表：当type=1或者13时：loginIds和depUuids必须存在一个；当type=16时，loginIds和depUuids都为空时，表示全机构；当为type=17时，用户多设备时，推送的设备为最近使用的单个设备。

<table>
   <tr>
      <td>业务参数</td>
      <td>类型</td>
      <td>是否必须</td>
      <td>字段约束</td>
      <td>说明</td>
   </tr>
   <tr>
      <td>ecid</td>
      <td>String</td>
      <td>是</td>
      <td>{1,20}</td>
      <td>机构标识(编码) ，不区分大小写</td>
   </tr>
	<tr>
      <td>type</td>
      <td>String</td>
      <td>否</td>
      <td>1|13|16|17|19</td>
      <td>值为1、13、16、19。1为系统消息，13为提示消息，16为订阅号推送，19为圈子推送消息，默认为1</td>
   </tr>
   <tr>
      <td>loginIds</td>
      <td>String[]</td>
      <td>是</td>
      <td>{1,36}</td>
      <td>登录帐号，非空字符串，不区分大小写，当按depUuid发送时，可填空。</td>
   </tr>
   <tr>
      <td>depUuids</td>
      <td>String[]</td>
      <td>是</td>
      <td>{1,36}</td>
      <td>部门标识，当选择按loginid发送时，可填空。</td>
   </tr>
   <tr>
      <td>title</td>
      <td>String</td>
      <td>是</td>
      <td>{1,40}</td>
      <td>通知标题</td>
   </tr>
   <tr>
      <td>content</td>
      <td>String</td>
      <td>是</td>
      <td>{1,500}</td>
      <td>通知内容，当type=1时，此字段有效。当type=13时，content不为空时有效，为空时使用titile值。</td>
   </tr>
<tr>
      <td>param</td>
      <td>String</td>
      <td>否</td>
      <td>{0,500}</td>
      <td>推送参数，当type=16时，有效。json格式字符串，{"key1":"val1","key2":"val2"}</td>
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
      <td>结果 1：成功 2：部分成功 3：全部失败</td>
   </tr>
   <tr>
      <td>failloginid</td>
      <td>String[]</td>
      <td>失败的用户列表</td>
   </tr>
   <tr>
      <td>faildepid</td>
      <td>String[]</td>
      <td>失败的部门列表</td>
   </tr>
</table>  

<h2 id="cid_5">短信发送接口1.3</h2>    

<font color="red">4.7.0版本以上支持</font>  

说明：用于批量发送短消息接口。 

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
      <td>mobileark.smspush</td>
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
      <td>phoneNumbers</td>
      <td>String[]</td>
      <td>是</td>
      <td>^((\\+86)|(86)|(0086)|(\\+852)|(852)|(00852)|(\\+853)|(853)|(00853)|(\\+886)|(886)|(00886))?[1][3|4|5|6|7|8|9]\\d{9}$</td>
      <td>接收方手机号码，多个号码用英文逗号隔开</td>
   </tr>
   <tr>
      <td>content</td>
      <td>String</td>
      <td>是</td>
      <td>{1,500}</td>
      <td>消息内容</td>
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