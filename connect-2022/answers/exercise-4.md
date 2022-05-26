
# Answers for Exercise 4

## Exercise 4.1

By using `position: absolute`, you can achieve the desired effect.

```css
.global-navigation {
  border: 1px solid #999;
  position: absolute;
}
```

## Exercise 4.2

If you inspect the `global-navigation` class in the Styles tab, you will see it has a `min-height: 100%` property. That means the menu will always stretch out to fit the height of the screen. We can change this to have the element be the same height as its contents by using the `auto` value.

```css
.global-navigation {
  border: 1px solid #999;
  position: absolute;
  min-height: auto;
}
```

## Exercise 4.3

By having used `position: absolute` on an element, we can also specify its position by usage of the `left`, `right`, `top` and `bottom` properties. 
For example:

```css
.global-navigation {
  border: 1px solid #999;
  position: absolute;
  min-height: auto;
  top: -10px;
  left: 15px;
}
```

## Exercise 4.4

If we inspect the `<div id='itrp-backdrop'>` element on larger screens, you will see that it has the property `display: none`. On mobile and small screens, when the menu is opened, it will change to `display: block`. 

Do you remember how in one of the early exercises, we figured out that when the hamburger menu is open, a class `global-nav-is-open` is added to the `body` element of the page? We can use this to achieve the desired effect!

```css
.global-nav-is-open #itrp-backdrop {
  display: block;
}
```

## Exercise 4.5

```css
.global-nav-is-open {
  box-shadow: 0 5px 10px 5px rgba(0, 0, 0, 0.3);
}
```
