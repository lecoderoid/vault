# Flow Control

## If-Test
- if-tests in rust are similar to most other languages:
```rust
let age = 58;
if age > 50 {
	println!("You are old");
}
```
- Note the ff points:
	- Test expression must be *bool*
	- No need for parentheses around test
	- Blocks must always be enclosed in {}

## If-Else-Test
- You can write an if-else test as follows:
```rust
let height = 1.68;

if height > 1.8{
	println!("You are tall");
} else {
	println!("You are not so tall");
}
```

## If-Else-If Test
- You can write an if-else-if as follows:
```rust
let swans_games = 500;

if swans_games > 300{
	println!("You are a loyal fan");
} else  if swans_games > 100 {
	println!("You are a discerning fan");
} else {
	println!("You are quite a new fan");
}
```

---
### Writing an If-Else Expression
- You can use if-else as an expression:
```rust
let msg = if age > 50 {"old"} else {"young"};

println!("You are {}", msg);
```
- This is similar to  *?:* in other languages