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
5. Update development in knexfile.js
6. Create index.js file
7. Create empty data folder
8. npx knex migrate:make create_x_table -- create your tables
9. Go into migrations and work on each of the files
10. npx knex migrate:latest
11. npx knex seed:make 001-dishes – create all seeds
12.	npx knex seed:run
13. Create dbConfig.js in database folder
14.	Create x-model.js in x folder
15.	Create auth folder
