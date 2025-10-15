# Browser

The available information about a browser.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | The name of the browser, non-empty. For example, \&quot;Chrome\&quot;. | [default to undefined]
**version** | **string** | The version of the browser, non-empty. For example, \&quot;79.0.3945.130\&quot;, \&quot;11\&quot; or \&quot;160.1\&quot;. | [default to undefined]
**type** | [**BrowserType**](BrowserType.md) |  | [default to undefined]

## Example

```typescript
import { Browser } from '@croct/export';

const instance: Browser = {
    name,
    version,
    type,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
