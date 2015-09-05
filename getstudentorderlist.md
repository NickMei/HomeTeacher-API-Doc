#getStudentOrderList
#### Description
学生个人中心请求我的订单
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


#### Request Parameters (Body) 

| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| order_type | STRING | YES | -- | order_all（全部） order_wait_payment（待支付）   order_executing（进行中）   order_finished（已完成） order_cancelled（已取消） |
####  示例程序：
#####  {"order_type":"order_all"}



#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Response | JSON | YES| | Response |


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/apistudentcentercontroller/getStudentOrderList" |
| --| -- |
| | |

#### Response Example

#####只有retcode 为0 才是成功响应，其他都是错误响应
```
{
    retcode: 0, 
    retmsg: "成功请求！",
    response: {
        "count" :  2, //满足条件总个数
        "list" :  [
            {
                complete_time: "2"
                course: "高中/语文"
                create_time: "2015-04-09 08:32:42"
                head_photo: "http://112.74.81.48/zhihuieducation/webApp/app/res/tutor_photo/6.jpg"
                name: "陈大文"
                order_id: "1"
                price: "100"
                status: "待支付"
                status_id: "1"
                teach_address: "深圳市福田区"
                teach_way: "老师上门"
                total_price: "600"
                total_time: "6"
            }
            {
                complete_time: "4"
                course: "高中/英语"
                create_time: "2015-02-11 20:52:52"
                head_photo: null
                name: null
                order_id: "2"
                price: "150"
                status: "执行中"
                status_id: "2"
                teach_address: "深圳市南山区"
                teach_way: "协商地点"
                total_price: "1500"
                total_time: "10"
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



