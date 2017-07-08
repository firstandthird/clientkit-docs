# Grid

## Variables

```yaml
grid-columns: 12
grid-gutters: 15px
```

### Breakpoints

```yaml
desktop-wide:
  max-width: 100vw
  min-width: 1440px
  content: 1440px
  col: xl
  default: '{{!core.mobileFirst}}'
  bleed: 1600px
desktop:
  max-width: 1439px
  min-width: 1024px
  content: 1024px
  col: lg
tablet:
  max-width: 1023px
  min-width: 768px
  content: 768px
  col: md
mobile:
  max-width: 767px
  min-width: 320px
  content: 100%
  col: sm
```

## Mixins

### container

#### Parameters

None

#### Usage

```scss
.container {
  @mixin container;
}
```

#### Output

```css
.container {
  box-sizing: border-box;
  width: 1400px;
  margin-right: auto;
  margin-left: auto;
  padding-right: 15px;
  padding-left: 15px;
}
```

### site-max

#### Parameters

None

#### Usage

```scss
.body {
  @mixin site-max;
}
```

#### Output

```css
.container {
  max-width: 1600px;
  margin-right: auto;
  margin-left: auto;
}
```

### grid

#### Parameters

None

#### Usage

```scss
@mixin grid;
```

### flex-grid

#### Parameters

None

#### Usage

```scss
@mixin flex-grid;
```

## Helpers

```css
.container
.row
.flex
```

## Fluid Grid

### Quick Start

```html
<div class="container">
  <div class="row">
    <div class="col-4">1/3 column</div>
    <div class="col-4">1/3 column</div>
    <div class="col-4">1/3 column</div>
  </div>
</div>
```

### Options

| | Default | Small | Medium | Large | Extra large |
| --- | --- | --- | --- | --- | --- |
| Container width | None (auto) | 320px - 767px  | 768px - 1023px | 1024px - 1439px | 1440px - 100vw |
| Class prefix | `.col-` | `.col-sm-` | `.col-md-` | `.col-lg-` | `.col-xl-` |
| # of columns | 12 | 12 | 12 | 12 | 12 |
| Gutter width | 15px on each side | 15px on each side | 15px on each side | 15px on each side | 15px on each side |
| Nestable | Yes | Yes | Yes | Yes | Yes |
| Offsets | Yes | Yes | Yes | Yes | Yes |
| Column ordering | Yes | Yes | Yes | Yes | Yes |

## Flex Grid

### Quick Start

```html
<div class="container">
  <div class="flex-row">
    <div class="flex-4">1/3 column</div>
    <div class="flex-4">1/3 column</div>
    <div class="flex-4">1/3 column</div>
  </div>
</div>
```

### Auto Sizing

Add as many to this example and they will size accordingly

```html
<div class="container">
  <div class="flex-row">
    <div class="flex-grow flex-no-shrink">1/3 column</div>
    <div class="flex-grow flex-no-shrink">1/3 column</div>
    <div class="flex-grow flex-no-shrink">1/3 column</div>
  </div>
</div>
```

### Options

| | Default | Small | Medium | Large | Extra large |
| --- | --- | --- | --- | --- | --- |
| Container width | None (auto) | 320px - 767px  | 768px - 1023px | 1024px - 1439px | 1440px - 100vw |
| Class prefix | `.flex-` | `.flex-sm-` | `.flex-md-` | `.flex-lg-` | `.flex-xl-` |
| # of columns | 12 | 12 | 12 | 12 | 12 |
| Gutter width | 15px on each side | 15px on each side | 15px on each side | 15px on each side | 15px on each side |
| Nestable | Yes | Yes | Yes | Yes | Yes |
| Offsets | Yes | Yes | Yes | Yes | Yes |
| Column ordering | Yes | Yes | Yes | Yes | Yes |
