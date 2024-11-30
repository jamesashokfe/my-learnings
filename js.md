Notes from,
- https://github.com/lydiahallie/javascript-questions

---

- JS is dynamically typed.

- `var` is global or function scoped.
- `let, const` are block scoped.
- multiple variables with same name is possible with `var` but not with `let, const`

- `abcd = 5;`
  - `global.abcd = 5` in Node.js
  - `window.abcd = 5` | `frames.abcd = 5` | `self.abcd = 5` in browsers
  - `self.abcd = 5` in web workers
  - `globalThis.abcd = 5` in all environments

- Arrow functions
  - `this` refers to current surrounding scope.

- unary plus tries to convert an operand to a number.
  - `+true` = 1
  - `+'123'` = 123
  - `+'Hi'` = NaN

- `3 !== new Number(3)`
- `3 == new Number(3)`

- Object
  - All object keys are strings. Any non string keys are automatically converted to strings.
  - If you have two keys with the same name, the key will be replaced. It will still be in its first position, but with the last specified value.

- All objects have prototype except the base object, `Object.prototype`
- A `function` is a speacial type of object.
- When using `new` keyword, `this` refers to the new empty object that we create. If we don't add `new` then `this` refers to the `global` object.

- 3 phases of event propagation: Capturing > Target > Bubbling: On capturing an event, it goes through the ancestor elements down to the target element. Once target element is reached, bubbling up begins.
  - can stop bubbling by `event.stopPropagation`
  - event handlers are executed in bubbling phase by default, unless `useCapture` is set to `true`

- Tagged template literals
  - `` someFunction`${expression1} some and ${expression2} and more` ``
    - Passed arguments - `["", " some and ", " and more"], <expression1>, <expression2>`

- `typeof` can return one of `undefined, boolean, number, bigint, string, symbol, function, object`
  - `typeof null` is `object`
  - The rest parameter `(...args)` collects all remaining arguments into an array. An array is an object, so `typeof args` returns `object`

- Storage
  - The data stored in `sessionStorage` is removed after closing the tab.
  - The data stored in `localStorage` is present forever, unless cleared like `localStorage.clear()`

- `continue` statement skips an iteration.

