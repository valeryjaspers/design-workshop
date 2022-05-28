
## What is Bootstrap?

`TODO: MOVE BOOTSTRAP INTRODUCTION TO PRESENTATION`

As explained during the workshop, 4me allows you to use Bootstrap to make it easier
to implement your design.

The idea of Bootstrap is that, rather than explicitly writing CSS code,
you add *classes* to your HTML elements to style them. Bootstrap has predefined
many of these classes, which are like small building blocks that you can combine
to build up a complex layout.

For example, `<button type="button">Delete</button>` is how you would write
a basic button in HTML. It gets the default browser style, which varies per browser. For example, in Chrome you get:

![](assets/exercise-1/bootstrap-button-1.png)

Bootstrap defines the `btn` class to change that into a more uniform style.
So `<button type="button" class="btn">Delete</button>` results in:

![](assets/exercise-1/bootstrap-button-2.png)

Now, to indicate that 'deleting' is a dangerous action, you can add the `btn-danger` class to it:
`<button type="button" class="btn btn-danger">Delete</button>`. The result:

![](assets/exercise-1/bootstrap-button-3.png)

Finally, to make the button a bit smaller, add `btn-sm`:
`<button type="button" class="btn btn-danger btn-sm">Delete</button>`. It looks like this:

![](assets/exercise-1/bootstrap-button-4.png)
