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
    response: {
      open_city_list: {
        0: {city_id: "199", city_name: "深圳市"}
        1: {city_id: "197", city_name: "广州市"}
        2: {city_id: "234", city_name: "重庆市"}
        3: {city_id: "213", city_name: "东莞市"}
    }
    retcode: "0"
    retmsg: "请求成功！"
}



其他错误响应情况

{
    retcode: 1, 
    retmsg: "错误",
    response: {
    }
}


```



