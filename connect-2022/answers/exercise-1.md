# Answers for Exercise 1

## Exercise 1.1

By adding `row` and `col` classes to the right `div` elements, your code for the cards should end up looking as followed:

```html
<div class="row">
  <div class="col">
    <a class="card" href="/self-service/notifications">
      <div class="card-header">
        <div><i class="ii icon-notification"></i></div>
        <div>My Notifications</div>
      </div>
      <div class="card-body counter-{{my_notifications_count}}">
        <div>{{my_notifications_count}}</div>
      </div>
    </a>
  </div>
  <div class="col">
    <a class="card" href="/self-service/inbox">
      <div class="card-header">
        <div><i class="ii icon-inbox"></i></div>
        <div>My Inbox</div>
      </div>
      <div class="card-body counter-{{my_inbox_count}}">
        <div>{{my_inbox_count}}</div>
      </div>
    </a>
  </div>
  <div class="col">
    <a class="card" href="/self-service/requests">
      <div class="card-header">
        <div><i class="ii icon-request"></i></div>
        <div>My Requests</div>
      </div>
      <div class="card-body counter-{{my_open_requests_count}}">
        <div>{{my_open_requests_count}}</div>
      </div>
    </a>
  </div>
</div>
```

## Exercise 1.2

So if we remember Bootstrap uses 12 cells of equal width per row, and we want the Inbox card to be twice as wide as the other two cards, we make the Inbox card 6 cells wide and the other two cards 3 cells wide. Keep in mind that the end number always has to be 12 (6 + 3 + 3)!

```html
<div class="row">
  <div class="col-3">
    <a class="card" href="/self-service/notifications">
      <div class="card-header">
        <div><i class="ii icon-notification"></i></div>
        <div>My Notifications</div>
      </div>
      <div class="card-body counter-{{my_notifications_count}}">
        <div>{{my_notifications_count}}</div>
      </div>
    </a>
  </div>
  <div class="col-6">
    <a class="card" href="/self-service/inbox">
      <div class="card-header">
        <div><i class="ii icon-inbox"></i></div>
        <div>My Inbox</div>
      </div>
      <div class="card-body counter-{{my_inbox_count}}">
        <div>{{my_inbox_count}}</div>
      </div>
    </a>
  </div>
  <div class="col-3">
    <a class="card" href="/self-service/requests">
      <div class="card-header">
        <div><i class="ii icon-request"></i></div>
        <div>My Requests</div>
      </div>
      <div class="card-body counter-{{my_open_requests_count}}">
        <div>{{my_open_requests_count}}</div>
      </div>
    </a>
  </div>
</div>
```

## Exercise 1.3

Change the `col` width to `3` and add `justify-content-center` to the `row` as per the Bootstrap documentation.

```html
<div class="row justify-content-center">
  <div class="col-3">
    <a class="card" href="/self-service/notifications">
      <div class="card-header">
        <div><i class="ii icon-notification"></i></div>
        <div>My Notifications</div>
      </div>
      <div class="card-body counter-{{my_notifications_count}}">
        <div>{{my_notifications_count}}</div>
      </div>
    </a>
  </div>
  <div class="col-3">
    <a class="card" href="/self-service/inbox">
      <div class="card-header">
        <div><i class="ii icon-inbox"></i></div>
        <div>My Inbox</div>
      </div>
      <div class="card-body counter-{{my_inbox_count}}">
        <div>{{my_inbox_count}}</div>
      </div>
    </a>
  </div>
  <div class="col-3">
    <a class="card" href="/self-service/requests">
      <div class="card-header">
        <div><i class="ii icon-request"></i></div>
        <div>My Requests</div>
      </div>
      <div class="card-body counter-{{my_open_requests_count}}">
        <div>{{my_open_requests_count}}</div>
      </div>
    </a>
  </div>
</div>
```

## Exercise 1.4

Change the `col` width to `lg-3` so that it only applies to the larger and above breakpoints.

```html
<div class="row justify-content-center">
  <div class="col-lg-3">
    <a class="card" href="/self-service/notifications">
      <div class="card-header">
        <div><i class="ii icon-notification"></i></div>
        <div>My Notifications</div>
      </div>
      <div class="card-body counter-{{my_notifications_count}}">
        <div>{{my_notifications_count}}</div>
      </div>
    </a>
  </div>
  <div class="col-lg-3">
    <a class="card" href="/self-service/inbox">
      <div class="card-header">
        <div><i class="ii icon-inbox"></i></div>
        <div>My Inbox</div>
      </div>
      <div class="card-body counter-{{my_inbox_count}}">
        <div>{{my_inbox_count}}</div>
      </div>
    </a>
  </div>
  <div class="col-lg-3">
    <a class="card" href="/self-service/requests">
      <div class="card-header">
        <div><i class="ii icon-request"></i></div>
        <div>My Requests</div>
      </div>
      <div class="card-body counter-{{my_open_requests_count}}">
        <div>{{my_open_requests_count}}</div>
      </div>
    </a>
  </div>
</div>
```

## Exercise 1.5

Change the `col` width to `col-sm 4 lg-3`. This means that on smaller and medium screens, the `col` width will be set to `4`, whereas on larger and above it will be set to `3`. Do note that on the smallest screensizes (mobile, the `xs` breakpoint) the width will be set to `12` as we left that unspecified and it is the default width.

