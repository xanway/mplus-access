# 服务发布接口

----------  

请求地址：http://ip:port/uploadservice  

第三方将应用与资源文件发送到上述地址：其中appkey为从mplus申请的账号，secret为密码。  

遵循mime的多媒体格式上传。  

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
      <td>service_id</td>
      <td>是</td>
      <td>服务id，必须和servicezip中解压的相同</td>
   </tr>
   <tr>
      <td>app_key</td>
      <td>是</td>
      <td>接入id</td>
   </tr>
   <tr>
      <td>timestamp</td>
      <td>是</td>
      <td>时间戳 yyyymmddHHmmss</td>
   </tr>
   <tr>
      <td>sign</td>
      <td>是</td>
      <td>签名值为ecid+ service_id+app_key+timestamp+app_type+secret 做MD5摘要</td>
   </tr>
   <tr>
      <td>app_type</td>
      <td>是</td>
      <td>服务类型 1：exmobi服务</td>
   </tr>
   <tr>
      <td>description</td>
      <td>是</td>
      <td>服务描述</td>
   </tr>
   <tr>
      <td>service_attachment</td>
      <td>是</td>
      <td>服务的zip包</td>
   </tr>
   <tr>
      <td>service_operatetype</td>
      <td>是</td>
      <td>操作类型 1 发布（升级），2 修改， 3 删除</td>
   </tr>
   <tr>
      <td>operateId</td>
      <td>是</td>
      <td>操作工单号service_operatetype（1，2时有效）</td>
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
      <td>serviceid</td>
      <td>string</td>
      <td>服务ID，服务在系统中的唯一标示</td>
   </tr>
</table>  