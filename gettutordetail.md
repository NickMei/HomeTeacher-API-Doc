# getTutorDetailInfo


#### Description

#### Resquet Method
GET
#### Request Parameters

| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| tutor_id | String | YES | -- |  |



#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Response | JSON | YES| |   |


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/apitutorinfocontroller/getTutorDetailInfo?tutor_id=1" |
| --| -- |


#### Response Example

```
{
    "basic_info": {
        "name": "陈大文",
        "head_photo": "http://112.74.81.48/zhihuieducation/webApp/app/res/tutor_photo/6.jpg",
        "signature": "没有教不会的学生",
        "gender_eng": "male",
        "career": "兼职教师",
        "self_intro": "我是一个富有热忱的大学生，希望用自己的努力做好家教工作",
        "address": "深圳市罗湖区",
        "address_url": "http://api.map.baidu.com/staticimage?width=348&height=205%26center=114.15639529324,%2022.581934478848&markers=114.15639529324,22.581934478848&zoom=14&markerStyles=s,A,0xff0000",
        "age": 25
    },
    "course_info": "高考/语文, 艺术/器乐/钢琴, 留学/GRE",
    "location_info": "荔湾区, 越秀区, 海珠区, 芳村区",
    "auth_info": {
        "is_identification_auth": true,
        "is_eduCer_auth": true,
        "is_teacherCer_auth": false,
        "is_professionalCer_auth": false
    },
    "comment_info": {
        "comments": 6,
        "rating": "98%",
        "like": 8,
        "teach_years": 2,
        "total_students": 5,
        "total_class_time": 30
    },
    "edu_info": [
        {
            "edu_id": "1",
            "start_datetime": "2013-07",
            "end_datetime": "2015-01",
            "edu_level": "研究生",
            "university": "江西大学",
            "major": "经济管理"
        },
        {
            "edu_id": "2",
            "start_datetime": "2011-06",
            "end_datetime": "2013-07",
            "edu_level": "本科",
            "university": "深圳大学",
            "major": "物理学"
        }
    ],
    "timetable_info": [
        {
            "time": "上午",
            "monday": "1",
            "tuesday": "1",
            "wednesday": "1",
            "thursday": "1",
            "friday": "1",
            "saturday": "0",
            "sunday": "0"
        },
        {
            "time": "下午",
            "monday": "0",
            "tuesday": "1",
            "wednesday": "0",
            "thursday": "0",
            "friday": "1",
            "saturday": "0",
            "sunday": "0"
        },
        {
            "time": "晚上",
            "monday": "0",
            "tuesday": "0",
            "wednesday": "0",
            "thursday": "0",
            "friday": "1",
            "saturday": "0",
            "sunday": "0"
        }
    ],
    "success_case_info": [
        {
            "case_id": "1",
            "stage": "艺术",
            "course": "声乐",
            "sub_course": "民族",
            "start_datetime": "2011-09",
            "end_datetime": "2011-12",
            "case_title": "全面提升学生水平",
            "case_desc": "通过全面地辅导培训，学生取得了进步，考取了优秀的声乐院校"
        },
        {
            "case_id": "2",
            "stage": "小学",
            "course": "数学",
            "sub_course": "",
            "start_datetime": "2015-07",
            "end_datetime": "2015-07",
            "case_title": "全面提升学生水平",
            "case_desc": "通过全面地辅导培训，学生取得了进步，考取了优秀的声乐院校"
        }
    ],
    "honour_exp__info": [
        {
            "case_id": "1",
            "start_datetime": "2014-09",
            "end_datetime": "2014-10",
            "case_title": "大学勤奋123",
            "case_desc": "大学期间在校勤奋，目前已结束的三个学期成绩均在本专业名列前茅。学习大一上学期在“活力社区”朱房中心为进城务工子弟辅导功课，主要辅导语文英语，在此过程中与小同学建立了良好的友谊，一定程度上也促进了他们的学习成绩的提升，获得学生的好评及机构的赞赏。"
        },
        {
            "case_id": "2",
            "start_datetime": "2012-12",
            "end_datetime": "2014-10",
            "case_title": "高中获奖",
            "case_desc": "2013年河南省高考，高中时成绩优异，曾多次取得年级前十名及高中所在县区前十名。曾获得校级作文大赛一等奖（第一名），英语写作大赛二等奖。"
        },
        {
            "case_id": "3",
            "start_datetime": "2008-09",
            "end_datetime": "2009-12",
            "case_title": "初中时成绩优秀",
            "case_desc": "初中时成绩优秀，尤以语文英语为佳，初中时在语文方面较擅长作文写作和阅读题作答；关于英语，在完形填空的答题和知识点的记忆方面有一定心得。多次荣获三好学生。曾多次参加演讲比赛、辩论赛、作文大赛、朗诵比赛，获奖项若干。有文章在校报发表。总成绩也多次位居年级前十名，初中结束时以优异成绩考取当地重点高中。"
        },
        {
            "case_id": "4",
            "start_datetime": "2015-07",
            "end_datetime": "2015-07",
            "case_title": "123",
            "case_desc": ""
        }
    ]
}
```





