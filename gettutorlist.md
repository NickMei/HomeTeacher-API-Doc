# getTutorList

#### Description
获取教师列表


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


#### Request Parameters (Body) 空对象JSON

| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
####  示例程序（JSON）, 全部为必填参数，没有的话可以填 ''，共（19个字段）
#####           var query_obj= {
            'is_app_query': 0,
            'tutor_name': '',
            'order_by': $scope.order_by,
            'order_direc': $scope.order_direc,
            'stage': $scope.stage, 
            'course': $scope.course,
            'sub_course': $scope.sub_course,
            'gender_eng': $scope.gender_eng,
            'career': $scope.career,
            'city_id': $rootScope.city_id,
            'district': $scope.district,
            'price_min': $scope.price_min,
            'price_max': $scope.price_max,
            'day_eng': $scope.day_eng,
            'period_eng': $scope.period_eng,
            'limit': $scope.limit, 
            'page': $scope.page,
            'longitude':  '',
            'latitude': ''
        };

#####参数（2个字段）
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| longitude | string | NO | -- | 用户位置经度 |
| latitude | string | NO | -- | 用户位置维度 |

#####参数（1个字段）
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| is_app_query | INT | NO | -- | 是否是app查询 |

#####顶部搜索教师姓名或者昵称（1个字段）
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| tutor_name | string | NO | -- | 教师姓名或者昵称 |

#####分页（2个字段）
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| page |int | YES | 1 | 第几页|
| limit |int | NO | 6 | 每页个数|

#####按照课程类别搜索（3个字段）
######如果该项选择了全部，就不添加该过滤字段， 或者添加all或者全部
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| stage | string | NO | -- | 阶段，如初中，高中，艺术 |
| course | string | NO | -- | 课程  如 语文， 数学， 声乐术 |
| sub_course | string | NO | -- | 细分课程 如 钢琴 水彩 |


#####筛选条件(8个字段)
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| gender_eng | string | NO | -- | 教师性别：全部 男教员 女教员，  API输入 male 或者 female |
| career | string | NO | -- | 教师职业：在职教师 兼职教师 大学生 |
| city | string | NO | -- |  按照城市搜索 |
| district | string | NO | -- |  按照城市区域搜索 |
| price_min | int | NO | -- | 教师价格最低值 |
| price_max | int | NO | -- | 教师价格最高值 |
| day_eng | string | NO | -- |  星期几：all monday tuesday wednesday thursday friday saturday sunday |
| period_eng | string | NO | -- |  时段：all morning afternoon evening， day_eng 和 period_eng可自由组合，不传的话默认选择all，相当于不限时段|



#####排序（2个字段）
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

|Request URL | "http://112.74.81.48/zhihuieducation/tutorinfo/getTutorList" |
| --| -- |


#### Response Example

```
{
    retcode: 0, 
    retmsg: "成功请求！",
    response: { 
        count: "7" //满足条件教师总个数
        list:
        [
            {
                career: "大学生"
                course_info: "高考/语文, 艺术/器乐/钢琴, 艺术/美术/水粉"
                distance: ""
                edu_level: "研究生"
                gender_eng: "male"
                head_photo: "http://112.74.81.48/zhihuieducation/webApp/app/res/tutor_photo/6.jpg"
                is_eduCer_auth: "1"
                is_identification_auth: "1"
                is_professionalCer_auth: "0"
                is_teacherCer_auth: "1"
                like_info: {
                    is_bookmarked: "0"
                    is_liked: "0"
                    num_of_like: "3"
                }
                location_info: "南山区"
                name: "陈大文"
                price: "0"
                rating: "5"
                signature: "没有教不会的学生"
                total_class_time: "10"
                tutor_id: "1"
                university: "江西大学"
            },
            {
            
            },
            {
        
            },
            {
        
            }
        ]
    }
}
```

### API变更记录


#### 2015-08-14 
1. 入参增加用户位置经纬度，用来计算距离







