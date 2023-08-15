### File Upload

> Base url: `/api/v1/upload`

**POST** `/`

**Authorization**: `Bearer <token>`

> ! Required `Admin`, `Supervisor` role

`Request`
```js
formdata: name="files"
```

`Response`

```json
{
    "message": "Files uploaded",
    "data": [
        {
            "id": 35,
            "filename": "batman-is-watching-beautiful-sunset-wallpaper-2560x1080_14 — копия.jpg",
            "path": "3328491b-cc7e-4aff-8544-41ac73ae505c.png"
        }
    ]
}
```

---

**GET**  `/files` or `?page=5&limit=10`

> request header => **Authorization** `Token`

> required role: `Admin`, `Supervisor`

`Response`

```json
{
    "message": "Retrive all files",
    "files": [
        {
            "id": 15,
            "path": "7e5dd7c5-6b89-4cc5-91b5-e02d33edface.png",
            "filename": "artistic-sunset-wallpaper-2560x1080_14.jpg"
        },
        {
            "id": 16,
            "path": "9f2231cb-9490-4976-b6d6-542f86fc9d3e.png",
            "filename": "astronaut-drinking-beer-on-moon-while-watching-earth-wallpaper-2560x1080_14.jpg"
        } 
    ]
}
```

---

**GET** `/:id` 

> request header => **Authorization** `Token`

> required role: `Admin`, `Supervisor`

`Response`

```json
{
    "message": "Retrive file",
    "file": {
        "id": 13,
        "path": "d4c995a0-bb27-4d4a-9b77-b395246aca23.png",
        "filename": "fantasy-world-wallpaper-2560x1080_14.jpg"
    }
}
```

---

**PUT** `/:id`

> `request header` - **Authorization**: `Token` 

> required role: `Admin`, `Supervisor`

`Request`

```js
formdata: name="files"
```

`Response`

```json
{
    "message": "New file uploaded",
    "data": [
        {
            "id": 12,
            "path": "18b133e9-11fa-4154-a20b-d997e991bc63.png",
            "filename": "batman-is-watching-beautiful-sunset-wallpaper-2560x1080_14.jpg"
        }
    ]
}
```

---

**DELETE** `/:id`

> `request header` - **Authorization**: `Token` 

> required role: `supervisor`

`Response`

```json
{
    "message": "File removed",
    "icon": {
        "id": 11,
        "path": "89279f28-5516-4edf-98ac-afd2b7c20cea.png",
        "filename": "beautiful-anime-girl-watching-beautiful-view-of-sunset-and-clouds-wallpaper-2560x1080_14.jpg"
    }
}
```