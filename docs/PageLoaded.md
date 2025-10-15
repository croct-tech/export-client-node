# PageLoaded

An event recording that a page was loaded.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **string** | The URL of the page. | [default to undefined]
**title** | **string** | The title of the page. | [default to undefined]
**lastModifiedTime** | **number** | The last time the page was modified. | [default to undefined]

## Example

```typescript
import { PageLoaded } from '@croct/export';

const instance: PageLoaded = {
    url,
    title,
    lastModifiedTime,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
