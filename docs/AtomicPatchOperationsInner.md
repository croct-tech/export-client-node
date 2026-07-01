# AtomicPatchOperationsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | The discriminator identifying the operation. | [default to undefined]
**path** | **string** | The path where to unset the value. | [default to undefined]
**value** | **any** | The value to set. Can be any JSON value. | [default to undefined]

## Example

```typescript
import { AtomicPatchOperationsInner } from '@croct/export';

const instance: AtomicPatchOperationsInner = {
    type,
    path,
    value,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
