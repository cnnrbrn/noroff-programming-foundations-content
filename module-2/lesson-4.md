# Lesson 4: Introduction to functions

It is often a source of confusion to new students to see functions all over the
code and not understand what they are used for.

Functions in JavaScript often appear in what seem to be strange places.

Understanding functions is very important, but it will take time to get used to them - that will happen as you use them more and more.

Here we only introduce them. In the JavaScript 1 course we will look at them in more depth.

---

We have already been using functions, `console.log()` is a function and so is `toLowerCase()` and `toUpperCase()`.

## Our first function

To use a custom function, we first need to declare it.

Declaring a function means creating it. We use the `function` keyword and a name of our choice to declare it.

```js
// declare the function
function logWord() {
	// the code we want the function to run goes here
}
```

Above, we've declared a function called `logWord`.

> Like other variables, functions can be called anything. **_Give your functions meaningful names_**, though, functions called `hi` or `function1` are not well-named functions.

The contents of a function live between the curly braces `{ }`. We don't have any code there except a comment so our function doesn't do anything at the moment. We will look at the purpose of the parenthesis (round brackets) `()` a bit later.

---

Let's make our function do something, log a string to the console:

```js
function logWord() {
	console.log("one");
}
```

The code inside the function won't run until we `call` (or `execute` or `invoke` <b>\*</b>) the function.

> <b>\*</b> In programming, similar actions or techniques often have different names, which can be confusing when the same thing is referred to by different names. When we mention alternative names for things it's because that is what they might be called in other learning materials you may read or watch.

Without calling the function, the JavaScript engine knows about it, but won't execute the code inside the function.

We call a function using its name and round brackets `()`.

```js
// declare the function
function logWord() {
	console.log("one");
}

// call the function
logWord();
```

Now the `logWord` functon will run and `"one"` will be logged to the console.

> Notice that we **_don't_** use the `function` keyword to `call` the function. We only use the `function` keyword when `declaring` the function.

## Arguments

Our `logWord` function isn't very useful at the moment, it will always just console log the word `"one"`. We may as well have just written the console log out directly without declaring and calling a function.

We can make the function far more useful by passing variables into it so that the code inside the function can use them.

The variables that we pass in to functions are called `arguments`. We place them inside the `()`.

> When we call `console.log("somne value");` the value we want to log is an argument passed to the `log()` function.

Let's add an argument called `theWord` to the `logWord` function:

```js
function logWord(theWord) {
	console.log("one");
}

logWord();
```

The code inside the function is still just logging `one` though.

We can use the variables we pass in, the `arguments`, inside the function just like any other variable. Let's pass in a value as the `theWord` argument and then log that value:

```js
function logWord(theWord) {
	console.log(theWord);
}

logWord("hello");
```

Run the code above and you will see `hello` gets logged.

> You will often hear about `parameters`. Technically, the values passed into the function are called `parameters`, and the variable names inside the `()` are called `arguments`. We will call both `arguments` for simplicity's sake.

Change the value you pass in:

```js
function logWord(theWord) {
	console.log(theWord);
}

logWord(50);
```

Now `50` will get logged.

Whatever you pass in as the value will get logged as long as you use the `argument`'s correct name.

```js
function logWord(theWord) {
	console.log(theWord);
}

logWord(true);
```

`true` will get logged.

If we changed the code to this

```js
function logWord(theWord) {
	console.log(word);
}

logWord("hello");
```

we will get an error, as the argument (the variable) is called `theWord` but we are trying to log the variable `word`. The variable `word` doesn't exist in this function.

Always make sure you are using the correct `argument` names in your function code.

---

## Mulitple arguments

Functions can have zero, one or more arguments. Let's write a function with two arguments:

```js
// declare a function with two arguments
function AddTwoNumbers(number1, number2) {
	var sum = number1 + number2;
	console.log(sum);
}

// call the function and pass two arguments in
AddTwoNumbers(3, 4);
// 7
```

---

## Returning from a function

A lot of the time we want to return a value from a function so that we can use it elsewhere. To return a value we use the keyword `return`.

> No code after a `return` keyword will run. The function stops running code and returns the value as soon as it sees a `return` statement.

We can return the `sum` variable from the `AddTwoNumbers` above like this:

```js
function AddTwoNumbers(number1, number2) {
	var sum = number1 + number2;
	return sum;
}
```

We can assign what is returned from a function to a variable like this:

```js
var result = AddTwoNumbers(3, 4);
```

This video is an introduction to functions and includes a more practical example of using functions than simply logging variable values.

<iframe src="https://player.vimeo.com/video/496478495" height="400" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

<a href="https://vimeo.com/496478495/d8e360cf54" target="_blank">Watch on Vimeo</a>

<a href="https://github.com/NoroffFEU/introduction-to-functions" target="_blank">Code from the video</a>

---

## Lesson Task

There are practice questions in the master branch of <a href="https://github.com/NoroffFEU/lesson-task-pf-module2-lesson4" target="_blank">this repo</a>.

There are example answers in the <a href="https://github.com/NoroffFEU/lesson-task-pf-module2-lesson4/blob/answers/js/script.js" target="_blank">answers branch</a>.

Try the exercises before checking the solutions.

---

[Go to the module assignment](ma)
