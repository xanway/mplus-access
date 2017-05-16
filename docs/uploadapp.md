# 应用发布接口

----------  

请求地址：http://ip:port/uploadapp  

请求采用mime的格式  

请求参数：  

<table>
   <tr>
      <td>参数</td>
      <td>必填项</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>ecid</td>
      <td>是</td>
      <td>企业ID</td>
   </tr>
   <tr>
      <td>app_id</td>
      <td>是</td>
      <td>应用ID，必须和下面发布的ID相同，hmtl5应用填空</td>
   </tr>
   <tr>
      <td>app_name</td>
      <td>是</td>
      <td>应用名称</td>
      <td></td>
   </tr>
   <tr>
      <td>app_version</td>
      <td>是</td>
      <td>应用版本</td>
   </tr>
   <tr>
      <td>app_key</td>
      <td>是</td>
      <td>接入id</td>
   </tr>
   <tr>
      <td>timestamp</td>
      <td>是</td>
      <td>时间戳 yyyymmddHHmmss 5分钟有效</td>
   </tr>
   <tr>
      <td>sign</td>
      <td>是</td>
      <td>签名 值为ecid+app_id+app_key+timestamp+app_type+secret 做MD5摘要</td>
   </tr>
   <tr>
      <td>app_type</td>
      <td>是</td>
      <td>应用类型 1：exmobi，2：android，3：ios，4：html5 5：iosappstore</td>
   </tr>
   <tr>
      <td>app_htmlModule</td>
      <td>是</td>
      <td>html5应用类型，当app_type为4时必填，0：远程应用  1：本地应用</td>
   </tr>
   <tr>
      <td>app_hiddenbackbutton</td>
      <td>是</td>
      <td>html5应用类型，当app_type为4时必填，隐藏返回按钮</td>
   </tr>
   <tr>
      <td>app_ hiddenmenubutton</td>
      <td>是</td>
      <td>html5应用类型，当app_type为4时必填，隐藏菜单按钮</td>
   </tr>
   <tr>
      <td>app_ hiddenclosebutton</td>
      <td>是</td>
      <td>html5应用类型，当app_type为4时必填，隐藏关闭按钮</td>
   </tr>
   <tr>
      <td>app_path</td>
      <td>是</td>
      <td>html5应用地址或启动页，当app_htmlModule为0时，填应用地址，当为1时，填启动页名称</td>
   </tr>
   <tr>
      <td>appstore_url</td>
      <td>是</td>
      <td>ios appstore地址 当app_type为5时生效</td>
   </tr>
   <tr>
      <td>filesize</td>
      <td>是</td>
      <td>文件大小，当app_type为5时生效</td>
   </tr>
   <tr>
      <td>icon</td>
      <td>否</td>
      <td>图标附件，对应icon文件夹中图片名称，空则使用默认解析出来的图片</td>
   </tr>
   <tr>
      <td>description</td>
      <td>是</td>
      <td>应用描述</td>
   </tr>
   <tr>
      <td>support_osversion</td>
      <td>是</td>
      <td>最低操作系统版本，app_type为2,3时生效</td>
   </tr>
   <tr>
      <td>isTablet</td>
      <td>是</td>
      <td>支持性，1-平板，2-手机，3-平板、手机，4-PC，5-PC、平板，6-PC、手机，7-PC、平板、手机，其中app_type=1和4时，应用支持发布到PC</td>
   </tr>
   <tr>
      <td>silent_install</td>
      <td>是</td>
      <td>静默安装，当app_type为1、4时生效 0非静默 1静默</td>
   </tr>
   <tr>
      <td>deliver_param</td>
      <td>否</td>
      <td>启动传参，格式如 username=${username}&password=${password} 当app_type为1、2、3时生效</td>
   </tr>
   <tr>
      <td>native_app</td>
      <td>否</td>
      <td>存在原生应用，当app_type为1时生效，当值为1时，解析原生应用</td>
   </tr>
   <tr>
      <td>app_attachment</td>
      <td>是</td>
      <td>应用附件</td>
   </tr>
   <tr>
      <td>phone_android</td>
      <td>否</td>
      <td>android_phone的安装包</td>
   </tr>
   <tr>
      <td>phone_ios</td>
      <td>否</td>
      <td>phone_ios的安装包</td>
   </tr>
   <tr>
      <td>pad_android</td>
      <td>否</td>
      <td>pad_android的安装包</td>
   </tr>
   <tr>
      <td>pad_ios</td>
      <td>否</td>
      <td>pad_ios的安装包</td>
   </tr>
   <tr>
      <td>module</td>
      <td>否</td>
      <td>模块配置当app_type为1、2、3时生效，采用josn格式<br/>内容：{“moduleurl”:”xxxx”,” module_param”:”xxxx”,modules:[{“def_concern”:”1”,”mod_name”:”OA待办”,” mod_scheme”:”username=${username}”,”mod_img”:”img1”},{“def_concern”:”1”,”mod_name”:”请假申请”,” mod_scheme”:”username=${username}”,”mod_img”:”img1”}]}，其中mod_img中的值，作为请求参数的key，存放模块图片的多媒体格式</td>
   </tr>
   <tr>
      <td>phone_1,2,3,4,5</td>
      <td>否</td>
      <td>手机截图，最多5张，逐一按顺序从phone_1、phone_2、phone_3、phone_4、phone_5设置</td>
   </tr>
   <tr>
      <td>pad_1,2,3,4,5</td>
      <td>否</td>
      <td>平板截图，最多5张，逐一按顺序从phone_1、phone_2、phone_3、phone_4、phone_5设置</td>
   </tr>
   <tr>
      <td>app_operatetype</td>
      <td>是</td>
      <td>应用操作方式，1-新增应用，2-修改应用  3-删除应用</td>
   </tr>
   <tr>
      <td> operateId</td>
      <td>是</td>
      <td>操作工单号 app_operatetype（1，2时有效）</td>
   </tr>
</table>

响应内容，json格式：  

<table>
   <tr>
      <td>参数</td>
      <td>类型</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>resultcode</td>
      <td>string</td>
      <td>返回码 0成功 -1：系统正忙，请稍后再试！</td>
   </tr>
   <tr>
      <td>resultmessage</td>
      <td>String</td>
      <td>返回码说明</td>
   </tr>
   <tr>
      <td>appid</td>
      <td>string</td>
      <td>应用ID，应用在系统中的唯一标示</td>
   </tr>
</table>  

  