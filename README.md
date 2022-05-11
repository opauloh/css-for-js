## CSS For JS Developers

Notes from the [CSS For JS dev](https://css-for-js.dev) course

## Terminology

Terminologies are important for building a solid mental mode of CSS.

- [Docs Reference](https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps/Getting_started)

### Property

Properties in CSS are the attributes you can specify values for, like `color` and `font-size`. In this case is the margin.

```css
p {
  margin: 32px;
}
```

### Selector

A selector is a descriptor that lets you target specific elements on the page. In this case, we're selecting all nodes with the “apple” class.

```css
.apple {
  background-color: red;
  border-radius: 50%;
}
```

### Declaration

A declaration is a combination of a property and a value. In this case, the first declaration has a property of "padding", and a value of "32px".

```css
.code-snippet {
  padding: 32px;
  white-space: pre-wrap;
}
```

### Rule

A rule, also known as a style, is a collection of declarations, targeting one or more selectors. A stylesheet is made up of multiple rules. In this case, all the below code is a rule.

```css
p {
  color: red;
  font-family: sans-serif;
}
```

### Unit

Some values have units, like px, %, or em. In this case, our padding-top has a value of 24px, which is measured in the "px" unit.

```css
p {
  padding-top: 24px;
}
```

## Media Queries

Media queries use the @media syntax. You can kinda think of it as an if statement in JavaScript:

```css
/* CSS */
@media (condition) {
  /* Some CSS that'll run if the condition is met. */
}
```

It's common to use media queries to have alternative interfaces depending on the screen size.

```css
.large-screens {
  display: none;
}

@media (min-width: 300px) {
  .large-screens {
    display: block;
  }
  .small-screens {
    display: none;
  }
}
```

```html
<div class="large-screens">I only show up on large screens.</div>
<div class="small-screens">Meanwhile, you'll only see me on small ones.</div>
```

Inside the parentheses, we typically use either `max-width` to add styles on small screens, or min-width to add styles on larger ones.

The syntax looks quite a lot like the declaration syntax, especially since `max-width`: 1023px is a valid CSS declaration! Unfortunately, this is misleading; In the context of a media query, `max-width` is a “media feature”, not a CSS property. They just happen to share the same name.
