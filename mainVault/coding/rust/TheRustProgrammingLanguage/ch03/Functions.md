- *Function* is a reusable block of code that performs a specific task
```rust
fn main(){
   println!("Hello, world");
   another_function();
}

fn another_function(){
   println!("Another function");
}
```

# Parameters
- *Parameters* are special variables that are part of a function's signature
```rust 
fn main(){
   another_function(5);
}

fn another_function(x: i32){
   println!("The value of x is : {x}");
}
```