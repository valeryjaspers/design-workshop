
# Answers for Exercise 4

## Exercise 6.1

If you inspect the search element, you will find that the `input` element has the class `search-q`. By using the pseudo-class `:focus` and the sibling combinator, 
we can target the `.search-btn` class of the icon, as it is a 'sibling' of the `input` element in the `search-fields` div element.

```css
.search-btn {
  display: none;
}

.search-q:focus ~ .search-btn {
  display: block;
}
```
