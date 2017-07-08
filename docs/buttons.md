# Buttons

A set of buttons with sizes, colors, and states.

## Variables

* `var(--button-radius-default)`: **3px** - default button radius for all buttons
* `var(--color-button-primary-bg)`: **{{stylesheets.color.accent1}}** - the default background and border color for primary buttons
* `var(--color-button-primary-color)`: **#fff** - the default text color for primary buttons
* `var(--color-button-secondary-bg)`: **{{stylesheets.color.accent2}}** - the background color for all secondary buttons
* `var(--color-button-secondary-color)`: **{{stylesheets.color.white}}** - the text color for all secondary buttons

## Mixins

### button $backgroundColor, $fontColor, $borderColor, $borderRadius, $hoverBackground, $hoverColor;

#### Parameters

* `$backgroundColor` **(required)** - Color
* `$fontColor` **(required)** - Color
* `$borderColor` **(required)** - Color
* `$borderRadius` **(required)** - CSS Unit
* `$hoverBackground` **(required)** - Color
* `$hoverColor` **(required)** - Color

#### Usage

```postcss
.btn {
  @mixin button blue, white, blue, 3px, white, blue;
}
```

#### Output

```scss
.btn {
  display: inline-block;
  border: 2px solid blue;
  border-radius: 3px;
  padding: 12px 14px;
  background-color: blue;
  color: white;
  font-size: 14px;
  line-height: 1;
  text-align: center;
  vertical-align: middle;
  cursor: pointer;
  transition: color 250ms var(--easing-out), background-color 250ms var(--easing-out);

  &:hover,
  &:active,
  &.active,
  &:focus {
    background-color: white;
    color: blue;
  }

  &:disabled {
    opacity: .7;
    cursor: not-allowed;
  }
}
```

### button-size $paddingY, $paddingX, $fontSize, $borderRadius

#### Parameters

* `$paddingY` **(required)** - CSS Unit; value for the y-axis, top and bottom
* `$paddingX` **(required)** - CSS Unit; value for the x-axis, left and right
* `$fontSize` **(required)** - CSS Unit
* `$borderRadius` **(required)** - CSS Unit

#### Usage

```postcss
.btn-lg {
  @mixin button-size 20px, 25px, 16px, 5px;
}
```

#### Output

```scss
.btn-lg {
  border-radius: 5px;
  padding: 20px 25px;
  font-size: 16px;
}
```

### button-outline $color

#### Parameters

* `$color` **(required)** - Color; border and text colors

#### Usage

```postcss
.btn-outline {
  @mixin button-outline blue;
}
```

#### Output

```scss
.btn-outline {
  border-color: blue;
  background-color: transparent;
  color: blue;

  &:hover,
  &:active,
  &.active,
  &:focus {
    background-color: blue;
    color: #fff;
  }
}
```

## Helpers

```css
.button
.button-alt
.button-outline
.button-lg
.button-sm
```

## Example

```html
<button class="button">Primary Button</button>
<a class="button">Primary Link Button</a>
```

### Alt

```html
<button class="button-alt">Alt Button</button>
<a class="button-alt">Alt Link Button</a>
```

### Outline

```html
<button class="button-outline">Outline Button</button>
<a class="button-outline">Outline Link Button</a>
```

### Sizes

```html
<button class="button button-lg">Large Button</button>
<button class="button button-sm">Small Button</button>
<button class="button-outline button-lg">Large Outline Button</button>
<button class="button-outline button-sm">Small Outline Button</button>
```

### Disabled

```html
<button class="button" disabled>Disabled Button</button>
```

