# WebContext

The context of the web client at the time the event was tracked.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tabId** | **string** | The ID that uniquely identifies the tab across the session. | [default to undefined]
**url** | **string** | The URL of the page that the client was on. | [default to undefined]

## Example

```typescript
import { WebContext } from '@croct/export';

const instance: WebContext = {
    tabId,
    url,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
