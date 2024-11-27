
Rust doesn't have exceptions - all possible error states are encoded in the return types of functions. 


`read_to_string` function doesn't return a string, but a `Result` object that either returns a string or an error of some type `std::io::Error` 

Since Result is an enum, you can use match to determine which it is. 

```
let result = std::fs::read_to_string("test.txt");
match result {
Ok(content) => {println!("File Content: {}", content)}
Err(error) => {println!("Oh noes: {}",error)}
}
```

