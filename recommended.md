# Extra material in preparation for JavaScript 1

This is neither a comprehensive nor an ordered list - just some of the concepts we will cover in the JavaScript 1 course.

### ES6

### More on variables

- Using const and let instead of var
- The modulus operator `%`

### More on functions

A good introductory video (now added to lesson 4) on functions:
https://www.youtube.com/watch?v=AY6X5jZZ_JE

- callbacks (passing functions in to other functions)
- setTimeout (waiting a certain amount of milliseconds before executing a function)
- setInterval (executing the same function at an interval set in milliseconds)
- fat arrow functions


### Array methods

#### filter method

The `filter` method creates a filtered array from an existing array. We will use it to filter results on a page when typing in a form's input element.

https://alligator.io/js/filter-array-method/

https://www.w3schools.com/jsref/jsref_filter.asp


### DOM selection 

DOM stands for `D`ocument `O`bject `M`odel.

It is an interface, an API, provided by browsers to interact with and manipulate web pages.

Some of these interactions and manipulations include selecting an HTML element (say for example, an `h1` tag) and changing its content.

A lot of tutorials will use `getElementById` to select an HTML element by its id attribute. This is perfectly valid. We, however, will concentrate on using the newer:

- `querySelector` (to select one element, such as a single `h1` element on a page)
- `querySelectorAll` (to select many elements, such as all the `li` tags in a `ul` element)


### DOM element creation

- createElement
- innerHTML


### Event Listeners

- click
- submit
- hover

### Retrieving variables from the querystring

The querystring is the part of a URL after the `?`.

If you do a google search and look at the URL, you will see it contains a lot of variables and values after the `?`.


### fetch

Fetch is built in to the browser version of the JavaScript engine. It is used to make API calls - to fetch data from servers, and to send data to servers.

It uses something called `promises`. Promises use `asynchronous` code which is going to look a little weird in the beginning.


### Form validation using regex and native HTML5 validation

Regex is - basically - used to check if a string value matches a pattern. It can be used for things like checking if a user entered an email address in the correct format. We are going to use regex to validate form inputs, but we won't go into too much detail on it.

HTML form inputs also have built-in ways to do this kind of validation.


### localStorage

localStorage provides a way to store variables in the browser and then retrieve them.

So we can save a variable on one page, go to another page, and get that same variable on the other page.

https://blog.logrocket.com/the-complete-guide-to-using-localstorage-in-javascript-apps-ba44edb53a36/


### CSS

We will provide the CSS you use in JavaScript 1 as we concentrate on JavaScript.

When we make API calls and are waiting for them to send the data back, we will display loaders coded similar to this:

https://www.w3schools.com/howto/howto_css_loader.asp

We will layout the results of the API calls use flexbox. If you haven't covered it very much until now, here is a good intro link and a more in-depth link.

