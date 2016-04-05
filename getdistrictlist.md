# getDistrictList

#### Description
get district list by city ID

#### 请求是否要认证
NO


#### Resquet Method
GET
#### Request Parameters

| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| city_id | Int | YES |  | city ID: obtain by api getOpenCityList |



#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Response | JSON | YES| | district list


#### Request Example
POST
|Request URL | "http://112.74.81.48/zhihuieducation/location/getDistrictList" |
| city_id| -- |
{'city_id':1}

#### Response Example

```
[
    {
        "district_id": "1769",
        "district_name": "罗湖区"
    },
    {
        "district_id": "1770",
        "district_name": "福田区"
    },
    {
        "district_id": "1771",
        "district_name": "南山区"
    },
    {
        "district_id": "1772",
        "district_name": "宝安区"
    },
    {
        "district_id": "1773",
        "district_name": "龙岗区"
    },
    {
        "district_id": "1774",
        "district_name": "盐田区"
    }
]
```



