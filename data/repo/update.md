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
### 2、批量发布数据

- **请求URL**
> [api/v1/data/repo/record/publish](#)

- **请求方式** 

> *** PUT *** 

- **请求参数**

| 请求参数      |     参数类型 |   参数说明   |
| -------------| -------------| ------ |
|batch_id      |array          |文件存儲ID数组，整数类型|

- **返回参数**

| 返回参数      |     参数类型 |   参数说明   |
| -------- | --------| ------ |
| errCode|   Integer|  错误码,正常为0|
| errMsg|   string|  执行结果code|
| data  |  Integer|发布成功的数量|
- **返回示例**  

```json
{
  "errCode":0,
  "errMsg":"",
  "data":1
}
```

### 3、修改数据

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
| id        | Integer | 数据存储ID           |
| name      | string   | 文件名               |
| owner     | string   | 所有者名称           |
| creator   | string   | 创建者名称           |
| file_type | string   | 文件类型             |
| file_ver  | string   | 文件版本             |
| description  | string   | 文件描述          |
| create_at | Integer | 创建时间，时间戳格式 |
| update_at | Integer | 更新时间，时间戳     |
| size      | Integer | 文件大小byte         |
| path      | string   | 文件路径             |
- **返回示例**  

```json
{
  "errCode":0,
  "errMsg":"",
  "data":{
    "id": 18,
    "name": "boston_house_prices.csv",
    "owner": "public",
    "creator": "chenjiear",
    "size": 0,
    "path": "data/chenjiear/boston_house_prices_v1.csv",
    "fileType": "文本",
    "fileVer": "v1",
    "description": "fdas324r2134234",
    "repoId": null,
    "sourceId": null,
    "createAt": 1608630957376,
    "updateAt": 1608635743824
  }
}
```



