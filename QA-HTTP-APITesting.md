<h3>What is the HTTP Protocol? Is it the same as API Testing?</h3>

The HTTP Protocol and API Testing are related concepts, but they focus on different aspects of software systems. Here's an explanation of each:
What is the HTTP Protocol?

HTTP (Hypertext Transfer Protocol) is a communication protocol used to transfer data between a client (e.g., a browser or application) and a server over the internet. It forms the foundation of data exchange on the web.
Key Components of HTTP:

    Request: Sent by the client to the server to fetch or modify data.
        Example:

    GET /index.html HTTP/1.1
    Host: www.example.com

Response: Sent by the server back to the client.

    Example:

        HTTP/1.1 200 OK
        Content-Type: text/html

    HTTP Methods: Define the action to be performed.
        GET: Retrieve data.
        POST: Submit data to the server.
        PUT: Update existing data.
        DELETE: Remove data.
        
    Status Codes: Indicate the result of the request.
        200 OK: Successful request.
        404 Not Found: Resource not found.
        500 Internal Server Error: Server-side error.

Purpose of HTTP:

    Facilitates communication between clients and servers.
    Used to access web pages, APIs, and other resources.

<hr>
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
