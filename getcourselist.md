# getCourseList


#### Description
get course list such as:  语文 数学 英语 物理 化学 生物 政治 地理 历史 奥数
#### Resquet Method
GET
#### Request Parameters

| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| stage_id | String | YES | -- | stage_id: obtain by getStageList |



#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Response | JSON | YES| | course list  |


#### Request Example

|Request URL | "http://112.74.81.48/ijiajiao/coursecontroller/getCourseList?stage_id=5" |
| --| -- |


#### Response Example

```
[
    {
        "course_id": "46",
        "stage_id": "5",
        "course_name": "全部",
        "priority": "1"
    },
    {
        "course_id": "47",
        "stage_id": "5",
        "course_name": "语文",
        "priority": "0"
    },
    {
        "course_id": "48",
        "stage_id": "5",
        "course_name": "数学",
        "priority": "0"
    },
    {
        "course_id": "49",
        "stage_id": "5",
        "course_name": "英语",
        "priority": "0"
    },
    {
        "course_id": "50",
        "stage_id": "5",
        "course_name": "物理",
        "priority": "0"
    },
    {
        "course_id": "51",
        "stage_id": "5",
        "course_name": "化学",
        "priority": "0"
    },
    {
        "course_id": "52",
        "stage_id": "5",
        "course_name": "生物",
        "priority": "0"
    },
    {
        "course_id": "53",
        "stage_id": "5",
        "course_name": "政治",
        "priority": "0"
    },
    {
        "course_id": "54",
        "stage_id": "5",
        "course_name": "地理",
        "priority": "0"
    },
    {
        "course_id": "55",
        "stage_id": "5",
        "course_name": "历史",
        "priority": "0"
    },
    {
        "course_id": "56",
        "stage_id": "5",
        "course_name": "奥数",
        "priority": "0"
    }
]
```






