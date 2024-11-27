 > Stack and Heap Comparision for program memory storage
 > Addresses are stored in stacks, and these addresses take you to the heap with storage. 
 

- Stack memory is used for storing variables during function calls that are of fixed size. Fixed size variables take up limited space and are easier to access via a stack in a LIFO fashion. 
- Heap memory is more slower, managed by the Rust Compiler, accesses memory, checks size and allocates variables accordingly , while returning a pointer as a reference. This is used mostly to allocate dynamic variables where the size of the data is not pre-determined. 


Scope: 

Variables within a scope exist as long as they  operate within the scope, post which they're destroyed. 