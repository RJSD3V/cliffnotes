
 > Command Line arguments
```
fn main(){
  let pattern = std::env::args().nth(1).expect("No pattern given");
  let path = std::env::args().nth(2).expect("no path given");

  println!("pattern: {:?}, path: {:?}", pattern, path);
}
```