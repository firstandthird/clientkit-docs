# Triangle

## Variables

None

## Mixins

### triangle size, direction

#### Parameters

* `$size` (optional) - CSS Unit; defaults to 4px
* `$direction` (optional) - up | right | down | left; defaults to 'down'

#### Usage

```postcss
.triangle-down {
  @mixin triangle 5px, down
}
```

#### Output

```scss
.triangle-down {
  display: inline-block;
  width: 0;
  height: 0;
  border-top 5px solid;
  border-right 5px transparent;
  border-left 5px transparent;
  vertical-align: middle;
  content: "";
}
```

## Helpers

Default size of 10px

```scss
.triangle-up
.triangle-right
.triangle-down
.triangle-left
```

## Example

```html
<b class="triangle-up"></b>
<b class="triangle-right"></b>
<b class="triangle-down"></b>
<b class="triangle-left"></b>
```
