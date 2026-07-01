# OrderSummary

The details of an order.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**orderId** | **string** | The ID that uniquely identifies the order across the store. | [default to undefined]
**currency** | **string** | The currency in which the monetary values are expressed in the order. | [default to undefined]
**quantity** | **number** | The quantity of items in the order. | [default to undefined]
**subtotal** | **number** | The total of all items and quantities in the order including applied item promotions. | [optional] [default to undefined]
**shippingPrice** | **number** | The total shipping price for the order, including any handling charges. | [optional] [default to undefined]
**taxes** | **object** | The taxes associated with the transaction. | [default to undefined]
**costs** | **object** | The costs associated with the transaction, such as manufacturing costs, shipping expenses not borne by the customer, or any other costs. | [default to undefined]
**discount** | **number** | The amount of the discount applied to the order. | [optional] [default to undefined]
**total** | **number** | The total revenue or grand total associated with the transaction. It includes shipping, tax, and any other adjustment. | [default to undefined]
**coupon** | **string** | The coupon applied to the order. For example, \\\&quot;SUPER_DEALS\\\&quot;. | [optional] [default to undefined]
**paymentMethod** | **string** | The payment method used in the payment. For example, \\\&quot;Credit Card\\\&quot;. | [optional] [default to undefined]
**installments** | **number** | The number of installments of the transaction, non-negative. | [optional] [default to undefined]
**status** | [**OrderStatus**](OrderStatus.md) |  | [optional] [default to undefined]

## Example

```typescript
import { OrderSummary } from '@croct/export';

const instance: OrderSummary = {
    orderId,
    currency,
    quantity,
    subtotal,
    shippingPrice,
    taxes,
    costs,
    discount,
    total,
    coupon,
    paymentMethod,
    installments,
    status,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
