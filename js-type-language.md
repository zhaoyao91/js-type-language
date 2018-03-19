# JS Type Language

Help define types for JS.

## Stage

- Version: 0.0.0

## What is a *Type*?

A *type* is a set of allowed values which share the features defined by this type.

The value set could be finite or infinite.

## Basic Types

- `Number`
- `String`
- `Boolean`
- `Object`
- `Array`
- `Function`
- `Promise`
- `Any`
- `Void` - used for output of function which mean to return nothing

## Literal Types

Literal types are types which each has only one value that you give.

- `null`
- `undefined`
- numerical literal type, such as: `1`, `256`, `NaN`
- string literal type, such as: `"Bob"`, `"Alice"`, `'doge'`

## Array Type

- `Type[]`
- `[item1, item2, item3]` - for tuple

## Object

- `{item1, item2, item3}` - each item must have name
- `{item1 => item1}` - for map from item1 to item2

## Function Type

- `(item1, item2 ...item3) => item`
- 
  ```
  (item1)
  (item1, item2)
  (item1, item2, item3)
  => item
  ```

## Promise Type

- `Promise => item`

## Generic Types

- `Set<Type>`
- `Map<Type, Type>`
- `Type<Type, ...>`

## Type Logic

- `Type1 | Type2` - type1 or type2
- `Type1 & Type2` - type1 and type2

## Item

Except of `null` and `undefined`, names are lower camel cases and types are upper camel cases.

In rare cases, use `-` to indicate a name and use `+` to indicate a type.

### name version

- `name` or `-Name`
- `name?`
- `name = value`

### type version

- `Type` or `+type`
- `Type?`
- `Type = value`

### full version

- `name: Type`
- `name: Type?` or `name?: Type`
- `name: Type = value`

### Notes

- If some item is with `?`, it is optional and its value could be `undefined`.
- If some item is with `= value` it is optional and if it is `undefined`, it will be set to `value`.

## Custom Type (Type Alias)

- `Type2 ~ Type1`
