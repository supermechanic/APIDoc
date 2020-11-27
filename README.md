# 项目简介

金融大脑项目后端API，包含前台后台页面
### 错误码

#### 通用表1

|HTTP状态码  |错误码(Error Code) 	   |错误消息(Error Message) 	                                        |描述(Description)|
|:---------:|:-----------------------|:------------------------------------------------------------------|:-----------------|
|411 	    |MissingContentLength 	 |Content-Length does not exist in http header when it is necessary. |没有提供必须的Content-Length请求头|
|415 	    |InvalidContentType 	 |Content-Type {type} is unsupported.                                |不支持Content-Type指定的类型|
|400 	    |MissingContentType 	 |Content-Type does not exist in http header when body is not empty. |没有为Body不为空的HTTP请求指定Content-T|
|400 	    |MissingBodyRawSize 	 |x-log-bodyrawsize does not exist in header when it is necessary. 	 |压缩场景下没有提供必须的x-log-bodyr|
|400 	    |InvalidBodyRawSize 	 |x-log-bodyrawsize is invalid. 	                                 |x-log-bodyrawsize的值无效|
|400 	    |InvalidCompressType 	 |x-log-compresstype {type} is unsupported. 	                     |x-log-compresstype指定的压缩方式不支持|
|400 	    |MissingHost 	         |Host does not exist in http header. 	                             |没有提供HTTP标准请求头Host|
|400 	    |MissingDate 	         |Date does not exist in http header. 	                             |没有提供HTTP标准请求头Date|
|400 	    |InvalidDateFormat 	     |Date {date} must follow RFC822. 	                                 |Date请求头的值不符合RFC822标准|
|400 	    |MissingAPIVersion 	     |x-log-apiversion does not exist in http header. 	                 |没有提供HTTP请求头x-log-apiversion|
|400 	    |InvalidAPIVersion 	     |x-log-apiversion {version} is unsupported. 	                     |HTTP请求头x-log-apiversion的值不支持|
|400 	    |MissAccessKeyId 	     |x-log-accesskeyid does not exist in header. 	                     |没有在Authorization头部提供AccessKeyId|
|401 	    |Unauthorized 	         |The AccessKeyId is unauthorized. 	                                 |提供的AccessKeyId值未授权|
|400 	    |MissingSignatureMethod  |x-log-signaturemethod does not exist in http header. 	             |没有提供HTTP请求头 x-log-signaturemethod| 
|400 	    |InvalidSignatureMethod  |signature method {method} is unsupported. 	                     |x-log-signaturemethod头部|
|400 	    |RequestTimeTooSkewed 	 |Request time exceeds server time more than 15 minutes.           	 |请求的发送时间超过当前服务处理时|
|404 	    |ProjectNotExists 	     |Project {name} does not exist. 	                                 |日志项目（Project）不存在|
|401 	    |SignatureNotMatch 	     |Signature {signature} is not matched. 	                         |请求的数字签名不匹配|
|403 	    |WriteQuotaExceed 	     |Write quota is exceeded. 	                                         |超过写入日志限额|
|403 	    |ReadQuotaExceed 	     |Read quota is exceeded. 	                                         |超过读取日志限额|
|500 	    |InternalServerError 	 |Internal server error message.                                   	 |服务器内部错误|
|503 	    |ServerBusy 	         |The server is busy, please try again later. 	                     |服务器正忙，请稍后再试|