# == vs === in JavaScript
Using `==` for equality
Using `===` for Identity
The identity (`===`) operator behaves identically to the equality (`==`) operator except no type conversion is done, and the types must be the same to be considered equal.
```javascript
"abc" == new String("abc")    // true
"abc" === new String("abc")   // false

'' == '0'           // false
0 == ''             // true
0 == '0'            // true

false == 'false'    // false, string type
false == '0'        // true

false == undefined  // false
false == null       // false
null == undefined   // true

' \t\r\n ' == 0     // true
```