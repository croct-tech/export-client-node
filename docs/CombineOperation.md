# CombineOperation

An operation to combine arrays or maps.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | The discriminator identifying the operation. | [default to undefined]
**path** | **string** | The path where to combine the values. | [default to undefined]
**value** | **any** | The array or map to combine. Can be any JSON value. | [default to undefined]

## Example

```typescript
import { CombineOperation } from '@croct/export';

const instance: CombineOperation = {
    type,
    path,
    value,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
