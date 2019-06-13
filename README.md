# node-cheatsheet
1. yarn init
2. In package.json, add:
```
"scripts": {
  "server": "nodemon index.js"
}
```
3. yarn add nodemon express helmet knex sqlite3 cors bcryptjs express-session connect-session-knex jsonwebtoken
4. npx knex init
•	Change development in knexfile.js
•	Create index.js file
•	Create empty data folder
•	npx knex migrate:make create_dishes_table
•	Go into migrations and work on each of the files
•	npx knex migrate:latest
•	Npx knex seed:make 001-dishes – create all seeds
•	Npx knex seed:run
•	Create dbConfig.js in database folder
•	Create x-model.js in x folder
•	Create auth folder
