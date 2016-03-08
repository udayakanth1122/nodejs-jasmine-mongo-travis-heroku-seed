# NodeJS + Express + Jasmine + MongoDB + Travis + Heroku
This is a seed project to showcase a RESTful webservice built with NodeJS, Express and Mongo. the project also contains sample unit test which are executed using Jasmine.
This project also has travis.yml to build and deploy the code using Travis onto Heroku cloud platform.

Here, we assume that a mongo database has already been set up. If the database has NOT been set up, follow the instructions below.

To start using this project, you need the following prerequisites

1. [NodeJS](www.nodejs.org)
2. [MongoDB](www.mongodb.org)
3. [Heroku](https://www.heroku.com)

After installing mongodb, set up your database. To do so, follow these steps

1. Open command prompt and navigate to your mongo install directory (Let's assume it's C:\mongo\bin)
2. Type `mongod -dbpath <path to your repo/data>` (Eg: `mongod -dbpath c:\nodejs\exampleWebservice\data`)
3. Open a *new terminal*, navigate to mongo install directory again and type `mongo`. This will open a mongo terminal.
4. In this mongo terminal, type `use nodetest2`. nodetest2 is the name of this project, which can be anything you want. See
   `app.js` to find that name
5. Insert some dummy record. Type `db.userlist.insert({'username' : 'test1','email' : 'test1@test.com','fullname' : 'Bob Smith','age' : 27,'location' : 'San Francisco','gender' : 'Male'})
`
6. That's it. Your database is up and running with one record.

Time to see the webservice at work.

1. Start your server by starting a *new terminal*, then navigate to your project folder (Ex: `C:\exampleWebservice`)
2. Type `npm start`
3. In a browser, navigate to this URL [http://localhost:3000/users/userlist](http://localhost:3000/users/userlist)

You will see a plain text JSON response that looks like this
```
[{"_id":"562e720109732b48137634a0",
  "username":"test1","email":"test1@test.com",
  "fullname":"Bob Smith",
  "age":27,
  "location":"San Francisco",
  "gender":"Male"}]
```

This means the API endpoint userlist is working.

Feel free to tweak and play around with this seed project (fork it first).
To learn more, follow [CWBUECHELER's tutorial](http://cwbuecheler.com/web/tutorials/2014/restful-web-app-node-express-mongodb/)
