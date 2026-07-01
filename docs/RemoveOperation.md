# RemoveOperation

An operation to remove a value from an array.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | The discriminator identifying the operation. | [default to undefined]
**path** | **string** | The path where to remove the content. | [default to undefined]
**value** | **any** | The value to remove. Can be any JSON value. | [default to undefined]

## Example

```typescript
import { RemoveOperation } from '@croct/export';

const instance: RemoveOperation = {
    type,
    path,
    value,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
