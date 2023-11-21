# CSS

```
[selector] {
  [property]: [value];
  [<--declaration--->]
}
```

- SMACSS - Scalable and Modular Architecture for CSS
- `@supports` CSS @rule to check if browser supports feature and then include certain styles.

## Colors
### HSL - Hue Saturation Lightness
- Hue - 0 to 360 deg on color wheel.
  - 0 is red | 120 is green | 240 is blue
- Saturation - 0 to 100% intensity of the color.
  - 100% is full color.
  - 50% is 50:50 color:gray
  - 0% is full gray.
- Lightness
  - 0% is full dark / black.
  - 100% is full light / white.

## Best Practices
- open for extension, but closed for modification
- Use separate `js-*` classes for JS interactions. Do not use these classes on CSS.
- Should be reusable, portable, extensible.

### Atomic Design
Atoms, Molecules, Organisms, Templates, Pages
