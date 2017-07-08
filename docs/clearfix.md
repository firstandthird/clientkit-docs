# Clearfix

## Variables

None

## Mixins

### clearfix

#### Parameters

None

#### Usage

```postcss
.clearfix {
  @mixin clearfix;
}
```

#### Output

```css
.clearfix {
  &::after {
    content: '';
    display: table;
    clear: both;
  }
}
```

## Helpers

```scss
.clearfix
```

## Example

```html
<div class="clearfix">
  <div class="pull-left">...</div>
  <div class="pull-left">...</div>
</div>
<p>Some text below</p>
```
