# Forms

## Variables

* `var(--color-input-background)`: **#fff**
* `var(--color-input-border)`: **#333**
* `var(--color-input-border-focus)`: **{{stylesheets.color.accent1}}**
* `var(--color-input-group-background)`: **rgb(241,241,241)**
* `var(--color-input-label)`: **gray**
* `var(--color-input-error)`: **red**

## Mixins

### input $background, $color, $colorDisabled, $border, $borderFocus, $borderDisabled

#### Parameters

* `$background` **(required)** - Color;
* `$color` **(required)** - Color;
* `$colorDisabled` **(required)** - Color;
* `$border` **(required)** - Color;
* `$borderFocus` **(required)** - Color;
* `$borderDisabled` **(required)** - Color;

#### Usage

```postcss
.input {
  @mixin input white, black, grey, black, blue, grey;
}
```

#### Output

```scss
.input {
  width: 100%;
  box-shadow: 0 1px 0 0 black;
  border: 0;
  padding: 0;
  background-color: white;
  color: black;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen-Sans, Ubuntu, Cantarell, 'Helvetica Neue', sans-serif;
  font-size: 16px;
  line-height: 1.1;
  transition: box-shadow var(--easing-out) 250ms;

  &:focus {
    outline: none;
    box-shadow: 0 2px 0 0 blue;
  }
  &:disabled {
    box-shadow: none;
    border-bottom: 1px dashed grey;
    color: grey;
  }
  &:read-only {
    cursor: text;
  }
}
```

## Helpers

None

## Example

```html
<form class="form">...</form>
```

### Labels

```html
<form class="form">
  <label>Example Input</label>
  <input id="exampleInput" type="text" placeholder="Example">
</form>
```

### Input types

```html
<form class="form">
  <!-- text -->
  <input type="text" placeholder="Text">
  <!-- read only -->
  <input type="text" value="Text can only be copied" readonly>
  <!-- email -->
  <input type="email" placeholder="Email">
  <!-- password -->
  <input type="password" placeholder="Password">
  <!-- url -->
  <input type="url" placeholder="Url">
  <!-- telephone -->
  <input type="tel" placeholder="Telephone">
  <!-- search -->
  <input type="search" placeholder="Search">
  <!-- number -->
  <input type="number" placeholder="Number">
  <!-- date -->
  <input type="date" placeholder="Date">
  <!-- date time -->
  <input type="datetime" placeholder="Date Time">
  <!-- date time local -->
  <input type="datetime-local" placeholder="Date Time Local">
  <!-- month -->
  <input type="month" placeholder="Month">
  <!-- week -->
  <input type="week" placeholder="Week">
  <!-- time -->
  <input type="time" placeholder="Time">
  <!-- textarea -->
  <textarea placeholder="Textarea"></textarea>
  <!-- select -->
  <select>
    <option>Option 1</option>
    <option>Option 2</option>
    <option>Option 3</option>
  </select>
</form>
```

### Errors

```html
<form class="form">
  <div class="error">
    <label>Some input</label>
    <input type="text" placeholder="Error">
    <small>This field is required</small>
  </div>
</form>
```

### Input Group

```html
<form class="form">
  <div class="input-group">
    <input type="text" placeholder="Enter your email">
    <button class="input-group-btn button">Sign Up</button>
  </div>
</form>
```
