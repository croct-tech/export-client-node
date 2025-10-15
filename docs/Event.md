# Event


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sessionId** | **string** | The ID of the session assigned to the event. | [default to undefined]
**userId** | **string** | The internal ID of the user who originated the event. | [default to undefined]
**timestamp** | **number** | The timestamp when the event was tracked, in milliseconds since epoch. | [default to undefined]
**context** | [**EventContext**](EventContext.md) |  | [default to undefined]
**payload** | [**EventPayload**](EventPayload.md) |  | [default to undefined]

## Example

```typescript
import { Event } from '@croct/export';

const instance: Event = {
    sessionId,
    userId,
    timestamp,
    context,
    payload,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
