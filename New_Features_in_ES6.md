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

4. Destructuring Assignment in ES6
```javascript
var {house, mouse} = $('body').data() // we'll get house and mouse variables

var {json: jsonMiddleware} = require('body-parser')

var {username, password} = req.body
```

Arrow functions 
```javascript
$('.btn').click((event) =>{
  this.sendData()
})
```

Promises
```javascript
var wait1000 =  new Promise((resolve, reject)=> {
  setTimeout(resolve, 1000)
}).then(()=> {
  console.log('Yay!')
})
```