                                                                                                                                                1. Difference between var, let, and const

var:

Function scoped (or global if declared outside function).

Can redeclare and update.

Hoisted with value undefined.

var a = 10;
var a = 20; //  works


let:

Block scoped.

Can update but cannot redeclare in the same scope.

Hoisted but not initialized (TDZ issue).

let b = 10;
b = 20;   //  works
let b = 30; //  error


const:

Block scoped.

Cannot be updated or redeclared.

Must initialize at declaration.

const c = 100;
c = 200;  error

2. Difference between forEach(), map(), and filter()

forEach():

Loops through each element.

Only performs action, no new array returned.

[1,2,3].forEach(n => console.log(n*2));


map():

Creates a new array.

Transforms each element.

const doubled = [1,2,3].map(n => n*2);
console.log(doubled); // [2,4,6]


filter():

Returns a new array.

Keeps only items that match a condition.

const even = [1,2,3,4].filter(n => n%2===0);
console.log(even); // [2,4]

3. Arrow Functions:

Shorter way to write functions.

Do not have their own this, they use parent scope’s this.

Cleaner syntax.

// Normal
function add(a, b) {
  return a+b;
}

// Arrow
const addArrow = (a, b) => a+b;

4. Destructuring Assignment

Lets you take values from arrays/objects directly into variables.

Array example:

const arr = [10, 20, 30];
const [x, y] = arr;
console.log(x, y); // 10 20


Object example:

const person = { name: "Rahim", age: 25 };
const { name, age } = person;
console.log(name, age); // Rahim 25

5. Template Literals

Use backticks `

Supports interpolation ${} and multi-line strings.

const name = "Rahim";
const age = 25;

// Old way
console.log("My name is " + name + " and I am " + age + " years old.");

// Template literal
console.log(`My name is ${name} and I am ${age} years old.`);


Difference:

Concatenation with + is messy.

Template literals are easier, cleaner, and allow multi-line.                                                           