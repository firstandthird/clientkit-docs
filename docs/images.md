# Images

## Variables

None

## Mixins

### bg-image $url

#### Parameters

* `$url` (optional) - String; path to the background image

#### Usage

```postcss
.bg-image {
  @mixin bg-image /path/to/file;
}
```

#### Output

```css
.bg-image {
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  background-image: /path/to/file;
}
```

## Helpers

```css
.bg-image
```

## Example
```html
<div class="bg-image"><div>
```
