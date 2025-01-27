
## Memory Management in Rust

Stack and heap are two essential concepts in Rust land. When variables are created, they are stored in either a stack or a heap like manner, depending on their structure. 

### Stack
Stack memory is fast, during the compilation and execution of a program, rust variables are stored onto a stack, be it numbers, (integers and floats), as this type of memory is faster, more local to the function call. But , having all these advantages, it is limited in size. 

## The Stack Frame
Whenever a function is called, a certain amount of memory is allocated for all the variables declared within that function. this allocation is called a stack frame (like a call stack, but for variables). As variables of primitive types like ints are declared, these are pushed on to the stack, and as the function body goes out of scope, they are deallocated , or popped from the stack frame. This happens automatically. 

Memory inside a computer is kind of like a giant array with indexes starting from 0 and going on to **x** gb. 10^9 or 2^ 30. Stack frame allocation is fast, since it is known beforehand how much memory would be needed, and so is deallocation. the only problem is the persistence of this memory allocation. 

It works like a stack of plates, as functions are nested, the outer function variables get first priority to be allocated onto the stack memory, with lower address numbers (let's assume 0), the more nested a function is within the main function, the later it will be pushed onto the stack, since it is called later in code as well. And as these functions finishe executing, and the variables go out of scope, they are **popped of** or deallocated from memory. 

## Heap
Heap memory on the other hand, is slower, and is explicitly allocated by the program based on the requirement of the data type that is being stored. But, It is unlimited in size, and is globally accessible. 

Heap memory allocation is less structured ergo slower, but it allows variables to have persistence across functions, where `Box<T>` is used. An `int32` number declared with `Box<T>` is then declared as a raw pointer on the stack memory, which points to where the number is actually stored. This could be anywhere in the memory, since heaps dont' follow a conventional allocation like a stack does. Due to this, heap allocation is slower, flexible and can accomodate variable values of any size. Another downside of this is that heap allocation is done inconsistently, which can leave **gaps** or "holes" in memory. This also depends on the strategy used by each programming language, for heap allocation. Rust uses **jemalloc** for this purpose. 

The `Box<T>` implementation also calls for the `Drop` method that deallocates the memory from heap once the function call is over and the reference is popped of the stack frame (In some cases). 

## Runtime Efficiency

Memory management on stacks are trivial. The machine increments and decrements a single stack pointer. The same is not true for heap, since memory is allocated and deallocated from arbitrary points in memory, and each point can have a memory block of an arbitrary size. 





