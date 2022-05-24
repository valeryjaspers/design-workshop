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
