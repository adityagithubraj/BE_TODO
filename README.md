# BE_TODO


## Deployed link

<br>
https://attractive-gray-goshawk.cyclic.app/
<br>

## Installation

```
npm install
```

## Start the Backend server 

```


npm run server
```


<br>

##  MVC Structure

```

     ├── config
     |    └── db.js
     ├── middleware
     |    └── auth.js
     |    
     ├── models
     |    └── todo.model.js
     |    └── User.model.js
     ├──routes
     |    └── todo.route.js
     |    └── user.route.js
     └── index.js
```
Things to do before starting the server:- 

-  create `.env` file and put "PORT", "URL", "SECRET_KEY".
- "PORT" is for listening the server.
- "MONGODB_URL" write your mongo url here.
- "SECRET_KEY" write your jwt secret key here

<br>

## Schema 

<br>

<h3><strong>Schema for signUp</strong><h3>

```js

{
  "name": "Your Name",
  "email": "your@email.com",
  "password": "your_password"
}

```

<h3><strong>Schema for login</strong><h3>

```js


    {
  "email": "your@email.com",
  "password": "your_password"
}

  

```


<h3><strong>Schema for creating/posting  Todo</strong><h3>

```js
{
  "title": "Your Todo Title",
  "description": "Your Todo Description",
  "completed": false
}

```

<h3><strong>Schema for Update Todo</strong><h3>

```js
{
  "title": "Updated Todo Title",
  "description": "Updated Todo Description"
}

```

## Endpoints

<table>
    <thead>
        <tr>
            <th>METHOD</th>
            <th>ENDPOINT</th>
            <th>DESCRIPTION</th>
            <th>STATUS CODE</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>POST</td>
            <td>/signup</td>
            <td>This endpoint should allow users to register</td>
            <td>201</td>
        </tr>
        <tr>
            <td>POST</td>
            <td>/login</td>
            <td>This endpoint should allow users to login.</td>
            <td>200</td>
        </tr>
        <tr>
            <td>POST</td>
            <td>/createTodo</td>
            <td>This endpoint is used to create new Todo  if valid token present in headers authorization with Bearer</td>
            <td>201</td>
        </tr>
         <tr>
            <td>GET</td>
            <td>/getTodoList</td>
            <td>This endpoint is used to get Todo list of authorized user if valid token present in headers authorization with Bearer</td>
            <td>200</td>
        </tr>
         <tr>
            <td>PUT</td>
            <td>/updateTodo/:id</td>
            <td>This endpoint is used to update Todo of authorized user by Todo id if valid token present in headers authorization with Bearer</td>
            <td>201</td>
        </tr>
        <tr>
            <td>DELETE</td>
            <td>/deleteTodo/:id</td>
            <td>This endpoint is used delete todo of authorized user if valid token present in headers authorization with Bearer</td>
            <td>200</td>
        </tr>
         <tr>
            <td>GET</td>
            <td>/getAllTodo</td>
            <td>This endpoint is used get all todo of all users if valid token present in headers authorization with Bearer</td>
            <td>200</td>
        </tr>
        
    </tbody>
</table>


<br>

