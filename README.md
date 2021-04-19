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