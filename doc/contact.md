# Contact API Spec

## Create Contact

Endpint : POST /api/contact

Request Header :

- X-API-TOKEN :token

Request Body :

```json
{
  "first_name": "Budi Sudarsono",
  "last_name": "Budi",
  "email": "budi@gmail.com",
  "phone": "0856232323333"
}
```

Response Body (Success)

```json
{
  "data": {
    "id": 1,
    "first_name": "Budi Sudarsono",
    "last_name": "Budi",
    "email": "budi@gmail.com",
    "phone": "08572323121"
  }
}
```

Response Body (Failed)

```json
{
  "errors": "frist_name must not blank"
}
```

## Get Contact

Endpint : GET /api/contact

Request Header :

- X-API-TOKEN :token

Response Body (Success)

```json
{
  "data": {
    "id": 1,
    "first_name": "Budi Sudarsono",
    "last_name": "Budi",
    "email": "budi@gmail.com",
    "phone": "08572323121"
  }
}
```

Response Body (Failed)

```json
{
  "errors": "Contact is not found"
}
```

## Update Contact

Endpint : PATCH /api/contact/:id

Request Header :

- X-API-TOKEN :token

Request Body :

```json
{
  "first_name": "Budi Sudarsono",
  "last_name": "Budi",
  "email": "budi@gmail.com",
  "phone": "0856232323333"
}
```

Response Body (Success)

```json
{
  "data": {
    "id": 1,
    "first_name": "Budi Sudarsono",
    "last_name": "Budi",
    "email": "budi@gmail.com",
    "phone": "08572323121"
  }
}
```

Response Body (Failed)

```json
{
  "errors": "frist_name must not blank"
}
```

## Remove Contact

Endpint : DELETE /api/contact/:id

Request Header :

- X-API-TOKEN :token

Response Body (Success)

```json
{
  "data": "OK"
}
```

Response Body (Failed)

```json
{
  "errors": "Contact is not found"
}
```

## Search Contact

Endpint : GET /api/contact

Query Paramater :

- name : string, contact first name or contact last name, optional
- phone : string, contact phone, optional
- email : string, contact email, optional
- page : number, default 1
- size : number, default 10

Request Header :

- X-API-TOKEN :token

Request Body :

```json
{
  "first_name": "Budi Sudarsono",
  "last_name": "Budi",
  "email": "budi@gmail.com",
  "phone": "0856232323333"
}
```

Response Body (Success)

```json
{
  "data": [
    {
      "id": 1,
      "first_name": "Budi Sudarsono",
      "last_name": "Budi",
      "email": "budi@gmail.com",
      "phone": "08572323121"
    },
    {
        "id" : 2,
        "first_name" : "Ani Sudarsono",
        "last_name" : "Ani",
        "email" : "ani@gmail.com",
        "phone" : "08561313122"
    }
  ],
  "paging" : {
    "current_page" : 1,
    "total_page" : 10,
    "size" : 10
  }
}
```

Response Body (Failed)

```json
{
  "errors": "Unauthorized"
}
```
