### 1、刪除数据

- **请求URL**
> [api/v1/data/repo/record/{id}](#)

- **请求方式** 

> *** DELETE *** 

- **请求参数**

| 请求参数      |     参数类型 |   参数说明   |
| -------- | --------| ------ |
|id          |Integer          |文件存儲ID,pathparam|

- **返回参数**

| 返回参数      |     参数类型 |   参数说明   |
| -------- | --------| ------ |
| errCode|   Integer|  错误码,正常为0|
| errMsg|   string|  执行结果code|
| data|   object|  返回数据|

- **返回示例**  

```json
{
  "errCode":0,
  "errMsg":"",
  "data":null
}
```

### 2、批量刪除数据

- **请求URL**
> [api/v1/data/repo/record](#)

- **请求方式** 

> *** DELETE *** 

- **请求参数**

| 请求参数      |     参数类型 |   参数说明   |
| -------- | --------| ------ |
|batch_id  |array    |文件存儲ID数组，整数类型,application/json, body|

- **返回参数**

| 返回参数      |     参数类型 |   参数说明   |
| -------- | --------| ------ |
| errCode|   Integer|  错误码,正常为0|
| errMsg|   string|  执行结果code|
| data|   object|  返回数据,删除成功的数量|

- **返回示例**  

```json
{
  "errCode":0,
  "errMsg":"ok",
  "data":2
}
```