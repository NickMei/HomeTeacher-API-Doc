#getCity
#### Description
获取用户的位置信息

#### 请求是否要认证
YES

#### Resquet Method
POST

#### Request Parameters (Body) 空对象JSON

| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
####  示例程序（空对象JSON）：
#####   var query_obj = {};


#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Response | JSON | YES| | Response |


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/location/getCity" |
| --| -- |
| | |

#### Response Example

#####只有retcode 为0 才是成功响应，其他都是错误响应
```
{
    retcode: 0, 
    retmsg: "成功请求！",
    response: {
        "city_id" :  "123",
        "city" :  "深圳"
    }
}

其他错误响应情况

{
    retcode: 1, 
    retmsg: "错误",
    response: {
    }
}


可能是丢失数据，或者token无效或者过期，提示用户重新登陆
{
    retcode: 2, 
    retmsg: "验证无法通过，请重新登陆",
    response: {
    }
}
```



