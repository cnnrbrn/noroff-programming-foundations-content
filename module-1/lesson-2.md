# Variables - strings, numbers and booleans

Variables are how a programming language stores information in a computer's memory. We can think of them as containers for data and once stored there, we can act on and use this data in other parts of our program.

<img src="/images/variable-containers.png" alt="variable containers" style="max-width: 379px" />

In JavaScript, variables don't have types, but the data the variables hold do.

We are going to look at these three types of data:

-   `string`
-   `number`
-   `boolean`

<img src="/images/variable-types.png" alt="variable types" style="max-width: 379px"/>

## Declaring variables

Before we can use variables, we need to`declare` (create) them.

Variables are declared with the `var` keyword. (We will use the `const` and `let` variables to declare variables in a later course.)

```js
var pet;
```

Above we've created a variable called `pet`. We haven't given `pet` a value, so it is empty or `undefined`. If you console log `pet` it will return a value of `undefined`. 

Giving a variable a value when you declare it is called `initialising` the variable.


## Strings

Strings are pieces of text. They can range in size from one character like `a` to a whole book of characters.

They're enclosed in either single `'` or double `"` quotes. At Noroff we use double quotes for our string variables.

Let's create our first string variable.

Variable names must start with a letter (`a` to `z` or `A` to `Z`), dollar sign `$` or underscore `_`. We are only going to use lowercase letters to begin our variable names.

 To declare a variable we use `var`, a name of our choice and a value if we are initialising it.

```js
var pet = "dog";
```

We've initialised the variable `pet` with the string value "dog". We can say we've `assigned` the value "dog" to `pet`, and now `pet` contains the value "dog".

<img src="/images/variable-string.png" alt="variable string" style="max-width: 167px" />

We can now use that variable in our code:

```js
console.log(pet);
```

---

Let's store a different string value in the variable called `pet`. 

Create your first JavaScript variable:

###### Create a variable called `pet` with a value of "cat"
~~parser js strings firstString~~

---

Letter case matters in JavaScript. "Cat" is not equal to "cat". In the question above, if you give the variable a value of "Cat", the code checker will complain that's it looking for "cat".

In JavaScript we would say

```js
// "Cat" is not equal to "cat"
"Cat" !== "cat"
```

(We will get to comparison operators like `!==` soon)

### Joining strings together

We can join strings together using the `+` sign. This is technically called `concatenation` but we'll call it joining.

```js
var letters = "a" + "b";

console.log(letters);
 // "ab"
```

Let's assign those string values to variables and then join them:

```js
var letter1 = "a";
var letter2 = "b";

var letters = letter1 + letter2;

console.log(letters);
 // "ab"
```

###### Join the strings "rab" and "bit" and assign them to a variable called `animal`
~~parser js strings stringConcatenation~~

---

Anything inside quotes is a string, even numbers. The variable `seven` below has a string value.

```js
var seven = "7";
```

###### Create a variable called `four` with a string value of "4"
~~parser js strings numberAsString~~


## Numbers

Numbers in JavaScript can be both integers (whole numbers) and decimals.

```js
var integer = 8;
var decimal = 7.1;
```

<img src="/images/variable-number.png" alt="variable number" style="max-width: 424px" />

###### Create a variable called `four` with a number value of 4
~~parser js numbers numberAsNumber~~


### Basic arithmetic operators

We can use the following operators with numbers in JavaScript.

| Operator      | Name           | Example  |
| ------------- |:-------------: | -----:   |
| +             | addition       | 3 + 2    |
| -             | subtraction    | 7 - 1    |
| *             | multiplication | 6 * 4    |
| /             | division       | 9 / 3    |
| %             | modulus        | 5 % 2    | 


We will cover the `modulus` (sometimes called `remainder`) operator in a later course.

<!-- ###### Create a variable called `multiply` and initialise it with a value of 7 times 3
~~parser js numbers multiplyNumbers~~ -->


## Booleans

Boolean values are either `true` or `false`.

```js
var isLoggedIn = true;
```

<!-- <img src="/images/variable-boolean.png" alt="variable boolean" style="max-width: 242px" /> -->

<img src="/images/variable-boolean.png" alt="variable boolean" style="max-width: 242px" />

---

Note that ***there are no quotes around boolean values***.

The variable `badBoolean` below has a `string` value, so it's not a boolean.
```js
var badBoolean = "true";
```

The variable `properBoolean` below has a boolean value.
```js
var properBoolean = true;
```

---

###### Create a variable called `lightIsOn` and initialise it with a value of false
~~parser js booleans firstBoolean~~

We can produce boolean variables using `comparison operators`, which we'll look at in the next lesson.

---

### Watch

The following Scrimba video covers variables and briefly examines comparison operators.

[Programming Foundations: Intro to Variables and Operators](https://scrimba.com/c/cdNRKKfk)

---

## Checking data types

We can use the `typeof` operator to check what type of data a variable holds. We can use it with or without brackets.

```js

var colour = "red";

typeof(colour);
// "string"

typeof("blue");
// "string"

typeof 14;
// "number"

typeof false;
// "boolean"

```

###### Write code that checks the type of the value: 23
~~parser js variables typeofNumber~~


---
## Acivities

#### Read

[Chapter 1](https://eloquentjavascript.net/01_values.html) from _Eloquent JavaScript_.

Read up to the **Operators** section.

---

#### Watch

[LinkedIn Learning: Learning the JavaScript Language](https://www.linkedin.com/learning/learning-the-javascript-language-2/)

Watch the following videos:

Section 2. Variables and Types:

- Declaring and assigning variables
- Strings
- Numbers 
- Booleans

Section 4. Operators and Control Structures:

- Arithmetic operators

---
- [Go to lesson 3](3) 
---