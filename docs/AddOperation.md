# AddOperation

An operation to add a value into an array, map or property.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | The discriminator identifying the operation. | [default to undefined]
**path** | **string** | The path where to add the value. | [default to undefined]
**value** | **any** | The value to add. Can be any JSON value. | [default to undefined]

## Example

```typescript
import { AddOperation } from '@croct/export';

const instance: AddOperation = {
    type,
    path,
    value,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
