### 1、获取所有数据

- **请求URL**
> [api/v1/data/repo](#)

- **请求方式** 

> *** GET *** 

- **请求参数**

| 请求参数 | 参数类型 | 参数说明             |
| -----------| -------- | -------------------- |
| currentPage| Interger | 文件内容             |
| pageSize   | Interger | 文件名称，包含后缀名 |
| search     | string   | 检索关键词，当前版本呢只支持文件名|
- **返回参数**

| 返回参数  | 参数类型 | 参数说明             |
| --------- | -------- | -------------------- |
| errCode   | Integer  | 错误码,正常为0       |
| errMsg    | string   | 执行结果code         |
| data      | object   | 返回数据             |
| id        | Interger | 数据存储ID           |
| name      | string   | 文件名               |
| owner     | string   | 创建者名称           |
| create_at | Interger | 创建时间，时间戳格式 |
| size      | Interger | 文件大小，kb         |
| path      | string   | 文件路径             |

- **返回示例**  

```json
{
  "errCode":0,
  "errMsg":"",
  "data":{
    "list":[
        {
            "id":1,
            "name":"test.csv",
            "owner":"tester1",
            "create_at":1606443441,
            "size":123123,
            "path":"/bucket/filename"
        },
        {
            "id":2,
            "name":"test2.csv",
            "owner":"tester2",
            "create_at":1606443441,
            "size":123123,
            "path":"/bucket/filename"
        },
        {
            "id":3,
            "name":"test3.csv",
            "owner":"tester1",
            "create_at":1606443441,
            "size":123123,
            "path":"/bucket/filename"
        },
    ],
    "total":100
    
  }
}
```

### 2、使用ID获取文件信息

- **请求URL**
> [api/v1/data/repo](#)

- **请求方式** 

> *** GET *** 

- **请求参数**

| 请求参数 | 参数类型 | 参数说明   |
| -------- | -------- | ---------- |
| id       | Integer  | 文件存储ID |

- **返回参数**

| 返回参数  | 参数类型 | 参数说明             |
| --------- | -------- | -------------------- |
| errCode   | Integer  | 错误码,正常为0       |
| errMsg    | string   | 执行结果code         |
| data      | object   | 返回数据             |
| id        | Interger | 数据存储ID           |
| name      | string   | 文件名               |
| owner     | string   | 创建者名称           |
| create_at | Interger | 创建时间，时间戳格式 |
| size      | Interger | 文件大小，kb         |
| path      | string   | 文件路径             |

- **返回示例**  

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