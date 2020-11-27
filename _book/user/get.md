### 1、获取用户信息

- **请求URL**
> [api/v1/user/{id}/](#)

- **请求方式** 
>**GET**

- **请求参数**
>
| 请求参数      |     参数类型 |   参数说明   |
| :-------- | :--------| :------ |
| id| Integer| 用户ID|

- **返回参数**
>
| 返回参数      |     参数类型 |   参数说明   |
| :-------- | :--------| :------ |
| success|   boolean|  请求成功与否|
| code|   Integer|  执行结果code|
| message|   String|  执行结果消息|
| data| Object| 执行结果集|

- **返回示例**
>    
```
{
  "success": true,
  "code": 200,
  "message": "操作正确",
  "data":{
    "user_id":1,
    "username":"XXX",
  }
}
```