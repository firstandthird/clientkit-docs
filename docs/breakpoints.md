# Breakpoints

## Variables

```yaml
desktop-wide:
  max-width: 100vw
  min-width: 1440px
  content: 1440px
  col: xl
  default: '{{!core.mobileFirst}}'
  bleed: 1600px
desktop:
  max-width: 1439px
  min-width: 1024px
  content: 1024px
  col: lg
tablet:
  max-width: 1023px
  min-width: 768px
  content: 768px
  col: md
mobile:
  max-width: 767px
  min-width: 320px
  content: 100%
  col: sm
```

There is a `breakpointHelper()` function in the `lib/` that is available for use
when building out responsive-based mixins. The functions signature requires you
to pass in an Object of styles as the first argument and the global `config` as
the last argument. Look at the `container.js` mixin or `grid.js` mixin for an
example.
