

## Cateory endpoints


---

> Base url: `/api/v1/category`


<br>

**POST** `/`

**Authorization**: `Token` 

> required ```Admin``` or `Supervisor` role

`Request`

```json
{
    "title": "Laptops",
    "iconId": 17
}
```

`Response`

```json
{
    "message": "Categroy created",
    "category": {
        "id": 12,
        "title": "telefonlar1",
        "icon": {
            "id": 17,
            "path": "df9d1306-3013-4353-b48f-c7ed51347569.png",
            "filename": "batman-is-watching-beautiful-sunset-wallpaper-2560x1080_14 — копия.jpg"
        }
    }
}
```

---

**GET** `/:id`

`Response`

```json
{
    "message": "Retrive category by id: 12",
    "category": {
        "id": 12,
        "title": "telefonlar1",
        "icon": {
            "id": 17,
            "path": "df9d1306-3013-4353-b48f-c7ed51347569.png",
            "filename": "batman-is-watching-beautiful-sunset-wallpaper-2560x1080_14 — копия.jpg"
        }
    }
}
```

---

**GET** `/` or `?page=3&limit=9` 

`Response`

```json
{
    "message": "Retrive all category",
    "category": [
        {
            "id": 4,
            "title": "13-Sichqoncha",
            "icon": null
        },
        {
            "id": 5,
            "title": "1111tq1wdsaelefon",
            "icon": {
                "id": 10,
                "path": "4fea9216-c41b-479f-a982-fbeb7ccb74e2.png",
                "filename": "beautiful-anime-girl-watching-beautiful-view-of-sunset-and-clouds-wallpaper-2560x1080_14 — копия.jpg"
            }
        }
    ]
}
```

---

**Put** `/:id` 

**Authorization**: `Token` 

> required ```Admin``` & `Supervisor` role 

`Request`

```json
{
    "title": "Telefon",
    "iconId": 24
}
```

`Reponse`

```json
{
    "message": "Category updated",
    "category": {
        "id": 3,
        "title": "Telefon",
        "icon": 24
    }
}
```

---

**DELETE** `/:id`

`request header` - **Authorization**: `Token` 

> ! required `supervisor`, `Admin` role

`Response`

```json
{
    "message": "Category deleted by id: 16",
    "category": {
        "id": 16,
        "title": "telefonlar",
        "icon": {
            "id": 22,
            "path": "ea234e02-39cf-4553-9114-565ecc30f44e.png",
            "filename": "alone-forever-wallpaper-2560x1080_14.jpg"
        }
    }
}
```