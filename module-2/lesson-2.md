
# Lesson 2 - Arrays

## Arrays

Arrays are lists of values in square brackets. Each value is separated by a comma `,`.

Here is an empty array:
```js
var emptyArray = [];
```

In module 1, [lesson 4](../1/4/#arrayloops), we used a `for loop` to loop through an array of strings, the array of colours.

```js
var colours = ["red", "blue", "green", "yellow"];
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

<!-- ###### Create a variable called `stringArray` and give it three string values
~~parser js arrays stringArray~~

###### Create a variable called `numberArray` and give it three number values
~~parser js arrays numberArray~~ -->

## Array properties and methods

#### Counting items in an array using `length`

In module 1, [lesson 4](../1/4/#arraylength) we saw how to get the number of items in an array using the `length` property.

```js
var colours = ["red", "blue", "green", "yellow"];
var numberOfColours = colours.length;
console.log(numberOfColours);
// 4
```

We don't really need that `numberOfColours` variable in the example above, we could log the length directly:

```js
console.log(colours.length);
// 4
```

<!-- ###### Create a variable called `arrayLength` with an array value, give it at least one value and log the number of items in it
~~parser js booleans arrayLength~~ -->

#### Adding items to an array using `push`

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

console.log(myArray)
// [19]
```

Let's add a colour to the `colour` array:

```js
var colours = ["red", "blue", "green", "yellow"];

// add purple to the colours array
colours.push("purple");

// now colours includes purple
console.log(colours);
// ["red", "blue", "green", "yellow", "purple"]

// now the length property will be 5 
console.log(colours.length);
// 5
```

<!-- ###### Create a variable called `arrayLength` with an array value, give it at least one value and log the number of items in it
~~parser js booleans arrayLength~~ -->


## So what are arrays used for?

Until now the example arrays haven't been much use, just some rather random lists.

But almost every website you visit uses arrays for the data they display. Some examples would be:

- posts on an Instagram page
- articles on a news site
- a Twitter feed

All of those would be fetched from the server as an array, and the browser would loop through the array to display them on the page.

<img src="/images/array-from-server.png" alt="Array from server" style="max-width: 480px" />

---

If you visited a website and all it did was loop through a list of strings like in the diagram, you might not visit it too often. 

Sites like Instagram loop through more complex data than simple types like strings or numbers. 

---

Let's say we wanted to build a simple Instagram clone, called *Norogram*.

Posts on *Norogram* would only include three variables:

- `imageUrl`, which would be a URL `string` like `https://path/to/bee-picture`
- `likeCounter`, which would be a `number` like `80`
- `likedByUser` - whether or not the user has liked the image. This would be a `boolean` value - `true` or `false` 

<img src="/images/norogram.png" alt="Norogram" style="max-width: 600px" />

According to the diagram we need an array of three items (posts), and each item has three variables: `imageUrl`, `likeCounter` and `likedByUser`.

We can store multiple variables in an item using `objects`.

---

In [lesson 3](3) we'll look at `objects` and `arrays of objects`.

---

- [Go to lesson 3](3) 
---
