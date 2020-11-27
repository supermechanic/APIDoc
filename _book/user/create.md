## 用户接口文档##

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
| success|   boolean|  请求成功与否|
| code|   Integer|  执行结果code|
| message|   String|  执行结果消息|

- **返回示例**
>    
```
{
  "success": true,
  "code": 200,
  "message": "操作正确"
}
```