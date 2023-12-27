# Contact API Spec

## Create Contact API

Endpoint: POST /api/contacts

Headers:

- Authorization: token

Request Body:

```json
{
  "first_name": "Cimod",
  "last_name": "Mod",
  "email": "cimod@gmail.com",
  "phone": "+6223849374824"
}
```

Request Body Success:

```json
{
  "data": {
    "id": 1,
    "first_name": "Cimod",
    "last_name": "Mod",
    "email": "cimod@gmail.com",
    "phone": "+6223849374824"
  }
}
```

Request Body Error:

```json
{
  "errors": "Email is not in valid format"
}
```

## Update Contact API

Endpoint: PUT /api/contacts/:contactId

Headers:

- Authorization: token

Request Body:

```json
{
  "first_name": "Cimod",
  "last_name": "Jr",
  "email": "cimod@gmail.com",
  "phone": "+6223849374824"
}
```

Request Body Success:

```json
{
  "data": {
    "id": 1,
    "first_name": "Cimod",
    "last_name": "Jr",
    "email": "cimod@gmail.com",
    "phone": "+6223849374824"
  }
}
```

Request Body Error:

```json
{
  "errors": "Email is not in valid format"
}
```

## Get Contact API

Endpoint: GET /api/contacts/:contactId

Headers:

- Authorization: token

Request Body Success:

```json
{
  "data": {
    "id": 1,
    "first_name": "Cimod",
    "last_name": "Mod",
    "email": "cimod@gmail.com",
    "phone": "+6223849374824"
  }
}
```

Request Body Error:

```json
{
  "errors": "Contact is not founds"
}
```

## Search Contact API

Endpoint: GET /api/contacts

Headers:

- Authorization: token

Query Params:

- name: Search by first_name or last_name using like query, optional
- email: Search by email using like, optional
- phone: Search by phone using like, optional
- page: Number of page, default 1
- size: Size per page, default 10

Request Body Success:

```json
{
  "data": [
    {
      "id": 1,
      "first_name": "Cimod",
      "last_name": "Mod",
      "email": "cimod@gmail.com",
      "phone": "+6223849374824"
    },
    {
      "id": 2,
      "first_name": "Fikri",
      "last_name": "Maulana",
      "email": "fikri.maulana@gmail.com",
      "phone": "+6223849374825"
    }
  ],
  "pagination": {
    "page": 1,
    "total_page": 3,
    "total_item": 30
  }
}
```

Request Body Error:

```json
{
  "errors": "Contact is not found"
}
```

## Remove Contact API

Endpoint: DELETE /api/contacts

Headers:

- Authorization: token

Request Body Success:

```json
{
  "data": "OK"
}
```

Request Body Error:

```json
{
  "errors": "Contact is not found"
}
```
