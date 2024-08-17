- An array is a fixed-size homogeneous collection collection
	- you can create an array using literal syntax \[a,b,c\]
	
- Declare the array as *mut* if you want to change its values
	- note, you can not change it's size

```rust
let a1 = [100, 101, 102] //fixed values
let mut a2 = [100, 101, 102] //mutable values
```

## Using an Array

- To access an element in an array
```rust
arr[index]
```

- Rust does bounds-checking at compile time and run time
	- the index must be 0 at length-1

- to get the length of an array:
```rust
arr.len()
```

- to iterate elements in an array:
```rust
for elem in arr { ... }
```