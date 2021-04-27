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
    "role": 1
}
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

Path Variables:
:userId

Authorization:
Bearer Token

Note: userId path variable and userId of the bearer token must match.
```
