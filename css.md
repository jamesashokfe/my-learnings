# CSS

```
[selector] {
  [property]: [value];
  [<--declaration--->]
}
```

- SMACSS - Scalable and Modular Architecture for CSS
- `@supports` CSS @rule to check if browser supports feature and then include certain styles.
- `::` for CSS3 pseudo elements, `:` for pseudo classes.
  - `::selection` for customising selected/highlighted text.
  - `:target` for customising active location `(#element-id)` in a document that is reached on clicking `<a href="#element-id">`
  - `:link` all unvisited links.
  - Order of appearance: `:link, :visited, :hover, :active`
- `%`
  - margins, paddings - % of container/parent width.
  - dimensions, positions - % of container/parent width/height.
- Clearfix - To fix a floated element taller than its containing element, causing "overflow" outside of its container.
```
.clearfix::after {
  content: "";
  clear: both;
  display: table;
}
```
- `display: inline` - no width, height, top-bottom margins.

---

- `[attribute~="value"]` contains `value` as a full word or space separated word
- `[attribute|="value"]` exactly the specified `value` or the `value-<other_words>`
- `[attribute^="value"]` starts with
- `[attribute$="value"]` ends with
- `[attribute*="value"]` contains
- `+` next adjacent sibling selector.
- `~` next general sibiling selector.

---

---

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
