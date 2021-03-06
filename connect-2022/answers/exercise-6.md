
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

## Exercise 6.2

The `global-header` element has flex attributes. We can change the `flex-direction` attribute to value `row-reverse` so that it literally reverses the contents of the element.

```
.global-header-outer-container .global-header-inner-container .global-header {
  flex-direction: row-reverse;
}
```

Our next goal is to make sure the avatar is on the left side. We can use the `order` attribute for this. You could give all elements an order, as such:

```
.widget-user-menu {
  order: 1;
}

.global_search_link {
  order: 2;
}

.widget-time-spent-today {
  order: 3;
}
```

But a nifty trick you could use if you only want to give one element an order, is by using negative value of `-1`:

```
.widget-user-menu {
  order: -1;
}
```

To make sure the menu that opens when you click the avatar, we have to set the `right` value of the menu to auto (instead of 4px):

```
.widget-user-menu .gmenu {
  right: auto;
}
```

Finally, the exercise instructed us to put the search and time entry icons on the right side. We can use the [flex-basis](https://developer.mozilla.org/en-US/docs/Web/CSS/flex-basis) attribute for this. Try experimenting with values to achieve the desired effect (you can use percentages). Remember to put a `width: 100%` on the `right` class, too!

```
.right {
  width: 100%;
}

.widget-user-menu {
  order: -1;
  flex-basis: 90%;
}
```

## Exercise 6.3

The widget `{{my_inbox_count}}` returns the number of items you have in your inbox. We can use this in a class value on an element. For example:

```
<div class="my-inbox">
  <h1 class="inbox-count-{{my_inbox_count}}">My inbox</h1>
  {{my_inbox}}
</div>
```

If there are no items in the inbox, the class will render as `inbox-count-0`. We can use this class to hide the data! In Homepage CSS:

```
.inbox-count-0 {
  display: none;
}
```

## Exercise 6.4

As mentioned in the hint, we can use a hidden checkbox to get a similar effect as the `<details>` tag. In Homepage HTML:

```
<label class="inbox-count-{{my_inbox_count}}">
  My inbox
  <input class="hidden-checkbox" name="inbox-checkbox" value="false" type="checkbox">

  {{my_inbox}}
</label>
```

Note that a checkbox always needs a `<label>`. This makes it so that the text in the label element can be used to check/uncheck the checkbox and thus show our content. Then, in Homepage CSS:


```
[class^="inbox-count"] {
  width: 100%;
}

.hidden-checkbox {
  display: none;
}

.hidden-checkbox:checked ~ .widget-my-inbox {
  display: block;
}
```

Note that `[class^="inbox-count"]` has been added here. This is a selector that will work for all classes *containing* the words `inbox-count`, so the style will apply no matter how many inbox items there are. This is because the default label element has styling that does not make the content full width.
