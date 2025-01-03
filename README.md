# Unexpected Layout Behavior with CSS Floats

This repository demonstrates an uncommon bug related to using CSS floats and how to resolve it.

The bug involves unexpected layout issues when using the `float` property, particularly when the total width of floating elements exceeds the container width. Some browsers handle this differently, resulting in inconsistencies.

## Bug Description

The main issue occurs with the following CSS:

```css
div {
  width: 50%;
  float: left;
}
```

This simple code, when applied to multiple elements within a container, can lead to unexpected wrapping or spacing behaviors in certain browsers, especially if the sum of widths exceeds 100%.

## Solution

The most robust solution is to avoid using floats entirely, opting instead for more modern layout techniques like `flexbox` or `grid`. However, if floats are absolutely required due to legacy code or other constraints, you can mitigate the issue by ensuring the content's width is correctly managed within the parent container.  You may also need to use clearfix hacks to clear the float and prevent the parent element from collapsing.