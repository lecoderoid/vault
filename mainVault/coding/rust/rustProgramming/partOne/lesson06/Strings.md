# Strings

- Rust has two kinds
	- String literals
		- text is allocated statically
		- text is immutable
	- Instances of the *String* type:
		- text is allocated on the heap
		- text is potentially mutable
		- text is deallocated at the end of the *String* object's lifetime

## Using String Literals

- you can use a string literal as follows:
``` rust
let s = "hello";
```

- Technically speaking, a string literal is a string slice with static lifetime
```rust
let s: &'static str = "hello";
```
 - A string slice knows the address of the first byte, and the number of bytes:
 ```rust
 println!("{} {:p}, {}", s, s.as_ptr(), s.len());
```