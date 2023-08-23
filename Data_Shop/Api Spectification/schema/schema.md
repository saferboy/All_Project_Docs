## Schema Endpoints


> Base url: `/api/v1/schema`

<br>

**POST** `/`

<br>

**Authorization**: `Token` 


> required ```Admin``` or `Supervisor` role


`Request`


```json
{
    "title": "Lap Top",
    "keys": [
        {
            "key": "protsessor",
            "type": "string"
        },
        {
            "key": "ram",
            "type": "string"
        },
        {
            "key": "ssd",
            "type": "string"
        }
    ]
}
```

`Response`

```json
{
    "message": "Schema created",
    "schema": {
        "id": 7,
        "title": "Lap Top",
        "keys": [
            {
                "id": 49,
                "key": "protsessor",
                "type": "string"
            },
            {
                "id": 50,
                "key": "ram",
                "type": "string"
            },
            {
                "id": 51,
                "key": "ssd",
                "type": "string"
            }
        ]
    }
}
```


---

**GET** `/` or `?page=2&limit10`


> required ```Admin``` or `Supervisor` role


- **Authorization**: `Token` 

- `Response`

```json
{
    "message": "Retrive all schema",
    "schema": [
        {
            "id": 2,
            "title": "Smartphone"
        },
        {
            "id": 3,
            "title": "Airpods"
        },
        {
            "id": 4,
            "title": "Shirts"
        },
        {
            "id": 7,
            "title": "Lap Top"
        }
    ]
}
```

---

**GET** `/:id`

**Authorization**: `Token` 

- Required role : ```Admin``` or `Supervisor` 

- `Response`

```json
{
    "message": "Retrive schema by id: 3",
    "schema": {
        "id": 3,
        "title": "Earphone",
        "keys": [
            {
                "id": 17,
                "key": "Color",
                "type": "string"
            },
            {
                "id": 18,
                "key": "Battery",
                "type": "string"
            }
        ]
    }
}
```

---

**DELETE** `/:id`

**Authorization**: `Token` 

- Required role : ```Admin``` or `Supervisor` 

- `Response`

```json
{
    "message": "Schema deleted",
    "schema": {
        "id": 2,
        "title": "Lap Top",
        "keys": [
            {
                "id": 9,
                "key": "protsessor",
                "type": "string"
            },
            {
                "id": 10,
                "key": "ram",
                "type": "string"
            },
            {
                "id": 11,
                "key": "ssd",
                "type": "string"
            }
        ]
    }
}
```