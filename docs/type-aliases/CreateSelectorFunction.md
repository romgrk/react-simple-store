[**react-simple-store**](../README.md)

***

[react-simple-store](../README.md) / CreateSelectorFunction

# Type Alias: CreateSelectorFunction()

> **CreateSelectorFunction** = \<`Args`, `Selectors`, `Combiner`\>(...`items`) => (...`args`) => `ReturnType`\<`Combiner`\>

Defined in: createSelectorType.ts:3

## Type Parameters

### Args

`Args` *extends* `any`[]

### Selectors

`Selectors` *extends* `ReadonlyArray`\<`Selector`\<`any`\>\>

### Combiner

`Combiner` *extends* (...`args`) => `any`

## Parameters

### items

...\[`...Selectors`, `Combiner`\]

## Returns

> (...`args`): `ReturnType`\<`Combiner`\>

### Parameters

#### args

...`Selectors`\[`"length"`\] *extends* `0` ? `MergeParams`\<`ReturnTypes`\<`Selectors`\>, `Parameters`\<`Combiner`\>\> : \[`StateFromSelectorList`\<`Selectors`\>, `...MergeParams<ReturnTypes<Selectors>, Parameters<Combiner>>`\]

### Returns

`ReturnType`\<`Combiner`\>
