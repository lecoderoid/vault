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

## Integers

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