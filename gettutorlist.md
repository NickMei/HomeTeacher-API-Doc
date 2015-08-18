# getTutorList
获取教师列表

#### Description

#### Resquet Method
GET
#### Request Parameters

#####参数
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| longitude | string | NO | -- | 用户位置经度 |
| latitude | string | NO | -- | 用户位置维度 |

#####顶部搜索教师姓名或者昵称
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| tutor_name | string | NO | -- | 教师姓名或者昵称 |

#####按照课程类别搜索
######如果该项选择了全部，就不添加该过滤字段， 或者添加all或者全部
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| stage | string | NO | -- | 阶段，如初中，高中，艺术 |
| course | string | NO | -- | 课程  如 语文， 数学， 声乐术 |
| sub_course | string | NO | -- | 细分课程 如 钢琴 水彩 |


#####筛选条件
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| gender_eng | string | NO | -- | 教师性别：全部 男教员 女教员，  API输入 male 或者 female |
| career | string | NO | -- | 教师职业：在职教师 兼职教师 大学生 |
| district | string | NO | -- |  按照城市区域搜索称 |
| price_min | int | NO | -- | 教师价格最低值 |
| price_max | int | NO | -- | 教师价格最高值 |
| day_eng | string | NO | -- |  星期几：all monday tuesday wednesday thursday friday saturday sunday |
| period_eng | string | NO | -- |  时段：all morning afternoon evening， day_eng 和 period_eng可自由组合，不传的话默认选择all，相当于不限时段|



#####排序
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| order_by | string | NO | -- | 排序参照列： general(综合排序)  rating（好评） total_class_time（总课时） price（价格）|
| order_direc  | string | NO | -- |  ASC(顺序) DESC(逆序)|
#####4种排序方式：

#####a)综合排序：现在默认按照好评由高到低排序
#####  不需要传递任何GET参数或者不添加值 ?order_by=general&order_direc=
#####b)评价最高： 按照好评由高到低排序  ?order_by=rating&order_direc=DESC
#####c)课时最多： 课时由多到少排序:  ?order_by=total_class_time&order_direc=DESC
#####d)价格最低：按照一课时价格由低到高排序:  ?order_by=price&order_direc=ASC
#####e)价格最高：按照一课时价格由高到底排序:   ?order_by=price&order_direc=DESC




#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Response | JSON | YES| |   |


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/apitutorinfocontroller/getTutorList" |
| --| -- |


#### Response Example

```
[
    {
        "tutor_id": "1",
        "name": "陈大文",
        "head_photo": "http://112.74.81.48/zhihuieducation/webApp/app/res/tutor_photo/6.jpg",
        "signature": "没有教不会的学生",
        "gender_eng": "male",
        "career": "兼职教师",
        "edu_level": "研究生",
        "university": "江西大学",
        "total_class_time": "10",
        "rating": "5",
        "price": "100",
        "distance": ""
    },
    {
        "tutor_id": "2",
        "name": "李文文",
        "head_photo": "http://112.74.81.48/zhihuieducation/webApp/app/res/tutor_photo/4.jpg",
        "signature": "相信自己一定可以",
        "gender_eng": "female",
        "career": "在职教师",
        "edu_level": "本科",
        "university": "广东工业大学",
        "total_class_time": "19",
        "rating": "4.5",
        "price": "100",
        "distance": ""
    },
    {
        "tutor_id": "11",
        "name": "赵同学",
        "head_photo": "http://112.74.81.48/zhihuieducation/webApp/app/res/tutor_photo/1.jpg",
        "signature": "我是数学大牛",
        "gender_eng": "male",
        "career": "大学生",
        "edu_level": "本科",
        "university": "吉林大学",
        "total_class_time": "15",
        "rating": "4.8",
        "price": "200",
        "distance": ""
    },
    {
        "tutor_id": "13",
        "name": "刘同学",
        "head_photo": "http://112.74.81.48/zhihuieducation/webApp/app/res/tutor_photo/2.jpg",
        "signature": "祝您圆梦",
        "gender_eng": "male",
        "career": "在职教师",
        "edu_level": "研究生",
        "university": "香港大学",
        "total_class_time": "43",
        "rating": "4.3",
        "price": "200",
        "distance": ""
    },
    {
        "tutor_id": "14",
        "name": "任同学",
        "head_photo": "http://112.74.81.48/zhihuieducation/webApp/app/res/tutor_photo/3.jpg",
        "signature": "没有教不会的学生",
        "gender_eng": "male",
        "career": "兼职教师",
        "edu_level": "博士",
        "university": "香港理工大学",
        "total_class_time": "8",
        "rating": "5",
        "price": "150",
        "distance": ""
    }
]
```

### API变更记录


#### 2015-08-14 
1. 入参增加用户位置经纬度，用来计算距离







