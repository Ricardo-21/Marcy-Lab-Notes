# Variables (Bindings)

| keyword | name | value |

_Declaration_ : When a program sets aside memory or 'space' for that variable.
Variables are declared with a keyword and name.

_Initialization_ : The starting (initial) value of a variable.

_Assignment and Reassignment_ : Explicitly giving a value or new value to variable.

_(side-note : you cannot redeclare let vars but you can reassign)_

_Scope_ : You are able to create a new variable with the same name, and have it 
not effect the variable outside of the block (curly brackets).

___

# Functions 

DRY - Don't Repeat Yourself _(a principle)_

_Function_- You take some materials (input), do some proccess on it, and then you
get something out of it. 

#### Declaring Functions

*Keyword- `function`
*name 
*parameter list- `()`
*function body- `{}`

It would look something like this 

```javascript
function AnyName (possible-parameter) {

}
```

Refrencing a function is different than invoking a function. A simple way to 
remember this is when invoking, you are using the function and when you reference
you are just 'looking' at it.

_control-flow_ is different as well, whenever you call(_invoke_) a function 
you are 'going back' to where the function is declared in order to run the body
of the function.

#### Parts of a function

* Inputs <- this would be the parameter/argument that goes into the function
* What the function does <- this is the body of the function what's going on in
the `{}`
* The output, aka 'return' value <- finally what is the output, what is it that
the function returns to you?

#### Function declaration vs Function expression

Mostly comes down to personal prefrence, 

Function declaration has something called _hoisting_ it wouldn't matter where it
is invoked in the code. Function expression does not get _hoisted_.

___

# Scope

#### What is Scope? 

* Determines the accessibility of variable 
* Where a variable is born, lives and dies

#### Lexical Scoping 

* Every inner level can access its outer levels.

___

# Best Practices 

#### White spacing is your friend 

* Use tabs to indent each block of code 
* Use spaces to improve readibility 

#### Naming Conventions
* snake_case
* camelCase
* CAPSLOCK

#### Mark Down 

* Use `` to create an inline code snippet
* Use ``` to create a block cose snippet 
* Preview in AWS and in Github

### Reading Error Messages

* In coding, it's called "throwing an error" 
[img](https://thumbs.dreamstime.com/b/hot-potato-20892390.jpg)
* Interpretting errors - Read the error message and AND the line number

#### Reference Error

*Creates an instance representing an error that occurs when de-referencing an 
invalid reference 
*Scoping problems

#### Syntax Error
* Creates an instance representing a syntax error
* Structural Problems
* Redeclaring something you can't redeclare

#### Type Error
* Creates an instance representing an error that occurs when a variable or 
parameter is not a valid type.
* Invoking something that is not a function 
* Reassigning something you can't reassign 

#### Debugging with console.logs

* Why is it called a bug? 
* Reading error message AND the line it's on! 
* What if there is no error message (silent failure)
** Check your assumptions

