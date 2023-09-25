# Favorite md

## Required Options

> ## Base URL
> ### `/api/v1/favorite`

> ## Required Access Token
> Req Header:
> - Authorization 
---

> ### `/POST`

`Request`
```json
{
    "productId": 3
}  
```

`Response`

```json
{
    "message": "Product has been added to favorites",
    "favorite": {
        "id": 5,
        "userId": 7,
        "product": {
            "id": 3,
            "title": "Olma111",
            "rating": 0,
            "discount": "90%",
            "sellPrice": "300$",
            "image": [
                {
                    "id": 4,
                    "path": "0b56c83b-19dc-421b-8f09-5ffebbfd713e.jpg",
                    "filename": "batman-is-watching-beautiful-sunset-wallpaper-2560x1080_14 — копия.jpg"
                },
                {
                    "id": 5,
                    "path": "17f27c8c-a5aa-4275-951f-dcf97596c2c5.jpg",
                    "filename": "batman-is-watching-beautiful-sunset-wallpaper-2560x1080_14.jpg"
                }
            ]
        }
    }
}
```
---

> ### Find Product By Id
>
> ### `/GET:id`

`Response`

```json
{
    "message": "Your favorite product",
    "favorite": {
        "id": 3,
        "userId": 7,
        "product": {
            "id": 3,
            "title": "Apple",
            "rating": 0,
            "discount": "90%",
            "sellPrice": "300$",
            "image": [
                {
                    "id": 4,
                    "path": "0b56c83b-19dc-421b-8f09-5ffebbfd713e.jpg",
                    "filename": "batman-is-watching-beautiful-sunset-wallpaper-2560x1080_14 — копия.jpg"
                }
            ]
        }
    }
}
```
---

> ### All Favorite Products
>
> `/GET` or `?page=1&limit=1`

`Response`

```json
{
    "message": "All favorite products",
    "favorite": [
        {
            "id": 3,
            "product": {
                "id": 3,
                "title": "Olma111",
                "rating": 0,
                "discount": "90%",
                "sellPrice": "300$",
                "image": [
                    {
                        "id": 4,
                        "path": "0b56c83b-19dc-421b-8f09-5ffebbfd713e.jpg",
                        "filename": "batman-is-watching-beautiful-sunset-wallpaper-2560x1080_14 — копия.jpg"
                    }
                ]
            }
        },
        {
            "id": 4,
            "product": {
                "id": 3,
                "title": "Olma111",
                "rating": 0,
                "discount": "90%",
                "sellPrice": "300$",
                "image": [
                    {
                        "id": 4,
                        "path": "0b56c83b-19dc-421b-8f09-5ffebbfd713e.jpg",
                        "filename": "batman-is-watching-beautiful-sunset-wallpaper-2560x1080_14 — копия.jpg"
                    }
                ]
            }
        }
    ]
}
```
---

## Delete Comment

> ### `/DELETE/:id`
>
> `Response`

```json
{
    "message": "Product has been removed from the favorites list",
    "favorite": {
        "id": 3,
        "userId": 3,
        "product": {
            "id": 3,
            "title": "Olma",
            "rating": 0,
            "discount": "90%",
            "sellPrice": "300$",
            "image": [
                {
                    "id": 4,
                    "path": "0b56c83b-19dc-421b-8f09-5ffebbfd713e.jpg",
                    "filename": "batman-is-watching-beautiful-sunset-wallpaper-2560x1080_14 — копия.jpg"
                }
            ]
        }
    }
}
```
