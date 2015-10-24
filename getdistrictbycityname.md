# getDistrictByCityName

#### Description
get district list by city chinese name

#### 请求是否要认证
NO

#### Resquet Method
POST

#### Request Header 请求头中传的参数
######uid没有登陆情况下为整形integer零 0， 登陆成功后使用user_id
######identity 根据用户选择的身份，student 或者 tutor
######checksum由三个步骤算出，参考下面图片JS代码和注释，包含token安全验证以及post数据完整性校验功能

| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| uid | int | YES |  | 0 |
| identity    | String | YES |  | tutor 或者 student|
| checksum    | String | YES |  | checksum|

#### Request Parameters

| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| cityName | String | YES |  | city chinese name|



#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Response | JSON | YES| | district list


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/location/getDistrictByCityName?cityName=深圳市" |
| --| -- |


#### Response Example

```
{
    "retcode": 0,
    "retmsg": "请求成功！",
    "response": {
                "district_list": [
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





