
# Custom CSS Selection Styling

Custom Selection Styling is fun! π

The ::selection CSS pseudo-element allows you to apply styles to your text when itβs highlighted. It's a great way to add some pizzaz to your site π


```css
p::selection {
  background: DeepPink;
  color: white;
}
```

For Firefox, you will need to use ::-moz-selection π

```css
p::-moz-selection {
  background: DeepPink;
  color: white;
}
```

## Resources

- https://css-tricks.com/almanac/selectors/s/selection/
