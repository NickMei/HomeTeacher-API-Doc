# getCityList

#### Description
get city list by province ID
#### Resquet Method
GET
#### Request Parameters

| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| provinceID | String | YES |  | province ID: obtain by api getProvinceList |



#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Response | JSON | YES| | city list


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/location/getCityList?provinceID=19" |
| --| -- |


#### Response Example

```
[
    {
        "CityID": "197",
        "CityName": "广州市"
    },
    {
        "CityID": "198",
        "CityName": "韶关市"
    },
    {
        "CityID": "199",
        "CityName": "深圳市"
    },
    {
        "CityID": "200",
        "CityName": "珠海市"
    },
    {
        "CityID": "201",
        "CityName": "汕头市"
    },
    {
        "CityID": "202",
        "CityName": "佛山市"
    },
    {
        "CityID": "203",
        "CityName": "江门市"
    },
    {
        "CityID": "204",
        "CityName": "湛江市"
    },
    {
        "CityID": "205",
        "CityName": "茂名市"
    },
    {
        "CityID": "206",
        "CityName": "肇庆市"
    },
    {
        "CityID": "207",
        "CityName": "惠州市"
    },
    {
        "CityID": "208",
        "CityName": "梅州市"
    },
    {
        "CityID": "209",
        "CityName": "汕尾市"
    },
    {
        "CityID": "210",
        "CityName": "河源市"
    },
    {
        "CityID": "211",
        "CityName": "阳江市"
    },
    {
        "CityID": "212",
        "CityName": "清远市"
    },
    {
        "CityID": "213",
        "CityName": "东莞市"
    },
    {
        "CityID": "214",
        "CityName": "中山市"
    },
    {
        "CityID": "215",
        "CityName": "潮州市"
    },
    {
        "CityID": "216",
        "CityName": "揭阳市"
    },
    {
        "CityID": "217",
        "CityName": "云浮市"
    }
]
```



