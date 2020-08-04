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

