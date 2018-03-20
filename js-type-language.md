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
- `Void` - alias to `undefined`

## Literal Types

Literal types are types which each has only one value that you give.

- `null`
- `undefined`
- numerical literal type, such as: `1`, `256`, `NaN`
- string literal type, such as: `"Bob"`, `"Alice"`, `'doge'`

## Array Type

- `Type[]`
- `[item1, item2, item3]` - for tuple
- `[item1, item2, ...]`
- `[ite1, item2, ...item3]`

## Object

- `{item1, item2, item3}` - each item must have name
- `{item1, item2, ...}` - there are more unknown fields in this object
- `{item1, item2, ...item3}` - there are more fields in this object besides item1 and item2 and they all form item3.
- `{item1 => item1}` - for map from item1 to item2

## Function Type

- `(item1, item2 ...item3) => item`

## Promise Type

- `Promise => item`

## Generic Types

- `Set<Type>`
- `Map<Type, Type>`
- `Type<Type, ...>`

## Type Logic

- `Type1 | Type2` - type1 or type2
- `Type1 & Type2` - type1 and type2

## Optional Type

- `Type?` - alias to `Type | Void | null`

## Item

An *item* is some name of some type. It is used in some context:

- as object field
- as array item
- as function argument
- to define a name to be of some type

Except of `null` and `undefined`, names are lower camel cases and types are upper camel cases.

In rare cases, use `-` to indicate a name and use `+` to indicate a type.

### name version (ignoring type)

- `name` or `-Name`
- `name?` - this item is optional, which means
  - in an object, this field may not exist
  - in an array, this item may be `Void`
  - in an function, this arg may be `Void`
- `name = value` - specify default value

### type version (ignoring name)

- `Type` or `+type`
- `Type?` - this item is of a maybe type, see [optional type](#optional-type)
- `?Type` - this item is optional, see [name?](#type-version-(ignoring-name))
- `Type = value` - specify default value

### full version

- `name: Type`
- `name: Type = value`
- `name: Type?`
- `name?: Type`
- `name?: Type?`

## Custom Type (Type Alias)

- `Type2 ~ Type1`
