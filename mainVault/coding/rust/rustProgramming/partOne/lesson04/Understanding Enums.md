# Enums
- an enum is a type with a closed set of values
	- example, a *Flight* enum might allow **Economy**, **Business**, **First**
	
- enums are very important and are used widely in Rust
	- both in the Rust lib, and in the code we write ourselves

---
## Defining an Enum Type:
- specify the enum type, starting with capital
- specify allowed values ([[variants]]), also starting with capitals

```rust
enum Color{
	Red,
	Gree,
	Blue
}
```

- to use an enum type:
	- use the enum type, followed by ::, followed by a variant
	- you often use *match* ([[Flow Control#^dc7c24]]) to test variant values
```rust
let c: Color = Color::Red;
match c {
	Color::Red => println!("coch"),
	Color::Green => println!("gwyrdd"),
	Color::Blue => println!("glas"),
}
```

---
## Defining Enums in a Separate File
- it's common to define enums in a separate file:

```rust
pub enum Color{ // make it public so it can be used in other files
	Red, Green, Blue
}

// mytype.rs
```

- you load the module into *main.rs*, and introduce symbols into scope:
```rust
// load the module
mod mytypes;

// introduce the Color type into the scope
use mytypes::Color;
```
