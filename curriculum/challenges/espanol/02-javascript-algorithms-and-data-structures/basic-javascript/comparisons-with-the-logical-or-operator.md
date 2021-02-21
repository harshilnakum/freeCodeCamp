---
id: 56533eb9ac21ba0edf2244d9
title: Comparisons with the Logical Or Operator
challengeType: 1
videoUrl: 'https://scrimba.com/c/cEPrGTN'
forumTopicId: 16800
dashedName: comparisons-with-the-logical-or-operator
---

# --description--

The <dfn>logical or</dfn> operator (`||`) returns `true` if either of the <dfn>operands</dfn> is `true`. Otherwise, it returns `false`.

The <dfn>logical or</dfn> operator is composed of two pipe symbols: (`||`). This can typically be found between your Backspace and Enter keys.

The pattern below should look familiar from prior waypoints:

```js
if (num > 10) {
  return "No";
}
if (num < 5) {
  return "No";
}
return "Yes";
```

will return "Yes" only if `num` is between `5` and `10` (5 and 10 included). The same logic can be written as:

```js
if (num > 10 || num < 5) {
  return "No";
}
return "Yes";
```

# --instructions--

Combine the two `if` statements into one statement which returns `"Outside"` if `val` is not between `10` and `20`, inclusive. Otherwise, return `"Inside"`.

# --hints--

You should use the `||` operator once

```js
assert(code.match(/\|\|/g).length === 1);
```

You should only have one `if` statement

```js
assert(code.match(/if/g).length === 1);
```

`testLogicalOr(0)` should return "Outside"

```js
assert(testLogicalOr(0) === 'Outside');
```

`testLogicalOr(9)` should return "Outside"

```js
assert(testLogicalOr(9) === 'Outside');
```

`testLogicalOr(10)` should return "Inside"

```js
assert(testLogicalOr(10) === 'Inside');
```

`testLogicalOr(15)` should return "Inside"

```js
assert(testLogicalOr(15) === 'Inside');
```

`testLogicalOr(19)` should return "Inside"

```js
assert(testLogicalOr(19) === 'Inside');
```

`testLogicalOr(20)` should return "Inside"

```js
assert(testLogicalOr(20) === 'Inside');
```

`testLogicalOr(21)` should return "Outside"

```js
assert(testLogicalOr(21) === 'Outside');
```

`testLogicalOr(25)` should return "Outside"

```js
assert(testLogicalOr(25) === 'Outside');
```

# --seed--

## --seed-contents--

```js
function testLogicalOr(val) {
  // Only change code below this line

  if (val) {
    return "Outside";
  }

  if (val) {
    return "Outside";
  }

  // Only change code above this line
  return "Inside";
}

testLogicalOr(15);
```

# --solutions--

```js
function testLogicalOr(val) {
  if (val < 10 || val > 20) {
    return "Outside";
  }
  return "Inside";
}
```