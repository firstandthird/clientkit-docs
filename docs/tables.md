# Tables

## Variables

* `var(--table-cell-padding)`: **10px**
* `var(--table-sm-cell-padding)`: **5px**
* `var(--table-bg)`: **transparent**
* `var(--table-bg-accent)`: **#f9f9f9**
* `var(--table-bg-hover)`: **#f5f5f5**
* `var(--table-bg-active)`: **#f5f5f5**
* `var(--table-border-width)`: **1px**
* `var(--table-border-color)`: **#eceeef**

## Mixins

None

## Helpers

```scss
.table
.table-sm
.table-bordered
.table-striped
.table-hover
.table-responsive
```

## Example

```html
<table class="table">
  <thead>
    <tr>
      <th>Header 1</th>
      <th>Header 2</th>
      <th>Header 3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Item 1</td>
      <td>Item 2</td>
      <td>Item 3</td>
    </tr>
  </tbody>
</table>
```

### Condensed with half padding

```html
<table class="table table-sm">
  <thead>
    <tr>
      <th>Header 1</th>
      <th>Header 2</th>
      <th>Header 3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Item 1</td>
      <td>Item 2</td>
      <td>Item 3</td>
    </tr>
  </tbody>
</table>
```

### Bordered version

Add borders all around the table and between all the columns.

```html
<table class="table table-bordered">
  <thead>
    <tr>
      <th>Header 1</th>
      <th>Header 2</th>
      <th>Header 3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Item 1</td>
      <td>Item 2</td>
      <td>Item 3</td>
    </tr>
  </tbody>
</table>
```

### Zebra-striping

Default zebra-stripe styles (alternating gray and transparent backgrounds)

```html
<table class="table table-striped">
  <thead>
    <tr>
      <th>Header 1</th>
      <th>Header 2</th>
      <th>Header 3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Item 1</td>
      <td>Item 2</td>
      <td>Item 3</td>
    </tr>
  </tbody>
</table>
```

### Hover effect

Placed here since it has to come after the potential zebra striping

```html
<table class="table table-hover">
  <thead>
    <tr>
      <th>Header 1</th>
      <th>Header 2</th>
      <th>Header 3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Item 1</td>
      <td>Item 2</td>
      <td>Item 3</td>
    </tr>
  </tbody>
</table>
```

### Responsive tables

Wrap your tables in `.table-responsive` and we'll make them mobile friendly
by enabling horizontal scrolling. Only applies <768px. Everything above that
will display normally.

`min-height: 0.01%` is a workaround for IE9 bug (see https://github.com/twbs/bootstrap/issues/14837)

```html
<div class-"table-responsive">
<table class="table">
  <thead>
    <tr>
      <th>Header 1</th>
      <th>Header 2</th>
      <th>Header 3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Item 1</td>
      <td>Item 2</td>
      <td>Item 3</td>
    </tr>
  </tbody>
</table>
</div>
```
