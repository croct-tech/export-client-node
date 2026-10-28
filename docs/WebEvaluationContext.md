# WebEvaluationContext


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timeZone** | **string** | The time-zone ID. For example, America/Sao_Paulo. | [default to undefined]
**campaign** | [**Campaign**](Campaign.md) |  | [default to undefined]
**page** | [**PageInfo**](PageInfo.md) |  | [default to undefined]
**attributes** | **{ [key: string]: any | undefined; }** | Custom attributes providing additional information about the current context. | [default to undefined]

## Example

```typescript
import { WebEvaluationContext } from '@croct/export';

const instance: WebEvaluationContext = {
    timeZone,
    campaign,
    page,
    attributes,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
