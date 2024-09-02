# If Expressions
- allows you to branch your code depending on conditions
```rust
fn main(){
   let number = 3;

   if number < 5 {
	  println!("condition was true"); 
   } else {
	  println!("condition was false"); 
   }
}
```
- the condition must be a `bool`

## Handlinng Multiple Conditions with `else if`

```rust
fn main(){
	let number = 6;
	if number % 4 == 0 {
		println!("number is divisible by 4");
	} else if number % 3 == 0 {
		println!("number is divisible by 3");
	} else if number % 2 == 0 {
		println!("number is divisible by 2");
	} else {
		println!("number is not divisible by 2, 3 or 4");
	}
}
```
- the program has four possible paths it can take

## Using `if` in a `let` Statement
- because `if` is an expression, we can use it on the right side of a `let` statement to assign the outcome to a variable
```rust
fn main(){
	let condition = true;
	let number = if condition { 5 } else { 6 };
	println!("The value of number is: {number}");
}
```
- results of both the `if` arm and the `else` arm must be of the same type
- we'll get an error if they are mismatched
- Rust needs to know at compile time what type the var `number` is


---

# Repetition with Loops
