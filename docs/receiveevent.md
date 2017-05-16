# 待办事件（开启签名校验）

----------  

<h2 id="cid_0">接收待办事件1.0</h2>  

<font color="red">3.0.1及以后版本支持</font>  

说明：此接口开启签名验证。（<font color="red">3.1.0以后版本支持机构编码和登录帐号不区分大小写</font> ）  

如果appType=1即为exmobi应用时，appid为必填项；如果appType=2即为原生应用时，appid和appid_ios不都为空。  

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
      <td>mobileark.receiveevent</td>
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
      <td>loginId</td>
      <td>String[]</td>
      <td>是</td>
      <td>{1,36}</td>
      <td>登录帐号，非空字符串，不区分大小写</td>
   </tr>
   <tr>
      <td>appid</td>
      <td>String</td>
      <td>是</td>
      <td>{1,256}</td>
      <td>应用id，当为Exmobi应用时，填写Exmobi应用的ID，当为原生应用时，填写android应用的ID。当该应用暂未移动化时，所以填写一个应用的唯一标识</td>
   </tr>
   <tr>
      <td>appid_ios</td>
      <td>String</td>
      <td>是</td>
      <td>{0,256}</td>
      <td>当为原生应用是，填写ios的应用ID，否则填空字符串</td>
   </tr>
   <tr>
      <td>appName</td>
      <td>String</td>
      <td>是</td>
      <td>{1,256}</td>
      <td>应用名称</td>
   </tr>
   <tr>
      <td>appType</td>
      <td>String</td>
      <td>是</td>
      <td>(1|2)</td>
      <td>应用类型，1：exmobi应用，2：原生应用</td>
   </tr>
   <tr>
      <td>events</td>
      <td>Event[]</td>
      <td>是</td>
      <td>{1,*}</td>
      <td>事件列表</td>
   </tr>
</table>  

Event对象   

<table>
   <tr>
      <td>业务参数</td>
      <td>类型</td>
      <td>是否必须</td>
      <td>字段约束</td>
      <td>说明</td>
   </tr>
   <tr>
      <td>title</td>
      <td>String</td>
      <td>是</td>
      <td>{1,128}</td>
      <td>标题</td>
   </tr>
   <tr>
      <td>summary</td>
      <td>String</td>
      <td>是</td>
      <td>{1,512}</td>
      <td>摘要。</td>
   </tr>
   <tr>
      <td>scheme</td>
      <td>String</td>
      <td>否</td>
      <td>{0,1024}</td>
      <td>应用启动传参，支持${username}、${password}、${token}等变量。例如：usename=${username}&password=${password}&module=1</td>
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
</table>  

请求响应报文：  

POST请求体

```
sign=4480F23DE6E9F449223A5D8BAB18E4DCB08B88FA
&appName=testaaa@c.com
&ecid=default
&v=1.0
&loginId=chenjiajia,1,3
&events={"events":[{"title":"11","summary":"ssss","scheme":"adff"},{"title":"22","summary":"sss3333s","scheme":"ad32342ff"}]}
&appid_ios=testf
&appid=111
&method=mobileark.receiveevent
&format=json
&appType=1
&appKey=EPM
```  

响应体  

```javascript
{"resultCode": "2","failloginid": ["3", "1"]}
```  

<h2 id="cid_1">接收待办事件1.1</h2>  

<font color="red">4.2及以后版本支持</font>  

说明：此接口开启签名验证。  

如果appType=1即为exmobi应用时，appid为必填项；如果appType=2即为原生应用时，appid和appid_ios不都为空。  

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
      <td>mobileark.receiveevent</td>
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
      <td>ecid</td>
      <td>String</td>
      <td>是</td>
      <td>{1,20}</td>
      <td>机构标识(编码) ，不区分大小写</td>
   </tr>
   <tr>
      <td>loginId</td>
      <td>String[]</td>
      <td>是</td>
      <td>{1,36}</td>
      <td>登录帐号，非空字符串，不区分大小写</td>
   </tr>
   <tr>
      <td>appid</td>
      <td>String</td>
      <td>是</td>
      <td>{1,256}</td>
      <td>应用id，当为Exmobi应用时，填写Exmobi应用的ID，当为原生应用时，填写android应用的ID。当该应用暂未移动化时，所以填写一个应用的唯一标识</td>
   </tr>
   <tr>
      <td>appid_ios</td>
      <td>String</td>
      <td>是</td>
      <td>{0,256}</td>
      <td>当为原生应用是，填写ios的应用ID，否则填空字符串</td>
   </tr>
   <tr>
      <td>appName</td>
      <td>String</td>
      <td>是</td>
      <td>{1,256}</td>
      <td>应用名称</td>
   </tr>
   <tr>
      <td>appType</td>
      <td>String</td>
      <td>是</td>
      <td>(1|2|3)</td>
      <td>应用类型，1：exmobi应用，2：原生应用 3.html5应用</td>
   </tr>
   <tr>
      <td>events</td>
      <td>Event[]</td>
      <td>是</td>
      <td>{1,*}</td>
      <td>事件列表</td>
   </tr>
