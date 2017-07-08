# Menu Slide

## Variables

None

## Mixins

### menu-slide $menuColor, $closeColor

#### Parameters

* `$menuColor` **(required)** - Color;
* `$closeColor` **(required)** - Color;

#### Usage

```postcss
.menu-slide {
  @mixin menu-slide black, white;
}
```

#### Output

```scss
.menu-slide {
  & .menu-btn {
    position: absolute;
    visibility: hidden;
    width: 28px;
    height: 28px;
    margin-left: -999em;
    -webkit-appearance: none;

    & + label {
      display: block;
      float: right;
      width: 28px;
      height: 28px;
      margin: 0;
      transition: color .3s ease-in-out;
      cursor: pointer;
      user-select:none;

      &::after {
        display: inline-block;
        vertical-align: middle;
        border: 0;
        padding: 0;
        background: transparent;
        color: black;
        font-family: Arial;
        font-size: 36px;
        line-height: 1;
        content: '\2261';
      }
    }
    &:checked {
      & + label {
        &::after {
          position: absolute;
          top: 0;
          right: 0;
          z-index: 1000;
          margin: 10px;
          border: 1px solid white;
          border-radius: 50%;
          padding: 2px 8px 0;
          color: white;
          content: '\00d7';
        }
      }
      & ~ .menu-container {
        right: 60%;
        overflow-y: auto;
      }
    }
    & ~ .menu-container {
      position: fixed;
      top: 0;
      right: -60%;
      z-index: 10;
      width: 60%;
      height: 100%;
      box-shadow: -3px 0 3px 0 rgba(0, 0, 0, 0.25);
      padding: 20px 0 40px;
      padding-top: 80px;
      background-color: black;
      transform: translate3d(100%, 0, 0);
      transition: transform 250ms cubic-bezier(0.35, 0.97, 0.57, 0.99),
                  right 250ms cubic-bezier(0.35, 0.97, 0.57, 0.99) 300ms;
    }
  }
  &.menu-left {
    & .menu-btn {
      & + label {
        float: left;
      }
      &:checked {
        & + label::after {
          right: auto;
          left: 0;
        }
        & ~ .menu-container {
          left: 60%;
        }
      }
      & ~ .menu-container {
        right: auto;
        left: -60%;
        box-shadow: 3px 0 3px 0 rgba(0, 0, 0, 0.25);
        transform: translate3d(-100%, 0, 0);
        transition: transform 250ms cubic-bezier(0.35, 0.97, 0.57, 0.99),
                    left 250ms cubic-bezier(0.35, 0.97, 0.57, 0.99) 300ms;
      }
    }
  }
}
```

## Helpers

None

## Example

### Right Side (default)

```html
<div class="col-9"><h1>ClientKit</h1></div>
<div class="col-3">
  <div class="menu-slide">
    <input id="header-menu" class="menu-btn" type="checkbox" />
    <label for="header-menu"></label>
    <div class="menu-container text-right">
      <nav class="menu-header-container">
        <a href="">Menu 1</a>
        <a href="">Menu 2</a>
        <a href="">Menu 3</a>
        <a href="">Menu 4</a>
      </nav>
    </div>
  </div>
</div>
```

### Left Side

```html
<div class="col-plain">
  <div class="menu-slide menu-left">
    <input id="header-menu" class="menu-btn" type="checkbox" />
    <label for="header-menu"></label>
    <div class="menu-container">
      <nav class="menu-header-container">
        <a href="">Menu 1</a>
        <a href="">Menu 2</a>
        <a href="">Menu 3</a>
        <a href="">Menu 4</a>
      </nav>
    </div>
  </div>
</div>
<div class="col-11"><h1>ClientKit</h1></div>
```
