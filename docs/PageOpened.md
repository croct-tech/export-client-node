# PageOpened

An event recording that a page was opened.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **string** | The URL of the page. | [default to undefined]
**userAgent** | **string** | The user-agent of the client. | [default to undefined]
**preferredLanguages** | **string** | An ordered list of the user\&#39;s preferred languages. | [default to undefined]
**referrer** | **string** | The URI of the page that linked to the page that was opened. The value is null when the user navigated to the page directly (not through a link, but by using a bookmark, for example). | [default to undefined]

## Example

```typescript
import { PageOpened } from '@croct/export';

const instance: PageOpened = {
    url,
    userAgent,
    preferredLanguages,
    referrer,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
