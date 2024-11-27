Learning rust by attempting to build a CLI app. 
following [this](https://rust-cli.github.io/book/tutorial/cli-args.html) tutorial:
[Build Your Own OS in Rust](https://osblog.stephenmarz.com/)
[Build your Own Text editor in Rust](https://www.flenker.blog/hecto/)


[[Rust Ownership Concepts]]

**Quick Notes**

Rust Installation: 

1. `cargo new <project-name>` followed by `cargo run` to run the project. 
2. to get arguments as command line arguments, you do the following
	- declare variable as `let pattern = std::env::args().nth(1).expect("No pattern given")`
	- then run the project: `cargo run -- cli-arg-1 cli-arg-2`
	- `std::env::args()` is a standard library function that gives you an **iterator** of the given arguments. 
	- The first entry 0 is the name of the program the ones that follow are the ones that are presumed to be entered by the user. 
3. CLI arguments as a Data Type
	 - It is common to look at programs in such a way that they are designed around the data they handle-
		```
		struct Cli {
		 pattern: String,
		 path: std::path::PathBuf,
		}
		```

      `<crate>::<module>::<function>`
      

	We started using the `clap` library for rust to parse command line arguments, by replacing the variable declaration with the following line: 
		`let args = Cli::parse();`
	This takes over the responsibility of looking for command line arguments, and pasting relevant messages if they don't exist when the cargo run function is called. 


```
#[derive(Parser)]
```
The Derive method makes sure you derive several functions and implementations and apply them to a specific struct or set of structs. methods from parser are implemented for the `Cli` struct. 

Note: Traits are a set of methods and items that can be implemented as an interface by structs.
example: An `Animal` trait can be implemented by a `Dog` Struct or a `Cat` Struct



## Error Reporting

Unlike other languages, objects don't throw errors, but are encoded in the return types of functions. the read_to_string function either returns a result object or an error. 