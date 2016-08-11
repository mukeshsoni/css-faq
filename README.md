# css-faq
Frequently asked questions in css

### What is `border-box` and why is it so popular?
CSS has a concept of box model for every element on the screen. What that means is that every element lives inside a rectangular box and treating everything like a rectangular box makes it easy to lay them out on a page. The box consists of margins, borders, padding and the content. The problem with current box model is that increasing the padding or adding a border to elements increases the size of the box. Giving a width to the element doesn't matter - it's always the content width + padding + border size. This leads to unpredictability on where other elements besides an element will be.

That lead to the introduction of `box-sizing` property. When `box-sizing` is set to `border-box` for an element, adding padding and border does not affect the width of the element any more. This makes life saner for css writers. That is why the base.css file for most project now has this rule - 

```
*, *:before, *:after {
    -moz-box-sizing: border-box;
    -webkit-box-sizing: border-box;
    box-sizing: border-box;
}
```

which makes all elements on the page to have `box-sizing` of `border-box`. I don't know why this is not the default in all browsers though.
