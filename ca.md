# Course Assignment

## Brief

The files for the assignment can be found <a href="https://github.com/NoroffFEU/programming-foundations-ca" target="_blank">here</a>.

Some of the questions don't provide variable names, and you must come up with them yourself. Choosing appropriate variable names will form part of your assessment, as will proper and consistent formatting of your code.

## Level 1

### Question 1

Create a variable called `outOfStock` and assign it a `boolean` value.

Create an `if else` statement that checks the value of `outOfStock`.

If it is `true`, console log `"Out of stock"`.
Otherwise log `"In stock"`.

---

### Question 2

Create a `for loop` that counts from 15 to 25. Console log the value of the counter variable inside the loop only if it's equal to 17 or 20.

---

### Question 3

Loop through the array below and add an `li` item to the `ul` element in the HTML containing the `title` and `rating` of each game only if the `rating` for the game is below `3.5`.

```js
var games = [
	{
		title: "Grand Theft Auto",
		rating: 4.48,
	},
	{
		title: "Portal 2",
		rating: 3.5,
	},
	{
		title: "Team Fortress",
		rating: null,
	},
	{
		title: "The Witcher",
		rating: 3.0,
	},
	{
		title: "The Elder Scrolls",
		rating: 2.9,
	},
];
```

The `ul` element should look similar to this after your code executes:

```html
<ul>
	<li>Name of game: rating</li>
	<li>Name of game: rating</li>
</ul>
```

---

### Question 4

Create a function called `whatIDontLike` that accepts one argument. Choose a good name for the argument.

Inside the function, check if the argument has a string value. If it doesn't log the message "Please send in a string".

If the argument is a string value, log the message `"I don't like "` together with the argument.

Call the function and pass in a value of your choice.

**Example:**<br>
If you pass in the value `"giraffes"`, the function should log: `"I don't like giraffes"`.

---

### Question 5

Create a function that accepts two arguments.

Inside the function, try to convert the arguments to numbers.

If either of the arguments cannot be converted to a number, return the value: `"Invalid argument(s)"`.

If both arguments are number values or can be converted to number values, subtract the second argument from the first and return the result from the function.

Call the function, pass in to two values and assign the return value to be the innerHTML value of the element with the id `subtraction`.

---

### Question 6

Select the button with the class `page`.

When the button is clicked do the following:

-   Change the title of the page (the value of the title element in the head) to "Updated title".
-   Change the background colour of the whole page to "yellow".
-   Change the color of the `h1` element to "green".
-   Change the `h1` element's font to "impact".
-   Change the value of the `h1` element to be a link.
-   Remove the list style and padding from the `ul` element.

The `h1` element should look like this after the click event:

```html
<h1><a href="#">Programming Foundations Course Assignment</a></h1>
```

---

### Question 7

Select the button with the class `page`.

When the button is clicked, loop through the array below, add all the prices and assign the total to be the innerHTML value of the element with the id `total`.

```js
var toys = [
	{
		name: "Lego",
		price: 15.6,
	},
	{
		name: "Master of the Universe",
		price: "28.3",
	},
	{
		name: "Barbie",
		price: null,
	},
	{
		name: "Mr Potato Head",
		price: 89.99,
	},
];
```

---

## Submission

-   All your answers should be in the `js/script.js` file.
-   You can submit only this file (zipped) or all the files from the repo (also zipped).
-   Write your answers with a comment above each answer indicating the question number:

```js
// question 1

// your answer for question 1 goes here

// question 2

// your answer for question 2 goes here

// etc
```

-   The zipped folder should be called `{your-name}-pf-ca.js` (without the curly braces).
-   Submit the zipped folder.
