# Buttons

## Variables

* ease-out: `cubic-bezier(0.000, 0.000, 0.580, 1.000)`
* button-primary-bg: `{{stylesheets.color.accent1}}`
* button-primary-color: `#fff`
* button-radius-default: `3px`

## Mixins

### @mixin button backgroundColor, fontColor, borderColor, borderRadius, hoverBackground, hoverColor;

Outputs:

```scss
display: inline-block;
border: 2px solid $border;
border-radius: $borderRadius;
padding: 12px 14px;
background-color: $background;
color: $color;
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
	background-color: $hoverBackground;
	color: $hoverColor;
}

&:disabled {
	opacity: .7;
	cursor: not-allowed;

&:hover,
&:active,
&.active,
&:focus {
	background-color: $background;
	color: $color;
}
```

### @mixin button-size paddingY, paddingX, fontSize, borderRadius

Outputs:

```scss
border-radius: $borderRadius;
padding: $paddingY $paddingX;
font-size: $fontSize;
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

