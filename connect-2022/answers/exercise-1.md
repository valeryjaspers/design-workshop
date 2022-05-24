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
