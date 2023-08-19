
# PicPay Simplificado

The main core of a payment system

Just run the file PicpaysimplificadoApplication.java




## Documentation

#### Add an user 

```http
  POST /users
```
#### Example Request:

```json
{
    "firstName": "Gabriel",
    "lastName": "Spacki",
    "email": "gabriel@gmail.com",
    "password": "mypassword",
    "document": "123",
    "userType": "COMMON",
    "balance": 12
}
```
#### Example Response:

```json
{
    "id": 1,
    "firstName": "Gabriel",
    "lastName": "Spacki",
    "document": "123",
    "email": "gabriel@gmail.com",
    "password": "mypassword",
    "balance": 12,
    "userType": "COMMON"
}
```

#### Create a transaction: 

```http
  POST /users
```
#### Example Request:

```json
{
    "senderId": "1",
    "receiverId": "3",
    "value": 5
}
```
#### Example Response:

```json
{
    "id": 1,
    "amount": 5,
    "sender": {
        "id": 1,
        "firstName": "Gabriel",
        "lastName": "Spacki",
        "document": "123",
        "email": "gabriel@gmail.com",
        "password": "mypassword",
        "balance": 7.00,
        "userTpye": "COMMON"
    },
    "receiver": {
        "id": 3,
        "firstName": "Laura",
        "lastName": "Larissa",
        "document": "321",
        "email": "laura@gmail.com",
        "password": "yourpassword",
        "balance": 17.00,
        "userTpye": "COMMON"
    },
    "timestamp": "2023-08-19T02:48:19.389766"
}
```
#### Return all users: 

```http
  GET /users
```
#### Example Response:

```json
[
    {
        "id": 1,
        "firstName": "Gabriel",
        "lastName": "Spacki",
        "document": "123",
        "email": "gabriel@gmail.com",
        "password": "mypassword",
        "balance": 7.00,
        "userTpye": "COMMON"
    },
    {
        "id": 3,
        "firstName": "Laura",
        "lastName": "Larissa",
        "document": "321",
        "email": "laura@gmail.com",
        "password": "yourpassword",
        "balance": 17.00,
        "userTpye": "COMMON"
    }
]
```
