## 数据仓库接口文档##

[TOC]

### 1、新增用户

- **请求URL**
> [api/v1/user](#)

- **请求方式** 
>**POST**

- **请求参数**
>
| 请求参数      |     参数类型 |   参数说明   |
| :-------- | :--------| :------ |
| username|  <mark>varchar(20),**不可为空**</mark>|  用户名|
| password|  <mark>varchar(20),**不可为空**</mark>|  用户密码|

- **返回参数**
>
| 返回参数      |     参数类型 |   参数说明   |
| :-------- | :--------| :------ |
| errCode|   Integer|  错误码,正常为0|
| errMsg|   string|  执行结果code|
| data|   object|  返回数据|
| id| Interger|数据存储ID|
| name|string|文件名|
| owner|string|创建者名称|
| create_at|Interger|创建时间，时间戳格式|
| size|Interger|文件大小，kb|
| path|string |文件路径|

- **返回示例**
>    
```json
{
  "errCode":0,
  "errMsg":"",
  "data":{
    "id":1,
    "name":"test.csv",
    "owner":"tester1",
    "create_at":1606443441,
    "size":123123,
    "path":"/bucket/filename"
  }
}
```