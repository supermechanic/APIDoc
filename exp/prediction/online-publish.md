### 1、新建在线预测

- **请求URL**
> [api/v1/predict/publish/online](#)

- **请求方式** 

> POST

- **请求参数**

| 请求参数      |     参数类型 |   参数说明   |
| -------- | --------| ------ |
|service_name|string |服务名称,不可重复，seldon对名称规则有限制|
|model_id| string | 模型列表返回的模型对应的ID|
|protocol|Integer |选择的协议对应的ID|
|params| Map|选择模型的参数，key为parameter的ID，value为parameter的value的ID|

- **请求示例**  
```json
{
    "model_id":"",
    "protocol":1,
    //服务名称
    "service_name":"",
    "params":{
        //代表参数1选择了值1，就是 method 的值为 predict
        "1":1,
        //暂时没有参数2，这里表示可以同时有多个参数
        "2":1

    }
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