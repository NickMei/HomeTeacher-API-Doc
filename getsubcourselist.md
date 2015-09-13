# getSubCourseList


#### Description
get sub course list such as:  全部 芭蕾舞 拉丁舞 街舞 现代舞 爵士舞 古典舞 民族舞 健美操 民间舞 国标舞 迪斯科 其它

#### 请求是否要认证
NO


#### Resquet Method
GET
#### Request Parameters

| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| course_id | String | YES | -- | course_id: obtain by getCourseList |



#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Response | JSON | YES| | sub course list  |


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/course/getSubCourseList?course_id=96" |
| --| -- |


#### Response Example

```
[
    {
        "course_sub_id": "35",
        "course_id": "96",
        "course_sub_name": "全部",
        "priority": "1"
    },
    {
        "course_sub_id": "36",
        "course_id": "96",
        "course_sub_name": "芭蕾舞",
        "priority": "0"
    },
    {
        "course_sub_id": "37",
        "course_id": "96",
        "course_sub_name": "拉丁舞",
        "priority": "0"
    },
    {
        "course_sub_id": "38",
        "course_id": "96",
        "course_sub_name": "街舞",
        "priority": "0"
    },
    {
        "course_sub_id": "39",
        "course_id": "96",
        "course_sub_name": "现代舞",
        "priority": "0"
    },
    {
        "course_sub_id": "40",
        "course_id": "96",
        "course_sub_name": "爵士舞",
        "priority": "0"
    },
    {
        "course_sub_id": "41",
        "course_id": "96",
        "course_sub_name": "古典舞",
        "priority": "0"
    },
    {
        "course_sub_id": "42",
        "course_id": "96",
        "course_sub_name": "民族舞",
        "priority": "0"
    },
    {
        "course_sub_id": "43",
        "course_id": "96",
        "course_sub_name": "健美操",
        "priority": "0"
    },
    {
        "course_sub_id": "44",
        "course_id": "96",
        "course_sub_name": "民间舞",
        "priority": "0"
    },
    {
        "course_sub_id": "45",
        "course_id": "96",
        "course_sub_name": "国标舞",
        "priority": "0"
    },
    {
        "course_sub_id": "46",
        "course_id": "96",
        "course_sub_name": "迪斯科",
        "priority": "0"
    },
    {
        "course_sub_id": "47",
        "course_id": "96",
        "course_sub_name": "其它",
        "priority": "0"
    }
]
```






