# JS Type Language

Help define types for JS.

## Stage

- Version: 0.0.0

## What is a *Type*?

A type is a set of allowed values which share the features defined in this type, and the set could be finite or infinite.

## Basic Types

- `number`
- `string`
- `bool` or `boolean`
- `object`
- `array`
- `function`
- `void` - used for output of function which mean to return nothing
- `any`
- `promise`

## Literal Types

Literal types are types which each has only one value that you give.

- `null`
- `undefined`
- numerical literal type, such as: `1`, `256`, `NaA`
- string literal type, such as: `"Bob"`, `"Alice"`, `"doge"`

## Array Type

- `type[]`
- `[item1, item2, item3]` - for tuple

## Object

- `{item1, item2, item3}` - each item must have name
- `{item => type}` - for map from given item to some item of given type
- `{item1 -> item2}` - for map from item1 to item2

## Function Type

- `(item1, item2, item3) => type`
- `(item1, item2, ...item3) => type`
- `(item1, item2, item3) -> item`
- `(item1, item2, ...item3) -> item`

## Promise Type

- `promise => type`
- `promsie -> item`

## Type Logic

- `type1 | type2` - type1 or type2
- `type1 & type2` - type1 and type2

## Item

### name version

- `a`
- `a?`
- `a = value`

### type version

- `:type`
- `:type?`
- `:type = value`

### full version

- `a: type`
- `a: type?`
- `a: type = value`

### Notes

- If some item is with `?`, it is optional and its value could be `undefined`.
- If some item is with `= value` it is optional and if it is `undefined`, it will be set to `value`.

## Custom Type (Type Alias)

- `Type ~ type` - generally, custom type should be capitalized
