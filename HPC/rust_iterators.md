
## Iterators 

Ranges like 0..10 are iterators on which next() like functions can be called repeatedly, and on which gives us a sequence of values. 

```
fn main(){
    
    let mut range = 0..10;
    
    loop{
        match range.next() {
            Some(x) => {
                println!("{}", x);
            }
            None => { break }
        }
    }
}
```

`for` loops aren't the only thing that use iterators, however,. Writing your own iterator involves implementing the `Iterator` trait. 

Rust provides a number of useful itertors to accomplish various tasks. But first, a few notes about limitations of ranges. 

Iterator usage allows us to skip bound checks an uncecessary indexing when it comes to looping over composite constructs like vectors. We can simply use the iterative construct's reference in our loop to loop over the elements directly, rather than having bound checks over defined ranges tied to the length of the vector. 

Iterators are fun, but not without accomplices that allow us to use and change sequence based values,and Rust provides very nifty ways to do the same: 

### Iterators, Iterator adoptors, and Consumers

- <i>Iterators</i> give you sequence values
- <i>Iterator adoptors</i> operate on an iterator, producing a new iterator witha d different output sequence
- <i>Consumers</i> operate on an iterator, producing some final set of values. 

A consumer operates on an iteratore, and returns a value or a set of values. The most common one is `collect()` 

```
// This won't compile. Rust needs type specification
let hundred_range = (1..100).collect();

// This will compile, since type definition has been given. 
let hundred_range = (1..100).collect()::<Vec<i32>>();

or 

let hundred_range = (1..100).collect()::<Vec<_>>();
//where '_' is an infered type placeholder. 
```


besides `collect()` now there exists also a `find()`  iterator, that looks for something in a vector and returns an `Option()` , based on whether that value exists  in the iterator or not. 




