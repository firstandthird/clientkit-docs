# Utilities

A set of utilities for general purposes.

## Variables

None

## Mixins

### hide $bp, $display

#### Parameters

* `$bp` (optional) - Array of Objects; an array of breakpoint objects; see the grid docs for more information
* `$display` (optional) - Display property; see [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/display) for a list of possible values

#### Usage

```postcss
@mixin hide;
```

#### Output

```scss
.hide-sm
.hide-md
.hide-lg
.hide-xl
.show-sm
.show-md
.show-lg
.show-xl
```

## Helpers

```scss
.pull-left
.pull-right
.display-block
.display-inline
.display-inline-block
.hide
```

## Example

```html
<div class="pull-left"></div>
<div class="pull-right"></div>
<div class="display-block"></div>
<div class="display-inline"></div>
<div class="display-inline-block"></div>
<div class="hide"></div>
```
