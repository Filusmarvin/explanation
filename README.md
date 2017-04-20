# explanation

### routes (routes/catalog.js)

* When express.Router() is called, a slightly different "mini app" is returned. It is still an object.Router  is to go through a couple of pages easily with out having it all on one page so the file does not look to hectic.
* routes/catalog.js is called in the routes folder. The routes folder then searches for /catalog/ and the information that comes after the second "/" which is /author/:id'. It searches the page for the corresponding paremeter and runs that function. router.get('/author/:id', author_controller.author_detail);

### controllers (controllers/authorController.js)

* What is called after the second "/" is /author/:id/. The corresponding function then is looked for in the controllers file and gets the .author_detail object.
* Then the function exports.author_detail is ran. Async.parallel = async.parallel() allows you to push a bunch of (potentially unrelated) asynchronous calls into an array. Once we have the array populated, we execute all the tasks inside it, then call a function when we’re done.


### models (models/Author.js and models/Book.js)

* Author.js file is needed when the variable author is called and mongoose will then .find() the info in the data base and return an object. That object is formatted with a schemas.

### schemas
* schemas takes the information and formats it to look a certain way like a theme.

### virtuals

* Virtuals takes the information and formats it but it is not saved in the DB. It is just held there for the moment.

### views (views/author_detail.pug)
* takes the information in like a handlebar and places the information on to the page.

### mongoose

* It is like a bridge that searches the DB and brings it back.
