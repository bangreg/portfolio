<h3>API testing of KasirAPI</h3>

View documentation at https://web.postman.co/workspace/43cf99e0-c01c-4daf-9e97-820563165189/documentation/12307865-cbdfed5a-ea4e-4815-8010-4c1b81d7e46d

Knowledge:
URL: https://api.example.com/users
<br>Metode HTTP:

    GET /users: Gets a list of users.
    POST /users: Adds a new user.
    GET /users/{id}: Gets details of a user with a specific ID.
    PUT /users/{id}: Updates the data of a user with a specific ID.
    DELETE /users/{id}: Deletes a user with a specific ID.

Practice at KasirAPI
<hr>
POST<br>
1. registration: https://kasir-api.belajarqa.com/registration
<br>response:

    {
      "name": "Toko Samuel",
      "email": "samuel@email.com",
      "password": "123adsfadf@"
    }

2. authentication: https://kasir-api.belajarqa.com/authentication
<br>response: 

       {
          "email":"samuel@email.com",
          "password":"123adsfadf@"
       }

3. users: https://kasir-api.belajarqa.com/users
<br>response:
<br>3.1 FailToCreateUsers

       {
          "email":"samuel@email.com",
          "password":"123adsfadf@"
        }
3.2 SucceddToCreateUsers

       {
          "status": "success",
          "message": "User berhasil ditambahkan",
          "data": {
            "userId": "3327a164-8988-4107-8bab-cbcb4a4e7c67",
            "name": "kasirsam-serbaguna"
          }
       }
<hr>
GET<br>
1. users: https://kasir-api.belajarqa.com/users/3327a164-8988-4107-8bab-cbcb4a4e7c67
<br>response:
    
    {    
    "status": "success",
    "data": {
        "user": {
            "id": "3327a164-8988-4107-8bab-cbcb4a4e7c67",
            "name": "kasirsam-serbaguna",
            "email": "usersam@example.com",
            "role": "kasir"
          }
        }
    }
2. userlist: https://kasir-api.belajarqa.com/users?q=kasir-serbaguna&p=1
<br>response:
    
       {
          "status": "success",
          "data": {
            "users": [
                {
                    "id": "3526f54d-1d08-4a05-900a-31a14e991a37",
                    "name": "kasir-serbaguna",
                    "email": "samuel@email.com",
                    "role": "kasir"
                }
            ],
            "meta": {
                "totalPages": 1,
                "total": 1,
                "page": 1
                }
          }
        }
<hr>
DELETE<br>
1. deleteUser: https://kasir-api.belajarqa.com/users/:userId
<br>response:
    
    {
      "status": "success",
      "message": "User berhasil dihapus"
    }
2. deleteUnit: https://kasir-api.belajarqa.com/units/:unitId
<br>response:


       {
         "status": "success",
         "data": {}
       }
<hr>
PUT<br>
1. updateUser: https://kasir-api.belajarqa.com/users/:userId
<br>response: 
      
      {
        "status": "success",
        "message": "User berhasil diupdate",
        "data": {
            "name": "update-user"
        }
      }
