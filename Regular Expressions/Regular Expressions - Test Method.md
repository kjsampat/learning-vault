# Test Method
- No need to use quote marks
- `.test()`
- takes the regex (what you want to match) and applies it to the string
- returns a `true` or `false`
- does not extract matching strings unlike the .match() method [[Regular Expressions - Match Method]]

```
let testStr = 'freeCodeCamp';
let testRegex = /Code/;
testRegex.test(testStr);

// returns true 
```

What this is saying...  
Test the string `Code` to see if its inside the string `freeCodeCamp` 
or 
Does the string `Code` exists inside the string `freeCodeCamp`?
or 
Can you find `Code` inside `freeCodeCamp`

Thoughts...
This feels backwards to me. I don't like using the `.test()` method on the regular expression


