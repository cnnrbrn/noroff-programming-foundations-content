# Lesson 3 - Making decisions


## Comparison operators

Comparison operators compare their operands (the values on either side of the operator) and return a boolean value.

<img src="/images/operator.png" alt="variable types" style="max-width: 316px"/>

---

#### List of operators

| Operator      | Description               | Example  | Result 
| ------------- |:----------------------:   | :-----:  |  :---:
| `===`           | equal to                  | 3 `===` 2  |  false 
| `!==`           | not equal to              | 3 `!==` 2  |  true  
| `>`             | greater than              | 6 `>` 4    |  true  
| `>=`            | greater than or equal to  | 5 `>=` 5   |  true
| `<`             | less than                 | 5 `>` 4    |  false
| `<=`            | less than or equal to     | 3 `>` 4    |  true


---

```js
var myNumber = 7;
var myString = "dog";

// is myNumber greater than 8?
(myNumber > 8) // false

// is myNumber less than or equal to 7?
(myNumber <= 8) // true

// is myString exactly equal to "dog">
(myString === "dog") // true

// is myString not equal to "cat">
(myString !== "cat") // true

```

These operators are commonly used with conditional statements (covered below) to make a code decision depending on the value of a variable.

>You may see the `==` and `!=` operators. These are similar to `===` and `!==`, and we'll cover the differences between them in module 2. For now it's enough to know that you should always use `===` instead of `==` and `!==` instead of `!=`.

## Conditional statements

### if...else

When we need to make decisions in our code, we use `conditional statements`.

We check if a certain condition is true using a comparison operator, and if it is, we run a block of code.

If it is false, we run different code.

<img src="/images/conditional-statement.png" alt="conditional statement" style="max-width: 600px"/>

To carry out the above, we use `if...else statements.`

`if` a certain condition is true, run this code.
`else`, run this other code.

<img src="/images/if-statement.png" alt="if statement" style="max-width: 450px"/>

Perhaps you need to check whether a user is logged in:

```js
var isLoggedIn = true;

if(isLoggedIn === true) {
    console.log("The user is logged in");
}
else {
    console.log("The user is logged out");
}
```

Or whether a user has entered valid data into an input field in a form:

```js
var inputIsValid = false;

if(inputIsValid === false) {
    // show error message
}
else {
    // hide error message
}
```

###  if...else if...else

Sometimes you'll need to check multiple conditions.

<img src="/images/if-else.png" alt="if else statement" style="max-width: 450px"/>

You might need to check that a number is
- less than 5
- greater than or equal to 5
- greater than or equal to 9

```js
var ageOfCar = 6;

if(ageOfCar < 5) {
    console.log("The car is less than 5 years old");
}
else if(ageOfCar >= 5) {
    console.log("The car is 5 years old or older);
}
else if(ageOfCar >= 9) {
    console.log("The car is 9 years old or older);
}
```

Or you may need to check for multiple values of a string:

```js
var colour = "red";

if(colour === "blue") {
    console.log("The colour is blue");
}
else if(colour === "red") {
    console.log("The colour is red");
}
else {
    console.log("The colour is neither blue nor red");
}
```

If we wanted to add more colour checks to the above code, we would need to add more `else if` statements. Our code would quickly become difficult read with so many `else if`s. In this scenario we can use `switch` statements.

### switch 

<!-- <img src="/images/switch.png" alt="switch statement" style="max-width: 450px"/> -->

```js
var colour = "red";

switch(colour) {
    case "blue":
        console.log("The colour is blue");
        break;
    case "red":
        console.log("The colour is red");
        break;
    case "green":
        console.log("The colour is green");
        break;
    case "yellow":
        console.log("The colour is yellow");
        break;
    default:
        console.log("The colour is not blue, red, green or yellow");
}

```

The `switch` statement receives a variable to check in parenthesis (round brackets). 

Inside the `curly braces` `{}` are several `case` blocks:

```js
case "blue":
    console.log("The colour is blue");
    break;
```

The above means: in the `case` of `colour` being equal to "blue", run the code after the colon `:` and before the `break`.

This is the equivalent of:

```js
if(colour === "blue") {
    console.log("The colour is blue");
}
```

The code after `default:` runs if none of the conditions in the case blocks are true. It's like an `else` block in an `if..else if...else` statement.

The `break` keyword is important. If you leave it out, the code will not break from the switch statement and will run the code in the default block.


### When to use switch instead of if

If you find yourself writing more than one `else if` statement, consider using a `switch` instead.


## Assignment vs comparison 

In the previous lesson we assigned values to variables using the `=` assignment operator.

A common mistake is to accidentally use the `=` operator instead of a comparison operator when peforming a check. When that happens the comparison will always return true:

```js
var myPet = "pig";

if(myPet = "sheep") {
    console.log("My pet is a sheep");
}
else {
    console.log("My pet is not a sheep");
}
```

Above, we've assigned "pig" to the variable `myPet` but in the `if` statement we've re-assigned `myPet` the value "sheep" because we've used the assignment operator rather than the equality comparison operator `===`.

So this statement will always log "My pet is a sheep". 

If your `if` statements are behaving strangely, remember to check for this easy-to-make mistake.

---

## Acivities

#### Watch

[LinkedIn Learning: Learning the JavaScript Language](https://www.linkedin.com/learning/learning-the-javascript-language-2/)

Watch the following videos under section 4. Operators and Control Structures:

- Simple comparisons
- Logical operators
- Conditionals: if
- Conditionals: switch
- Terse ifs

---
- [Go to lesson 4](4) 
---