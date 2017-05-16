# 发布结果接口

----------  

请求地址：http://ip:port/uploadresult  

第三方服务发布和应用发布结果接口。  

Post请求，请求体为json格式：  

<table>
   <tr>
      <td>参数</td>
      <td>类型</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>operateIds</td>
      <td>List<string></td>
      <td>工单号</td>
   </tr>
   <tr>
      <td>appKey</td>
      <td>string</td>
      <td>接入id</td>
   </tr>
   <tr>
      <td>timeStamp</td>
      <td>string</td>
      <td>时间戳 yyyymmddHHmmss</td>
   </tr>
   <tr>
      <td>sign</td>
      <td>string</td>
      <td>签名 值为appKey+timeStamp+secret 做MD5摘要</td>
   </tr>
</table>  

响应体：json格式：  

<table>
   <tr>
      <td>参数</td>
      <td>类型</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>resultCode</td>
      <td>string</td>
      <td>返回码 0成功 -1：系统正忙，请稍后再试！</td>
   </tr>
   <tr>
      <td>resultMessage</td>
      <td>string</td>
      <td>查询成功</td>
   </tr>
   <tr>
      <td>operateInfos</td>
      <td>List<OperateInfo></td>
      <td></td>
   </tr>
</table>  

OperateInfo对象：  

<table>
   <tr>
      <td>参数</td>
      <td>类型</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>operateId</td>
      <td>是</td>
      <td>工单号</td>
   </tr>
   <tr>
      <td>operateStatus</td>
      <td>是</td>
      <td>工单状态 0,1,-1</td>
   </tr>
   <tr>
      <td>operateMessage</td>
      <td>是</td>
      <td>结果描述<br/>0：成功<br/> 1：处理中<br/>-1：失败</td>
   </tr>
   <tr>
      <td>startTime</td>
      <td>是</td>
      <td>开始时间</td>
   </tr>
   <tr>
      <td>endTime</td>
      <td>是</td>
      <td>结束时间（处理中时为空）</td>
   </tr>
</table>