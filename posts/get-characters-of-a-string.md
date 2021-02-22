---
title: Get characters of a string
category: tip
tags:
  - posts
layout: layouts/post.njk
---

Use ES6 destructing to get the first and the remaining characters of a string:

```js
const [first, ...rest] = 'Hello';
// first = 'H'
// rest = ['e', 'l', 'l', 'o'] 
```

We can use it to [capitalize](https://1loc.dev/#capitalize-a-string) or [decapitalize](https://1loc.dev/#decapitalize-a-string) a string:

```js
capitalize = ([first, ...rest]) => (
  `${first.toUpperCase()}${rest.join('')}`
);

decapitalize = ([first, ...rest]) => (
  `${first.toLowerCase()}${rest.join('')}`
);

capitalize('hello world');  // 'Hello world'
```