# Lesson 4 - Loops

`Loops` are used to do the same thing over and over again. 

If we wanted to console log a number value from 1 to 3, we could do something like this:

```js
console.log(1);
console.log(2);
console.log(3);
```

Seems reasonable enough. 

But what if we wanted to log 1 to 100 or 1000? 

What if we wanted to log 1 to a number stored in a variable? Or from a number stored in a variable to another number stored in a variable. When writing the code, we wouldn't know either the start or end number.

That's where loops come in.

## for loop

```js
for(var count = 1; count <= 10; count++) {
    console.log(count);
}
```

Run the code above and you'll see that it logs 1 to 10.

Let's break it down.

Inside `for`'s brackets, we first have `var count = 1;`. This is the counter variable. It's just a variable so we could call it anything. Often the variable is called `i`.

<!-- ```js
for(var i = 1; i <= 10; i++) {
    console.log(i);
}
``` -->

`var count = 1` is the starting value for the loop. We've set it to start at `1`. 

Next is `count <= 10`. This is the condition that gets checked each time the loop runs. Each pass through the loop, the code will check if `count` is less than or equal to `10`. If it is, the code inside the curly braces `{}` will run. If not, the loop will stop.


The `count++` part is the `iterator`. On each loop, it adds a value to the `count` variable. `count++` is shorthand for `count = count + 1`.

So we could could rewrite the loop like this:
```js
for(var count = 1; count <= 10; count = count + 1) {
    console.log(count);
}
```

Some developers prefer to declare the variable outside the loop without initialising it:

```js
var count;

for(count = 1; count <= 10; count++) {
    console.log(count);
}
```

---

Let's write a loop that counts from `5` to `25`:

```js
for(var i = 5; i <= 25; i++) {
    console.log(i);
}
```

We're calling the variable `i` this time. We've set it to start at `5`. The loop will run until the condition (`i <= 25`) returns false.

We could write the condition differently:

```js
for(var i = 5; i < 26; i++) {
    console.log(i);
}
```

The result here is exactly the same, we've just modified the condition to check that `i` is less than `26`.

---

## Looping through arrays

You can think of `arrays` as lists or collections of variables. We will cover them more in module 2, but here we will write code to loop over a list of colours.

Here is an array of string variables, a list of colours. An array's variables live inside square brackers `[]`.

```js
var colours = ["red", "blue", "green", "yellow"];
```

To get an item from an array, we use the `index` of the array. In JavaScript, like many programming languages, counting begins at `0`, not `1`. The first item in an array has an index of `0`. We access the item by using the index inside the square brackets.

To get the first item from colours we would use:

```js
var firstItem = colours[0]; // the first item in the array is at index 0
console.log(firstItem);
// "red"
```

The second item would be at index 1:
```js
var secondItem = colours[1]; // the second item in the array is at index 1
console.log(secondItem);
// "blue"
```

This is quite a laborious process, getting each item manually by its index. We can use a `for` loop and its counter variable to get each item in the array programmatically.

We could log each colour like this:

```js
console.log(colours[0]);
console.log(colours[1]);
console.log(colours[2]);
console.log(colours[3]);
```

This would log:

```js
"red"
"blue"
"green"
"yellow"
```

Let's do that in a loop.

We need to know how many items are in the array, so that the `for` loop knows when to exit.

We can get the amount of items in an array using its `length` property:

```js
var numberOfColours = colours.length;
console.log(numberOfColours)
// 4
```

We are going to start the loop at `0`, since that is the first index of the array:

```js
for(i = 0; i < numberOfColours; i++) {
    console.log(colours[i]);
}
```

Our condition (`i < numberOfColours`) is checking to see if `i` is less than the number of items in the array.

It's important to note that we are not checking for less than or equal to (`<=`) `numberOfColours`, but only less than. 

Because we are starting at 0, we want to count from 0 to 3, rather than 1 to 4.

Running the code above will produce:

```js
"red"
"blue"
"green"
"yellow"
```

It doesn't matter how many items there were in the array, whether it's 1 or 1000, the same code will log each item.

---

We will look at another way to loop through arrays in module 2.

---

## Acivities

#### Watch

[LinkedIn Learning: Learning the JavaScript Language](https://www.linkedin.com/learning/learning-the-javascript-language-2/)

Watch the following videos:

Section 5. Iterating with Loops

- For loops: Sequential


---
- [Go to lesson module assignment](ma) 
---