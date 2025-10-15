# Device

The available information about a device.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | The name of the device, non-empty. For example, \&quot;Mac\&quot;, \&quot;iPhone\&quot; or \&quot;Nexus 10\&quot;. | [default to undefined]
**vendor** | **string** | The vendor of the device, non-empty. For example, \&quot;Apple\&quot;, \&quot;Samsung\&quot; or \&quot;LG\&quot;. | [default to undefined]
**category** | [**DeviceCategory**](DeviceCategory.md) |  | [default to undefined]
**operatingSystem** | [**OperatingSystem**](OperatingSystem.md) |  | [default to undefined]

## Example

```typescript
import { Device } from '@croct/export';

const instance: Device = {
    name,
    vendor,
    category,
    operatingSystem,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
