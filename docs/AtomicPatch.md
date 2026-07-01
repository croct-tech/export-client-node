# AtomicPatch

A sequence of operations to apply atomically to a target value.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**operations** | [**Array&lt;AtomicPatchOperationsInner&gt;**](AtomicPatchOperationsInner.md) | The list of operations to be applied atomically. | [default to undefined]

## Example

```typescript
import { AtomicPatch } from '@croct/export';

const instance: AtomicPatch = {
    operations,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
