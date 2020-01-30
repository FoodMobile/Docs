# Rest Api

## POST

??? warning "api/v1/signup"
    ### api/v1/signup
	
	#### Parameters
	username(String)

	#### Response type
	type (JSON representing the new user)

	#### Payload example:
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

??? warning "api/v1/login"
    ### api/v1/login

	This authenticates the user with the backend so the server can provide the best results for the specific individual

	#### Parameters
	username (string), ==required==  
	password (string), ==required== 

	#### Response type
	type (JSON representing the current user)

	#### Payload example:
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
	- <span style="color:green">200</span> : Authentication successful  
	- <span style="color:orange">403</span> : Improper Username or Password  
	- <span style="color:red">500</span> : Server error occurred.

## GET

??? success "api/v1/test"
	Test

## PUT

??? info "api/v1/test"
	Test

## DELETE

??? danger "api/v1/test"
	Test