# Lesson 1 - Getting started

## Introduction

Programming is the act of writing instructions for a computer to follow.

Computers only speak `binary`, in `0`s and `1`s. In order to communicate with them we use programming languages which are eventually translated into
binary.

In web browsers, `JavaScript` is the programming language we use. A program inside the browser called a JavaScript engine translates the code and delivers it to the computer to execute.

Everything dynamic on a web page, from news feeds to like buttons and games is created with JavaScript.

## Writing JavaScript

### Using the development console

> We recommend using [Chrome](https://www.google.com/chrome/) as your web browser when developing for the web, and the instructions will be for that browser.

We can use a browser's `console` tab in the developer tools to write and run JavaScript without needing any other program.

To open the developer tools, do one of the following:

- right-click anywhere on a web page and select `Inspect` from the menu
- From the menu in the top right <img src="/images/chrome-menu.png" alt="chrome menu" style="max-width: 12px; margin: 0.8em 0;" /> go to `More Tools` and then `Developer Tools`
- use the keyboard shortcut `Ctrl` `Shift` `J` (Windows) or `Cmd Option J` (Mac).

Once open, select the `console` tab.

Inside the console, enter the words `"hello world"` (with the quotes) and press enter.

The console prints (logs) the return value of the code you entered, in this case it returns the `string` "hello world".

<img src="/images/console-hello-world.png" alt="console hello world" style="max-width: 400px" />

Enter `10 + 5` and press enter. The console returns the result of what you entered.

Type `alert("hello")` and press enter. An alert should pop up with the text you entered in the quotes. Try and enter different text in the quotes. 

> You can press `Ctrl` `L` on Windows or `Cmd` `K` on Mac to clear the console


Although we will be writing our JavaScript in files, ***paying attention to the console in your browser is very important*** as this is where errors in your code will appear.

Type `hello` (without quotes) into the console and press enter. Because the text is not in quotes, the browser doesn't know what to do with that instruction and prints out an error. You will see lots of errors in your console on your JavaScript journey.

---

If you'd prefer the dev tools dark theme to the default light one, [here are instructions on enabling it](https://developers.google.com/web/tools/chrome-devtools/customize/dark-theme).

---

### Adding JavaScript to an HTML page

Instead of typing directly into the developer tools console, we can use the `console.log` function. Using this function we can programmatically do what we manually did above, i.e. log (or print) the values to the console. To log the variables we entered above, we pass them in to the log function:

```js
console.log("hello world");
console.log(10 + 5);
```

#### Using script tags in an HTML page

> We recommed using [Visual Studio Code (VSCode)](https://code.visualstudio.com/) as your editor.

Create a new folder called `beginning-js` where you keep all your code and open it in VSCode.

Create a new file called `index.html` by right-clicking in the left pane and selecting `New File` or by using the `File` menu.

Type `html:5` inside the new file and press `Tab` on your keyboard.

This is a quick way to scaffold a new HTML file. You can read more about these kind of shortcuts [here](https://code.visualstudio.com/docs/editor/emmet).

If that shortcut doesn't work, copy the following into the file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Beginning JS</title>
</head>
<body>
    
</body>
</html>
```

Add `<script></script>` tags to the HTML, right before the closing `</body>` tag. Inside the tags add the console logs from above:

```html
    <script>
        console.log("hello world");
        console.log(10 + 5);
    </script>
</body>
</html>
```

Open `index.html` in a browser, open the dev tools and look for the output from the logs in the console.

> [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) is a VSCode plugin that will allow you to run a local server from within VSCode and reload your pages automatically when code changes. Once installed, right-click on an html page and select `Open with Live Server`.


### Adding an external JavaScript file

We will write most of our code in external JavaScript files, rather than inside `<script>` tags.

Remove the code inside the `<script>` tags and add a `src` attribute:

```html
    <script src="js/script.js"></script>
    </body>
</html>
```

The `root` of your project is the parent folder for all your files. Until you start using advanced tools, only `.html` files should be in the root. Keep other types of files in folders dedicated to them.

Keep your js files in a folder called `js`. Create a file called `script.js` in that folder.

<img src="/images/file-arrangement.png" alt="File arrangement" style="max-width: 300px" />

Inside `js/script.js` add the console logs from above:

```js
console.log("hello world from an external js file");
console.log(10 + 5);
```

Reload the `index.html` and check the browser console for the above messages.

This is the most common way you will use JavaScript, writing code in `.js` files and linking to them from an `html` file.

## Formatting

Formatting your code properly is ***very important***. Well-formatted code is far easier to read and follow, for you and other developers, and it makes it easier to catch bugs and mistakes.

For now, concentrate on the following:
- consistent indentation - use tabs to properly align your code
- use semi-colons after your code statements

This is an example of poorly formatted and indented code:
```js
console.log( " hello")
	console.log(  "world");
```

This is an example of well-formatted and indented code:
```js
console.log("hello");
console.log("world");
```

We will mention other formatting rules as we go.

VSCode comes with built-in formatting. Right-click anywhere inside a file and select `Format Document`.

[Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) is a very useful and time-saving tool for JavaScript formatting. [Here](https://scotch.io/tutorials/code-formatting-with-prettier-in-visual-studio-code) is a good tutorial on setting it up in VSCode.

## Live share

[Live Share](https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare) is a plugin that will allow you to share the code on your computer with a tutor (or anyone else). 

### A note on semi-colons

Semi-colons at the end of statmements are only technically necessary if you have more than one statement on a line. 

For the most part, using semi-colons is a matter of preference. Different companies and dev studios will have their own `style guides` - a set of rules, including whether to use semi-colons or not, that all devs must follow. You will be given our style guide to follow in the JavaScript 1 course.

For now, as Noroff's preference is to use semi-colons, please include them in your code. 

## Comments

Comments are statements in our code that are not run by the JavaScript engine, but are used to provide information to ourselves and other developers.

Comments can be single-line comments using double forward slashes `//`:

```js
// this is a single-line comment
```

They can also be multi-line comments using a single forward slash `/` and an asterisk `*`:

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

Comments are also often used to explain what we want to do in the future at a particular place in the code, either for ourselves or other people.

When asking a tutor for help, you will often find they use comments to indicate what code you should write in that position in your code.

```js
// create a for loop here that counts from 1 to 10
```


---

In [lesson 2](2) we'll look at `string`, `number` and `boolean` variables.

---

## Acivities


### Watch

The following Scrimba video covers getting set up with JavaScript.

[Programming Foundations: Getting Set up with JavaScript](https://scrimba.com/c/cdNRKmtz)

---


### Read

[Introduction](https://eloquentjavascript.net/00_intro.html) from _Eloquent JavaScript_.

Read up to the **Code, and what to do with it** section.


### Extra stuff

[The Weird History of JavaScript (video)](https://www.youtube.com/watch?v=Sh6lK57Cuk4)

---
- [Go to lesson 2](2) 
---