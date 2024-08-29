- Rust is a *statically typed* language, which means that it must know the types of all vars at compile time
```rust 
let guess: u32 = "42".parse().expect("Not a number!");
```
- we'll get an error if we don't add `: u32` type annotation

# Scalar Types
- *Scalar* type represents a single value
	- [[integers]] ^345688
	- [[floating-point]]
	- [[booleans]]
	- [[characters]]

## Integer Types

- an *integer* is an number without a fractional component

**Int Types**

| **Length** | **Signed** | **Unsigned** |
| ---------- | ---------- | ------------ |
| 8-bit      | i8         | u8           |
| 16-bit     | i16        | u16          |
| 32-bit     | i32        | u32          |
| 64-bit     | i64        | u64          |
| 128-bit    | i128       | u128         |
| arch       | isize      | usize        |
- each signed variant can store numbers from -(2$^{2-1}$) to 2$^{n-1}$ - 1 inclusive where *n* is the number of bits that variant uses
- the `isize` and `usize` types depends on the architecture of the computer your program is running on
- int types default to `i32`

## Floating-Point Types
- *floating-point* numbers, are numbers with decimal points
- Rust floating-point types are `f32` and `f64` 
- the default type is `f64`
```rust
fn main(){
	let x = 2.0 //f64
	let y: f32 = 3.0 // f32
}
```


## Numeric Operations
- Rust supports the basic math operations: addition, subtraction, multiplication, division and remainder
- Integer division truncates toward zero to the nearest int
```rust
fn main() {
    let sum = 5 + 10;
    let diff = 95.5 - 4.3;
    let product = 4 * 30;
    let qoutient = 56.7 / 32.2;
    let truncated = 10 / 3;
    let remainder = 43 % 5;

    println!(
    "sum:{}, difference:{}, product:{}, qoutient:{}, truncated:{}, remainder:{}",
        sum, diff, product, qoutient, truncated, remainder
        );
}
```


## Boolean Type
- *Boolean* type has two possible values: `true` and `false`
- one byte in size
```rust
fn main(){
    let t = true; 
    let f: bool  = false; 
}
```
- main way to use *boolean* values is through conditionals

## Character Types
- *Char* literals are specified with single quotes
```rust 
fn main(){
   let c = 'z';
   let z: char = 'ℤ' // explicit type annotation
   let heart_eyed_cat = '😻';
}
```
- rust `char` type is four bytes in size and represents a Unicode Scalar Value