### -  &&
`(a && b)` does not even evaluate `b` if `a` is falsy and returns `a` straight away; but if `a` is truthy, the it evaluates and returns `b`

### - ||
`(a || b)` does not even evaluate `b` if `a` is truthy and returns `a`, but if it's falsy, then it evaluates and returns `b`



# Nullish coalescing operator (??)

The **nullish coalescing (`??`)** operator is a logical operator that returns its right-hand side operand when its left-hand side operand is [`null`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) or [`undefined`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined), and otherwise returns its left-hand side operand.

```js
const foo = null ?? 'default string';
console.log(foo);
// Expected output: "default string"

const baz = 0 ?? 42;
console.log(baz);
// Expected output: 0

```

It's a Special version of Logical OR operator that returns its RHS operand when its LHS is null, undefined or false.

# Chaining Operator(.)

The chaining operator `.` is used to access properties or methods of an object.


# Optional chaining (?.)

The **optional chaining (`?.`)** operator accesses an object's property or calls a function. If the object accessed or function called using this operator is [`undefined`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined) or [`null`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null), the expression short circuits and evaluates to [`undefined`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined) instead of throwing an error.

The `?.` operator is like the `.` chaining operator, except that instead of causing an error if a reference is [nullish](https://developer.mozilla.org/en-US/docs/Glossary/Nullish) ([`null`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) or [`undefined`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined)), the expression short-circuits with a return value of `undefined`. When used with function calls, it returns `undefined` if the given function does not exist

Example -1 
```js
const adventurer = {
  name: 'Alice',
  cat: {
    name: 'Dinah',
  },
};

const dogName = adventurer.dog?.name;
console.log(dogName);
// Expected output: undefined

console.log(adventurer.someNonExistentMethod?.());
// Expected output: undefined

```

Example-2
```js
const user = {
  profile: {
    name: 'John Doe',
    address: {
      city: 'New York'
    }
  }
};

// Without optional chaining
const city = user && user.profile && user.profile.address && user.profile.address.city;

// With optional chaining
const city = user?.profile?.address?.city;

console.log(city); // Output: 'New York'

```

In the example above, using ==?.== ensures that if any part of the chain is `null` or `undefined` , the expression will short-circuit and return undefined instead of throwing an error.