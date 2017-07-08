# Tooltip

## Variables

* `var(--color-tooltip-bg)`: **rgba(17,17,17,.9)**

## Mixins

None

## Helpers

The base class of `.tooltip` sets up the tooltip, but in order to get it working
properly, you need to add a direction as well.

### Base tooltip

```scss
.tooltip
```

### Directions

```scss
.tooltip-up
.tooltip-right
.tooltip-down
.tooltip-left
```

## Example

```html
<button class="tooltip tooltip-up" data-tooltip-title="Whats up!">Tooltip Up</button>
<button class="tooltip tooltip-right" data-tooltip-title="Whats up!">Tooltip Right</button>
<button class="tooltip tooltip-down" data-tooltip-title="Whats up!">Tooltip Down</button>
<button class="tooltip tooltip-left" data-tooltip-title="Whats up!">Tooltip Left</button>
```
