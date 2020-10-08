---
title: getSiblings
tags: browser,array,intermediate
---

Returns an array containing all the siblings of the given element.

- Use `Node.prototype.parentNode` and `Node.prototype.childNodes` to get a `NodeList` of all the elements contained in the element's parent.
- Use the spread operator (`...`) and `Array.prototype.filter()` to convert to an array and remove the given element from it.

```js
const getSiblings = el =>
  [...el.parentNode.childNodes].filter(node => node !== el);
```

```js
getSiblings(document.querySelector('head')); // ['body']
```
