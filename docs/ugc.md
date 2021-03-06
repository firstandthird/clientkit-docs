# User-Generated Content

When dealing with content that may come from an admin or CMS, wrap a parent
element in the `.ugc` class to reset all of the elements to match the Clientkit
style.

## Variables

None

## Mixins

### ugc

### Parameters

None

### Usage

```postcss
@mixin ugc;
```

#### Output

```scss
.ugc {
  & h1,
  & h2,
  & h3,
  & h4,
  & h5,
  & h6,
  & p,
  & ol,
  & ul {
    @mixin spacing margin, top, none;
    @mixin spacing margin, bottom, md;
  }
  & h1 {
    @mixin heading var(--heading-1-size), var(--heading-1-mobile-size);
  }
  & h2 {
    @mixin heading var(--heading-2-size), var(--heading-2-mobile-size);
  }
  & h3 {
    @mixin heading var(--heading-3-size), var(--heading-3-mobile-size);
  }
  & h4 {
    @mixin heading var(--heading-4-size), var(--heading-4-mobile-size);
  }
  & h5 {
    @mixin heading var(--heading-5-size), var(--heading-5-mobile-size);
  }
  & ul,
  & ol {
    padding-left: 25px;
  }
  & ul li {
    list-style-type: disc;
  }
  & table {
    width: 100%;
    & th {
      text-align: left;
    }
  }
}
```

## Helpers

```scss
.ugc
```

## Example

```html
<div class="ugc">
  <h1>Heading 1</h1>
  <h2>Heading 2</h2>
  <h3>Heading 3</h3>
  <h4>Heading 4</h4>
  <h5>Heading 5</h5>
  <p>Default body font</p>
  <ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
  </ul>
  <ol>
    <li>Ordered Item 1</li>
    <li>Ordered Item 2</li>
    <li>Ordered Item 3</li>
  </ol>
  <table>
    <thead>
      <tr>
        <th>Table Header 1</th>
        <th>Table Header 2</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Table Header 1</td>
        <td>Table Header 2</td>
      </tr>
    </tbody>
  </table>
</div>
```
