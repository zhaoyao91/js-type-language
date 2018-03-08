# JS Type Comment Language

Doc your JS things using comment and JS type language.

## Stage

- Version: 0.0.0
- JS Type Language: ^0.0.0

## Definition

Right above the thing you'd like to doc, write a comment section:

```ecmascript 6
/**
 * ... 
 */
function buildBob(name, age) {return {name, age}}
```

Then, write a type using JS type language, which denotes the type of the thing you are documenting:

```ecmascript 6

/**
 * (name: String, age: String) => Result
 */
function buildBob(name, age) {return {name, age}}
```

Below the type, you can write more types, which can further define any custom types mentioned above:

```ecmascript 6

/**
 * (name: String, age: String) => Result
 * 
 * Result ~ {
 *   name: String,
 *   age: Number,
 * }
 */
function buildBob(name, age) {return {name, age}}
```

You can add more arbitrary comments with leading `//`:

```ecmascript 6

/**
 * // create a great Bob
 * (name: String = 'Bob', age: String) => Result
 * 
 * Result ~ {
 *   name: String, // the name of Bob
 *   age: Number, // the age of Bob
 * }
 */
function buildBob(name = 'Bob', age) {return {name, age}}
```
