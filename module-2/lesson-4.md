# Lesson 4: Functions

It is often a source of confusion to new students to see functions all over the
code and not understand what they are used for.

Functions in JavaScript often appear in what seem to be strange places.

Understanding functions is very important, but it will take time to get used to them - that will happen as you use them more and more.

Here we only introduce them. In the JavaScript 1 course we will look at them in more depth.

---

Let's consider one of the main uses for functions:

- to run code more than once


## Repeatedly running the same code

The less code you write, the fewer bugs and mistakes your code will have.

If you find yourself writing code that does the same thing or something very similar, it's time to use a function.

Say we wanted to console log three words on new lines:

```js
// one
// two
// three
```

We *could* write the code to do that like this:

```js
console.log("one");
console.log("two");
console.log("three");
```

But we've got three lines of very similar code, and it's easy to make mistakes like this:

```js
console.log(one);
consol.log("two");
console.log("three);
```

All three lines have errors in them, and the way to avoid making these kind of errors and having fewer places to check for bugs, is to convert this code into a function.


## Our first function

To use a function, we first need to declare it. Declaring a function means writing the code for what we want it to do. We use the `function` keyword and a name of our choice to declare it.

```js
// declare the function
function logWord() {
    // the code we want the function to run goes here
}
```

Above, we've declared a function called `logWord`.

> Like other variables, functions can be called anything. **_Give your functions meaningful names_**, though, functions called `hi` or `function1` are not well-named functions.

The contents of a function live between the curly braces `{ }`. We don't have any code there except a comment so our function doesn't do anything at the moment. We will look at the purpose of the parenthesis (round brackets) `()` a bit later in the lesson.

---

###### Create an empty function called `emptyFunction`
~~parser js functions firstFunction~~

--- 

Let's make our function do something, log a string to the console:

```js
function logWord() {
    console.log("one");
}
```

Delete everything in `js/script.js`, save the above code and watch the console. 

The console is empty.

<img src="/images/no-error.png" alt="Empty console" style="max-width: 600px" />

The code inside the function, in this case:

```js
console.log("one");
```

won't run until we `call`  (or `execute` or `invoke` <b>*</b>) the function.

> <b>*</b> In programming, similar actions or techniques often have different names, which can be confusing when the same thing is referred to by different names. When we mention alternative names for things it's because that is what they might be called in other learning materials you may read or watch.

 Without calling the function, the JavaScript engine knows about it, but won't execute the code inside the function.

We call a function using its name and round brackets `()`.

```js
logWord();
```

Inside `js/script.js` call the function after declaring it:

```js
function logWord() {
    console.log("one");
}

logWord();
```

Now the `logWord` functon will run and `one` will be logged to the console.

```js
// one
```

> Notice that we **_don't_** use the `function` keyword to call the function. We only use the `function` keyword when `declaring` the function.


<!-- <img src="images/function-process.png" alt="function process" width="600" height="313" /> -->


###### Create a function called `sayHello` that console logs the string "hello"
~~parser js functions consoleLog~~

## Arguments

Our `logWord` function isn't very useful at the moment, it will always just console log the word `one`. We may as well have just written the console log out directly without declaring and calling a function.

We can make the function far more useful by passing variables into it so that the code inside the function can use them.

The variables that we pass in to functions are called `arguments`. We place them inside the `()`.

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

> You will often hear about `parameters`. Technically, the values passed into the function are called `parameters`, and the variable names inside the `()` are called `arguments`. For now we will just call both `arguments` for simplicity's sake.

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

Now we can rewrite this code

```js
console.log("one");
console.log("two");
console.log("three");
```

to use the `logWord` function:

```js
function logWord(theWord) {
    console.log(theWord);
}

logWord("one");
logWord("two");
logWord("three");

// one
// two
// three
```

Looks like we've only succeeded in writing *more* code than we originally had.

Let's change the function so that it always logs a string value together with whatever we pass in:

```js
function logWord(theWord) {
    console.log("The word passed in is " + theWord);
}

logWord("one");
logWord("two");
logWord("three");

// The word passed in is one
// The word passed in is two
// The word passed in is three
```

The words `The word passed in is` are getting logged every time we call the function without us having to pass them in each time.

If we wanted to change the sentence `The word passed in is` to something else, we only need to change it in one place:

```js
function logWord(theWord) {
    console.log("The argument is " + theWord);
}

logWord("one");
logWord("two");
logWord("three");

// The argument is one
// The argument is two
// The argument is three
```
---

Let's go back to our *Norogram* posts and add the word `likes` next to the `likeCounter` variable:

<img src="/images/norogram-with-likes.png" alt="Norogram" style="max-width: 600px" />


Let's create a function that has the `likeCounter` variable as an argument and prints the number of likes out:

```js
function printLikeCounter(likeCounter) {
    // we're adding a space before the word "likes"
    console.log(likeCounter + " likes");
}

printLikeCounter(80);
printLikeCounter(120);
printLikeCounter(34);

// 80 likes
// 120 likes
// 34 likes

```

If we wanted to change our design to use the word `loves` instead of `likes`

<img src="/images/norogram-with-loves.png" alt="Norogram" style="max-width: 600px" />

we just need to change that in one place in our function:

```js
function printLikeCounter(likeCounter) {
    console.log(likeCounter + " loves");
}

printLikeCounter(80);
printLikeCounter(120);
printLikeCounter(34);

// 80 loves
// 120 loves
// 34 loves

```

## Returning from a function

A lot of the time we want to return a value from a function so that we can use it elsewhere. To return a value we use the keyword `return`.

> No code after a `return` keyword will run. The function stops running code and returns the value as soon as it sees a `return` statement. 

---

Let's change the `printLikeCounter` function to a `createLikeCounter` function that returns the like count:


```js
function createLikeCounter(likeCounter) {
    return likeCounter + " likes";
}
```

If we call this function now, it will look like nothing is happening as there are no console log statements in the function anymore.

```js
function createLikeCounter(likeCounter) {
    return likeCounter + " likes";
}

createLikeCounter(80);
```

We need to assign the return value of the function to a variable. Then we can do something with it.

```js
function createLikeCounter(likeCounter) {
    return likeCounter + " likes";
}

var counter = createLikeCounter(80);
```

Now we can log the `counter` variable:

```js
console.log(counter);
// 80 likes
```

Let's create some HTML in the function and return it:

```js
function createLikeCounter(likeCounter) {
    // we're adding <b></b> tags around the likeCounter variable
    return "<b>" + likeCounter + "</b> likes";
}

var counter = createLikeCounter(80);
// <b>80</b> likes
```

Let's add a `<div>` tag around everything we return:

```js
function createLikeCounter(likeCounter) {
    // we're adding <b></b> tags around the likeCounter variable
    // and <div></div> tags around everything
    return "<div><b>" + likeCounter + "</b> likes</div>";
}

var counter = createLikeCounter(80);
// <div><b>80</b> likes</div>
```

## Mulitple arguments

Functions can have zero, one or more arguments. Above, our `createLikeCounter` function had only one argument. Let's write a function with two:

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

## Acivities

### Watch

[Programming Foundations: Functions](https://scrimba.com/c/cnkpKnhZ)

---