# CheckoutStarted

An event recording that a shopping cart started the checkout process.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cart** | [**Cart**](Cart.md) |  | [default to undefined]
**orderId** | **string** | The ID that uniquely identifies the order across the store. | [default to undefined]

## Example

```typescript
import { CheckoutStarted } from '@croct/export';

const instance: CheckoutStarted = {
    cart,
    orderId,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
