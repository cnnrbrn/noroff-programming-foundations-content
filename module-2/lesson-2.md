# Lesson 2 - Arrays

## Introduction to arrays

So far we've been using single values stored in a variable:

```js
var colour1 = "red";
var colour2 = "pink";
var colour3 = "yellow";
```

Arrays provide a way to store multiple values in a single variable.

Arrays are lists of values in square brackets. Each value is separated by a comma `,`.

Here is an empty array:

```js
var emptyArray = [];
```

Here are the three values above stored in a single array variable:

```js
var colours = ["red", "pink", "yellow"];
```

Arrays can hold any kind of values.

Here is an array of numbers:

```js
var numbers = [6, 54, 17, 108];
```

Here is an array of booleans:

```js
var booleans = [true, false, false, true];
```

They can also hold different types of values:

```js
var mixedValues = ["blue", 17, false, 108, null];
```

<iframe src="https://player.vimeo.com/video/496045418" height="500" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

<a href="https://vimeo.com/496045418/9b01233bbe" target="_blank">Watch on Vimeo</a>

<a href="https://github.com/NoroffFEU/introduction-to-arrays/blob/master/script.js" target="_blank">Code from the video</a>

### Counting items in an array using `length`

Previously we saw how to get the number of characters in a string using the `length` property.

We can use the same property to get the numbers of items in array:

```js
var colours = ["red", "pink", "yellow"];
var numberOfColours = colours.length;
console.log(numberOfColours);
// 3
```

### Adding items to an array using `push`

We can add new items to an array using the `push` method:

Let's add a variable to an empty array:

```js
// here is the empty array
var myArray = [];

// its length will be 0 as there are no items in it
console.log(myArray.length);
// 0

// let's add a number to the array
myArray.push(19);

// now the length will be 1
console.log(myArray.length);
// 1

console.log(myArray);
// [19]
```

Let's add a colour to the `colours` array:

```js
var colours = ["red", "pink", "yellow"];

// add purple to the colours array
colours.push("purple");

// now colours includes purple
console.log(colours);
// ["red", "pink", "yellow", "purple"]

// now the length property will be 4
console.log(colours.length);
// 4
```

---

## Accessing items in arrays

We can access items inside an array using the index of the item.

The index is the position of the item in the array. The first item in the array is at position 0.

We use square brackets to access an item by its index:

```js
var colours = ["red", "pink", "yellow"];

var firstItem = colours[0];
// red

var thirdItem = colours[2];
// yellow
```

We can use a for loop to access every item in an array.

Because the first item in array is at index 0, our counter variable will begin at 0 and we will execute the loop only while the counter variable is less than the number of items in the array.

```js
var colours = ["red", "pink", "yellow"];

for (var i = 0; i < colours.length; i++) {
	var col = colours[i];
	console.log(col);
}
// red
// pink
// yellow
```

<iframe src="https://player.vimeo.com/video/496109329" height="500" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

<a href="https://vimeo.com/496109329/62318a0066" target="_blank">Watch on Vimeo</a>

<a href="https://github.com/NoroffFEU/looping-through-arrays/blob/master/script.js" target="_blank">Code from the video</a>

## So what are arrays used for?

Most websites you visit use arrays to display data. Some examples would be:

-   posts on an Instagram page
-   articles on a news site
-   a Twitter feed

But sites like Instagram loop through more complex data than simple value types like strings or numbers.

In JavaScript, complex data is stored in `objects`.

In [lesson 3](3) we'll look at `objects` and `arrays of objects`.

---

## Lesson Task

There are practice questions in the master branch of <a href="https://github.com/NoroffFEU/lesson-task-pf-module2-lesson2" target="_blank">this repo</a>.

There are example answers in the <a href="https://github.com/NoroffFEU/lesson-task-pf-module2-lesson2/tree/answers" target="_blank">answers branch</a>.

Try the exercises before checking the solutions.

---

[Go to lesson 3](3)

---
