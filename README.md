# node-boilerplate-cheatsheet
1. yarn init
2. In package.json, add:
```
"scripts": {
  "server": "nodemon index.js"
}
```
3. yarn add nodemon express helmet knex sqlite3 cors bcryptjs express-session connect-session-knex jsonwebtoken
4. npx knex init
5. Update knexfile.js -- *filename: location and name of your database, migrations and seeds locations:*
```
module.exports = {
  development: {
    client: 'sqlite3',
    useNullAsDefault: true,
    connection: {
      filename: './database/auth.db3',
    },
    pool: {
      afterCreate: (conn, done) => {
        conn.run('PRAGMA foreign_keys = ON', done);
      },
    },
    migrations: {
      directory: './database/migrations',
    },
    seeds: {
      directory: './database/seeds',
    },
  },
};

```
6. Create index.js file:
```
const server = require('./api/server.js');

const port = process.env.PORT || 5000;
server.listen(port, () => console.log(`\n** Running on port ${port} **\n`));
```
7. npx knex migrate:make create_x_table  --  *to create your tables*
8. Go into migrations and work on each of the tables
9. npx knex migrate:latest
10. npx knex seed:make 001-dishes  --  *to create seeds if needed*
11.	npx knex seed:run
12. Create dbConfig.js in database folder
```
const knex = require('knex');
const config = require('../knexfile.js');

const environment = process.env.DB_ENV || "development";
  
module.exports = knex(config[environment]);
```
13.	Create x-model.js in x folder
14.	Create auth folder
