# Advanced Javascript
https://evercommerce.udemy.com/course/javascript-advanced/

### What is Strict Mode and what does it do?
`"use strict";`  
- makes debugging easier
- shows errors that would normally not show up
- this is written as a string
- can applied at the top of a function block
	```
	// Not strict mode.. 
	function newCode() {
		"use strict";
		// strict mode...
	}
	```
- wont let you delete variables, functions and args
- makes eval() safer to use. 


### Does JS pass variables as parimeters by reference or by value?
- Primitive types - strings, numbers and booleans are passed by value
- Objects are passed by reference
- What is pass by value?
- What is pass by reference? 
- What will the below code print out? 
``` 
"use strict";
var a = 1;
var b = {};
function foo(x, y) {
	x = 2;
	y.moo = 3;
}

foo(a, b);
console.log("a = " + a + "; b = " + JSON.stringify(b));
```
- Answer
	- a = 1; b = {'moo':3}
	- "a" is passed by value so updates to "a" in function foo will NOT be visible outside of the function foo. 

### What are rest operators?

### What is the spread operator?

### What are template strings? 

### What are template string tags?

