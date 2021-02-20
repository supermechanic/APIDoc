### 1、新建在线预测

- **请求URL**
> [api/v1/predict/online/id/{id}/type/{type}](#)

- **请求方式** 

> DELETE

- **请求参数**

| 请求参数      |     参数类型 |   参数说明   |
| -------- | --------| ------ |
|id        |Integer|记录id|
|type      |Integer|0,删除；1,停止

- **请求示例**  

url/api/v1/predict/online/id/2/type/1

- **返回参数**

| 返回参数      |     参数类型 |   参数说明   |
| -------- | --------| ------ |
|code      |int      |错误码|
|message   |string   |错误信息|

- **返回示例**  

```json
{
    "code":0,
    "message":"success"
}

{
    "code":0,
    "message":"internal error"
}
```