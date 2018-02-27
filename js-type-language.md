# JS Type Language

Help define types for JS.

## Stage

- Version: 0.0.0

## Basic Types

- `number`
- `string`
- `bool / boolean`
- `object`
- `array`
- `function`
- `null`
- `undefined`
- `void` - used for functions which mean to return nothing
- `any`

## Array Type

- `type[]`
- `[item1, item2, item3]` - for tuple

## Object

- `{item1, item2, item3}` - each item must have name
- `{item1 => item2}` - for map from item1 to item2

## Function Type

- `(item1, item2, item3) => item`
- `(item1, item2, ...item3) => item`

The formats below are generally used for high order functions: 

- `(item1, item2, item3) -> type`
- `(item1, item2, ...item3) -> type`

## Type Logic

- `type1 | type2` - type1 or type2

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

- `Type: type` - custom type must be capitalized
