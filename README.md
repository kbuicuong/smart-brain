##API Key

Must register your own Clarifai API key to use this app.

##Database

Install postGresql
Create two tables called 'login' and 'users'

CREATE TABLE login (
    id serial PRIMARY KEY,
    hash VARCHAR(100) NOT NULL,
    email text UNIQUE NOT NULL
);

CREATE TABLE users (
    id serial PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    email text UNIQUE NOT NULL,
    entries BIGINT DEFAULT 0,
    joined TIMESTAMP NOT NULL
);

##Run

npm start