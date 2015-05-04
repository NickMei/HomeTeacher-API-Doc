# getCourseList


#### Description
get course list such as:  全部 器乐 声乐 舞蹈 美术 书法 其它
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

|Request URL | "http://112.74.81.48/ijiajiao/coursecontroller/getCourseList?stage_id=10" |
| --| -- |


#### Response Example

```
[
    {
        "course_id": "93",
        "stage_id": "10",
        "course_name": "全部",
        "priority": "1"
    },
    {
        "course_id": "94",
        "stage_id": "10",
        "course_name": "器乐",
        "priority": "0"
    },
    {
        "course_id": "95",
        "stage_id": "10",
        "course_name": "声乐",
        "priority": "0"
    },
    {
        "course_id": "96",
        "stage_id": "10",
        "course_name": "舞蹈",
        "priority": "0"
    },
    {
        "course_id": "97",
        "stage_id": "10",
        "course_name": "美术",
        "priority": "0"
    },
    {
        "course_id": "98",
        "stage_id": "10",
        "course_name": "书法",
        "priority": "0"
    },
    {
        "course_id": "99",
        "stage_id": "10",
        "course_name": "其它",
        "priority": "0"
    }
]
```






