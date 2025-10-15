# TestGroupAssigned

An event recording that a test group was assigned to a user.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**testId** | **string** | The ID of the test. For example, \&quot;black-friday-banner\&quot; or \&quot;home-banner-cta\&quot;. | [default to undefined]
**groupId** | **string** | The ID of the test group, also known as \&quot;variant\&quot;. For example, \&quot;black-friday-promo\&quot; or \&quot;black-friday-shipping\&quot;. | [default to undefined]

## Example

```typescript
import { TestGroupAssigned } from '@croct/export';

const instance: TestGroupAssigned = {
    testId,
    groupId,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
