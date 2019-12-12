# Lesson 1

## Introduction

Programming is the act of writing instructions for a computer to follow.

Computers only speak `binary`, in `0`s and `1`s. In order to communicate with them we use programming languages which are eventually translated into
binary.

In web browsers, `JavaScript` is the programming language we use. A program inside the browser called a JavaScript engine translates the code and delivers it to the computer to execute.

Everything dynamic on a web page, from news feeds to like buttons and games is created with JavaScript.

We are not going to go into too much theory, let's rather get coding.

## Writing JavaScript

In JavaScript, instructions for the computer are called `statements`.

### Using the development console

We recommend using [Chrome](https://www.google.com/chrome/) as your web browser when developing for the web, and the instructions and screenshots will be from that browser.

We can use a browser's `console` to write and run JavaScript without needing any other program.

To open the console, do one of the following:

- right-click anywhere on a web page and select `Inspect` from the menu
- 

We will be writing our JavaScript in files, but paying attention to the console in your browser is important as this is where errors in your code will appear.

### Using script tags in an HTML page

We recommed using [Visual Studio Code (VSCode)](https://code.visualstudio.com/) as your editor.

Create a new folder called `beginning-js` where you keep your code and open it in VSCode.

Create a new file called `index.html` by right-clicking in the left pane and selecting `New File` or by using the `File` menu.

Type `html:5` inside the new file and press `Tab` on your keyboard.

<img src="/images/html5.png" alt="html:5" width="600" height="177" />

This is a quick way to scaffold a new HTML file. You can read more about these kind of shortcuts [here](https://code.visualstudio.com/docs/editor/emmet).


### Adding a JavaScript file to an HTML page

Instead of typing directly into the developer tools console, we can use the `console.log` function. Using this function we can programmatically do what we manually did above, i.e. log (or print) the values to the console. To log the variables we entered above, we pass them in to the log function:

```js
console.log("hello");
console.log(10 + 5);
```

### Connecting and arranging your code



Before the closing `</body>` tag, add a `<script>` tag with a `src` attribute whose value is the path to a JavaScript file that we will create next:

```html
    <script src="js/script.js"></script>
    </body>
</html>
```

The `root` of your project is the parent folder for all your files. Until you start using for advanced tools, only `.html` files should be in the root. Keep other types of files in folders dedicatd to them:

Keep your js files in a folder called `js`. Create a file called `script.js` in that folder.

<img src="/images/file-arrangement.png" alt="File arrangement" width="600" height="198" />

### A note on semi-colons


### Setting up Visual Studio Code (VSCode) as your editor

VSCode comes with built-in formatting. Right-click anywhere inside a file and select `Format Document`.

## Statements

## Comments

Comments are statements in our code that are not run by the JavaScript engine, but are used to provide information to ourselves and other developers.

Comments can be single-line comments using double forward slashes `//`:

```js
// this is a single-line comment
```

They can also be multi-line comments use a single forward slash `/` and an asterisk `*`:

```js
/*
this is a multi-line comment
notice that the / and * are inverted when the comment is closed
*/
```

Single-line comments are often combined together:

```js
// this is a single-line comment
// with another single-line comment
```

## Values

## Variables

Variables are how a programming language stores information in a computer's memory. We can think of them as containers for data and once stored there, we can act on and use this data in other parts of our program.

<img src="/images/variable-containers.png" alt="variable containers" width="379" height="110" />

In JavaScript, variables don't have types, but the data the variables hold do.

We are going to look at these three types of data:

-   `string`
-   `number`
-   `boolean`

<img src="/images/variable-types.png" alt="variable types" width="379" height="114" />

## Declaring variables

Variables are declared with the `var` keyword. (We will use the `const` and `let` variables to declare variables in a later course.)

Variable names must start with a letter (a to z or A to Z), dollar sign (\$) or underscore (\_). We are only going to use lowercase letters to begin our variable names.


## Strings

Strings are pieces of text. They can range in size from one character like `a` to a whole book of characters.

They're enclosed in either single `'` or double `"` quotes. You can use either but stick with one throughout your code. We'll use double quotes in the course material.

Let's create our first string variable. To declare a variable we use `var` and a name of our choice:

```js
var pet = "dog";
```

We're storing the string "dog" in a variable (container) called `pet`. We can say we've `assigned` the value "dog" to `pet`, and now `pet` contains the value "dog".

<img src="/images/variable-string.png" alt="variable string" width="167" height="114" />

We can now use that variable anywhere in our code:

```js
console.log(pet);
```

---

Let's store a different string in the variable called `pet`. 

Create your first JavaScript variable:

###### Create a variable called `pet` with a value of "cat"
~~parser js strings firstString~~

---

Letter case matters in JavaScript. "Cat" is not equal to "cat". In the question above, if you give the variable a value of "Cat", the code checker will complain that's it looking for "cat".

In JavaScript we would say

```js
// "Cat" is not equal to "cat"
"Cat" !== "cat"
```

(We will get to equality operators like `!==` soon)

### Joining strings together

We can join strings together using the `+` sign. This is technically called `concatenation` but we'll call it joining.

```js
var letters = "a" + "b";

console.log(letters);
 // "ab"
```

Let's assign those string values to variables and then join them:

```js
var letter1 = "a";
var letter2 = "b";

var letters = letter1 + letter2;

console.log(letters);
 // "ab"
```

###### Join the strings "rab" and "bit" and assign them to a variable called `animal`
~~parser js strings joinStrings~~

---

Anything inside quotes is a string, even numbers. The variable `seven` below has a string value.

```js
var seven = "7";
```

###### Create a variable called `four` with a string value of "4"
~~parser js strings numberAsString~~


## Numbers

Numbers in JavaScript can be both integers (whole numbers) and decimals.

```js
var integer = 6;
var decimal = 5.1;
```

###### Create a variable called `four` with a number value of 4
~~parser js strings numberAsNumber~~