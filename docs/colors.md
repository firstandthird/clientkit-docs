# Colors

All variables are namespaced under `stylesheets.color` which means they can be accessed within a yaml or configuration file as such: `'{{ stylesheets.color.<color> }}'`, where `<color>` is one of the values listed below. When accessing them within a stylesheet, use the following format: `var(--color-<color>)`.

## Variables

* `var(--color-accent1)`: **#336699**
* `var(--color-accent2)`: **orange**
* `var(--color-body)`: **#333**
* `var(--color-white)`: **#fff**
* `var(--color-background-default)`: **#fff**
* `var(--color-background-alt)`: **rgb(95, 95, 95)**
* `var(--color-text-color-error)`: **red**

## Mixins

### bg-colors

Will take any of the above variables that are prefixed with `background-` and
create a class that is prefixed with `.bg-`.  This means that the variable of
`background-alt` has a helper class of `.bg-alt`.

#### Parameters

None

#### Usage

```postcss
@mixin bg-colors;
```

#### Output

```scss
.bg-alt {
  background-color: rgb(95, 95, 95);
}
```

### text-colors

Will take any of the above variables that are prefixed with `text-color-` and
create a class that is prefixed with `.text-color-`.  This means that the
variable of `text-color-error` has a helper class of `.text-color-error`.

#### Parameters

None

#### Usage

```postcss
@mixin text-colors;
```

#### Outputs:

```scss
.text-color-error {
  color: red;
}
```

## Helpers

```postcss
body {
  background-color: var(--color-background-default);
}
```

## Example

```html
<div class="bg-alt">...</div>
<p class="text-color-error">...</p>
```
