# Dropdown

## Variables

* `var(--color-dropdown-bg): **#fff**

## Mixins

None

## Helpers

None

## Example

```html
<div class="dropdown open">
  <button class="button dropdown-toggle">Dropdown Button</button>
  <div class="dropdown-menu" style="min-width: 125px;">
    <button class="dropdown-item disabled">Disabled Button item</button>
    <button class="dropdown-item active">Active Button item</button>
    <a href="" class="dropdown-item">Link item</a>
    <a href="" class="dropdown-item">Link item</a>
  </div>
</div>
```

### Right-side Menu

```html
<div class="dropdown open">
  <button class="button dropdown-toggle">Dropdown Button</button>
  <div class="dropdown-menu dropdown-menu-right" style="min-width: 125px;">
    <button class="dropdown-item disabled">Disabled Button item</button>
    <button class="dropdown-item active">Active Button item</button>
    <a href="" class="dropdown-item">Link item</a>
    <a href="" class="dropdown-item">Link item</a>
  </div>
</div>
```
