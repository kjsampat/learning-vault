# Quantity specifier 
- You can specify an upper and lower number a quantity specifier 
- The `+` plus sign can used be used to find 1 or more characters
- The `*` asterisk sign can be used to find 0 or more characters

Range
- You can search for a specified number of characters by using the `{}` curly brackets
- example `{3, 5}` looks for a minimum of 3 characters and a max of 5 characters
- `/a{3,5}h/` would match the letter a between 3 and 5 times and the letter h. 

Lower number only
- You can match only a minimum number of characters by leaving off the max
- example `{3,}` - would match a minimum of 3 characters with no max.

Specific number only
- You can match a specific number of characters by including just the number in the curly braces without the comma
- example {3} - matches for only 3 characters