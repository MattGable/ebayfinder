#Package installation instructions
ebayfinder is a node.js add-on and is a quick way to search ebay for an item based <br />
on its maximum price.<br />
##Dependencies used (dotenv, ebay-api)
```shell
npm install dotenv ebay-api --save
```
##Adding this dependency (manually)
Edit your package.json to include:
```javascript
"ebayfinder": "git+https://github.com/MattGable/ebayfinder.git"
```
##Using ebayfinder
1) ebayfinder suggests dotenv, which requires a .env file (a place to hide your API key).<br />
Add a .env file to the root of your application with the following variable:
```shell
KEY=<Your ebay API key>
```
1a) Inserting your key via your choice of security measure (see ebay-api examples)<br />
is currently suggested for projects not utilizing dotenv, though eliminating this<br />
dependency is planned.
2) You also need to include ebayfinder in your code!
```javascript
var myFunctionName = require('ebayfinder');
```
3) Since ebayfinder has only one function, you can use its require as the function.
```javascript
myFunctionName("nameOfProduct", 99, function(err, res){
    console.log("Inside ebayfinder's function call...");
    //The output of this function is also automatically logged to your console.
});
```
