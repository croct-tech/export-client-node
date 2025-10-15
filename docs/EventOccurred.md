# EventOccurred

An event recording a domain-specific occurrence.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | The name of the event. For example, \&quot;pollAnswered\&quot; or \&quot;onboardingStarted\&quot;. | [default to undefined]
**details** | **object** | The details about the event. | [default to undefined]

## Example

```typescript
import { EventOccurred } from '@croct/export';

const instance: EventOccurred = {
    name,
    details,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
