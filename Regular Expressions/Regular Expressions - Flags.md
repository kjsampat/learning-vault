# Flags
## Ignore Case Flag
- `i`
- example `/ignorecase/i` - this regex would match the following
	- ignoreCase
	- IgnoreCase
	- iGNorecaSe
- add the flag after the closing / to ignore cases. 

## All Matches Flag
- `g`
- this flag matches more that just the first match. It matches multiples.

Example

```
let testStr = "Repeat Repeat Repeat";
let ourRegex = /Repeat/;
testStr.match(ourRegex);

// return ["Repeat"] since there is no g flag

let ourRegex = /Repeat/g;

// return ["Repeat", "Repeat", "Repeat"] since the g flag is added
```

- you can have mulitple flags on a regex like this... `/search/gi`