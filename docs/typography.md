# Typography

## Variables

### Colors

* `var(--color-heading)`: **#333**
* `var(--color-heading-light)`: **#fff**
* `var(--color-link)`: **{{stylesheets.color.accent1}}**
* `var(--color-link-hover)`: **color({{stylesheets.color.accent1}} blackness(+20%))**
* `var(--hr-color)`: **{{stylesheets.color.body}}**

### Families

* `var(--font-primary)`: **-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen-Sans, Ubuntu, Cantarell, 'Helvetica Neue', sans-serif**
* `var(--font-secondary)`: **-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen-Sans, Ubuntu, Cantarell, 'Helvetica Neue', sans-serif**
* `var(--font-heading)`: **-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen-Sans, Ubuntu, Cantarell, 'Helvetica Neue', sans-serif**

### Sizes

* `var(--font-size-body)`: **body: 14px**
* `var(--font-size-large)`: **16px**
* `var(--font-size-small)`: **12px**
* `var(--font-mobile-size-body)`: **14px**
* `var(--font-mobile-size-large)`: **16px**
* `var(--font-mobile-size-small)`: **12px**

### Weights

* `var(--font-weight-body)`: **normal**
* `var(--font-weight-light)`: **300**
* `var(--font-weight-regular)`: **400**
* `var(--font-weight-semibold)`: **600**
* `var(--font-weight-bold)`: **700**
* `var(--font-weight-xbold)`: **800**

### Headings

* `var(--heading-line-height)`: **1.2**
* `var(--heading-font-weight)`: **bold**
* `var(--heading-1-size)`: **45px**
* `var(--heading-1-mobile-size)`: **30px**
* `var(--heading-2-size)`: **30px**
* `var(--heading-2-mobile-size)`: **25px**
* `var(--heading-3-size)`: **25px**
* `var(--heading-3-mobile-size)`: **20px**
* `var(--heading-4-size)`: **20px**
* `var(--heading-4-mobile-size)`: **16px**
* `var(--heading-5-size)`: **16px**
* `var(--heading-5-mobile-size)`: **14px**
* `var(--heading-6-size)`: **14px**
* `var(--heading-6-mobile-size)`: **12px**

### Miscellaneous

* `var(--line-height)`: **1.1**
* `var(--line-height-large)`: **1.5**
* `var(--stretch-spacing)`: **2px**
* `var(--hr-max-width)`: **3.5em**
* `var(--hr-height)`: **3px**

## Mixins

### link $color, $hoverColor

#### Parameter

* `$color` **(required)** - Color
* `$hoverColor` **(required)** - Color

#### Usage

```postcss
.link {
  @mixin link blue, darkblue;
}
```

#### Output

```scss
.link {
  color: blue;
  text-decoration: none;
  cursor: pointer;
}

.link:hover {
  color: darkblue;
}
```

### headings $size, $mobileSize

#### Parameter

* `$size` **(required)** - CSS Unit
* `$mobileSize` **(required)** - CSS Unit

#### Usage

```postcss
.h1 {
  @mixin headings 16px, 24px;
}
```

#### Output

```scss
.h1 {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen-Sans, Ubuntu, Cantarell, 'Helvetica Neue', sans-serif;
  color: #333;
  line-height: 1.2;
  font-weight: bold;
  font-size: 16px;
}

@media (--mobile) {
  .h1 {
    font-size; 24px;
  }
}
```

### fancy-underline $backgroundColor, $linkColor, $hoverColor, $offset, $width, $activeOffset

#### Parameter

* `$backgroundColor` **(required)** - Color
* `$linkColor` **(required)** - Color
* `$hoverColor` **(required)** - Color
* `$offset` (optional) - Number; defaults to 1;
* `$width` (optional) - Number; defaults to 1;
* `$activeOffset` (optional) - Number; defaults to 1;

#### Usage

```postcss
.fancy-underline {
  @mixin fancy-underline white, blue, darkblue;
}
```

#### Output

```css
.fancy-underline {
  color: blue;
  text-decoration: none;
  text-shadow: -1px -1px 0 white, 1px -1px 0 white, -1px 1px 0 white, 1px 1px 0 white;
  background-image: linear-gradient(bottom, transparent, transparent 1px, blue 1px, blue 2px, transparent 2px);
  transition: color 200ms ease, background-image 200ms ease;
}
.fancy-underline:hover, .fancy-underline:focus {
  color: darkblue;
  background-image: linear-gradient(bottom, transparent, transparent 1px, darkblue 1px, darkblue 2px, transparent 2px);
},
.fancy-underline:active {
  color: darkblue;
  background-image: linear-gradient(bottom, transparent, transparent 1px, darkblue 1px, darkblue 2px, transparent 3px);
},
.fancy-underline:focus {
  outline: 0,
  color: blue
}
```

## Helpers

### Colors

```css
.heading--light
.text-color-body
.text-color-heading
.text-color-light
```

### Families

```css
.font-primary
.font-secondary
```

### Sizes

```css
.font-large
.font-small
.font-body
```

### Weights

```css
.font-weight-light
.font-weight-regular
.font-weight-semibold
.font-weight-bold
.font-weight-xbold
```

### Alignment

```css
.text-left
.text-center
.text-right
.text-justify
```

### Transforms

```css
.text-nowrap
.text-truncate
.text-lowercase
.text-uppercase
.text-capitalize
.text-stretch
```

### Headings

```css
.heading-1
.heading-2
.heading-3
.heading-4
.heading-5
.heading-6
```

### Lists

```css
.list-unstyle
.list-inline
```

### Horizontal Rules

```css
hr
```
