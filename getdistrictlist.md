# getDistrictList

#### Description
get district list by city ID
#### Resquet Method
GET
#### Request Parameters

| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| cityID | String | YES |  | city ID: obtain by api getCityList |



#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Response | JSON | YES| | district list


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/location/getDistrictList?cityID=199" |
| --| -- |


#### Response Example

```
[
    {
        "DistrictID": "1769",
        "DistrictName": "罗湖区"
    },
    {
        "DistrictID": "1770",
        "DistrictName": "福田区"
    },
    {
        "DistrictID": "1771",
        "DistrictName": "南山区"
    },
    {
        "DistrictID": "1772",
        "DistrictName": "宝安区"
    },
    {
        "DistrictID": "1773",
        "DistrictName": "龙岗区"
    },
    {
        "DistrictID": "1774",
        "DistrictName": "盐田区"
    }
]
```



