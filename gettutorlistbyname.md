# getTutorListByName


#### Description
使用教师姓名或者昵称快速搜索教师

#### Resquet Method
GET
#### Request Parameters

| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| tutor_name | String | YES | -- | 教师的姓名或者昵称 |



#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Response | JSON | YES| | 教师列表数组  |


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/apitutorinfocontroller/getTutorListByName?tutor_name=陈大文" |
| --| -- |


#### Response Example

```
[
    {
        "tutor_id": "14",
        "name": "任同学",
        "head_photo": "http://112.74.81.48/zhihuieducation/webApp/app/res/tutor_photo/3.jpg",
        "signature": "没有教不会的学生",
        "gender_eng": "male",
        "career": "兼职教师",
        "edu_id": "2",
        "edu_level": "本科",
        "university": "深圳大学",
        "total_class_time": "8",
        "rating": "5",
        "price": "150",
        "distance": ""
    }
]
```






