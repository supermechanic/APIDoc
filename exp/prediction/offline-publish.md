### 1、新建离线预测

- **请求URL**
> [api/v1/predict/publish/offline](#)

- **请求方式** 

> POST

- **请求参数**

| 请求参数      |     参数类型 |   参数说明   |
| -------- | --------| ------ |
|predict_name|string |预测名称,不可重复|
|model_id| string | 模型列表返回的模型对应的ID|
|data_id|Integer |数据ID|
|creator| String |创建者|

- **请求示例**  
```json
{
    "model_id":"",
    "data_id":1,
    //服务名称
    "predict_name":"",
    "creator":"ddd",
}
```

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