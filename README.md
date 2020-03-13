# 11ty-liquid-filters-ceil

Comparing LiquidJS's `ceil` filter to Nunjucks' `round` filter.

## USAGE

### LiquidJS

```liquid
{{ 1.2 | ceil }}
<!-- Expected: 2 -->
```

### Nunjucks

```liquid
{{ 1.2 | round(0, "ceil") }}
<!-- Expected: 2 -->
```

If you want to polyfill [LiquidJS's <code>ceil</code> filter](https://github.com/harttle/liquidjs/blob/0f25017d5d9861f99b7783f488b1c11f8c7f36fe/src/builtin/filters/math.ts#L7) into Nunjucks, you can add the following snippet to your .eleventy.js config file:

```js
eleventyConfig.addNunjucksFilter("ceil", value => Math.ceil(value));
```
