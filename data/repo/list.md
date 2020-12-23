### 1、获取所有数据

- **请求URL**
> [api/v1/data/repo/record/list](#)

- **请求方式** 

> *** POST *** 

- **请求参数**

| 请求参数 | 参数类型 | 参数说明             |
| -----------| -------- | -------------------- |
| currentPage| Integer | 文件内容,application/json, body|
| pageSize   | Integer | 文件名称，包含后缀名,application/json, body |
| search     | string   | 检索关键词，当前版本呢只支持文件名,application/json, body|
| owner      | string   | 所有者名称，数据仓库请求使用public,字段为空时查询,application/json, body当前用户|
- **返回参数**

| 返回参数  | 参数类型 | 参数说明             |
| --------- | -------- | -------------------- |
| errCode   | Integer  | 错误码,正常为0       |
| errMsg    | string   | 执行结果code         |
| data      | object   | 返回数据             |
| id        | Integer | 数据存储ID           |
| name      | string   | 文件名               |
| owner     | string   | 所有者名称           |
| file_type | string   | 文件类型             |
| file_ver  | string   | 文件版本             |
| description  | string   | 文件描述             |
| creator   | string   | 创建者名称           |
| create_at | Integer | 创建时间，时间戳格式 |
| update_at | Integer | 更新时间，时间戳     |
| size      | Integer | 文件大小byte         |
| path      | string   | 文件路径            |

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
            "file_type":"文本",
            "file_ver":"v1",
            "description":"",
            "owner":"",
            "creator":"tester1",
            "create_at":1606443441,
            "size":123123,
            "path":"/bucket/filename"
        },
        {
            "id":2,
            "name":"test2.csv",
            "file_type":"文本",
            "file_ver":"v1",
            "description":"",
            "owner":"",
            "creator":"tester2",
            "create_at":1606443441,
            "size":123123,
            "path":"/bucket/filename"
        },
        {
            "id":3,
            "name":"test3.csv",
            "file_type":"文本",
            "file_ver":"v1",
            "description":"",
            "owner":"",
            "creator":"tester1",
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
> [api/v1/data/repo/{id}](#)

- **请求方式** 

> *** GET *** 

- **请求参数**

| 请求参数 | 参数类型 | 参数说明   |
| -------- | -------- | ---------- |
| id       | Integer  | 文件存储ID,pathparam |

- **返回参数**

| 返回参数  | 参数类型 | 参数说明             |
| --------- | -------- | -------------------- |
| errCode   | Integer  | 错误码,正常为0       |
| errMsg    | string   | 执行结果code         |
| data      | object   | 返回数据             |
| id        | Integer | 数据存储ID           |
| name      | string   | 文件名               |
| owner     | string   | 所有者名称           |
| file_type | string   | 文件类型             |
| file_ver  | string   | 文件版本             |
| description  | string   | 文件描述             |
| creator   | string   | 创建者名称           |
| create_at | Integer | 创建时间，时间戳格式 |
| update_at | Integer | 更新时间，时间戳     |
| size      | Integer | 文件大小byte         |
| path      | string   | 文件路径            |

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
    "description":"",
    "owner":"",
    "creator":"tester1",
    "create_at":1606443441,
    "size":123123,
    "path":"/bucket/filename"
  }
}
```