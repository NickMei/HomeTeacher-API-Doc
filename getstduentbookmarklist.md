#getStudentBookmarkList
#### Description
学生个人中心请求学生收藏的教师列表

#### 请求是否要认证
YES

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
| page | INT | YES | -- |  |
| limit | INT | YES | -- |  |
####  示例程序（空对象JSON）：
#####   var query_obj = {"page": 1, "limit": 6};
#####   var json_str = JSON.stringify(query_obj);



#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Response | JSON | YES| | Response |


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/studentcenter/getStudentBookmarkList" |
| --| -- |
| | |

#### Response Example

#####只有retcode 为0 才是成功响应，其他都是错误响应
```
{
    retcode: 0, 
    retmsg: "成功请求！",
    response: {
        "count" :  2, //满足条件总的个数，大于等于当前个数
        "list" :  [
            {
                tutor_id: "1",
                head_photo："http://112.74.81.48/zhihuieducation/webApp/app/res/tutor_photo/6.jpg”,
                name: "陈大文",
                course: "高考/语文, 艺术/器乐/钢琴, 艺术/美术/水粉"
            },
            {
                tutor_id: 20,
                head_photo："http://112.74.81.48/zhihuieducation/webApp/app/res/tutor_photo/gd2.jpg",
                name: 江同学,
                course: "初中/英语, 高中/英语"
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


可能是丢失数据，或者token无效或者过期，提示用户重新登陆
{
    retcode: 2, 
    retmsg: "验证无法通过，请重新登陆",
    response: {
    }
}
```



