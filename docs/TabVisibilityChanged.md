# TabVisibilityChanged

An event recording that the visibility of a tab has changed.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tabId** | **string** | The ID that uniquely identifies the tab across the session. | [default to undefined]
**visibility** | [**TabVisibility**](TabVisibility.md) |  | [default to undefined]

## Example

```typescript
import { TabVisibilityChanged } from '@croct/export';

const instance: TabVisibilityChanged = {
    tabId,
    visibility,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
