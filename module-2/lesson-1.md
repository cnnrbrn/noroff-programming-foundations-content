
# Lesson 1 - Errors and some JavaScript silliness

Finding errrors and bugs in your code can be frustrating as they often appear to be "small" things like spelling mistakes or a missing keyword like `var`. These aren't small things to the JavaScript engine, though, and your code needs to be exact.

We mentioned in [lesson 1](../1/1/) of module 1 that paying attention to the console in your browser is very important as this is where errors in your code will appear. When asking a tutor for help with code that doesn't work, the first thing they are likely to ask is if there are any errors in the console.

Let's look at one error that occurs often to try and get a sense of what we look for when trying to find solutions to errors.

Delete anything that may be in `js/script.js` that we created in [lesson 1](../1/1/) of module 1. Enter the following and save:

```js
myVar;
```

Reload the `index.html` page (if you aren't using [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)) and look at the console output. You should see something similar to this:

<img src="/images/error-not-defined.png" alt="Not defined" style="max-width: 600px" />


You'll see this error if you've tried to create a variable but left out the `var` keyword. The JavaScript engine doesn't know that you want `myVar` to be a variable. 

Add the `var` keyword and check the console again.

```js
var myVar;
```

Now there are no more errors in the console:

<img src="/images/no-error.png" alt="No error" style="max-width: 600px" />


If you console log `myVar` now 

```js
var myVar;
console.log(myVar);
```

and check the console, you will see it says `undefined`. 

<img src="/images/error-undefined.png" alt="Undefined" style="max-width: 600px" />

This can be a bit confusing. `undefined` doesn't mean there is an error, it just means that `myVar` (or any other variable) hasn't been assigned a meaningful value yet. 

In general, serious errors will appear in red in the console. Warnings, or errors that may not break your code, will appear in orange.

---

## Undefined and null

We saw that an uninitialised variable (a variable that has been declared but not assigned a value), like `myVar` above, receives a value of `undefined`. 

`undefined` is a valid value in JavaScript, but you can think of it as an `empty value` - we can't do much with it. 

JavaScript has another `empty value` called `null` which you will often see too. In practical terms, there is not really any difference between `undefined` and `null`, they are both empty value types.

So why have two empty value types and confuse everyone?

The original version of JavaScript was written in ten days in the 1990s on a tight deadline. Some of the decisions made by the developer were not too great, but we have to live with them as there is an enormous amount of code written that takes into account these decisions. 


## `===` versus `==`

Over the past few years, enhancements to the language have improved it a lot and it's a much nicer language to work with now. 

But it's important to be aware of the language's existing quirks, and another one that we briefly mentioned in module 1 was the triple equals equality operator `===` and the double equals equality operator `==`. The teachers love to stomp their feet when you use the `==` version.

In module 1, [lesson 2](../1/2/), we looked at three types of values:

-   `string`
-   `number`
-   `boolean`

(We've also now added `undefined` and `null` to the list of value types).

Say we had the following two variables:

```js
var stringFour = "4";
var numberFour = 4;
```

If we wanted to use an `if` statement to check to see if they were equal, similar to what we did with the comparison operators in module 1, [lesson 3](../1/3/), we could write the comparison in two ways. 


In module 1 we used `===`:

```js
var stringFour = "4";
var numberFour = 4;

if(stringFour === numberFour) {
    console.log("equal");
}
else {
    console.log("not equal");
}
```

Copy and run that code and you will see that `not equal` is logged. The `stringFour` variable has a string value, the `numberFour` variable has a number value. Using `===` makes sure that `string` values and `number` values can never be equal. This is a ***good*** thing and prevents lots of bugs.

If we use the same code with the `==` operator, `equal` will be logged. 

```js
var stringFour = "4";
var numberFour = 4;

if(stringFour == numberFour) {
    console.log("equal");
}
else {
    console.log("not equal");
}
```

This is because JavaScript will try to convert the value of one type to the value of another. In this case it will convert the `string` value `"4"` to a `number` value `4`. Technically this is called `type coercion`. It may not seem like it, but this is a ***bad*** thing. Lots of weird and unexpected things start to happen.

The same applies to the `not equal to` operators `!==` and `!=`.

Please always use `===` and `!==`. 

---

In [lesson 2](2) we'll look at `arrays`.

---

---
- [Go to lesson 2](2) 
---