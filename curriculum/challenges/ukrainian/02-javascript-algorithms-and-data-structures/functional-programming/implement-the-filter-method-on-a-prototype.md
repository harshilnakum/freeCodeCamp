---
id: 587d7b8f367417b2b2512b64
title: Реалізація методу фільтра для прототипу
challengeType: 1
forumTopicId: 301231
dashedName: implement-the-filter-method-on-a-prototype
---

# --description--

Ви можете багато дізнатись про метод `filter`, якщо ви реалізуєте вашу власну версію. Рекомендується використовувати код циклу `for` або `Array.prototype.forEach()`.

# --instructions--

Напишіть ваш власний `Array.prototype.myFilter()`, який буде поводити себе точно так як `Array.prototype.filter()`. Не варто використовувати вбудований метод `filter`. Приклад `Array` може бути доступним за допомогою методу `myFilter` з використанням `this`.

# --hints--

`[23, 65, 98, 5, 13].myFilter(item => item % 2)` should equal `[23, 65, 5, 13]`.

```js
const _test_s = [23, 65, 98, 5, 13];
const _callback = item => item % 2;
assert(JSON.stringify(_test_s.filter(_callback)) === JSON.stringify(_test_s.myFilter(_callback)));
```

Не використовуйте метод `filter` для вашого коду.

```js
assert(!code.match(/\.?[\s\S]*?filter/g));
```

# --seed--

## --seed-contents--

```js
Array.prototype.myFilter = function(callback) {
  const newArray = [];
  // Only change code below this line

  // Only change code above this line
  return newArray;
};
```

# --solutions--

```js
Array.prototype.myFilter = function(callback) {
  const newArray = [];
  for (let i = 0; i < this.length; i++) {
    if (callback(this[i])) newArray.push(this[i]);
  }
  return newArray;
};

// Test case
const s = [23, 65, 98, 5];
const odd_s = s.myFilter(item => item % 2 === 1);
```
