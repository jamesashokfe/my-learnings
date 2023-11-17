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
