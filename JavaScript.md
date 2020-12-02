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
___

#### Ternary operators

``` javascript
  function stringy(a) {
  // Write your code here
  let str = '';
  for (let i = 1; i <= a; i++){
    !(i % 2)  ? str += `0` : str += `1`;
  }
  return str;
}```

* ternary operators, like if statements, can use truthy values to check a condition. In this case `i%2` will 
have a value of either 0 or any remainder. As we know 0 has a boolean value of falsy and any other number has a 
value of truthy 

___

# Arrays 

#### What are arrays and why are they useful?

* Arrays are lists/ data structures, that may be used to hold a series of
information

#### What is a *data structure*? 

* A thing that holds a series of information

### Pass by value 

* Primitive data types: pass by value 

``` javascript 
let original = 10;

function double(num) {
	num = num * 2;
	return num;
}

let copy = double(original);
console.log("copy is", copy)
console.log("original is", original);
```
### Pass by reference

* Non-primitive data types: pass by refernce

``` javascript 
let ogArray = [10];

function doubleArray(arr) {
	arr[0] = arr[0] * 2;
	return arr;
}

let copyArr = doubleArray(ogArray);
console.log(copyArr);
console.log(ogArray);
``` 
### Important Array Tools

* What happens when you invoke a function with extra arguments?

** Well what happens is that it ignores any extra argument beyond the amount 
of arguments it accepts.

* What is the purpose of rest parameters?

** What rest parameters does is it allows the arguments to be passed as an array
given that there is given extra arguments. `function (a,b, ...manyMoreArgs){`

*Destructure a javascript array. It breaks down the array, similar to arguments in
a function 

``` javascript
const x = [1, 2, 3, 4, 5];
const [y, z] = x;

console.log(y); // 1
console.log(z); // 2
```

* What is the purpose of the spread operator? `...`
In a sense it allows arrays/ objects to be passed through. Instead to be treated
as arguments instead of an array. 

``` javascript
function myFunction(v, w, x, y, z) { }
let args = [0, 1];
myFunction(-1, ...args, 2, ...[3]);
```

___

# Objects 

### What is an object and why are they useful?

* Another *data structure* !
* How are they different from arrays? 
** They organize properties, in a sense they collect and organize data in a way
that arrays cannot.
** EX : 
```
["Ann", 28, true] // "lists"
{age: 28, teacher: true, name: "Ann"} //organize, property, we can move around the
properties of the object.

```

### Syntax to create an object

To create an object it would like: 

``` javascript 
let person = {
	"crewmate": true,
	"color": "red",
	"imposter": false
};
```

### Parts of an object 
* key -> must be a string (or symbol...)
* value -> can be anything
** it can even be another object
* property

### Getting values from an Object - Dot notation
* `obj.key` -> key is a STRING
* `obj[key]` -> key is a VARIABLE or EXPRESSION
* EX:

``` javascript 
person.crewmate;
/// this is expected to return true

person["color"]
/// Expected return is red
``` 

### Iterating through objects 

* How to get all the keys of an Object as an Array
	* Object.keys(obj)

EX:

``` javascript 
keyNames = Object.keys(person);
///expected return ["crewamte","color","imposter"]

for(let i = 0; i < keyNames.length; i++) {
	let key = keyName[i];
	console.log(key);
	console.log(person[key]);
}

/// Now the for loop's expected to log the values of the properties.
``` 

* `for...in` loops
	* A more eloquent way to iterate over all Object keys

EX:

``` javascript 
for (let key in person) {
	console.log(`the key is: ${key} and the value is: ${person[key]}`)
}
/// Expected to log both key and value

___ 

#UNIT-4 OBJECT-ORIENTED PROGRAMMING 

### Encapsulation and Objects

* Absraction 
- take away (hide) the implementation details 
- not to be concerned under the hood
- private vs public data 
- JS has public data only

* Encapsulation 
- package together (state) data properties and (behavior) methods

- Inheritence 
-Polymorphism

___

# `this` in the Global scope 

- Execution Context (Running Environment)
- global object / globalThis

# The Global Object

-global variables declared with let or const are NOT added to the global obj

- And how does it relate to global variables?
- Global variables are properties that are starred on the global object

# `this` in a function/method

- function invocation 
	* is the global object
- method invocation 
	* is the object that called the method

# What is Execution Context?

- Mental model 
- Let's review scope
- When and how is the binding of `this` determined?