# OperatingSystem

The available information about an operating system.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | The name of the operating system, non-empty. For example, \&quot;macOS\&quot;, \&quot;iOS\&quot; or \&quot;Android\&quot;. | [default to undefined]
**version** | **string** | The version of operating system, non-empty. For example, \&quot;10.15.1\&quot;, \&quot;NT 5.1\&quot; or \&quot;8.4\&quot;. | [default to undefined]

## Example

```typescript
import { OperatingSystem } from '@croct/export';

const instance: OperatingSystem = {
    name,
    version,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
