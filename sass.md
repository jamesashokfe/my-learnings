# Sass - Syntatically Awesome Style Sheets

- Scope of variables within the block it is defined.
- `!global` to override the default scope behavior of variables.
- Sass can nest rules as well as properties. For example,

```
font: {
  family: abc;
  size: 123;
  weight: xyz;
}

will transpile to,

font-family: abc;
font-size: 123;
font-weight: xyz;
```

- DRY - Don't Repeat Yourself
- hyphens and underscores are considered same in Sass
- Sass strings start at index 1
- Sass has modules that provide functions to process strings, numbers, lists, maps, selectors, colors, introspection/debugging...
- Sass unit testing - https://www.educative.io/blog/sass-tutorial-unit-testing-with-sass-true
- Competitors: Less, Stylus
- Other Tools: PostCSS, cssnext

---

- All special function calls return unquoted strings. Interpolation always return unquoted strings.
- `margin: if($condn, 16px, null);` -  If a declaration’s value is null or an empty unquoted string, Sass won’t compile that declaration to CSS at all.
- Unquoted strings are also the identifiers.

---

- `&` is parent selector.
- A stylesheet can define variables with the !default flag to make them configurable.

---

- Prefer `@use` over `@import`. Why?
  - `@import` brings all mixins, variables... to global scope.
  - `@import` can cause bloated / duplicate output.
  - no way to define private members.
  - `@use`and the new module system addresses all the above issues.
  - `@use` must be on top of the file. Only one url per statement.

---

- `@mixin new-makeup($color, $selectors...)` - here `$selectors` will be a list that can receive any number of arguments.
  - `meta.keywords($selectors)` returns the passed arguments as a map.

---

- Falsey / Truthy
  - `false` and `null` are falsey.
  - empty list/string, 0 are truthy.

---

- `@for`
  - `@for <variable> from <expression> to <expression> { ... }` - final expr excluded.
  - `@for <variable> from <expression> through <expression> { ... }` - final expr included.


## Best Practices

- Organizing Sass (Folder Structure)
  - https://sass-guidelin.es/#the-7-1-pattern
  - https://github.com/KittyGiraudel/sass-boilerplate
- On main.scss - add `@charset 'utf-8';` first thing before importing any styles.
- Reduce mixins, embrace placeholders - mixins can create lots of duplicate codes.
  - Use mixins to pass parameters.
  - @extends do not work across media queries.
- Use single quoted strings. Quotes not required for CSS values/identifiers.
- Wrap computations in a parantheses.
- Keep It Simple
- Use @functions for mathematical calculations.
  - @functions to output values not CSS.
- Restrict nesting to 3 levels.
