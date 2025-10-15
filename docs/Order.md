# Order

An order placed in an online store.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**orderId** | **string** | The ID that uniquely identifies the order across the store. | [default to undefined]
**currency** | **string** | The currency in which the monetary values are expressed in the order. The currency should be specified using the 3-letter currency codes defined by the ISO 4217 standard. For currencies having no official recognition in ISO 4217, as is the case with cryptocurrencies, it is allowed the use of non-ISO codes adopted locally or commercially. For example, \&quot;BRL\&quot; for Brazilian real or \&quot;BTC\&quot; for Bitcoin. | [default to undefined]
**items** | [**Array&lt;OrderItem&gt;**](OrderItem.md) | The list of items in the order. | [default to undefined]
**subtotal** | **number** | The total of all items and quantities in the order including applied item promotions. Applied order discounts, estimated shipping, and applied shipping discounts should be excluded from the subtotal amount. | [default to undefined]
**shippingPrice** | **number** | The total shipping price for the order, including any handling charges. | [default to undefined]
**taxes** | **object** | The taxes associated with the transaction. | [default to undefined]
**costs** | **object** | The costs associated with the transaction, such as manufacturing costs, shipping expenses not borne by the customer, or any other costs. | [default to undefined]
**discount** | **number** | The amount of the discount applied to the order. | [default to undefined]
**total** | **number** | The total revenue or grand total associated with the transaction. It includes shipping, tax, and any other adjustment. | [default to undefined]
**coupon** | **string** | The coupon applied to the order. For example, \&quot;SUPER_DEALS\&quot;. | [default to undefined]
**paymentMethod** | **string** | The payment method used in the payment. For example, \&quot;Credit Card\&quot;, \&quot;Paypal\&quot; or \&quot;Wallet\&quot;. | [default to undefined]
**installments** | **number** | The number of installments of the transaction, non-negative. | [default to undefined]
**status** | [**OrderStatus**](OrderStatus.md) |  | [default to undefined]

## Example

```typescript
import { Order } from '@croct/export';

const instance: Order = {
    orderId,
    currency,
    items,
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
