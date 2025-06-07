[**store-x-selector**](../README.md)

***

[store-x-selector](../README.md) / Store

# Class: Store\<State\>

Defined in: Store.ts:3

## Type Parameters

### State

`State`

## Constructors

### Constructor

> **new Store**\<`State`\>(`state`): `Store`\<`State`\>

Defined in: Store.ts:12

#### Parameters

##### state

`State`

#### Returns

`Store`\<`State`\>

## Properties

### state

> **state**: `State`

Defined in: Store.ts:4

## Methods

### apply()

> **apply**(`changes`): `void`

Defined in: Store.ts:35

#### Parameters

##### changes

`Partial`\<`State`\>

#### Returns

`void`

***

### getSnapshot()

> **getSnapshot**(): `State`

Defined in: Store.ts:24

#### Returns

`State`

***

### set()

> **set**\<`T`\>(`key`, `value`): `void`

Defined in: Store.ts:44

#### Type Parameters

##### T

`T`

#### Parameters

##### key

keyof `State`

##### value

`T`

#### Returns

`void`

***

### subscribe()

> **subscribe**(`fn`): () => `void`

Defined in: Store.ts:17

#### Parameters

##### fn

`Listener`\<`State`\>

#### Returns

> (): `void`

##### Returns

`void`

***

### update()

> **update**(`newState`): `void`

Defined in: Store.ts:28

#### Parameters

##### newState

`State`

#### Returns

`void`

***

### create()

> `static` **create**\<`T`\>(`state`): `Store`\<`T`\>

Defined in: Store.ts:8

#### Type Parameters

##### T

`T`

#### Parameters

##### state

`T`

#### Returns

`Store`\<`T`\>
