# Carousels

## Variables

None

## Mixins

### row-carousel

#### Parameters

None

#### Usage

```postcss
.row-carousel {
  @mixin row-carousel;
}
```

#### Output

```scss
.row-carousel {
  width: 100%;
  height: 100%;
  overflow-y: hidden;
  overflow: auto;
  margin: 0;
  white-space: nowrap;
  -webkit-overflow-scrolling: touch;
  scroll-snap-type: mandatory;
  scroll-snap-destination: 0% 100%;
  scroll-snap-points-x: repeat(100%);

  & [class*="col-"] {
    display: inline-block;
    float: none;
    vertical-align: top;
    white-space: normal;
  }
}
```

## Helpers

```scss
.row-sm-carousel
.row-md-carousel
.row-lg-carousel
.row-xl-carousel
```

## Example

```html
<div class="row-sm-carousel"></div>
```
