# Welcome to Flight Service

## Project Setup
- clone the project on your local
- Execute `npm install` on the same path as of your root directory of teh downloaded project
- Create a `.env` file in the root directory and add the following environment variable
     -`PORT=3000`
- Inside the `src/config` folder create a new file `config.json` and then add the following piece of json

```
{
 "development": {
    "username": "<your db login name>",
    "password": "<your db password>",
    "database": "Flights_Search_DB_DEV",
    "host": "127.0.0.1",
    "dialect": "mysql"
  }
}
```
- once you've added your db config as listed above, go to the src folder from your terminal and execute `npx sequelize db:create`

`npx sequelize model:generate --name City --attributes name:string`
`npx sequelize db:migrate`

# DB Design 
 - Airplane Table
 - Flight
 - Airport
 - City

 - A flight belong to an anirplane but one airplane can be used to multiple flight
 - A City has many airplane but one airplane belongs to a city
 - One airplane can have many flights, but a flight belongs to one airport