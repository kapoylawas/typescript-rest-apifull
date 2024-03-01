# Address API Spec

## Create Address

Endpoint : POST /api/contact/:idContact/addresses

Request Header :

- X-API-TOKEN : token

Request Body :

```json
{
  "street": "Jalan Apa",
  "city": "Kota Apa",
  "province": "Provinsi Apa",
  "country": "Negara Apa",
  "postal_code": "232312"
}
```

Response Body (Failed)

```json
{
  "errors": "Postal code is required"
}
```

Response Body (Success)

```json
{
  "data": {
    "id": 1,
    "street": "Jalan Apa",
    "city": "Kota Apa",
    "province": "Provinsi Apa",
    "country": "Negara Apa",
    "postal_code": "232312"
  }
}
```

## Get Address

Endpoint : GET /api/contact/:idContact/addresses/:idAddress

Request Header :

- X-API-TOKEN : token

Response Body (Success)

```json
{
  "data": {
    "id": 1,
    "street": "Jalan Apa",
    "city": "Kota Apa",
    "province": "Provinsi Apa",
    "country": "Negara Apa",
    "postal_code": "232312"
  }
}
```

Response Body (Failed)

```json
{
  "errors": "Address is not found"
}
```

## Update Address

Endpoint : PUT /api/contact/:idContact/addresses/:idAddress

Request Header :

- X-API-TOKEN : token

Request Body :

```json
{
  "street": "Jalan Apa",
  "city": "Kota Apa",
  "province": "Provinsi Apa",
  "country": "Negara Apa",
  "postal_code": "232312"
}
```

Response Body (Failed)

```json
{
  "errors": "Address is not found"
}
```

Response Body (Success)

```json
{
  "data": {
    "id": 1,
    "street": "Jalan Apa",
    "city": "Kota Apa",
    "province": "Provinsi Apa",
    "country": "Negara Apa",
    "postal_code": "232312"
  }
}
```

## Remove Address

Endpoint : DELETE /api/contact/:idContact/addresses/:idAddress

Request Header :

- X-API-TOKEN : token

Response Body (Success)

```json
{
  "data": "ok"
}
```

Response Body (Failed)

```json
{
  "errors": "Address is not found"
}
```

## List Address

Endpoint : GET /api/contact/:idContact/addresses

Request Header :

- X-API-TOKEN : token

Response Body (Success)

```json
{
  "data": [
    {
      "id": 1,
      "street": "Jalan Apa",
      "city": "Kota Apa",
      "province": "Provinsi Apa",
      "country": "Negara Apa",
      "postal_code": "232312"
    },
    {
      "id": 2,
      "street": "Jalan Apa",
      "city": "Kota Apa",
      "province": "Provinsi Apa",
      "country": "Negara Apa",
      "postal_code": "232312"
    }
  ]
}
```

Response Body (Failed)

```json
{
  "errors": "Contact is not Found"
}
```
