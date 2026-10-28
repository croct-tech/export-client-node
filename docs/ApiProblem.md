# ApiProblem


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **string** |  | [default to undefined]
**type** | **string** |  | [default to undefined]
**status** | **number** |  | [default to undefined]
**detail** | **string** |  | [default to undefined]
**instance** | **string** |  | [default to undefined]
**violations** | [**Array&lt;ApiProblemViolationsInner&gt;**](ApiProblemViolationsInner.md) |  | [optional] [default to undefined]
**resourceType** | **string** |  | [optional] [default to undefined]
**resourceId** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { ApiProblem } from '@croct/export';

const instance: ApiProblem = {
    title,
    type,
    status,
    detail,
    instance,
    violations,
    resourceType,
    resourceId,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
