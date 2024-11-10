# What is node js
 Node js is a runtime environment for javascript, so that we can run our javascript without a web server..
> It is asnchronus, and non blocking I/0

#### Is node a web server
> no node is not a web server

#### Why is node used in webservers
> As node can handle heavy I/O, and with only a small code footprint

#### Modules
> in node each file is called a module <br />

You can run a .js file i node using command ``` node <filnanme.js> ```

### Exporting for modules - using `exports` and `require` methods
- you can export fuctions, varibles etc from one file to another using `exports` method
- `export` for now just represent your module in form of object
- `require('<filelocation>')` is used to get get acces to that object
- For example in file `lib.js`
  ```
  exports.sum = (a, b) => {
   return a + b
  }
  ```
- And to acces this in `index.js` file we use
  ```
  const lib = require('./lib.js')
  ```
- Now to use the fuctions just use
  ```
  console.log(lib.sum(a + b))
  ```
