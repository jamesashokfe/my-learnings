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
  - Order of appearance: `:link, :visited, :hover, :active, :focus`
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
- `box-reflect`: `below`|`above`|`left`|`right` - for reflection of elements.
- `filter`: none | blur() | brightness() | contrast() | drop-shadow() | grayscale() | hue-rotate() | invert() | opacity() | saturate() | sepia() | url()
- `object-fit`: fill|contain|cover|scale-down|none
- `outline-offset` - space between outline & border.
- `var(--name, fallback_value)`
- `accent-color` property specifies the accent color for user-interface controls.
- `caret-color` input cursor color.

---

- `[attribute~="value"]` contains `value` as a full word or space separated word
- `[attribute|="value"]` exactly the specified `value` or the `value-<other_words>`
- `[attribute^="value"]` starts with
- `[attribute$="value"]` ends with
- `[attribute*="value"]` contains
- `+` next adjacent sibling selector.
- `~` next general sibiling selector.

---

Counters
- `counter-reset` - Creates or resets a counter
- `counter-increment` - Increments a counter value
- `content` - Inserts generated content
- `counter()` or `counters()` function - Adds the value of a counter to an element

```
body {
  counter-reset: section; // init counter.
}

h2::before {
  counter-increment: section;
  content: "Section " counter(section) ": ";
}
```

---

Specificity Hierarchy
  - Inline styles - 1000
  - IDs - add 100
  - Classes, pseudo-classes, attribute selectors - add 10
  - Elements and pseudo-elements - add 1
  - \* - 0

---

Border Images
- `border-image`
  - `border-image-source`
  - `border-image-slice`
  - `border-image-width`
  - `border-image-outset`
  - `border-image-repeat`

---

Backgrounds
- bg-size
  - `contain` - bg image will be fully visible.
  - `cover` - bg image may be stretched / clipped to fill the container.
- bg-origin: padding-box|border-box|content-box
- bg-clip: border-box|padding-box|content-box

---

Texts
- `text-justify`: auto|inter-word|inter-character|none
- `text-overflow`: clip|ellipsis|*string*
- `word-break`: normal|break-all|keep-all|break-word
- `word-wrap`: normal|break-word
- `writing-mode`: horizontal-tb|vertical-rl|vertical-lr
- `direction`: ltr|rtl
- `white-space`: normal|nowrap|pre|pre-line|pre-wrap

---

Transitions
- transition
  - transition-delay
  - transition-duration
  - transition-property
  - transition-timing-function

Animations
- @keyframes
  - animation
  - animation-name
  - animation-duration
  - animation-timing-function
  - animation-delay
  - animation-iteration-count
  - animation-direction - normal|reverse|alternate|alternate-reverse
  - animation-fill-mode - none|forwards|backwards|both
  - animation-play-state - paused|running

---

Multiple Columns
- column-count
- column-fill: balance|auto
- column-gap
- column-rule-style
- column-rule-width
- column-rule-color
- column-rule
- column-span
- column-width
- columns: shorthand for column-width, column-count

---

Flex
- `flex-flow` - shorthand for `flex-direction` & `flex-wrap`
- `align-content` - aligns flex lines when flex-wrap used

Flex Item
- order
- flex-grow
- flex-shrink
- flex-basis
- `flex` - shorthand for `flex-grow, flex-shrink & flex-basis`
- align-self

Grid
- `grid`: shorthand for `grid-template-rows, grid-template-columns, grid-template-areas, grid-auto-rows, grid-auto-columns & grid-auto-flow`
- `grid-area`: name of grid item (or) shorthand for `grid-row-start, grid-column-start, grid-row-end & grid-column-end`
- `grid-auto-columns` - default col size
- `grid-auto-rows` - default row size
- `grid-auto-flow` - specify how `auto` items are placed on grid.
- `grid-column: grid-column-start / grid-column-end`
- `grid-row: grid-row-start / grid-row-end`
- `grid-template: none|grid-template-rows / grid-template-columns|grid-template-areas|initial|inherit`

---

```
// Display at least 4 lines at the bottom and 2 lines at the top of each page:
@media print {
  orphans: 4;
  widows: 2;
}
```

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
