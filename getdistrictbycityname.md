# getDistrictByCityName

#### Description
get district list by city chinese name
#### Resquet Method
GET
#### Request Parameters

| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| cityName | String | YES |  | city chinese name|



#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Response | JSON | YES| | district list


#### Request Example

|Request URL | "http://112.74.81.48/ijiajiao/locationcontroller/getDistrictByCityName?cityName=深圳市" |
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





