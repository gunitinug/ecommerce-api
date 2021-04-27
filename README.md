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
