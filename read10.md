# Call Stack

A call stack is a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function, etc.

* When a script calls a function, the interpreter adds it to the call stack and then starts carrying out the function.

* Any functions that are called by that function are added to the call stack further up, and run where their calls are reached.

* When the current function is finished, the interpreter takes it off the stack and resumes execution where it left off in the last code listing.

* If the stack takes up more space than it had assigned to it, it results in a "stack overflow" error.

## How does the call stack handle function calls?

```
function firstFunction(){
  console.log("Hello from firstFunction");
}

function secondFunction(){
  firstFunction();
  console.log("The end from secondFunction");
}

secondFunction();
```

1. When `secondFunction()` gets executed, an empty stack frame is created. It is the main (anonymous) entry point of the program.
2. `secondFunction()` then calls `firstFunction()`which is pushed into the stack.
3. `firstFunction()` returns and prints “Hello from firstFunction” to the console.
4. `firstFunction()` is pop off the stack.
5. The execution order then move to `secondFunction()`.
6. `secondFunction()` returns and print “The end from secondFunction” to the console.
7. `secondFunction()` is pop off the stack, clearing the memory.


## Temporarily store:

When a function is invoked (called), the function, its parameters, and variables are pushed into the call stack to form a stack frame. This stack frame is a memory location in the stack. The memory is cleared when the function returns as it is pop out of the stack.

![](https://cdn-media-1.freecodecamp.org/images/QgR2uIk7tW0YNz0Xm8g0jAPeRFI0e4sCejsv)

## JavaScript error messages && debugging

![](https://miro.medium.com/max/2100/1*LHpmsxV3f2znpxhuAFuIqA.png)

### Reference errors

The ReferenceError object represents an error when a non-existent variable is referenced.

### Syntax errors

An exception caused by the incorrect use of a pre-defined syntax. Syntax errors are detected while compiling or parsing source code.

### Range errors

A RangeError is thrown when trying to pass a value as an argument to a function that does not allow a range that includes the value.

### Type errors


The TypeError object represents an error when an operation could not be performed, typically (but not exclusively) when a value is not of the expected type.


## Debugging

To debug your JS code, the easiest and maybe the most common way its to simply console.log() the variables you want to check or, by using chrome developer tools, open your page with your JS code (press cmd+o in macOS or Ctrl+o in Windows) and choose your file to debug, click the line you wanna debug and refresh your page again (F5).

If the line you selected was run you will be able to see what has happened before that point and you can try and evaluate the next lines to check if everything is outputting what you are expecting.

The breakpoint can also be achieved by putting a debugger statement in your code in the line you want to break.
