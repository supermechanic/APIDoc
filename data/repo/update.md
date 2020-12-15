### 1、发布数据

- **请求URL**
> [api/v1/data/repo/record/publish/{id}](#)

- **请求方式** 

> *** PUT *** 

- **请求参数**

| 请求参数      |     参数类型 |   参数说明   |
| -------------| -------------| ------ |
|id            |int          |数据记录ID|

- **返回参数**

| 返回参数      |     参数类型 |   参数说明   |
| -------- | --------| ------ |
| errCode|   Integer|  错误码,正常为0|
| errMsg|   string|  执行结果code|

- **返回示例**  

```json
{
  "errCode":0,
  "errMsg":"",
}
```

### 2、修改数据

- **请求URL**
> [api/v1/data/repo/record/{id}](#)

- **请求方式** 

> *** PUT *** 

- **请求参数**

| 请求参数      |     参数类型 |   参数说明   |
| -------------| -------------| ------ |
| id           |int          |数据记录ID|
| desb         |string       |描述      |
| file_ver     |string       |文件版本  |
| file_type    |string       |文件类型  |
- **返回参数**

| 返回参数      |     参数类型 |   参数说明   |
| -------- | --------| ------ |
| errCode|   Integer|  错误码,正常为0|
| errMsg|   string|  执行结果code|
| data      | object   | 返回数据             |
| id        | Interger | 数据存储ID           |
| name      | string   | 文件名               |
| owner     | string   | 所有者名称           |
| file_type | string   | 文件类型             |
| file_ver  | string   | 文件版本             |
| describe  | string   | 文件描述             |
| creater   | string   | 创建者名称           |
| create_at | Interger | 创建时间，时间戳格式 |
| size      | Interger | 文件大小byte         |
| path      | string   | 文件路径             |
- **返回示例**  

```json
{
  "errCode":0,
  "errMsg":"",
  "data":{
    "id":1,
    "name":"test.csv",
    "file_type":"文本",
    "file_ver":"v1",
    "describe":"",
    "owner":"",
    "creater":"tester1",
    "create_at":1606443441,
    "size":123123,
    "path":"/bucket/filename"
  }
}
```