</table>  

Event对象  

<table>
   <tr>
      <td>业务参数</td>
      <td>类型</td>
      <td>是否必须</td>
      <td>字段约束</td>
      <td>说明</td>
   </tr>
   <tr>
      <td>title</td>
      <td>String</td>
      <td>是</td>
      <td>{1,128}</td>
      <td>标题</td>
   </tr>
   <tr>
      <td>summary</td>
      <td>String</td>
      <td>是</td>
      <td>{1,512}</td>
      <td>摘要。</td>
   </tr>
   <tr>
      <td>scheme</td>
      <td>String</td>
      <td>否</td>
      <td>{0,1024}</td>
      <td>应用启动传参，支持${username}、${password}、${token}等变量。例如：usename=${username}&password=${password}&module=1<br/>html5应用时为地址：例如https://www.baidu.cm</td>
   </tr>

   <tr>
      <td>eventId</td>
      <td>String</td>
      <td>否</td>
      <td>{1,36}</td>
      <td>待办唯一ID，用于主动取消待办</td>
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
</table>  

请求响应报文：  

Post请求体：  

```
loginId=chenjiajia&events={"events":[{"title":"加班申请","summary":"您有一条加班申请","scheme":"username=${username}modulename=加班申请","eventId":"123455"}]}&appid_ios=&locale=zh_CN&appid=com.baidu.netdisk&format=json&ecid=default&appName=百度云&sign=E1FE26F4AD8D37F9B1E8C0CDCBA1474B70470271&v=1.1&method=mobileark.receiveevent&appType=2&appKey=mos
```  

响应体：  

```javascript
{"resultCode":"1","failloginid":[]}
```  

<h2 id="cid_2">接收待办事件1.2</h2>  

<font color="red">4.4.0及以后版本支持</font>  

说明：此接口开启签名验证。  

如果appType=1即为exmobi应用时，appid为必填项；如果appType=2即为原生应用时，appid和appid_ios不都为空。  

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
      <td>mobileark.receiveevent</td>
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
      <td>ecid</td>
      <td>String</td>
      <td>是</td>
      <td>{1,20}</td>
      <td>机构标识(编码) ，不区分大小写</td>
   </tr>
   <tr>
      <td>loginId</td>
      <td>String[]</td>
      <td>是</td>
      <td>{1,36}</td>
      <td>登录帐号，非空字符串，不区分大小写</td>
   </tr>
   <tr>
      <td>appid</td>
      <td>String</td>
      <td>是</td>
      <td>{1,256}</td>
      <td>应用id，当为Exmobi应用时，填写Exmobi应用的ID，当为原生应用时，填写android应用的ID。当该应用暂未移动化时，所以填写一个应用的唯一标识</td>
   </tr>
   <tr>
      <td>appid_ios</td>
      <td>String</td>
      <td>是</td>
      <td>{0,256}</td>
      <td>当为原生应用是，填写ios的应用ID，否则填空字符串</td>
   </tr>
   <tr>
      <td>appName</td>
      <td>String</td>
      <td>是</td>
      <td>{1,256}</td>
      <td>应用名称</td>
   </tr>
   <tr>
      <td>appType</td>
      <td>String</td>
      <td>是</td>
      <td>(1|2|3)</td>
      <td>应用类型，1：exmobi应用，2：原生应用 3.html5应用</td>
   </tr>
   <tr>
      <td>events</td>
      <td>Event[]</td>
      <td>是</td>
      <td>{1,*}</td>
      <td>事件列表</td>
   </tr>
</table>  

Event对象<font color="red">（title和summary至少存在其中一个）</font>  

<table>
   <tr>
      <td>业务参数</td>
      <td>类型</td>
      <td>是否必须</td>
      <td>字段约束</td>
      <td>说明</td>
   </tr>
   <tr>
      <td>title</td>
      <td>String</td>
      <td>是</td>
      <td>{0,128}</td>
      <td>标题</td>
   </tr>
   <tr>
      <td>summary</td>
      <td>String</td>
      <td>是</td>
      <td>{0,512}</td>
      <td>摘要</td>
   </tr>
   <tr>
      <td>scheme</td>
      <td>String</td>
      <td>否</td>
      <td>{0,1024}</td>
      <td>应用启动传参，支持${username}、${password}、${token}等变量。例如：usename=${username}&password=${password}&module=1<br/>html5应用时为地址：例如https://www.baidu.cm</td>
   </tr>
   <tr>
      <td>eventId</td>
      <td>String</td>
      <td>否</td>
      <td>{1,36}</td>
      <td>待办唯一ID，用于主动取消待办</td>
   </tr>
   <tr>
      <td>param</td>
      <td>String</td>
      <td>否</td>
      <td>{0,512}</td>
      <td>待办提醒扩展参数，使用Base64编码。非空时，解码后的参数必须为json格式。</td>
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
</table>  

<h2 id="cid_3">接收待办事件1.3</h2>  

<font color="red">5.1及以后版本支持</font>  

说明：此接口开启签名验证。  

