# Exercise 3: Sidebar menu

First, revert the Globalnet Design back to the default design.
Go to https://globalnet.4me-demo.com/account/self_service_design,
remove all content from each tab, and press Save.

Now take another look at the default design by going to https://globalnet.4me-demo.com/self-service.
Notice that there is a hamburger menu icon in the upper left corner.
When you press it, a sidebar menu appears.

Click on "My Inbox". Notice that the page refreshes, but the sidebar menu remains visible.
Press the hamburger icon again to hide the sidebar menu again.

On a mobile device, the sidebar menu slides in from the left on top of the content.

### Exercise 3.1

Give this a try using the developer tools. Next to the element inspector,
there's the icon for the "toggle device toolbar". When you click it,
you can simulate various mobile devices.

Next, from the sidebar menu, go to My Inbox and click on the request that's in there.
Set the device toolbar to "responsive" and use the resize handles to smoothly adjust the width of the window.  

Now switch *off* the device toolbar.
With the Element tab of the developer tools open, click a few times on the hamburger icon
to open and close the menu. What happens in the element tab?

<details>
  <summary>Click here for the answer.</summary>
  A class will be added and removed to the `body` element based on whether or not you have the menu open. If the menu is open, the element will have the class `global-nav-is-open`
</details>

---

What happens when you press the hamburger icon is done by a tiny bit of Javascript included by 4me.
This is enough to support many scenarios via pure CSS, including a dropdown menu or a menu that is always visible.

In this exercise, we'll make a menu that is always visible, at least on large screens.
On small screens, we will keep the current behavior.

### Exercise 3.2

On https://globalnet.4me-demo.com/self-service,
use the element inspector to find the menu - that is, the HTML element that is shown / hidden
when you click on the hamburger icon.
Which CSS property is responsible for showing or hiding the menu?

<details>
  <summary>Click here for the answer.</summary>
  The `display` property is used to display or hide the menu.
</details>

Toggle the appropriate property, so that the menu is always shown.

Unfortunately, changes made in the developer tools are not saved in the Self Service Design.
When you refresh the browser, it reverts back and your changes are gone...

Can you make the appropriate change in https://globalnet.4me-demo.com/account/self_service_design,
so that the menu is always shown?

> [You can find the answer here.](answers/exercise-3.md#exercise-32)

### Exercise 3.3

The hamburger icon no longer has any visible effect now. We should always hide it.

Can you implement this? 

Note that this should have no effect on small screens: the hamburger icon should then still be visible.
Refer to [Bootstrap's documentation on media queries](https://getbootstrap.com/docs/4.1/layout/overview/#responsive-breakpoints) to achieve this effect.

> [You can find the answer here.](answers/exercise-3.md#exercise-33)

# Up Next

Done with this exercise? [Continue to the Dropdown Menu exercise](4-dropdown-menu.md)

Or if these exercises were too easy for you or you would like to learn more about this specific subject, feel free to try out the optional exercises below first!


## Optional exercises 

If you have time left, give the exercises below a try.

### Exercise 3.4

With a sidebar menu that's always visible,
the main content area (the area to the right of the menu) is a bit narrow on large screens.

Can you make it wider, let's say 960px wide?

> [You can find the answer here.](answers/exercise-3.md#exercise-34)

### Exercise 3.5

Once you make the main content area wider, the elements in the header no longer line up with the rest of the page. Can you fix that?

> [You can find the answer here.](answers/exercise-3.md#exercise-35)

### Exercise 3.6

On a small screen, the menu slides in from the left. Can you make it slide in from the right instead?
Remember [media queries](https://getbootstrap.com/docs/4.1/layout/overview/#responsive-breakpoints)!

> [You can find the answer here.](answers/exercise-3.md#exercise-36)
