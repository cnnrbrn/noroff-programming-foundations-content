# Lesson 3 - Objects and arrays of objects

`Objects` are used to store related variables. Variables inside objects are called `properties`. Everything in an object lives inside curly braces: `{}`

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
    numberOfLegs: 3
}
```

We've created a variable called `dog` with a value type of `object`. The `object` has three properties, `name`, `breed` and `numberOfLegs`.

Each property has a `key` and a `value`. The `key` is on the left; it's the variable name. The `value` is on the right and is the... value.

Each value can be any of the JavaScript value types we've covered so far:

- `string`
- `number`
- `boolean`
- `undefined`
- `null`

```js
var dog = {
    name: "Tripod", // name is the key, "Tripod" is the value, a string value
    breed: "labrador", // breed is the key, "labrador" is the value, a string value
    numberOfLegs: 3, // numberOfLegs is the key, 3 is the value, a number value
}
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

---

Let's create objects for our *Norogram* items.

First we'll reduce *Norogram* down to one post (item).

<img src="/images/norogram-one-post.png" alt="Norogram one post" style="max-width: 231px" />

As noted in the previous lesson, we need the following properties for an item:

- imageUrl, a `string`
- likeCounter, a `number`
- likedByUser, a `boolean`

We can create a post object with these properties like this:

```js
var postItem = {
    imageUrl: "https://path/to/bee-picture",
    likeCounter: 80,
    likedByUser: true
}
```

Because we want an array of items to loop through, we'll store this object in an array.

If we had no items in our *Norogram* posts, the array would be empty:

```js
var posts = [];
```

Since this version of *Norogram* has one item, we need one item in the array, the object above.

When we store objects in arrays, we don't need the variable name:

```js
// we can remove the variable name
{
    imageUrl: "https://path/to/bee-picture",
    likeCounter: 80,
    likedByUser: true
}
```

Now we can store that object in the posts array:

```js
var posts = [
    {
        imageUrl: "https://path/to/bee-picture",
        likeCounter: 80,
        likedByUser: true
    }
];
```

Since we have one item in the array, the object, the array's length will be 1:

```js
console.log(posts.length);
// 1
```

Let's use a `for loop` to loop through the `posts` array and console log the properties' values in the object.

First, let's just log the whole object.

```js
for(var i = 0; i < posts.length; i++) {

    // we access each item in the array using its index
    // we use the i variable as the index
    console.log(posts[i]);
}
```

This will log the whole object:

```js
// {
//     imageUrl: "https://path/to/bee-picture",
//     likeCounter: 80,
//     likedByUser: true
// }
```

Now let's get the `imageUrl` property value of the item using dot `.` notation:

```js
for(var i = 0; i < posts.length; i++) {

    // we use . and then the property name to access it
    var image = posts[i].imageUrl;
    console.log(image);
    // "https://path/to/bee-picture"

    // or we can log it directly without the variable
    console.log(posts[i].imageUrl);
    // "https://path/to/bee-picture"
}
```

Let's log all the properties' values:

```js
for(var i = 0; i < posts.length; i++) {

    console.log(posts[i].imageUrl);
    // "https://path/to/bee-picture"

    console.log(posts[i].likeCounter);
    // 80

    console.log(posts[i].likedByUser);
    // true
}
```

Let's add another post.

<img src="/images/norogram-two-posts.png" alt="Norogram two posts" style="max-width: 438px" />

Now we need another object in the array:

```js
var posts = [
    // first item
    {
        imageUrl: "https://path/to/bee-picture",
        likeCounter: 80,
        likedByUser: true
    },
    // second item
    {
        imageUrl: "https://path/to/tree-picture",
        likeCounter: 120,
        likedByUser: false
    }
];
```

We use the same `for loop` no matter how many items in the array.

Let's log only the `imageUrl` value:

```js
for(var i = 0; i < posts.length; i++) {

    console.log(posts[i].imageUrl);
}
```

This will log each `imageUrl` value:

```js
// "https://path/to/bee-picture"
// "https://path/to/tree-picture"
```


Let's go back to the original three posts:

<img src="/images/norogram-no-legend.png" alt="Norogram" style="max-width: 600px" />

We need to add a third object to the array:

```js
var posts = [
    // first item
    {
        imageUrl: "https://path/to/bee-picture",
        likeCounter: 80,
        likedByUser: true
    },
    // second item
    {
        imageUrl: "https://path/to/tree-picture",
        likeCounter: 120,
        likedByUser: false
    },
    // third item
    {
        imageUrl: "https://path/to/bat-picture",
        likeCounter: 34,
        likedByUser: true
    }
];
```

Again, we use the same `for loop`. This time we'll log the `likeCounter` value:

```js
for(var i = 0; i < posts.length; i++) {
    console.log(posts[i].likeCounter);
}
```

This will log:

```js
// 80
// 120
// 34
```

Let's log all the properties' values:

```js
for(var i = 0; i < posts.length; i++) {
    console.log(posts[i].imageUrl);
    console.log(posts[i].likeCounter);
    console.log(posts[i].likedByUser);
}
```

This will log:

```js
// "https://path/to/bee-picture"
// 80
// true
// "https://path/to/tree-picture"
// 120
// false
// "https://path/to/bat-picture"
// 34
// true
```

---

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

A good way to see the data we can fetch from a server is to use [Postman](https://www.getpostman.com/downloads/).

To fetch data from an API we use a `GET` request. (A `POST` request sends data to the server).

Once Postman is installed, enter `https://elephant-api.herokuapp.com/elephants` in the GET field and hit `Send`:

<img src="/images/postman.png" alt="Postman" style="max-width: 600px" />

Below you will see the API returns an array of objects like this:

```js
[
    {
        "_id": "5cf1d0db3cfbe0fcbb6c4c93",
        "index": 1,
        "name": "Abul-Abbas",
        "affiliation": "Charlemagne",
        "species": "Asian",
        "sex": "Male",
        "fictional": "false",
        "dob": "Unavailable",
        "dod": "810",
        "wikilink": "https://en.wikipedia.org/wiki/Abul-Abbas",
        "image": "https://elephant-api.herokuapp.com/pictures/001.jpg",
        "note": "An elephant given to Carolingian emperor Charlemagne by the Abbasid caliph Harun al-Rashid."
    },
    {
        "_id": "5cf1d0db8c4845fb358b91d6",
        "index": 2,
        "name": "Arjuna",
        "affiliation": "Dasara",
        "species": "Asian",
        "sex": "Male",
        "fictional": "false",
        "dob": "1960",
        "dod": "-",
        "wikilink": "https://en.wikipedia.org/wiki/Arjuna_(elephant)",
        "image": "https://elephant-api.herokuapp.com/pictures/002.jpg",
        "note": "A lead elephant of the world-famous Mysore Dasara procession."
    }
]
```

There will be many more objects than the two displayed above.

This looks a lot like our *Norogram* `posts` array, the objects just have more properties.

---

In the JavaScript 1 course, we will use API calls to fetch data, loop over it with JavaScript and display it with HTML and CSS.

---

In [lesson 4](4) we'll look at `functions`.

---

- [Go to lesson 4](4) 
---
