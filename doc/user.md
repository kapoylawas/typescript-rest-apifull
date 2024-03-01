# User API Spec

## Register User
Endpoint : POST /api/users

Request Body :

```json
{
    "username" : "budi",
    "password" : "rahasia",
    "name" : "Budi Sudarsono"
}
```

Response Body (Success) :

```json
{
    "data" : {
        "username" : "budi",
        "name" : "Budi Sudarsono"
    }
}
```

Response Body (Failed) :

```json
{
    "errors" : "Username not found...!!"
}
```

## Login User
Endpoint : POST /api/users/login

Request Body :

```json
{
    "username" : "budi",
    "password" : "rahasia",
}
```

Response Body (Success) :

```json
{
    "data" : {
        "username" : "budi",
        "name" : "Budi Sudarsono",
        "token" : "uuid"
    }
}
```

Response Body (Failed) :

```json
{
    "errors" : "Username or password wrong....!!"
}
```

## Get User

Endpoint : GET /api/users/current

Request Header :
- X-API-TOKEN : token

Response Body (Success) :

```json
{
    "data" : {
        "username" : "budi",
        "name" : "Budi Sudarsono"
    }
}
```

Response Body (Failed) :

```json
{
    "errors" : "Unauthorized...!!"
}
```

## Update User
Endpoint : PATCH /api/users/current

Request Header :
- X-API-TOKEN : token

Request Body :

```json
{
    "password" : "rahasia", // tidak wajib
    "name" : "Budi Sudarsono" // tidak wajib
}
```

Response Body (Success) :

```json
{
    "data" : {
        "username" : "budi",
        "name" : "Budi Sudarsono",
    }
}
```

Response Body (Failed) :

```json
{
    "errors" : "Unauthorized....!!"
}
```

## Lougout User
Endpoint : DELETE /api/users/current

Request Header :
- X-API-TOKEN : token

Request Body (Success) :

```json
{
    "data" : "OK"
}
```

Response Body (Failed) :

```json
{
    "errors" : "Unauthorized....!!"
}
```