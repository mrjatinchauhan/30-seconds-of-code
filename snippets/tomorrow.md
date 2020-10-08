---
title: tomorrow
tags: date,intermediate
---

Results in a string representation of tomorrow's date.

- Use `new Date()` to get the current date, increment by one using `Date.getDate()` and set the value to the result using `Date.setDate()`.
- Use `Date.prototype.toISOString()` to return a string in `yyyy-mm-dd` format.

```js
const tomorrow = () => {
  let d = new Date();
  d.setDate(d.getDate() + 1);
  return d.toISOString().split('T')[0];
};
```

```js
tomorrow(); // 2018-10-19 (if current date is 2018-10-18)
```
