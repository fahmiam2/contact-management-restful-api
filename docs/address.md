# Address API Spec

## Create Address API

Endpoint: POST /api/contacts/:contactId/addresses

Headers:

- Authorization: token

Request Body:

```json
{
  "street": "Jl. Durian runtuh",
  "city": "Serang",
  "province": "Banten",
  "country": "Indonesia",
  "postal_code": "15348"
}
```

Response Body Success:

```json
{
  "data": {
    "id": 1,
    "street": "Jl. Durian runtuh",
    "city": "Serang",
    "province": "Banten",
    "country": "Indonesia",
    "postal_code": "15348"
  }
}
```

Response Body Error:

```json
{
  "errors": "Country is required, please fill it"
}
```

## Update Address API

Endpoint: PUT /api/contacts/:contactId/addresses

Headers:

- Authorization: token

Request Body:

```json
{
  "street": "Jl. Durian runtuh No. 1",
  "city": "Serang",
  "province": "Banten",
  "country": "Indonesia",
  "postal_code": "15348"
}
```

Response Body Success:

```json
{
  "data": {
    "id": 1,
    "street": "Jl. Durian runtuh No. 1",
    "city": "Serang",
    "province": "Banten",
    "country": "Indonesia",
    "postal_code": "15348"
  }
}
```

Response Body Error:

```json
{
  "errors": "Country is required. Please fill it"
}
```

## Get Address API

Endpoint: GET /api/contacts/:contactId/addresses/:addressId

Headers:

- Authorization: token

Response Body Success:

```json
{
  "data": {
    "id": 1,
    "street": "Jl. Durian runtuh",
    "city": "Serang",
    "province": "Banten",
    "country": "Indonesia",
    "postal_code": "15348"
  }
}
```

Response Body Error:

```json
{
  "errors": "Contact is not found"
}
```

## List Address API

Endpoint: GET /api/contacts/:contactId/addresses

Headers:

- Authorization: token

Response Body Success:

```json
{
  "data": [
    {
      "id": 1,
      "street": "Jl. Durian runtuh",
      "city": "Serang",
      "province": "Banten",
      "country": "Indonesia",
      "postal_code": "15348"
    },
    {
      "id": 2,
      "street": "Jl. Durian mantong",
      "city": "Serang",
      "province": "Banten",
      "country": "Indonesia",
      "postal_code": "15349"
    }
  ]
}
```

Response Body Error:

```json
{
  "errors": "Contact is not found"
}
```

## Remove Address API

Endpoint: POST /api/contacts/:contactId/addresses

Headers:

- Authorization: token

Response Body Success:

```json
{
  "data": "OK"
}
```

Response Body Error:

```json
{
  "errors": "Contact is not found"
}
```
