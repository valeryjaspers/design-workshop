# Advanced exercises

The exercises below are for advanced designers.
You will need a lot of HTML and CSS knowledge to be able to solve them.

However, even if you are unable to solve them just now, 
it may be worth reading through them to get inspiration for your own design.

Before you get started, 
go to https://globalnet.4me-demo.com/account/self_service_design and once again remove all content from all the tabs.   

## 6.1 Search icon

The search bar on the homepage contains a search icon on the right (a small magnifying glass).

Can you adjust it, so that the icon is visible *only* when the search input field is focused - that is, when the user puts the cursor in the search field?

<details>
  <summary>Click here for a hint</summary>
  Use pseudo-classes and the sibling combinator: https://developer.mozilla.org/en-US/docs/Web/CSS/General_sibling_combinator
</details>

> [You can find the answer here.](answers/exercise-6.md#exercise-61)

## 6.2 Header icons

The hamburger icon in the header is on the left, and the other header icons are on the right.
Can you swap them?

It should work on all pages of Self Service, not just the homepage.

Once you have done that, can you put the person avatar (which is still right of the search and time entry icons) on the left?

The dropdown menu that appears when you click on the person avatar should appear in the correct direction (down and to the right of the person avatar).

![](assets/exercise-6/user-menu-left.png)

Can you put the search and time entry icons on the right, as in the image below?

![](assets/exercise-6/icons-right.png)

<details>
  <summary>Click here for a hint</summary>
  You can solve this using various properties related to CSS flexbox layouts.
  Have a look at https://css-tricks.com/snippets/css/a-guide-to-flexbox/.
</details>

> [You can find the answer here.](answers/exercise-6.md#exercise-62)

## 6.3 My inbox widget with header

You can add an inbox to the homepage by adding the following HTML to the Homepage HTML field of the Self Service Design:

```
<div class="my-inbox">
  <h1>My inbox</h1>
  {{my_inbox}}
</div>
```

However, when the user's inbox is empty, the header "My inbox" is still displayed.

Can you adjust it, so that the header is visible *only* when there is something in the inbox?


<details>
  <summary>Click here for a hint</summary>
  The widget `{{my_inbox_count}}` might come in handy.
</details>

> [You can find the answer here.](answers/exercise-6.md#exercise-63)

## 6.4 Summary and details (hard)

This one's a bit tricky..
Suppose you want to add a number of widgets to the homepage, that are by default *collapsed*.
That is, initially you see only the header - "My inbox", "My requests", and so on.
When you click on the header, the widget expands and shows the list of items.

There is a useful HTML element that you can use for this, the [`<details>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/details) element:

```
<details class="my-inbox">
  <summary>My inbox</summary>
  {{my_inbox}}
</details>
```

Unfortunately, however, this is not supported in Internet Explorer.

Can you think of a way to implement this functionality in such a way, that it also works in Internet Explorer?

<details>
  <summary>Click here for a hint</summary>
  Use a hidden checkbox and the sibling combinator: https://developer.mozilla.org/en-US/docs/Web/CSS/General_sibling_combinator
</details>

> [You can find the answer here.](answers/exercise-6.md#exercise-64)

# End

You have reached the absolute end of this Connect's Self-Service Design workshop. Well done! If you *still* have time left, perhaps there is a self-service design you are really proud of and would like to show the group? Or maybe you have a question or idea that you would like to talk about?
