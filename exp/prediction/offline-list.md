### 1、离线预测列表

- **请求URL**
> [api/v1/predict/offline](#)

- **请求方式** 

> POST

- **请求参数**

| 请求参数      |     参数类型 |   参数说明   |
| -------- | --------| ------ |
|current_page|Integer|当前页码|
|page_size|Integer|页面大小|
|condition  |String |检索条件|

- **请求示例**  
```json
{
    "current_page":1,
    "page_size":10,
    "condition":""
}
```

- **返回参数**

| 返回参数      |     参数类型 |   参数说明   |
| -------- | --------| ------ |
|code      |Integer      |错误码|
|message   |String   |错误信息|
|data      |Object   |返回数据|
|total     |Integer  |总记录数|
|list      |Array    |当前页数据|
|id        |Integer  |id|
|predict_name|string| 预测名称|
|model_path  |string| 模型地址|
|data_path   |string| 数据地址|
|store_path  |string| 存储地址|
|creator     |string| 创建者  |
|creat_time  |string| 创建时间|
|status      |string| 状态    |
- **返回示例**  

```json
{
    "code": 0,
    "messsage": "success",
    "data": {
        "total": 4,
        "list": [
            {}
        ]
    }
```