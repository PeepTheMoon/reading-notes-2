when you forget your heroku url, type in terminal
heroku config:get DATABASE_URL

app.use(express.urlencoded({ extended: false }));
to use the urlencoded forms

npm run setup-db to drop and reseed tables

npx create-alchemy-sql-be my-cool-project to spin up a backend

Change all the files in the data directory to match the data model of your app.
Run heroku create
Run npm run setup-heronpmku to create a heroku SQL database in the cloud to go with your heroku app.
Run heroku config:get DATABASE_URL to get your heroku sql database url from the cloud. Put this in your .env file, under DATABASE_URL
Run npm run setup-db
Run npm run start:watch to start the dev server

npm i bcryptjs jsonwebtoken

npx create-react-app
starts a react app.  cd into it, code .
npm i react-router-dom, superagent 


make sure the below is in server.js in order to use the urlencoded form selection in postman (use json in the dropdown, not text)

app.use(express.json());
app.use(express.urlencoded({ extended: false }));
app.use(require('./middleware/error'));

using <form> allows user to press enter to submit or use a button!

