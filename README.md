# Awesome Project Build with TypeORM

Steps to run this project:

1. Run ```npm i``` command
2. Setup database settings inside ```ormconfig.json``` file
3. Run ```npm start``` command

# How to use:

Run `npm install -g typeorm`\
Run ```typeorm init --database postgres --express``` the database could be MySQL / MariaDB / Postgres / SQLite / Microsoft SQL Server / Oracle / sql.js / MongoDB
- Run `npm install`
- Run `npm install -s helmet cors jsonwebtoken bcryptjs class-validator ts-node-dev` for additional dependencies
- Run `npm install -s @types/bcryptjs @types/body-parser @types/cors @types/helmet @types/jsonwebtoken`

- To create a new user we need an ADMIN. This firt user will be created by a migration process:
- run `typeorm migration:create -n CreateAdminUser` this will create the CreateAdminUser_someNumbers under the migrations folder, which is then modified as you see in this example project
- to start the project run `npm start` 
- now the migration can be run, to insert the new admin user 
`npm run migration:run`
- To access the login route, for example, you will call:
`http://localhost:3000/auth/login`

# Explanations

helmet:\
     - Helps us to secure our application by setting various HTTP headers
cors:\
     - Enable cross-origin Requests
body-parser:\
     - Parses the client’s request from json into javascript objects
jsonwebtoken:\
     - Will handle the jwt operations for us
bcryptjs:\
     - Help us to hash user passwords
typeorm:\
     - The ORM we are going to use to manipulate database
reflect-metadata:\
     - allow some annotations features used with TypeORM
class-validator:\
     - A validation package that works really well with TypeORM
ts-node-dev:\
     - Automatically restarts the server when we change any file
