# Pass arguments as an object

- it's clear what these arguments mean
- the order doesn't matter

```js
const createBook = ({ title, author, publicationDate }) => {
    console.log(`${title} is written by ${author} and published at ${publicationDate}`)
}

createBook({
    title: 'Pass arguments as an object',
    author: 'jnyo',
    publicationDate: '2021-02-14'
});
```

- it's unclear what these arguments mean
- the order is important
  
```js
const createBook = (title, author, publicationDate) => {
    console.log(`${title} is written by ${author} and published at ${publicationDate}`)
}

creatBook('Pass arguments as an object', 'jnyo', '2021-02-14');
```
