# getTutorComment


#### Description

#### Resquet Method
GET
#### Request Parameters

| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| tutor_id | String | YES | -- | -- |
| comment_type | String | YES | -- | all：全部评价  good：好评  middle： 中评  bad： 差评 |


#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Response | JSON | YES| |   |


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/tutorinfo/getTutorComment?tutor_id=1&comment_type=all" |
| --| -- |


#### Response Example

```
{
    "num_of_comments": 3,
    "rating": "4.9",
    "comments": [
        {
            "comment_type": "good",
            "create_datetime": "2014-01-01",
            "student_id": 1,
            "student_photo_url": "http://112.74.81.48/zhihuieducation/webApp/app/res/tutor_photo/jz.png",
            "teach_way": "教员上门",
            "student_name": "张同学",
            "comment": "讲解认真专业"
        },
        {
            "comment_type": "middle",
            "create_datetime": "2014-01-01",
            "student_id": 2,
            "student_photo_url": "http://112.74.81.48/zhihuieducation/webApp/app/res/tutor_photo/jz.png",
            "teach_way": "教员上门",
            "student_name": "刘同学",
            "comment": "准时耐心，提升了我的学习兴趣"
        },
        {
            "comment_type": "bad",
            "create_datetime": "2014-01-01",
            "student_id": 3,
            "student_photo_url": "http://112.74.81.48/zhihuieducation/webApp/app/res/tutor_photo/jz.png",
            "teach_way": "教员上门",
            "student_name": "李妈妈",
            "comment": "老师一般"
        }
    ]
}
```






