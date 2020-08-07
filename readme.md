# Node Review
This ReadMe will discuss how to create a node for reference later.

### Steps
- set up file
- importing data
- 

#### Set up File
- In terminal, cd into a directory. type "npm init"
- The terminal will walk through default information for your node set up. If you don't wish to view defaul install you may have typed "npm init -y".
- Open in vs code with "code ."
- note that conditions will link to index.js by default, if it doesn't exist you will need to create one, or change this default to your .js name.
- test if functional with node index.js in the terminal, will output index.js commands. 

#### Importing Data
- you can call data from another js file into your file by creating modules.
For example in myModule.js
``` JavaScript 
module.exports.beBasic = () => "That's so fetch!"
```
draw into index.js with 
``` JavaScript
const myModule = require('./myModule.js')
console.log(myModule.beBasic())
```
#### NPM Node Package Manager
- NPM is a website or something with open source code. Many times people use this code to not "start from scratch" in their projects. Especially as people will share issues and code that solves them etc.

- You can add an NPM to your directory using " npm install X" X, meaning the command of your NPM.
- To upload to git, you'll want to move NPM's files to be .gitignore. You can set this by touch .gitignore and indicating the directory of folders in the body of this file before pushing to github.
- In class we've used modules like express, chalk, moment and ejs.
- To add to a node app, call into your js.
``` JavaScript 
var express = require('express');
var app = express();
app.listen(3000)
```
- In using express we us "app." and can choose from different route methods on how to utilize the information. Some common examples below.
```JavaScript
app.get('/', function (req, res) {
  res.send('GET request to the homepage')
})
```
Where '/' indicates the html line. 
- You can add a view to your route like:
```JavaScript
app.get('/animals', function (req, res) {
  res.render('animals')
})
```
Where express will look in "views" for file "animals" and call it on localhost:3000/animals.

- Templates
Add templte engine like ejs
``` JavaScript
app.set('view engine', 'ejs');
```
rename hmtl files to .ejs, also use res.render.
Using <% %> tags to indicate javaScript in ejs files. within html boilerplate. Add = to print.
- Layouts
npm install express-ejs-layouts
``` JavaScript
var ejsLayouts = require('express-ejs-layouts');
app.use(ejsLayouts);
```
Will need to use layout.ejs in our views to create template.
- Controllers
Controllers are used to simplify your app calls. and create one document for your navigation pages.
create controllers folder, each .js in the folder will navigate to a new line. 
```JavaScript
var express = require('express');
var router = express.Router();

router.get('/foods', function(req, res) {
  res.render('faves/foods', {title: 'Favorite Foods', foods: ['coconut', 'avocado']});
});

router.get('/animals', function(req, res) {
  res.render('faves/animals', {title: 'Favorite Animals', animals: ['sand crab', 'corny joke dog']})
});

module.exports = router;
```

