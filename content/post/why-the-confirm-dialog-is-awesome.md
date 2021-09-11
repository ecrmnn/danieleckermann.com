+++
date = 2021-09-09T00:00:00Z
description = "The perfect confirmation dialog is already built into your browser"
title = "Why the confirm dialog is awesome"

+++
You've probably encountered this hundreds of times. You’re building an app and you want to prompt your users before performing a harmful or an non-undoable action.

Maybe you’re building an SPA with Vue or React - or maybe vanilla JavaScript. You search endlessly trying to find the right npm package. They all seem too complex with too much overhead. You want something simple, that won’t stop working when you some day in the future update your framework.

I’ve been there so many times, searching for the perfect package. What I didn’t realize was that it was built into my browser all along.
If you reach for the native `confirm` dialog you can forget about dependencies, browser support and overriding styles. 
I'm not saying it's the best option for everything, but when you need something simple it's the right tool for the job.

## Why it's awesome
- Browser support / Built in
- Does not require bundling
- No added dependencies
- No styling required

## Examples
Here’s an example of `confirm` dialog using onclick on a plain link.
```html
<a href="https://www.example.com" target="_blank" onclick="return confirm('Processed?')">Click me</a>
```

Here’s an example of using the `confirm` dialog in Vue 2. The action within the conditional will only be executed when the user clicks “OK”.
```js
methods: {
  removeItem(index) {
    if (window.confirm('Confirm deletion')) {
        this.items.splice(index, 1);
    }
  },
},
```

Finally here’s an example using `onsubmit` on a simple HTML form.
```html
<form action="..." onsubmit="return confirm('Proceed?');">
    <button type="submit">Submit</button>
</form>
```

If you liked this post you should [follow me](https://www.twitter.com/ecrmnn) on Twitter to receive updates about future posts.