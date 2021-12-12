---
date: 2021-10-22
title: Making POST requests from Drummer
tags: tech
---

That build hook URL for Netlify requires a POST request. But Drummer lets you run a script from the Iconbar. Here's mine.

```js
const xhr = new XMLHttpRequest();
const hookUrl = 'https://api.netlify.com/build_hooks/XXX'; // XXX is given to you by Netlify
xhr.open('POST', hookUrl, true);
xhr.setRequestHeader('Content-Type', 'application/json');
xhr.send(JSON.stringify({}));
```
