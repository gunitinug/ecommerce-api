# ecommerce-api
kaloraat's ecommerce node app's API end points

## Demo
- [Setting up reverse proxy](https://www.youtube.com/watch?v=MEnyPUpoe5E)

## sign up User

```
POST {{your_ip}}/ecommerce/api/signup

Request Body:
{
    "name": "michael",
    "email": "michael@ms.com",
    "password": "m123456",    
}

Note: role is 0 by default. This means regular non-admin user.
role is not required when signing up User.
```

## sign in User

```
POST {{your_ip}}/ecommerce/api/signin

Request Body:
{
  "email": "michael@ms.com",
  "password": "m123456"
}

Note: If successful token is generated. 
```
## sign out User

```
GET {{your_ip}}/ecommerce/api/signout
```

## get User information

```
GET {{your_ip}}/ecommerce/api/user/:userId

Path Variables:
:userId

Authorization:
Bearer Token

Note: userId path variable and userId of the bearer token must match.
```

## update User information

```
PUT {{your_ip}}/ecommerce/api/user/:userId

Request Body:
{
    "role": 1
}

Path Variables:
:userId

Authorization:
Bearer Token

Note: userId path variable and userId of the bearer token must match.
Here we are making the user admin (role equals 1).
```

## create Category
```
POST {{your_ip}}/ecommerce/api/category/create/:userId

Request Body:
{
    "name": "react"
}

Path Variables:
:userId

Authorization:
Bearer Token

Note: userId path variable and userId of the bearer token must match.
```

## get Category information

```
GET {{your_ip}}/ecommerce/api/category/:categoryId

Path Variables:
:categoryId
```

## update Cateory

```
PUT {{your_ip}}/ecommerce/api/category/:categoryId/:userId

Path Variables:
:categoryId,
:userId

Authorization:
Bearer Token

Note: userId path variable and userId of the bearer token must match.
```

## delete Category

```
DELETE {{your_ip}}/ecommerce/api/category/:categoryId/:userId

Path Variables:
:categoryId,
:userId

Authorization:
Bearer Token

Note: userId path variable and userId of the bearer token must match.
```
## list all Categories

```
GET {{your_ip}}/ecommerce/api/categories
```

## create Product

```
POST {{your_ip}}/ecommerce/api/product/create/:userId

Request Body (form-data)
name,
description,
price,
sold,
category,
shipping,
photo,
quantity

Path Variables:
:userId

Authorization:
Bearer Token

Note: userId path variable and userId of the bearer token must match.
Request body is passed from form elements in the front-end.
```

## update Product

```
PUT {{your_ip}}/ecommerce/api/product/:productId/:userId

Request Body (form-data)
name,
description,
price,
sold,
category,
shipping,
photo,
quantity

Path Variables:
:productId
:userId

Authorization:
Bearer Token

Note: userId path variable and userId of the bearer token must match.
Request body is passed from form elements in the front-end.
```
