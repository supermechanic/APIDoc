### 1、上传数据

- **请求URL**
> [api/v1/data/repo/record](#)

- **请求方式** 

> *** POST *** 

- **请求参数**

| 请求参数      |     参数类型 |   参数说明   |
| -------- | --------| ------ |
|file          |file          |文件内容,form-data|
|file_ver    |string          |文件版本,form-data|
|file_type   |string          |文件类型,form-data|
|file_dscb   |string          |文件描述,form-data|

- **返回参数**

| 返回参数      |     参数类型 |   参数说明   |
| -------- | --------| ------ |
| errCode|   Integer|  错误码,正常为0|
| errMsg|   string|  执行结果code|
| data|   object|  返回数据|
| id| Integer|数据存储ID|
| name|string|文件名|
| owner|string|所有者名称|
| creator |string |创建者名称|
| create_at|Integer|创建时间，时间戳格式|
| description  | string   | 文件描述          |
| size|Integer|文件大小，kb|
| path|string |文件路径|

- **返回示例**  

```json
{
    "errCode": 0,
    "errMsg": "OK",
    "data": {
        "id": 26,
        "name": "boston_house_prices.csv",
        "owner": "chenjiear",
        "creator": "chenjiear",
        "size": 34742,
        "path": "data/chenjiear/boston_house_prices_v3.csv",
        "fileType": "文本",
        "fileVer": "v3",
        "description": "fdas324r2134234",
        "repoId": null,
        "sourceId": null,
        "createAt": 1608690101275,
        "updateAt": 1608690101275
    }
}
```