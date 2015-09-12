#getOpenCityList
#### Description
请求已开通城市列表

#### 请求是否要认证
NO

#### Resquet Method
POST

#### Request Header 请求头中传的参数
无

#### Request Parameters (Body) 
无


#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Response | JSON | YES| | Response |


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/location/getOpenCityList" |
| --| -- |
| | |

#### Response Example

#####只有retcode 为0 才是成功响应，其他都是错误响应
```
{
    "retcode": 0,
    "retmsg": "请求成功！",
    "response": {
        "city_list": [
            "深圳",
            "广州",
            "重庆",
            "东莞",
            "惠州",
            "珠海"
        ]
    }
}

其他错误响应情况

{
    retcode: 1, 
    retmsg: "错误",
    response: {
    }
}


```



