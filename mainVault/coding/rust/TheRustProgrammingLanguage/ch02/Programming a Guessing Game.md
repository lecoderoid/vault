## Processing a Guess
```rust
use std::io;

fn main() {
    println!("Guess the number!");

    println!("Please input your guess.");

    let mut guess = String::new();

    io::stdin()
        .read_line(&mut guess)
        .expect("Failed to read line");

    println!("You guessed: {guess}");
}
```

- bring *`io`* into scope
``` rust
use std::io;
```

- *`main`* function is the entry point of the program
```rust
fn main(){
```

---
## [[Storing Values with Variables]]
---

- *`String::new()`* - a function that returns a new instance of a *[[String]]*
-  the `::` syntax in `::new` line indicates the `new` is an associated function of the *String* type
- an *associated function* is a function that's implemented on a type

## Receiving User Input
- use *`stdin`* function from `io` module, which will allow us to handle user input
```rust
io::stdin().read_line(&mut guess);
```
- the `stdin` function returns an instance of `std::io::Stdin`, which is a type that represents a handle to the standard input for the terminal
- `read_line(&mut guess)` calls the `read_line` method on the standard input handle to get the input from the user
- the `&` indicates that this arg is a [[reference]], which gives you a way to let multiple parts of your code access one piece of data without needing to copy that data into memory multiple times

## Handling Potential Failure with Result
- `read_line` function returns a *Result* value
	- *Result* is an [[enumeration]] (enum), which is a type that can be in one of multiple possible states (we call them *variants*)
	- *Result*'s variants (states) are *ok* and *Err*
```rust
 .expect("Failed to read line");
```
- an instance of *Result* has an *expect* method

## Printing Values with *println!* Placeholders
```rust
    println!("You guessed: {guess}");
```
- `{}` - this set of curly brackets is a placeholder



