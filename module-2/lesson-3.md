# Lesson 3 - null, Objects and arrays of objects

## null

We saw that an uninitialised variable (a variable that has been declared but not assigned a value), receives a value of `undefined`.

You can think of `undefined` as an empty value - we can't do much with it.

JavaScript has another empty value called `null` which you will often see too. In practical terms, there is not really any difference between undefined and null, they are both empty value types.

So why have two empty value types and confuse everyone?

The original version of JavaScript was written in ten days in the mid-1990s on a tight deadline. Some of the decisions made by the developer were maybe not the best but we have to live with them as there is an enormous amount of code written that takes into account these decisions.

When a variable or object property (discussed below) has no real value it will often be given the value `null`.

---

## Introduction to objects

`Objects` are used to store related variables.

Variables inside objects are called `properties`. Everything in an object lives inside curly braces: `{}`

Objects can have none or many properties.

Here is an empty object with no properties:

```js
var emptyObject = {};
```

---

It can be useful to compare objects in JavaScript to objects in the real world.

A dog in the real world has certain properties like `name`, `breed` and `numberOfLegs`.

We can represent these properties in an object in JavaScript like this:

```js
var dog = {
	name: "Tripod",
	breed: "labrador",
	numberOfLegs: 3,
};
```

We've created a variable called `dog` with a value type of `object`. The `object` has three properties, `name`, `breed` and `numberOfLegs`.

Each property has a `key` (or `name`) and a `value`. The `key` is on the left; it's the variable name. The `value` is on the right and is the... value.

Each value can be any of the JavaScript value types we've covered so far:

-   `string`
-   `number`
-   `boolean`
-   `undefined`
-   `null`

```js
var dog = {
	name: "Tripod", // name is the key, "Tripod" is the value, a string value
	breed: "labrador", // breed is the key, "labrador" is the value, a string value
	numberOfLegs: 3, // numberOfLegs is the key, 3 is the value, a number value
};
```

We can access an object's properties using dot `.` notation.

To get the `dog`'s `name` value:

```js
console.log(dog.name);
// "Tripod"
```

To get the `dog`'s `breed` value:

```js
console.log(dog.breed);
// "labrador"
```

<iframe src="https://player.vimeo.com/video/496270832" height="500" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

<a href="https://vimeo.com/496270832/44859ca45f" target="_blank">Watch on Vimeo</a>

<a href="https://github.com/NoroffFEU/introduction-to-objects/blob/master/script.js" target="_blank">Code from the video</a>

---

## Arrays of objects

Here are two product objects:

```js
var product1 = {
	id: 327,
	name: "Product 1",
	price: 99.99,
};

var product2 = {
	id: 968,
	name: "Product 2",
	price: 50.95,
};
```

If we wanted to store these products in a list we would need to use an array, since arrays are how we hold lists of variables.

Items in an array are placed between square brackets and are separated by a comma:

```js
var products = [product1, product2];
```

Now we have an array of objects.

We can loop through the array of objects like any other array, using a for loop.

This code will log each object in the array:

```js
for (var i = 0; i < products.length; i++) {
	console.log(products[i]);
}
```

To log a property from each object we can use dot notation.

This will log each product's `name` property:

```js
for (var i = 0; i < products.length; i++) {
	var productName = products[i].product;
	console.log(productName);
}
```

When you fetch live data in your projects, the data will be sent as objects or arrays of objects, this is why we are covering these topics.

A list of products containing the objects above sent from a server would look like this, with the objects placed directly into the array, rather than in variables.

```js
[
	{
		id: 327,
		name: "Product 1",
		price: 99.99,
	},
	{
		id: 968,
		name: "Product 2",
		price: 50.95,
	},
];
```

This video looks at looping through arrays of objects and includes a practical use for the object properties, i.e. creating HTML from them.

<iframe src="https://player.vimeo.com/video/496371287" height="400" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

<a href="https://vimeo.com/496371287/211fcb39fe" target="_blank">Watch on Vimeo</a>

<a href="https://github.com/NoroffFEU/arrays-of-objects" target="_blank">Code from the video</a>

---

<!--
## A real world example of an array of objects

### APIs

A `REST` `API` is one way to fetch data from a server.

`API` stands for `A`pplication `P`rogramming `I`nterface.

An `API` is a way for programs to communicate with each other.

`REST` stands for `Representational state transfer`.

A `REST` `API` gives us `URL`s that allow a browser to communicate with a server and fetch data that it can use JavaScript to loop over and display.

The data that a REST API sends to the browser will look a lot like the arrays of objects that we've been discussing.

Let's take a look at an example.

### Testing a free API

There are many free APIs frontend developers can use to test fetching data.

They can be found through google searches or on sites like [Rapid API](https://rapidapi.com/collection/list-of-free-apis).

A nice and simple API URL to use and display an array of objects is `https://elephant-api.herokuapp.com/elephants`. This URL will fetch an array of elephant objects.

A good way to test fetching data from a server is to use [Postman](https://www.getpostman.com/downloads/).

To fetch data from an API we use a `GET` request. (A `POST` request sends data to the server).

Once Postman is installed, click the `+` tab to create a new request:

<img src="/images/postman-plus-tab.png" alt="Postman plus tab" style="max-width: 276px" />

Enter `https://elephant-api.herokuapp.com/elephants` in the GET field and hit `Send`:

<img src="/images/postman.png" alt="Postman" style="max-width: 600px" />

Below you will see the API returns an array of objects like this:

```js
[
	{
		_id: "5cf1d0db3cfbe0fcbb6c4c93",
		index: 1,
		name: "Abul-Abbas",
		affiliation: "Charlemagne",
		species: "Asian",
		sex: "Male",
		fictional: "false",
		dob: "Unavailable",
		dod: "810",
		wikilink: "https://en.wikipedia.org/wiki/Abul-Abbas",
		image: "https://elephant-api.herokuapp.com/pictures/001.jpg",
		note: "An elephant given to Carolingian emperor Charlemagne by the Abbasid caliph Harun al-Rashid.",
	},
	{
		_id: "5cf1d0db8c4845fb358b91d6",
		index: 2,
		name: "Arjuna",
		affiliation: "Dasara",
		species: "Asian",
		sex: "Male",
		fictional: "false",
		dob: "1960",
		dod: "-",
		wikilink: "https://en.wikipedia.org/wiki/Arjuna_(elephant)",
		image: "https://elephant-api.herokuapp.com/pictures/002.jpg",
		note: "A lead elephant of the world-famous Mysore Dasara procession.",
	},
];
```
--- -->

## Lesson Task

There are practice questions in the master branch of <a href="https://github.com/NoroffFEU/lesson-task-pf-module2-lesson3" target="_blank">this repo</a>.

There are example answers in the <a href="https://github.com/NoroffFEU/lesson-task-pf-module2-lesson3/blob/answers/js/script.js" target="_blank">answers branch</a>.

Try the exercises before checking the solutions.

---

[Go to lesson 4](4)

---
