# SlotPersonalized

An event recording a slot personalization.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | The event type identifier. | [default to undefined]
**personalization** | [**SlotPersonalizedPersonalization**](SlotPersonalizedPersonalization.md) |  | [default to undefined]
**metadata** | [**SlotPersonalizedMetadata**](SlotPersonalizedMetadata.md) |  | [default to undefined]

## Example

```typescript
import { SlotPersonalized } from '@croct/export';

const instance: SlotPersonalized = {
    type,
    personalization,
    metadata,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
