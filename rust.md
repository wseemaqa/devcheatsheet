---
Title: Rust Cheat Sheet
Description: A Rust cheat sheet for Rustaceans
---

## Rust Cheat Sheet

### A simple hello world in Rust

```rs
fn main() {
    println!("Hello, world!"); // prints hello world to the console
}
```

### Rust Primitive Types

`bool` Boolean (true / false)

`char` character

`f32, f64` 32-bits, 64-bits floats

`i64, i32, i16, i8` signed 16-bits integers

`u64, u32, u16, u8` unsigned 16-bits integers

`isize` pointer-sized signed integers

`usize` pointer-sized unsigned integers

### Rust Operators

`e == f` e is equal to f

`e != f` e is NOT equal to f

`e < f` e is less than f

`e > f` e is greater f

`e <= f` e is less than or equal to f

`e >= f` e is greater or equal to f

`a + b` a is added to b

`a - b` b is subtracted from a

`a / b` a is divided by b

`a % b` gets the remainder of a by dividing with b

`a * b` a is multiplied with b

`&` AND

`|` OR

`^` XOR

`<<` LEFT

`>>` RIGHT

`&&` AND

`||` OR

`!` NOT

### Data Types

|Data Type|Description|
|:----:|:------:|
|struct S {}| Defines a struct(a type that is composed of other types) with the specified field |
|struct S {x: T}| Defines a struct with the name and Type specified|
|struct S(T)| Defines a tupled struct with numbered field and Type|
|struct S|Defines a zero sized unit struct, that occupies no space|
|enum E{}| Defines an enum|
|enum E { A, B(), C {} }|Defines different variants of an enum|
|enum E { A = 1 }| For variants that are only unit-like|
|enum E {}| Enum without variants, and can't be instantiated|
|static X:T = T()| A global variable with static lifetime, and single memory allocation|
|const X: T = T()| Defines a constant that is scoped into a temporary memory allocation|
|let x: T|Allocates Types as bytes on stack that is bound as x|
|let mut x: T| Allows for mutability of x|
|x = y| Transfers x into y|

### Rust Learning

Interested in learning Rust, check the Rust learning repository on [Github](https://github.com/ctjhoa/rust-learning).

### Cargo Commands

|Command|Description|
|:----:|:------:|
|cargo init|generates a new rust project with the latest rust version|
|cargo generate (github repo link)| Generates a new project template from a github repository|
|cargo check|checks if the project will compile much faster|
|cargo build| Builds your rust project|
|cargo test| Runs tests for your rust projects|
|cargo doc --open| generate documentation for your code and dependencies locally|
|cargo run| run rust project|
|cargo run --bin b| run binary b|
|cargo run -p w| run main of sub-workspace w|
|cargo ,,, --timing| shows what crates caused your build to take much longer|
|cargo tree| shows the dependency graph|
|cargo +[nightly, stable]| use the given toolchain for command|
|rustc -- -Zunpretty=expanded|show expanded macros|
|rustup doc|opens the offline documentation including the rust book|

### Algorithms and Data Structures in Rust

This [github](https://github.com/TheAlgorithms/Rust) repository contains several examples of data structures and algorithms in Rust.
