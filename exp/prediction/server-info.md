 ### 1、预测协议

- **请求URL**
> [api/v1/predict/protocol](#)

- **请求方式** 

> GET 

- **请求参数**

无

- **请求示例**  
```json
{}
```
- **返回参数**

| 返回参数      |     参数类型 |   参数说明   |
| -------- | --------| ------ |
|code      |int      |错误码|
|message   |string   |错误信息|
|data      |map      |协议列表信息,key为协议名称，value为协议ID|

- **返回示例**  

```json
{
    "code": 0,
    "message": "",
    "data": {
        "SeldonCoreV1": 1,
        "SeldonCoreV1Alpha1": 2,
        "SeldonCoreV1Alpha2": 3
    }
}
```

### 2、预测框架及参数

- **请求URL**
> [api/v1/predict/params](#)

- **请求方式** 

> GET

- **请求参数**

无

- **请求示例**  
```json
{}
```

- **返回参数**

| 返回参数      |     参数类型 |   参数说明   |
| -------- | --------| ------ |
|code      |int      |错误码|
|message   |string   |错误信息|
|data      |map      |server信息，key为serverID，value为server信息|
|name      |string   |server名称|
|params    |map      |参数信息，key为ID，value为参数信息结构体|
|name      |string   |参数名称|
|type      |string   |参数类型|
|values    |map      |可选参数值|
- **返回示例**  

```json
{
    "code": 0,
    "message": "ok",
    "data": {
        "1": {
            "name": "SKLEARN_SERVER",
            "params": {
                "1": {
                    "name": "method",
                    "type": "STRING",
                    "values": {
                        "1": "predict",
                        "2": "predict_prob:default",
                        "3": "dicision_function"
                    }
                }
            }
        },
        "2": {
            "name": "TENSORFLOW_SERVER",
            "params": {}
        }
    }
}
```