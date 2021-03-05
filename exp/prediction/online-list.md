### 1、在线预测列表

- **请求URL**
> [api/v1/predict/online](#)

- **请求方式** 

> POST

- **请求参数**

| 请求参数      |     参数类型 |   参数说明   |
| -------- | --------| ------ |
|current_page|Integer|当前页码|
|page_size|Integer|页面大小|
|condition  |String |检索条件|
|creator   |String |当前用户名|
- **请求示例**  
```json
{
    "current_page":1,
    "page_size":10,
    "condition":"",
    "creator":"mayxe"
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
|serviceName|String  |服务名称|
|creator   |String   |创建者|
|status    |string   |状态|
|serviceType|string |server|
|protocol  |string   |发布使用的新协议|
|time       |string  |时间  |
|address   |string   |服务地址|
|params    |Array    |参数列表|
- **返回示例**  

```json
{
    "code": 0,
    "messsage": "success",
    "data": {
        "total": 4,
        "list": [
            {
                "id": 1,
                "serviceName": "test-publish-iris",
                "creator": "",
                "status": "",
                "serviceType": "SKLEARN_SERVER",
                "protocol": "SeldonCoreV1",
                "time": "2021/02/07 03:23:14",
                "address": "",
                "params": []
            },
            {
                "id": 2,
                "serviceName": "test-publish-iris-v1",
                "creator": "",
                "status": "",
                "serviceType": "SKLEARN_SERVER",
                "protocol": "SeldonCoreV1",
                "time": "2021/02/07 09:02:57",
                "address": "",
                "params": []
            },
            {
                "id": 3,
                "serviceName": "test-publish-iris-v2",
                "creator": "",
                "status": "",
                "serviceType": "SKLEARN_SERVER",
                "protocol": "SeldonCoreV1",
                "time": "2021/02/08 02:40:07",
                "address": "",
                "params": []
            },
            {
                "id": 4,
                "serviceName": "test-publish-iris-v3",
                "creator": "",
                "status": "",
                "serviceType": "SKLEARN_SERVER",
                "protocol": "SeldonCoreV1",
                "time": "2021/02/08 12:04:51",
                "address": "",
                "params": []
            }
        ]
    }
```