# Lazy Matching
- greedy vs lazy
- a greedy match finds the longest possible part of a string to match
- a lazy match finds the smallest possible part of a string to match

Example of Greedy - `/t[a-z]*i/` to the string `titanic` returns `titani` because the expression is looking for pattern that starts with `t` and ends with `i` with some letters in between 

- `?` for lazy match
- How do you know where this goes? - It acts on the previous token. 
- Whats a token? 