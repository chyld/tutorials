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

Let's discuss the `Number` type first.

A number is either whole or fractional. We call these integers or floats (for floating point). Let's create some numbers using variables. The first time you use a variable you have to create it. You create a variable by using the `var` keyword. Like this.

`var x = 3`

This created a variable called `x` that is assigned the value of 3. Think of a variable as a box and the number 3 is inside that box.
