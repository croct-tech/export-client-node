# UnsetOperation

An operation to unset a value.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | The discriminator identifying the operation. | [default to undefined]
**path** | **string** | The path where to unset the value. | [default to undefined]

## Example

```typescript
import { UnsetOperation } from '@croct/export';

const instance: UnsetOperation = {
    type,
    path,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
