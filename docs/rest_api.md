# REST API Documentation

This documentation is current a work in progress. Things may change as this project progresses, but currently this should be the most up to date reference of what will be. This documentation can be helpful for prototyping. Some requests listed in this document may be working on the server, but they are probably 'dummy' responses for testing purposes.

## Customer

[/api/c/authenticate](#apicauthenticate)

[/api/c/truckinfo](#apictruckinfo)

[/api/c/nearbytrucks](#apicnearbytrucks)

[/api/c/getprofileinfo](#apicgetprofileinfo)

[/api/c/setprofileinfo](#apicsetprofileinfo)

### /api/c/authenticate

Authenticates users with the REST api. Responses with a token on success which will be used for other requests.

| Parameter name          | Type         | Example value                | Description                                                                          |
| ----------------------- | ------------ | ---------------------------- | ------------------------------------------------------------------------------------ |
| username                | string       | joe / 3365797837             | Either the phone number / username or other auth of the user to login.               |
| password                | string       | password123$                 | The password corresponding to the username                                           |

Example request:

```json
{
  "username": "joe",
  "password": "password123$"
}
```

Example response:

```json
{
    "token": "kjlejrlksjlrklsjljfjskfjeskjeflk",
    "errorCode": 0,
    "errorMessage": "Login successful"
}
```

### /api/c/truckinfo

Gets more information about a specific truck. 

| Parameter name          | Type         | Example value                | Description                                                                          |
| ----------------------- | ------------ | ---------------------------- | ------------------------------------------------------------------------------------ |
| token                   | string       | sdfkhdkfjhksjdhkfhdsh        | Token provided by /api/authenticate                                                  |
| id                      | string       | password123$                 | The password corresponding to the username                                           |

Example request:

```json
{
  "token": "sdfkhdkfjhksjdhkfhdsh",
  "id": "truck-guid-here"
}
```

Example response:

```json
{
    "errorCode": 0,
    "errorMessage": "Success",
    "truck_info": {
        "company_name": "Bob's Tacos"
    }
}
```

### /api/c/getprofileinfo

Gets the profile information of the currently authenticated user

| Parameter name          | Type         | Example value                | Description                                                                          |
| ----------------------- | ------------ | ---------------------------- | ------------------------------------------------------------------------------------ |
| token                   | string       | sdfkhdkfjhksjdhkfhdsh        | Token provided by /api/authenticate                                                  |

Example request:

```json
{
  "token": "sdfkhdkfjhksjdhkfhdsh",
}
```

Example response:

```json
{
    "errorCode": 0,
    "errorMessage": "Success",
    "profile_info": {
        "first_name": "Jonathan",
        "family_name": "Cooper",
        "addr_line_1": "1400 Spring Garden St",
        "addr_line_2": "",
        "zip": "27410",
        "state": "NC",
        "city": "Greensboro"
    }
}
```

### /api/c/setprofileinfo

Sets the profile information of the currently authenticated user

| Parameter name          | Type         | Example value                | Description                                                                          |
| ----------------------- | ------------ | ---------------------------- | ------------------------------------------------------------------------------------ |
| token                   | string       | sdfkhdkfjhksjdhkfhdsh        | Token provided by /api/authenticate                                                  |
| first_name              | string       | Jonathan                     | The new first name for the user                                                      |
| family_name             | string       | Cooper                       | The new family name for the user                                                     |
| addr_line_1             | string       | 123 Spring Garden            | The new first address line for the user                                              |
| addr_line_2             | string       | Apt 123 #A                   | The new second address line for the user                                             |
| zip                     | string       | 27410                        | The new zip code for the user                                                        |
| city                    | string       | Greensboro                   | The new city for the user                                                            |

Example request:

```json
{
    "token": "sdfkhdkfjhksjdhkfhdsh",
    "first_name": "Jonathan",
    "family_name": "Cooper",
    "addr_line_1": "1400 Spring Garden St",
    "addr_line_2": "",
    "zip": "27410",
    "state": "NC",
    "city": "Greensboro"
}
```

Example response:

```json
{
    "errorCode": 0,
    "errorMessage": "Success"
}
```

### /api/c/nearbytrucks

Gets the trucks near the provided latitude and longitude. 

| Parameter name          | Type         | Example value                | Description                                                                          |
| ----------------------- | ------------ | ---------------------------- | ------------------------------------------------------------------------------------ |
| token                   | string       | sdfkhdkfjhksjdhkfhdsh        | Token provided by /api/authenticate                                                  |
| lat                     | float        | 123.0123                     | The current latitude coordinate of the user                                          |
| long                    | float        | 123.0123                     | The current longitude coordinate of the user                                         |

Example request:

```json
{
  "username": "joe",
  "password": "password123$"
}
```

Example response:

```json
{
    "errorCode": 0,
    "errorMessage": "Success",
    "trucks": [
        {
            "id": "truck-guid",
            "lat": 512.0123,
            "long": 151.1231
        }
    ]
}
```
