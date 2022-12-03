# Variables
Talking aboud programming languages, variables are the names given to memory locations that stores data in them. Those data usually change according to the program flow and needs. The deffinition holds same in the Rust programming language as well. In rust *let* keyword is used to declare a variable which is done as in below example:

```rust
fn main(){
    let variable = 320; // This is the variable decleration in rust.
    println!("The value of variable is {variable}"); //This prints the value of variable in console.
}
```

# Mutability of variables
Variables in Rust are by default immutable, despite their definitions states they can change. Immutable means that once assigned the values cannot be changed again through out the program's executuion.
```rust
fn main(){
        let variable = 320; // This variable's value cannot be changed again.
        println!("The value of variable is {variable}"); //This prints the value of variable in console.
        variable = 32;
        // This gives an error as "cannot assign twice to immutable variable"
    }
```
However, it is possible to make a variable mutable. This is done by using *mut* keyword. This will allow variable to be changed again and again. Following is the syntax.
```rust
fn main(){
        let mut variable = 320; // This variable's value can be changed again.
        println!("The value of variable is {variable}"); //This prints the value of variable in console.
        variable = 32;
        // This won't give an error as before.
    }
```
# Constants
Immutable variables acts like a constant variable, however there are many differences and some of them are listed below:
1. *mut* cannot be used with constant variables during decleration.
2. *const* keyword is used to declare a constant.
3. It is mandatory to use specify the data type of the constants.
4. Constants' value cannot be set to an expresstion that is computed at runtime.
5. Constant variable's names are always all upper case with words seperated by underscore.
```rust
const CONSTANT_VARIABLE: u32 = 300; // constant of a unsigned 32 bit data type.
```


# Variable shadowing
In rust there exist the concept of variable shadowing, where varibles with same name can be declared twice. Then the compiler will recognige the variable as the second variable whenever the variable is used after that. The shadowing is done by redeclaring a variable using *let* keyword.
