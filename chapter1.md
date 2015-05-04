**1. /getMovieMetaDataByKeyword **
#### Description
search movie by keyword and filter type 
#### Resquet Method
POST
#### Request Parameters

| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| localeCode | String | YES |  | locale |
| keyword    | String | YES |  | keyword |
| page_size | Int | YES |  | page size |
| page_num | Int | YES |  | page num |
| In_member_id | Int | Yes |  | member id |
| type | String | No |  | Filter type |

#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| searched movie list | array | YES| | Movie List |

#### Example
|Request | "locale_code=en-us_ios_hls&keyword=allen&page_size=500&page_num=1&In_member_id=0" |
| --| -- |


#### Response 

```
[{
"RowNum":"1",
"total_num":"1",
"movie_id":"20039",
"title":"Transformers: Revenge of the Fallen","duration":"150",
"genre":"Action, Adventure",
"release_datetime":"6/24/2009 12:00:00 AM",
"poster_sd_v":"http://moviestoreclickplayhk.blob.core.windows.net/movie-poster/20039/transformersrevengeofthefallen-Portrait_over.jpg",
"has_trailer":"False",
"priority":"0",
"censorship":"IIA",
"type:"typeA"
},
  {
"RowNum":"1",
"total_num":"4",
"movie_id":"20040",
"title":"Transformers: Revenge of the Fallen","duration":"150",
"genre":"Action, Adventure",
"release_datetime":"6/24/2009 12:00:00 AM",
"poster_sd_v":"http://moviestoreclickplayhk.blob.core.windows.net/movie-poster/20039/transformersrevengeofthefallen-Portrait_over.jpg",
"has_trailer":"False",
"priority":"0",
"censorship":"IIA",
"type:"typeB"
},
  {
"RowNum":"1",
"total_num":"4",
"movie_id":"20041",
"title":"Transformers: Revenge of the Fallen","duration":"150",
"genre":"Action, Adventure",
"release_datetime":"6/24/2009 12:00:00 AM",
"poster_sd_v":"http://moviestoreclickplayhk.blob.core.windows.net/movie-poster/20039/transformersrevengeofthefallen-Portrait_over.jpg",
"has_trailer":"False",
"priority":"0",
"censorship":"IIA",
"type:"typeC"
},
  {
"RowNum":"1",
"total_num":"4",
"movie_id":"20042",
"title":"Transformers: Revenge of the Fallen","duration":"150",
"genre":"Action, Adventure",
"release_datetime":"6/24/2009 12:00:00 AM",
"poster_sd_v":"http://moviestoreclickplayhk.blob.core.windows.net/movie-poster/20039/transformersrevengeofthefallen-Portrait_over.jpg",
"has_trailer":"False",
"priority":"0",
"censorship":"IIA",
"type:"typeD"
},
]```



