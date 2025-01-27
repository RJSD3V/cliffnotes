### How Rust Fixes C’s Undefined Behavior 

As fundamental as C is as a language to the functioning of most systems out there, it does have several problems below the surface, which when looked into seem to have catastrophic consequences….

I recently took an interest in understanding systems more deeply. I have spent the last 8–10 months doing a massive pivot into AI , specifically GenAI , which I can confidently say I am confident that I know nothing about it. Its a growing field and since the internet is a thing, everyone seems to be better at it than me. I digress….

I focussed on building systems that support AI applications and training, rather than simply run those applications and look at cool outputs LLM’s are capable of generating. I was fortunate enough to peek under the hood. Which got me (as a former data engineer) interested heavily in developing applications, if possible from scratch, on baremetal linux machines. Which is where C comes in. 

I picked up a very popular book with a very peculiar title. “Learn C the hard way by Zed Shaw”. This book stood out to me because I felt I did have to learn C the hard way, since that’s how I had learned most things in life ( I wasn’t a very bright student). 

The first few passages of the book I read, said that C , being the perfect language it is, had inconsistencies in its definition. At its core, based on the standard ANSI C specifications, it had certain places where its behavior as a language was **undefined**.

####   

#### The Undefined Behavior of C

Lets’ get a breakdown of how C behaves , but before that, we need to understand what undefined behavior is, in the context of a programming language: 

Most languages, especially languages that were written to write embedded software, are proposed to have one quality — to be deterministic in behavior. If I print x, I should see x in the console, or wherever I chose. But certain aspects of a language, especially when it comes to defining and moving variables, (which is about 90% of what a piece of code does) there are certain aspects of C code that are not clearly deterministic in nature. So basically, 

> A piece of code could do something different than what it was intended to do — depending on how ambiguously the compiler reads it. 

  

  

1. Uninitialized Variables: 
2. Integer Overflow
3. Null Pointer Dereferencing
4. Array Index Out of Bounds
5. Modifying Objects between Sequence Points: