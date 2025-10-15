# EventContext

The context of the client when the event was tracked.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** |  | [default to 'web']
**metadata** | **{ [key: string]: string | undefined; }** |  | [optional] [default to undefined]

## Example

```typescript
import { EventContext } from '@croct/export';

const instance: EventContext = {
    type,
    metadata,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
