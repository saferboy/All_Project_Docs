#  Comment All Api

## Required Options

> ## Base URL
> '/api/v1/comment'

> ### Required Role For All Routes
>  - Admin
>  - Supervisor


> ## Required Access Token
> Req Header:
> - Authorization 

---

## Create Comment with Product `Id`

> ### `/POST`
> 
> ### **`Request`**
> 
> ```json
> {
>    "productId": 3,
>    "comment": "nice product",
>    "rate": 1
> }
> ``` 


> ### **`Response`**
>
> ```json
> {
>    "message": "Your comment is sending",
>    "comment": {
>        "user": {
>            "id": 1,
>            "name": "John"
>        },
>       "id": 34,
>        "comment": "nays product",
>        "rate": 1
>    }
> }
> ```


---

## Find Comment By `Id`

> ### `/GET:Id`
>
>  ### **`Response`**
>
> 
> ```json
> {
>    "message": "Retrive comment by id: 26",
>    "comment": {
>        "user": {
>            "id": 1,
>            "name": "1"
>        },
>        "productId": 3,
>        "id": 26,
>        "comment": "nays product",
>        "rate": 1
>    }
> } 
> ```    

---


## All Comment

> ### `/GET` or `?page=1&limit=1`
>
> ### **`Response`** 
> ```json
> {
>    "message": "Retrive all comments",
>    "comments": [
>        {
>            "userId": 1,
>            "productId": 4,
>            "id": 26,
>            "comment": "nays product",
>            "rate": 1
>        },
>        {
>            "userId": 1,
>            "productId": 3,
>            "id": 27,
>            "comment": "bad product",
>            "rate": 1
>        }
>    ]
> } 
> ```

---

## Delete Comment

> ### `/DELETE/:id`
>
> ### **`Response`**
> ```json
> {
>    "message": "Comment removed",
>    "comment": {
>        "userId": 1,
>        "productId": 3,
>        "id": 26,
>        "comment": "Gavno product",
>        "rate": 1
>    }
> }
> ```
