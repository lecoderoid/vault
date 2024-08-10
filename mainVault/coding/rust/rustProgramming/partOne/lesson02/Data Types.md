# Data types
## Signed Integer Types
- Rust has several signed int types of knows size:
	- i8
	- i16
	- i32
	- i64
	- i128

---

### Platform-Specific Int Types
- Rust has platform-specific int types:
	- isize
	- usize
- These types are optimized for the natural word size of your platform
	- for max efficiency
---

## Floating-Point Types
- Rust has two floating-points types:
	-  f32 - use f;64 generally, for max precision
	-  f64 - only use f32 if you need to save space
- you can specify the number of decimal places:
``` rust
	let f1: f32 = 1.23456;
	println!("Float to 2dp {:.2}", f1);
```
- you can specify a field width:
``` rust
	println("L-aligned {:<10.2}", f1);
	println("R-aligned {:>10.2}", f1);
```
- you can specify a fill character:
``` rust
	println("L-aligned with tilde {:~<10.2}", f1);
	println("L-aligned with tilde {:~>10.2}", f1);
```
### Using Scientific Notation
- you can use scientific notation for float values:
``` rust
let f3: f32 = -1.60217663e-16;
let f4: f64 = -2.99792458e8;
```
- you can display floats using scientific notation:
``` rust
pritnln!("\nElectron charge {:e}", f3);
```
