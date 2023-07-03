# Character Classes
- define a group of characters inside brackets `[ ]`
- example `/b[aiu]g/` matches bag, big and bug

Set a range
- you can set a range of characters
- example `[a-e]` matches all characters from a to e 
- You can also match numbers and letters for example `/[a-z0-9]/`

Match multiples
- `+`
- greedy
- match characters that appear one or more times in a row
- appears at least once
- must repeat one after another
- example `/a+/g`  would find one match in `abc` and return `[a]`
- example `/a+/g` would also find only one match in `aabc` and return `aa`
- How is `+` different from `g` flag? `+` matches consecutive characters where as `g` returns all matches so it wont stop after just the first match. 

Match Zero or more times
- `*`
- the asterisk or star is used to match zero or more times
- how is this used in a character set?