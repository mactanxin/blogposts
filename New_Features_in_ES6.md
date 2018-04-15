# New Features in ES6
Default Parameters
```javascript
var link = function (height, color, url) {
    var height = height || 50
    var color = color || 'red'
    var url = url || 'http://azat.co'
    ...
}

var link = function(height = 50, color = 'red', url = 'http://azat.co') {}
```

in ES6 we can use a new syntax ${NAME} inside of the back-ticked string:
```javascript
var name = `Your name is ${first} ${last}.`
var url = `http://localhost:3000/api/messages/${id}`
```

Multi-lines Strings with backticks:
```javascript
var roadPoem = `Then took the other, as just as fair,
    And having perhaps the better claim
    Because it was grassy and wanted wear,
    Though as for that the passing there
    Had worn them really about the same,`
```

## Destructuring Assignment in ES6
```javascript
var {house, mouse} = $('body').data() // we'll get house and mouse variables

var {json: jsonMiddleware} = require('body-parser')

var {username, password} = req.body
```

## Arrow functions 
```javascript
$('.btn').click((event) =>{
  this.sendData()
})
```

## Promises
```javascript
var wait1000 =  new Promise((resolve, reject)=> {
  setTimeout(resolve, 1000)
}).then(()=> {
  console.log('Yay!')
})
```

## Block-Scoped Constructs Let and Const
 In ES6, we use let to restrict the scope to the blocks. Vars are function scoped.
```javascript
function calculateTotalAmount (vip) {
  var amount = 0 // probably should also be let, but you can mix var and let
  if (vip) {
    let amount = 1 // first amount is still 0
  } 
  { // more crazy blocks!
    let amount = 100 // first amount is still 0
    {
      let amount = 1000 // first amount is still 0
      }
  }  
  return amount
}

console.log(calculateTotalAmount(true))
```
The value is 0, because the if block also has let. If it had nothing (amount=1), then the expression would have been 1.

## Classes in ES6
 It makes writing classes and inheriting from them as easy as liking a comment on Facebook.
```javascript
class baseModel {
  constructor(options = {}, data = []) { // class constructor
    this.name = 'Base'
    this.url = 'http://azat.co/api'
    this.data = data
    this.options = options
  }

    getName() { // class method
      console.log(`Class name: ${this.name}`)
    }
}
```
The AccountModel inherits from baseModel with class NAME extends PARENT_NAME:
```javascript
class AccountModel extends baseModel {
  constructor(options, data) {
  }
}
```
To call the parent constructor, effortlessly invoke super() with params:
```javascript
    super({private: true}, ['32113123123', '524214691']) //call the parent method with super
     this.name = 'Account Model'
     this.url +='/accounts/'
   }
```

Modules in ES6
```javascript
module.exports = {
  port: 3000,
  getAccounts: function() {
    ...
  }
}
```
How to Use ES6 Today (Babel)
ES6 is finalized, but not fully supported by all browsers (e.g., ES6 Firefox support). To use ES6 today, get a compiler like [Babel · The compiler for writing next generation JavaScript](https://babeljs.io/). 