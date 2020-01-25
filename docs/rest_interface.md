# Rest Api

# User 
---
## /signup

<b style="text-decoration: underline;">POST:</b>

Parameters:
- username (string),

## /login
This authenticates the user with the backend so the server can provide the best results for the specific individual.

<b style="text-decoration: underline;">POST:</b>

Parameters:
- username (string), `required`
- password (string), `required` 

Response:
- type (JSON representing the current user)

Response Ex:
```json
{
	"name":"Andrew",
	"id":"abcd123",
	"preferences":{
		"radius":10,
		"radiusDistanceType":"mi"
	},
	"favorites":[
		{
			"name":"Jim Beams truck",
			"id":"hijklmno123",
			"genre":"Haitian"
		}
	]
}
```

Response Codes:
- 200 : Authentication successful
- 403 : Improper Username or Password
- 500 : Server error occurred.
