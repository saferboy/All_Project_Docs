


## User management routes

---

> Base URL: `/api/v1/user`

> Any routes required `admin` roles
 
> Any  routes required `supervisor` roles

> Any  routes required `user` roles


<br>


**GET** `/users`

**Authorization**: `Token` 

> required ```Admin``` or `Supervisor` role 

`Response`

```json
{
    "message": "Retrive all users",
    "user": [
        {
            "id": 3,
            "name": "Muxtor",
            "surname": "Saferboy",
            "phone": [
                "+93-557-03-87"
            ],
            "email": "1test@gmail.com",
            "address": "Xorazm",
            "role": "user"
        },
    ]
}
```

---

**GET** `/:id` 

**Authorization**: `Token` 

> required ```Admin``` or `Supervisor` role 

`Response`

```json
{
    "message": "Retrive user",
    "user": {
        "id": 3,
        "name": "Muxtor",
        "surname": "Saferboy",
        "phone": [
            "+93-557-03-87"
        ],
        "email": "1test@gmail.com",
        "address": "Xorazm",
        "role": "user"
    }
}
```

---

**PUT** `/:id`

`Change user's personal data`

`request header` - **Authorization**: `Token` 

> ! required `User` role

`Request`

```json
{
    "name": "Amirbek",
    "surname": "Amirbek",
    "phone": "123445566",
    "email": "amir@gmail.com",
    "address": "Xiva",
    "password": "2"
}
```

`Reponse`

```json
    {
    "message": "Update user info",
    "user": {
        "id": 2,
        "name": "Amirbek",
        "surname": "Amirbek",
        "phone": [
            "123445566"
        ],
        "email": "amir@gmail.com",
        "address": "Xiva",
        "password": "$2b$10$8hUCowUndas243fq6OyezuAYpy"
    }
}
```
---

**PUT** `/role/:id` 

`request header` - **Authorization**: `Token` 

> ! required `supervisor` role

`Request`

```json
{
    "role": "admin"
}
```

`Response`

```json
{
    "message": "User's role has changed",
    "user": {
        "id": 12,
        "name": "Muxtor",
        "role": "user"
    }
}
```

---

**DELETE** `/:id`

`request header` - **Authorization**: `Token` 

> ! required `supervisor` role

`Response`

```json
{
    "message": "User removed",
    "user": {
        "id": 1,
        "name": "Muxtor",
        "surname": "Saferboy",
        "phone": [
            "+93-557-03-87"
        ],
        "email": "test@gmail.com",
        "address": "Xorazm",
        "password": "$2b$10$lLXiy5jiVD0w1os6YPmcGDmEZTmR6",
        "role": "admin"
    }
}
```