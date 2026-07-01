# DecrementOperation

An operation to decrement a number.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | The discriminator identifying the operation. | [default to undefined]
**path** | **string** | The path where to decrement the value. | [default to undefined]
**value** | **any** | The amount to decrement. Can be any JSON value. | [default to undefined]

## Example

```typescript
import { DecrementOperation } from '@croct/export';

const instance: DecrementOperation = {
    type,
    path,
    value,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
