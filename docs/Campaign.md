# Campaign


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | The product promotion or strategic campaign. For example, \&quot;super_promo\&quot;. | [optional] [default to undefined]
**source** | **string** | The advertiser that sent traffic to the application. For example, \&quot;newsletter4\&quot;. | [optional] [default to undefined]
**medium** | **string** | The advertising or marketing medium. For example, \&quot;email\&quot;. | [optional] [default to undefined]
**content** | **string** | The specific content item related the campaign. For example, \&quot;Buy now!\&quot;. | [optional] [default to undefined]
**term** | **string** | The search keywords. Foe example, \&quot;web personalization\&quot; | [optional] [default to undefined]

## Example

```typescript
import { Campaign } from '@croct/export';

const instance: Campaign = {
    name,
    source,
    medium,
    content,
    term,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
