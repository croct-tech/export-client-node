# MergeOperation

An operation to merge arrays or maps.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | The discriminator identifying the operation. | [default to undefined]
**path** | **string** | The path where to merge the values. | [default to undefined]
**value** | **any** | The array or map to merge. Can be any JSON value. | [default to undefined]

## Example

```typescript
import { MergeOperation } from '@croct/export';

const instance: MergeOperation = {
    type,
    path,
    value,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
