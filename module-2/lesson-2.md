
except that if the operands are not of the same type, JavaScript will convert them both to the same type and then compare them.
>
>This means that numbers in strings and actual number values can be compared.
>
>```js
>var isEqual = "3" == 3;
>// true
>```
>
>This can cause problems. Strings shouldn't be compared to numbers, they are different types. Using `===`, which does not perform any conversions, the above statement will return false:
>
>```js
>var isEqual = "3" === 3;
>// false
>```

>As a rule, don't use `==` or `!==`, always use `===` and `!==`.
>