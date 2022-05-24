# Exercise 3

## Exercise 3.2

In the CSS tab of Self-Service Design, you can add the following styling to make the menu always visible:

```css
body:not(.global-nav-is-open) .global-navigation {
  display: block;
}
```

## Exercise 3.3

When clicking on the hamburger icon using the Inspector tool, you will see it is part of a `button` element. Highlight this element in the Elements tab, and look at the Styles tab. Press the `+` icon in the top right and add the property `display: none`.

Now, in the CSS tab of Self-Service Design, you can copy-paste this code and use it in there.

```css
button.widget-hamburger-menu.hamburger-menu-toggler.header-button.nav-bar-button.no-tap-highlight.js-show-global-nav {
  display: none;
}
```

However, this will also hide it on mobile, which is not what we wanted. We only want it to be hidden on medium and larger screens. 
Using Bootstrap's documentation, we can do this as followed:

```css
@media (min-width: 768px) {
  button.widget-hamburger-menu.hamburger-menu-toggler.header-button.nav-bar-button.no-tap-highlight.js-show-global-nav {
    display: none;
  }
}
```

## Exercise 3.4

In the HTML in the Elements tab, we can find the following element `<div class="page-container">`. Clicking on it will reveal it has a `max-width: 960px` in the Styles tab.

If we select the menu item with the inspector tool, we can see in the Styles tab that it has a `max-width: 14em`. If you press the Computed tab and scroll down, you can see the `max-width` value in pixels (`210px` in this case).

With this knowledge, we know that the main content area is `960px` - `210px` = `750px` wide. So all we have to do is change the `page-container` max-width and increase it by `210px`. This will allow the main content area's width to scale up to `960px`, because the navigation width stays the same.

```css
.page-container {
  max-width: 1170px;
}
```

## Exercise 3.5

If we hover over the header element, we will notice it has a child element called `global-header-inner-container` in the Elements tab. Select this element, and you will see it has a `max-width: 960px` value in the Styles tab. We have to change this to our new width value of `1170px`.

```css
.global-header-outer-container .global-header-inner-container {
  max-width: 1170px;
}
```

However, you will notice it still looks off... Inspect the `div` element below it with the class `global-header`, and you will notice this element also has a set `width`. So we also have to change this value.

```css
.global-header-outer-container .global-header-inner-container .global-header {
  width: 1170px;
}
```

**Note:** Because `.global-header` is a child element of `.global-header-inner-container`, we could use a nifty trick called nested CSS to combine the two previous code blocks and save us from re-writing the same CSS elements:

```css
.global-header-outer-container .global-header-inner-container {
  max-width: 1170px;
  
  .global-header {
    width: 1170px;
  }
}
```
