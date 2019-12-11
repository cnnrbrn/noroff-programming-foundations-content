# Lesson 1

## Introduction

Programming is the act of writing instructions for a computer to follow.

Computers only speak `binary`, in `0`s and `1`s. In order to communicate with them we use programming languages which are eventually translated into
binary.

In web browsers, `JavaScript` is the programming language we use. A program inside the browser called a JavaScript engine translates the code - this is called `interpretation` - and delivers it to the computer to execute.

We are not going to go into too much more theory, but rather get you coding writing JavaScript as soon as possible.

## Writing JavaScript

### Using the development console

We recommend using [Chrome](https://www.google.com/chrome/) as your web browser when developing for the web, and the instructions and screenshots will be from that browser.

We can use a browser's `console` to write and run JavaScript without needing any other program.

To open the console, do one of the following:

- right-click anywhere on a web page and select `Inspect` from the menu
- 

We will be writing our JavaScript in files, but paying attention to the console in your browser is important as this is where errors in your code will appear.

### Adding a JavaScript file to an HTML page

Instead of typing directly into the developer tools console, we can use the `console.log` function. Using this function we can programmatically do what we manually did above, i.e. log (or print) the values to the console. To log the variables we entered above, we pass them in to the log function:

```js
console.log("hello");
console.log(10 + 5);
```

### Connecting and arranging your code

We recommed using [Visual Studio Code (VSCode)](https://code.visualstudio.com/) as your editor.

Create a new folder called `beginning-js` where you keep your code and open it in VSCode.

Right-click in the left pane

<img src="/images/vscode-pane.png" alt="VSCode pane" width="600" height="246" />

and create a new file called `index.html`. Type `html:5` inside the new file and press `Tab` on your keyboard.

<img src="/images/html5.png" alt="html:5" width="600" height="177" />

This is a quick way to scaffold a new HTML file. You can read more about these kind of shortcuts [here](https://code.visualstudio.com/docs/editor/emmet).

Before the closing `</body>` tag, add a `<script>` tag with a `src` attribute whose value is the path to a JavaScript file that we will create next:

```html
    <script src="js/script.js"></script>
    </body>
</html>
```

The `root` of your project is the parent folder for all your files. Until you start using for advanced tools, only `.html` files should be in the root. Keep other types of files in folders dedicatd to them:

Keep your js files in a folder called `js`. Create a file called `script.js` in that folder.

<img src="/images/file-arrangement.png" alt="File arrangement" width="600" height="198" />

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

Variables are how a programming language store information in a computer's memory.

Variable names must start with a letter (a to z or A to Z), dollar sign (\$) or underscore (\_). We are only going to use lowercase letters to being our variable names.

We are going to look at these three types of variables:

-   `string`
-   `number`
-   `boolean`

## Other tools
