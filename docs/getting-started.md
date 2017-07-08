# Getting Started

Clientkit is an opinionated CSS framework.

## Desktop first

we've written the project to be desktop friendly from the start. This means the breakpoints and grid are all written to to scale down from desktop sizes down to mobile. This can be changed by flipping the switch in the `conf/default-stylesheets.yaml` file under the key `mobileFirst`.

## Box-sizing

For more straightforward sizing in CSS, we switch the global `box-sizing` value from `content-box` to `border-box`. This ensures padding does not affect the final computed width of an element, but it can cause problems with some third party software like Google Maps and Google Custom Search Engine.

On the rare occasion you need to override it, use something like the following:

```
.selector-for-some-widget {
  box-sizing: content-box;
}
```

With the above snippet, nested elements—including generated content via `::before` and `::after`—will all inherit the specified `box-sizing` for that `.selector-for-some-widget`.

Learn more about [box model and sizing at CSS Tricks](https://css-tricks.com/box-sizing/).

## Normalize.css

For improved cross-browser rendering, we use [Normalize.css](http://necolas.github.io/normalize.css/), a project by [Nicolas Gallagher](https://twitter.com/necolas) and [Jonathan Neal](https://twitter.com/jon_neal). On top of that we reset the margin on all `<h* />` tags and `<p />` tags.

## How to Read the Docs

Each file will be formatted the same way with 3-4 sections.

* **Variables** - these are the variables that are related to the file itself
* **Mixins** - a listing of mixins with the signature, usage and sample output
* **Helpers** - a list of all helpers that are intended to call a mixin in a specific way
* **Example** - An HTML outputted example to show how to use
