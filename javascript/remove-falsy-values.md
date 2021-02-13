# Remove falsy values

```js
const arr = [undefined, null, NaN, 0, "", false, 1, 'a', true]

let filterd = arr.filter(Boolean);
// [1, "a", true]


Boolean("");
// false
```

In JavaScript, following values are falsy

- `false`
- `0`
- `-0`
- `0n`, `-0n`
- `"" (empty string)`
- `null`
- `undefined`
- `NaN`
- `document.all`

references:

https://developer.mozilla.org/en-US/docs/Glossary/Falsy

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean