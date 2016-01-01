# getPriceRangeList


#### Description
获取教师搜索条件的价格区间列表

#### 请求是否要认证
NO

#### Resquet Method
POST

#### Request Parameters
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |



#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Response | JSON | YES| |   |


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/tutorinfo/getPriceRangeList" |
| --| -- |


#### Response Example

```
{
    "retcode":"0",
    "retmsg":"成功请求",
    "response":[
        {
            "range":"不限",
            "price_min":"all",
            "price_max":"all"
        },
        {
            "range":"￥0-100",
            "price_min":"0",
            "price_max":"100"
        },
        {
            "range":"￥100-200",
            "price_min":"100",
            "price_max":"200"
        },
        {
            "range":"￥200-300",
            "price_min":"200",
            "price_max":"300"
        },
        {
            "range":"￥300-500",
            "price_min":"300",
            "price_max":"500"
        },
        {
            "range":"￥500以上",
            "price_min":"500",
            "price_max":"all"
        }
    ]
}
```