```html
<div class="row justify-content-center">
  <div class="col-sm-4 col-lg-3">
    <a class="card" href="/self-service/notifications">
      <div class="card-header">
        <div><i class="ii icon-notification"></i></div>
        <div>My Notifications</div>
      </div>
      <div class="card-body counter-{{my_notifications_count}}">
        <div>{{my_notifications_count}}</div>
      </div>
    </a>
  </div>
  <div class="col-sm-4 col-lg-3">
    <a class="card" href="/self-service/inbox">
      <div class="card-header">
        <div><i class="ii icon-inbox"></i></div>
        <div>My Inbox</div>
      </div>
      <div class="card-body counter-{{my_inbox_count}}">
        <div>{{my_inbox_count}}</div>
      </div>
    </a>
  </div>
  <div class="col-sm-4 col-lg-3">
    <a class="card" href="/self-service/requests">
      <div class="card-header">
        <div><i class="ii icon-request"></i></div>
        <div>My Requests</div>
      </div>
      <div class="card-body counter-{{my_open_requests_count}}">
        <div>{{my_open_requests_count}}</div>
      </div>
    </a>
  </div>
</div>
```

# Optional exercises

## Exercise 1.6

Add `text-center` to the `div` element with the `col` classes, such as:

```html
<div class="col-sm-4 col-lg-3 text-center">
  <a class="card" href="/self-service/notifications">
    <div class="card-header">
      <div><i class="ii icon-notification"></i></div>
      <div>My Notifications</div>
    </div>
    <div class="card-body counter-{{my_notifications_count}}">
      <div>{{my_notifications_count}}</div>
    </div>
  </a>
</div>
```

## Exercise 1.7

You can use the [Spacing utilities from the Bootstrap documentation](https://getbootstrap.com/docs/4.1/utilities/spacing/). For example, on the searchbar you can use `my-5`. This means add a margin value to both the top and bottom of the searchbar element. For the cards, you could use something like `mx-5`, where the `x` indicates left and right.

```html
<div class="row my-5">
  <div class="col">
    {{search placeholder="How can we help you?"}}
  </div>
</div>
```

## Exercise 1.8

The spacing utilities can be used on images as well, such as:

```html
<div class="row">
  <div class="col">
    <img class="mx-auto" src="https://learning.4me.com/images/globalnet-logo.png" alt="GlobalNet Logo">
  </div>
</div>
```

## Exercise 1.9

If you look at the [Bootstrap documentation for Images](https://getbootstrap.com/docs/4.1/content/images/#responsive-images), you see we can use class `img-fluid` to very easily make images responsive.

```html
<div class="row">
  <div class="col">
    <img class="img-fluid" src="https://learning.4me.com/images/globalnet-logo.png" alt="GlobalNet Logo">
  </div>
</div>
```

## Exercise 1.10

If we remember that a Bootstrap `row` is made of 12 `cols`, then on larger screens we can go for `col-4` (3x4), and on medium we can go for `col-6` (2x6). On lower breakpoints, we do not specify anything, as it will automatically use the full width and stack them vertically. To make sure we have some nice spacing inbetween the cards, we can add `my-3`.

```html
<div class="row justify-content-center">
  <div class="col-md-6 col-lg-4 my-3">
    <a class="card" href="/self-service/notifications">
      <div class="card-header">
        <div><i class="ii icon-notification"></i></div>
        <div>My Notifications</div>
      </div>
      <div class="card-body counter-{{my_notifications_count}}">
        <div>{{my_notifications_count}}</div>
      </div>
    </a>
  </div>
  <div class="col-md-6 col-lg-4 my-3">
    <a class="card" href="/self-service/inbox">
      <div class="card-header">
        <div><i class="ii icon-inbox"></i></div>
        <div>My Inbox</div>
      </div>
      <div class="card-body counter-{{my_inbox_count}}">
        <div>{{my_inbox_count}}</div>
      </div>
    </a>
  </div>
  <div class="col-md-6 col-lg-4 my-3">
    <a class="card" href="/self-service/requests">
      <div class="card-header">
        <div><i class="ii icon-request"></i></div>
        <div>My Requests</div>
      </div>
      <div class="card-body counter-{{my_open_requests_count}}">
        <div>{{my_open_requests_count}}</div>
      </div>
    </a>
  </div>
  <div class="col-md-6 col-lg-4 my-3">
    <a class="card" href="/self-service/notifications">
      <div class="card-header">
        <div><i class="ii icon-notification"></i></div>
        <div>My Notifications</div>
      </div>
      <div class="card-body counter-{{my_notifications_count}}">
        <div>{{my_notifications_count}}</div>
      </div>
    </a>
  </div>
  <div class="col-md-6 col-lg-4 my-3">
    <a class="card" href="/self-service/inbox">
      <div class="card-header">
        <div><i class="ii icon-inbox"></i></div>
        <div>My Inbox</div>
      </div>
      <div class="card-body counter-{{my_inbox_count}}">
        <div>{{my_inbox_count}}</div>
      </div>
    </a>
  </div>
  <div class="col-md-6 col-lg-4 my-3">
    <a class="card" href="/self-service/requests">
      <div class="card-header">
        <div><i class="ii icon-request"></i></div>
        <div>My Requests</div>
      </div>
      <div class="card-body counter-{{my_open_requests_count}}">
        <div>{{my_open_requests_count}}</div>
      </div>
    </a>
  </div>
</div>
```
