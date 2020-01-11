# Extra material in preparation for JavaScript 1

### ES6

### More on variables

- Using const and let instead of var
- Modulus operator

### More on functions

- callbacks (passing functions in to other functions)
- setTimeout
- setInterval
- fat arrow functions


### Array methods

- filter
- map


### DOM selection 

- querySelector
- querySelectorAll

### Event Listeners

- click
- submit
- hover

### Retrieving variables from the querystring

The querystring is the part in a URL after the `?`.

If you do a google search and look at the URL, you will see it contains a lot of variables and values after the `?`.


### fetch

Fetch is built in to the browser version of the JavaScript engine. It is used to make API calls - to fetch data from servers, and to send data to servers.

It uses something called `promises`. Promises use `asynchronous` code which is going to look a little weird in the beginning.


### Form validation using regex and native HTML5 validation

Regex is, basically, used to check if a string value matches a pattern. It can be used for things like checking if a user entered an email address in the correct format. We are going to use regex to validate form inputs, but we won't go into too much detail on it.

HTML form inputs have built-in ways to do this kind of validation too.

### localStorage

localStorage provides a way to store variables in the browser and then retrieve them.

So we can save a variable on one page, go to another page, and get that same variable on the other page.

https://blog.logrocket.com/the-complete-guide-to-using-localstorage-in-javascript-apps-ba44edb53a36/


### CSS

We will provide the CSS you use in JavaScript 1 as we concentrate on JavaScript.

When we make API calls and are waiting for them to send the data back, we will display loaders coded similar to this:

https://www.w3schools.com/howto/howto_css_loader.asp

We will layout the results of the API calls use flexbox. If you haven't covered it very much until now, here is a good intro link and a more in-depth link.