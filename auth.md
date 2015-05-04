**/auth **
#### Description
auth user login account
#### Resquet Method
POST
#### Request Parameters

| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| username | String | YES |  | username |
| password    | String | YES |  | password |


#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Auth Response | JSON | YES| | Auth Response |


#### Request Example

|Request URL | "http://112.74.81.48/ijiajiao/authcontroller/auth" |
| --| -- |
| POST| JSON: {userInfo: {username: $username, password: $md5HashedPassword}}|

#### Response Example

```
{login_success: true, login_response: "成功登陆"}
```



