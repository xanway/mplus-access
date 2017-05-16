# 个人文档接口

----------  

<font color="red">4.0及以后版本支持</font>  

<h2 id="cid_0">获取文档列表1.0</h2>  

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
      <td>mobileark.getpersondocs</td>
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
      <td>机构标识(编码) ，不区分大小写</td>
   </tr>
   <tr>
      <td>userUuid</td>
      <td>String</td>
      <td>是</td>
      <td>{1,36}</td>
      <td>用户标识</td>
   </tr>
   <tr>
      <td>folderId</td>
      <td>String</td>
      <td>否</td>
      <td>{0,36}</td>
      <td>当为-1时，获取根企业目录。默认为-1</td>
   </tr>
   <tr>
      <td>folderNameSearch</td>
      <td>String</td>
      <td>否</td>
      <td>{0,200}</td>
      <td>文件名检索</td>
   </tr>
   <tr>
      <td>sort</td>
      <td>String</td>
      <td>否</td>
      <td>(0|1)</td>
      <td>0为升序，1为降序；默认为0</td>
   </tr>
   <tr>
      <td>sortName</td>
      <td>String</td>
      <td>否</td>
      <td>(0|1|2)</td>
      <td>0 大小 1 时间 2 名称 默认2</td>
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
      <td>documentList</td>
      <td>DocumentList[]</td>
      <td>用户文件列表</td>
   </tr>
   <tr>
      <td>folderList</td>
      <td>FolderList[]</td>
      <td>文件夹列表</td>
   </tr>
</table>  

FolderList对象  

<table>
   <tr>
      <td>参数</td>
      <td>类型</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>folderId</td>
      <td>String</td>
      <td>文件夹ID</td>
   </tr>
   <tr>
      <td>folderName</td>
      <td>String</td>
      <td>文件夹名称</td>
   </tr>
   <tr>
      <td>createTime</td>
      <td>String</td>
      <td>创建时间 YYYY-MM-DD HH-mm-ss</td>
   </tr>
</table>  

DocumentList对象  

<table>
   <tr>
      <td>参数</td>
      <td>类型</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>documentName</td>
      <td>String</td>
      <td>文件名称</td>
   </tr>
   <tr>
      <td>documentId</td>
      <td>String</td>
      <td>文件id</td>
   </tr>
   <tr>
      <td>type</td>
      <td>String</td>
      <td>jpg、png….</td>
   </tr>
   <tr>
      <td>folderId</td>
      <td>String</td>
      <td>上级文件夹ID</td>
   </tr>
   <tr>
      <td>createTime</td>
      <td>String</td>
      <td>文件创建时间</td>
   </tr>
   <tr>
      <td>size</td>
      <td>String</td>
      <td>文件大小，单位K </td>
   </tr>
   <tr>
      <td>documentDesc</td>
      <td>String</td>
      <td>文件摘要</td>
   </tr>
   <tr>
      <td>documentCreator</td>
      <td>String</td>
      <td>文件上传者</td>
   </tr>
</table>  

<h2 id="cid_1">获取预览/下载地址1.0</h2>  

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
      <td>mobileark.getdocurl</td>
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
      <td>documentId</td>
      <td>String</td>
      <td>是</td>
      <td>{1,36}</td>
      <td>文档标识</td>
   </tr>
   <tr>
      <td>type</td>
      <td>String</td>
      <td>否</td>
      <td>（0|1）</td>
      <td>0-获取文档下载地址，1-获取文档预览地址，默认为0</td>
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
      <td>docUrls</td>
      <td>String[]</td>
      <td>当type=0时，为文件下载地址，type=1时，为预览地址</td>
   </tr>
</table>  