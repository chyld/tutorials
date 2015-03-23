# JavaScript Basics

### Required Tools
* Web Browser (Chrome, Firefox)
* Text Editor (Atom, Sublime)

### Getting Started
Create a directory somewhere on your computer. Probably on your deskop or in your documents. Call this folder `js-basics`. Now create two files inside the `js-basics` folder: `index.html` and `main.js`.

Open up both files in your text editor.

Let's start with the `index.html` file first. Here's the contents:
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>JS Basics</title>
  </head>
  <body>
    <h1>JS Basics</h1>
    <script src="main.js"></script>
  </body>
</html>
```

This is some basic HTML 5 boilerplate code. The most important line, for us, is where we load in our javascript file, `main.js`. When this HTML file gets loaded into the browser, it reads each line sequentially. Once it gets to the `<script src="main.js"></script>` line, it will stop reading the HTML and start reading/executing the code inside of `main.js`.

This is the file that we will be focusing on during this tutorial.

Let's add a simple `alert` to our `main.js` file. Open up `main.js` and add `alert('hello, world');` as the only line in the file. Save both files. Open up `index.html` in Chrome or Firefox. You can do this easily by just double-clicking on the `index.html` file.

You should see the JS Basics text on the screen and a popup with the content **hello, world** should of appeared. You are now ready to start the tutorial.

### Types and Variables
In JavaScript there are 5 primitive types and 1 object type, for a total of 6 types. The primitive types are:
- Number
- String
- Boolean
- Null
- Undefined

#### Number

Let's discuss the `Number` type first.

A number is either whole or fractional. We call these integers or floats (for floating point). Let's create some numbers using variables. The first time you use a variable you have to create it. You create a variable by using the `var` keyword. Like this.

`var x = 3;`

This created a variable called `x` that is assigned the value of 3. Think of a variable as a box and the number 3 is inside that box. Place a semicolon at the end of the assignment statement. This is optional, but is a good practice. 

Create 3 numbers and add them together into a sum. Display the sum.

```js
var a = 5;
var b = 8;
var c = 3;
var sum = a + b + c;
console.log(sum);
```

This creates the variables `a`, `b`, `c` with their corresponding values and then creates another variable, `sum`, which is the total of 5, 8 and 3. Open up your development tools by holding down `CMD` + `ALT` + `i`. Click on the tab labeled `console`. Now, refresh your browser: `CMD` + `r`. You should see in the console the number 16.

This works exactly the same using decimals or floats. Example.

```js
var x = 3.14;
var y = 2.26;
var sum = x + y;
console.log(sum) // => 5.4
```

Above, I used //. This is a single line comment in JavaScript. Anything after this is ignored by the compiler. I'm showing the output of the console.log statement.

#### String

The `String` type is next. A `String` is basically a string of letters, numbers, symbols that not to be used for numerical calculations. Strings can be created in either single or double quotes. Additionally, you can concatinate one string onto another by using the `+` operator.

```js
var first = 'Bob';
var last = "Jones";
var fullName = first + ' ' + last;
console.log('The fullName is', fullName); // => The fullName is Bob Jones
```

I first create `Bob` inside the `first` variable with single quotes. `Jones` is created using double quotes. Then fullName, which is camel cased, is the `first` concatinated with a space concatinated with `last`. Finally I log out to the console `The fullName is Bob Jones`.

#### Boolean

The `Boolean` type has a limited range. It can only be `true` or `false`. We use this type when we want to make a decision. Go left if something is true, else go right.

```js
var a = 3;
var b = 20;
var isAsmallerThanB = a < b;

if(isAsmallerThanB)
  console.log('A is smaller than B'); // => This one runs
else
  console.log('A is larger than B');
```

A lot is going on here.

I create two numbers, `a` and `b`. Then I create a variable `isAsmallerThanB` which is the result of the boolean expression `a < b`. This is asking a question, is `a` less than `b`. The result is either `true` or `false`. The next line is an `if` statement. If the expression in the `if` statement is true, then the first console.log gets executed. If it is false, then the statement below the `else` gets executed.

Here, because `a` is less than `b`, the console will display `A is smaller than B`.

#### Null

`null` means the variable has no value associated with it. If you said `var a = null;`, then you are creating the `a` variable, but are assigning it nothing.

```js
var a = null;

if(a)
  console.log('a is truthy');
else
  console.log('a is falsy'); // => This one runs
```

Here, `null` is considered a `false` value in JavaScript. So, the bottom condition runs.

#### Undefined

`undefined` means you are trying to access a variable that has not yet been defined, or assigned a value.

```js
var a; // a is undefined

if(a)
  console.log('a is truthy');
else
  console.log('a is falsy'); // => This one runs
```

Here, `undefined` is also considered `false`, just as `null`, `0`, `''` and `NaN`. This is zero, empty string and `Not a Number`.

### All Together

Time to put all this knowledge together to build a simple app. We will need a way to get user input. Do do this we'll use the `prompt` function. It will allow us to ask the user, or prompt them, for some information. We will use this information to make our program feel more alive.

```js
  var name = prompt('What is your name?');
  var age = prompt('What is your age?');
  age = parseInt(age);
  
  if(age < 21)
    console.log('You are too young to drink alcohol');
  else
    console.log('You are legally permitted to drink');
```

I first prompt the user for their name. The result goes into the variable `name`. I then ask for their age. But if you were to look into the `age` variable, you would see that it is a `String` type, like "33". `prompt` always gives you a string. We need to convert this string to a number. We do this with the `parseInt` function. It takes a string and will give you a number. So now `age` has been converted from a `String` type to a `Number` type. Next we have an `if` condition. If the person's age is less than 21 then we print out the first string to the console. If it is greater than or equal to 21, then we display the second string.

### Exploration

Take what you have learned and try and build a simple calculator. Ask the user for a first number, a second number and then what type of operation they would like to perform. Maybe they would enter `+` for addition or `*` for multiplication.

Display the results of the calculation to the user.
