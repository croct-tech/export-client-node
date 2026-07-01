# ClearOperation

An operation to clear the content of an array, map or property.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | The discriminator identifying the operation. | [default to undefined]
**path** | **string** | The path where to clear the content. | [default to undefined]

## Example

```typescript
import { ClearOperation } from '@croct/export';

const instance: ClearOperation = {
    type,
    path,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
