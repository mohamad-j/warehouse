## Create a project with Apico

### Create a folder and call it like you project name.

### Open the folder from Visual Studio Code

### Init NPM by runnin:
` npm init `

### Install apico 
` npm install apico `

### Initiate Apico project
` npx lh init `

### Add apps that you need for your project
` npx lh app app-name `  *Change app-name with the name of app you want to add*

### Add an endpoint
Every request to the server need to be handled by an endpoint.
All endpoints must be exist under the **/routes** folder.
It is up to you to orgnize your endpoints. But it is preffered that you group your endpoints into files.

For instance if you want to create en points for getting/adding/updating/deleting users, it is better to have all this endpoints in one file **/routes/users**.

this is how you create all thses endpoints.
``` jAVAsCRIPT
const router = require('express').Router();
const { app } = require('apico/server.js');

/** Declare routes for Router */


/// http://localhost:3000/customers/all
router.post('/all', function( req, res ){

    res.json({"message":"OK"});
});


/// http://localhost:3000/customers/create
router.post('/create', function( req, res ){

    res.json({"message":"OK"});
});


/// http://localhost:3000/customers/update
router.post('/update', function( req, res ){

    res.json({"message":"OK"});
});


/// http://localhost:3000/customers/delete
router.post('/delete', function( req, res ){

    res.json({"message":"OK"});
});



app.use( '/users', router );
```


