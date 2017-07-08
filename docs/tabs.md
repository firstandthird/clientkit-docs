# Tabs

## Variables

## Mixins

### tabs $number, $borderRadius

#### Parameters

* `$number` **(required)** - Number; the number of tabs desired
* `$borderRadius` **(required)** - CSS Unit;

#### Usage

```postcss
.tabs {
  @mixin tabs 2, 3px;
}
```

#### Output

```scss
.tabs {
  display: flex;
  flex-wrap: wrap;
  max-width: 100%;
  position: relative;
  list-style: none;
  border-radius: 3px;
}
.tabs .tab {
  display: none;
}
.tabs .tab:first-of-type:not(:last-of-type) + label {
  border-top-right-radius: 0;
  border-bottom-right-radius: 0;
}
.tabs .tab:not(:first-of-type):not(:last-of-type) + label {
  border-radius: 0;
}
.tabs .tab:last-of-type:not(:first-of-type) + label {
  border-top-left-radius: 0;
  border-bottom-left-radius: 0;
}
.tabs .tab:checked + label {
  cursor: default;
}
.tabs .tab + label {
  box-sizing: border-box;
  display: block;
  flex-grow: 3;
  border-radius: 3px 3px 0 0;
  text-decoration: none;
  cursor: pointer;
  user-select: none;
}
.tabs .tab-content {
  position: absolute;
  left: 0;
  z-index: -1;
  width: 100%;
  border-radius: 3px;
  opacity: 0;
  transform: translateY(-3px);
}
.tabs .tab:checked:nth-of-type(1) ~ .tab-content:nth-of-type(1) {
  position: relative;
  top: 0;
  z-index: 100;
  opacity: 1;
  transform: translateY(0px);
  transition: 0.5s opacity ease-in, 0.8s transform ease;
}
.tabs .tab:checked:nth-of-type(2) ~ .tab-content:nth-of-type(2) {
  position: relative;
  top: 0;
  z-index: 100;
  opacity: 1;
  transform: translateY(0px);
  transition: 0.5s opacity ease-in, 0.8s transform ease;
}
```

## Helpers

Defaults to 5 tabs with a 6px border-radius

```scss
.tabs
```

## Example

```html
<div class="tabs">
  <!-- active tab on page load gets checked attribute -->
  <input type="radio" id="tab1" name="tabGroup1" class="tab" checked>
  <label for="tab1">Short</label>

  <input type="radio" id="tab2" name="tabGroup1" class="tab">
  <label for="tab2">Medium</label>

  <input type="radio" id="tab3" name="tabGroup1" class="tab">
  <label for="tab3">Long</label>

  <div class="tab-content">
    <h3>Short Section</h3>
    <p>Praesent nonummy mi in odio. Nullam accumsan lorem in dui. Vestibulum turpis sem, aliquet eget, lobortis pellentesque, rutrum eu, nisl. Nullam accumsan lorem in dui. Donec pede justo, fringilla vel, aliquet nec, vulputate eget, arcu.</p>
  </div>

  <div class="tab-content">
    <h3>Medium Section</h3>
    <p>Praesent nonummy mi in odio. Nullam accumsan lorem in dui. Vestibulum turpis sem, aliquet eget, lobortis pellentesque, rutrum eu, nisl. Nullam accumsan lorem in dui. Donec pede justo, fringilla vel, aliquet nec, vulputate eget, arcu.</p>
    <p>In enim justo, rhoncus ut, imperdiet a, venenatis vitae, justo. Morbi mattis ullamcorper velit. Pellentesque posuere. Etiam ut purus mattis mauris sodales aliquam. Praesent nec nisl a purus blandit viverra.</p>
  </div>

  <div class="tab-content">
    <h3>Long Section</h3>
    <p>Praesent nonummy mi in odio. Nullam accumsan lorem in dui. Vestibulum turpis sem, aliquet eget, lobortis pellentesque, rutrum eu, nisl. Nullam accumsan lorem in dui. Donec pede justo, fringilla vel, aliquet nec, vulputate eget, arcu.</p>
    <p>In enim justo, rhoncus ut, imperdiet a, venenatis vitae, justo. Morbi mattis ullamcorper velit. Pellentesque posuere. Etiam ut purus mattis mauris sodales aliquam. Praesent nec nisl a purus blandit viverra.</p>
    <p>Praesent nonummy mi in odio. Nullam accumsan lorem in dui. Vestibulum turpis sem, aliquet eget, lobortis pellentesque, rutrum eu, nisl. Nullam accumsan lorem in dui. Donec pede justo, fringilla vel, aliquet nec, vulputate eget, arcu.</p>
    <p>In enim justo, rhoncus ut, imperdiet a, venenatis vitae, justo. Morbi mattis ullamcorper velit. Pellentesque posuere. Etiam ut purus mattis mauris sodales aliquam. Praesent nec nisl a purus blandit viverra.</p>
  </div>
</div>
```
