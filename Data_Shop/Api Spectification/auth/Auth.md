

## User authorization endpoints


---

> Base url: `/api/v1/auth`

<br>

**POST** `/login`

```json
{
    "email": "shashvarbek@gmail.com",
    "password": "password"
}
```

`Response`

```json
{
    "smessage": "Succesfuly login",
    "user": {
        "id": 5,
        "name": "Shashvarbek",
        "surname": "Alibek",
        "phone" : [
            "+999-93-123-45-67"
        ],
        "email": "shashvarbek@gmail.com",
        "address": "Xarizma",
        "role": "user"
    },
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOjYsImVtYWlsIjoiM0BnbWFpbC5jb20iLCJh"
}
```

---

**POST** `/register`

`Request`

```json
{
    "name": "Alibek",
    "surname": "Alibek",
    "phone": "+998-90-123-45-67",
    "email": "shashvarbek@gmail.com",
    "address": "Xarizma",
    "password": "1112eda2wed"
}
```

Response

```json
{
    "message": "Verification code sended to email",
    "email": "korakbek@gmail.com",
    "verificationId": "aade4420-533c-45bc-8103-cf6632abb342"
    "timeOut": 300, 
}
```

**POST** `/resend`

`Request`

```json
{
    "email": "shashvarbek@gmail.com"
}
```

`Response`

```json
{
    "message": "Verification code sended to email",
    "email": "korakbek@gmail.com",
    "verificationId": "aade4420-533c-45bc-8103-cf6632abb342",
    "timeOut": 300
}
```

---

**POST** `/verify`

`Request`

```json
{
    "code": "14243",
    "verificationId": "aade4420-533c-45bc-8103-cf6632abb342"
}
```

`Response`

```json
{
    "message": "Succesfuly registered",
    "user": {
        "id": 5,
        "name": "Shashvarbek",
        "surname": "Alibek",
        "phone" : [
            "+999-93-123-45-67"
        ],
        "email": "shashvarbek@gmail.com",
        "address": "Xarizma",
        "role": "user"
    },
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOjYsImVtYWlsIjoiM0BnbWFpbC5jb20iLCJh"
}
```