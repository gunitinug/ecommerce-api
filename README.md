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

### sign in User

```
POST {{your_ip}}/ecommerce/api/signin

Request Body:
{
  "email": "michael@ms.com",
  "password": "m123456"
}
```
