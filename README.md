# Get started with POSTGRES 

https://blog.logrocket.com/nodejs-expressjs-postgresql-crud-rest-api-example/

https://docs.microsoft.com/en-us/windows/wsl/tutorials/wsl-database

https://marketplace.visualstudio.com/items?itemName=ms-ossdata.vscode-postgresql

https://marketplace.visualstudio.com/items?itemName=cweijan.vscode-mysql-client2

## Install

sudo apt update
sudo apt upgrade
sudo apt install postgresql postgresql-contrib

sudo service postgresql start

sudo passwd postgres

sudo -u postgres psql

CREATE ROLE me WITH LOGIN PASSWORD 'password';
ALTER ROLE me CREATEDB;

Connect
Create database api

CREATE TABLE users (
  ID SERIAL PRIMARY KEY,
  name VARCHAR(30),
  email VARCHAR(30)
);

INSERT INTO users (name, email)
  VALUES ('Jerry', 'jerry@example.com'), ('George', 'george@example.com');

## API

GET /users
```
[
    {
        "id": 1,
        "name": "Jerry",
        "email": "jerry@example.com"
    },
    {
        "id": 2,
        "name": "George",
        "email": "george@example.com"
    },
    {
        "id": 3,
        "name": "Kramer",
        "email": "kramer@example.com"
    },
    {
        "id": 4,
        "name": "Elaine",
        "email": "elaine@example.com"
    }
]
```

GET /users/id
```
[
    {
        "id": 2,
        "name": "George",
        "email": "george@example.com"
    }
]
```

POST /users
BODY
```
{
    "name": "Kramer",
    "email": "kramer@example.com"
}
```
RESPONSE
```
User added with ID: 14
```

PATCH /users/id
BODY
```
{
    "name": "Kramer",
    "email": "kramer@example.com"
}
```
RESPONSE
```
User modified with ID: 4
```

DELETE /users/id
```
User deleted with ID: 4
```