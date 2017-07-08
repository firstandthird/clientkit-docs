# Messages

## Variables

* `var(--color-body)`: **#333** - the default color of text inherits from the body
* `var(--color-message-error)`: **#f2dede** - for error messages
* `var(--color-message-info)`: **#f0f0f0** - for info messages
* `var(--color-message-success)`: **#dff0d8** - for success messages
* `var(--message-border-radius)`: **2px** - default border radius for all messages

## Mixins

### message $color

#### Parameters

* `$color` **(required)** - Color; used to create the background and border

#### Usage

```postcss
.message-blue {
  @mixin message blue;
}
```

#### Output

```postcss
.message-blue {
  border: 1px solid color(blue lightness(-10%));
  border-radius: 2px;
  padding: 5px 10px;
  background-color: blue;
  color: #333;
}
```

## Helpers

```postcss
.message-error
.message-info
.message-sucess
```

## Example

```html
<div class="message-info">This is an info message</div>
<div class="message-success">This is an success message</div>
<div class="message-error">This is an error message</div>
<div class="message-error">
  This is multiple error messages
  <ul>
    <li>Error message 1</li>
    <li>Error message 2</li>
  </ul>
</div>

```