如果appType=1即为exmobi应用时，appid为必填项；如果appType=2即为原生应用时，appid和appid_ios不都为空。当只发送PC侧待办时，apptype=4，当需要移动端和PC端同时发送待办时，可以在apptype=1或者2同时携带PC待办信息。  

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
      <td>mobileark.receiveevent</td>
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
      <td>ecid</td>
      <td>String</td>
      <td>是</td>
      <td>{1,20}</td>
      <td>机构标识(编码) ，不区分大小写</td>
   </tr>
   <tr>
      <td>loginId</td>
      <td>String[]</td>
      <td>是</td>
      <td>{1,36}</td>
      <td>登录帐号，非空字符串，不区分大小写</td>
   </tr>
   <tr>
      <td>appid</td>
      <td>String</td>
      <td>是</td>
      <td>{1,256}</td>
      <td>应用id，当为Exmobi应用时，填写Exmobi应用的ID，当为原生应用时，填写android应用的ID。当该应用暂未移动化时，所以填写一个应用的唯一标识</td>
   </tr>
   <tr>
      <td>appid_ios</td>
      <td>String</td>
      <td>是</td>
      <td>{0,256}</td>
      <td>当为原生应用是，填写ios的应用ID，否则填空字符串</td>
   </tr>
   <tr>
      <td>appid_pc</td>
      <td>String</td>
      <td>是</td>
      <td>{0,256}</td>
      <td>当此条代办存在PC端提示时，则填写应用ID ，任务类型的apptype均可以填写，允许一条待办同时提醒手机和PC</td>
   </tr>
   <tr>
      <td>appName</td>
      <td>String</td>
      <td>是</td>
      <td>{1,256}</td>
      <td>应用名称</td>
   </tr>
   <tr>
      <td>appType</td>
      <td>String</td>
      <td>是</td>
      <td>(1|2|3)</td>
      <td>应用类型，1：exmobi应用，2：原生应用 3.html5应用 4：仅PC侧提醒</td>
   </tr>
   <tr>
      <td>events</td>
      <td>Event[]</td>
      <td>是</td>
      <td>{1,*}</td>
      <td>事件列表</td>
   </tr>
</table>  

Event对象<font color="red">（title和summary至少存在其中一个）</font>  

<table>
   <tr>
      <td>业务参数</td>
      <td>类型</td>
      <td>是否必须</td>
      <td>字段约束</td>
      <td>说明</td>
   </tr>
   <tr>
      <td>title</td>
      <td>String</td>
      <td>是</td>
      <td>{0,128}</td>
      <td>标题</td>
   </tr>
   <tr>
      <td>summary</td>
      <td>String</td>
      <td>是</td>
      <td>{0,512}</td>
      <td>摘要</td>
   </tr>
   <tr>
      <td>scheme</td>
      <td>String</td>
      <td>否</td>
      <td>{0,1024}</td>
      <td>应用启动传参，支持${username}、${password}、${token}等变量。例如：usename=${username}&password=${password}&module=1;<br/>html5应用时为地址：例如https://www.baidu.cm</td>
   </tr>
   <tr>
      <td>pcscheme</td>
      <td>String</td>
      <td>否</td>
      <td>{0,1024}</td>
      <td>当本待办支持PC外链时，系统会获取PC应用的访问协议、地址端口，拼接该参数，如下填写该项，支持${username}、${token}等变量替换。例如：index.html?usename=${username}&password=${password}&module=1</td>
   </tr>
   <tr>
      <td>eventId</td>
      <td>String</td>
      <td>否</td>
      <td>{1,36}</td>
      <td>待办唯一ID，用于主动取消待办</td>
   </tr>
   <tr>
      <td>param</td>
      <td>String</td>
      <td>否</td>
      <td>{0,512}</td>
      <td>待办提醒扩展参数，使用Base64编码。非空时，解码后的参数必须为json格式。</td>
   </tr>
</table>  

param说明：  

该参数用于摘要的扩展信息展示，使用json格式存储，json格式为{“summaryextend”:[“创建人：aaaa”,”状态：xxxx”]}。  

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
</table>  

<h2 id="cid_4">取消待办事件1.0</h2>  

<font color="red">4.2及以后版本支持</font>  

说明：此接口开启签名验证。<font color="red">（3.1.0以后版本支持机构编码和登录帐号不区分大小写）</font>  

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
      <td>mobileark.cancelevent</td>
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
      <td>loginId</td>
      <td>String[]</td>
      <td>否</td>
      <td>{1,36}</td>
      <td>登录帐号，非空字符串，不区分大小写</td>
   </tr>
   <tr>
      <td>eventId</td>
      <td>String[]</td>
      <td>是</td>
      <td>[a-zA-Z0-9_-]{1,36}</td>
      <td>取消待办的ID列表</td>
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
</table>  

请求响应报文：  

Post请求体  

```
sign=6596199D831373B9BBD2142F52C4936918135DFE&ecid=default&v=1.0&loginId=chenjiajia&eventId=123455&locale=zh_CN&method=mobileark.cancelevent&format=json&appKey=mos
```  

响应体  

```javascript
{"resultCode":"1","failloginid":[]}
```

