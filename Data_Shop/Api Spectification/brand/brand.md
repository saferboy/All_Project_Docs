

## Cateory endpoints


---

> Base url: `/api/v1/brand`


<br>

**POST** `/`

**Authorization**: `Token` 

> required ```Admin``` or `Supervisor` role

`Request`

```json
{
    "categoryId": 7,
    "title": "Redmi",
    "iconId": 2
}
```

`Response`

```json
{
    "message": "Brand created",
    "brand": {
        "id": 9,
        "title": "Redmi",
        "logo": {
            "id": 2,
            "path": "863fff25-9bf5-4662-b93c-3f25d53a828b.png",
            "title": "artistic-sunset-wallpaper-2560x1080_14.jpg"
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
        "title": "Samsung",
        "icon": {
            "id": 17,
            "path": "df9d1306-3013-4353-b48f-c7ed51347569.png",
            "filename": "batman-is-watching-beautiful-sunset-wallpaper-2560x1080_14 — копия.jpg"
        }
    }
}
```

---

**GET** `/` 

`Response`

```json
{
    "message": "Retrive all brands",
    "brand": [
        {
            "id": 4,
            "title": "Hp",
            "icon": {
                "id": 16,
                "path": "9f2231cb-9490-4976-b6d6-542f86fc9d3e.png",
                "filename": "astronaut-drinking-beer-on-moon-while-watching-earth-wallpaper-2560x1080_14.jpg"
            }
        }
        {
            "id": 3,
            "title": "Xiaomi1",
            "icon": {}
        }
    ]
}
```

---

**Put** `/:id` 

**Authorization**: `Token` 

> required `Admin` & `Supervisor` role 

`Request`

```json
{
    "title": "Apple",
    "iconId": 32
}
```

`Reponse`

```json
{
    "message": "Brand updated",
    "id": 2,
    "title": "Apple",
    "logo": {
        "id": 32,
        "path": "a6790c43-1e97-41b5-83cc-bb7e07832d9f.png",
        "filename": "astronaut-drinking-beer-on-moon-while-watching-earth-wallpaper-2560x1080_14.jpg"
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
    "message": "Brand deleted",
    "brand": {
        "id": 2,
        "title": "Apple",
        "logo": {
            "id": 32,
            "path": "a6790c43-1e97-41b5-83cc-bb7e07832d9f.png",
            "filename": "astronaut-drinking-beer-on-moon-while-watching-earth-wallpaper-2560x1080_14.jpg"
        }
    }
}
```