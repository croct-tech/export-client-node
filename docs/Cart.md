# Cart

A shopping cart in an online store.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currency** | **string** | The currency in which the monetary values are expressed in the shopping cart. The currency should be specified using the 3-letter currency codes defined by the ISO 4217 standard. For currencies having no official recognition in ISO 4217, as is the case with cryptocurrencies, it is allowed the use of non-ISO codes adopted locally or commercially. For example, \&quot;BRL\&quot; for Brazilian real or \&quot;BTC\&quot; for Bitcoin. | [default to undefined]
**items** | [**Array&lt;CartItem&gt;**](CartItem.md) | The list of items in the shopping cart. | [default to undefined]
**subtotal** | **number** | The total of all items and quantities in the shopping cart including applied item promotions. Applied order discounts, estimated shipping, and applied shipping discounts should be excluded from the subtotal amount. | [default to undefined]
**shippingPrice** | **number** | The total shipping price for the items in the shopping cart, including any handling charges. | [default to undefined]
**taxes** | **object** | The taxes associated with the transaction. | [default to undefined]
**costs** | **object** | The costs associated with the transaction, such as manufacturing costs, shipping expenses not borne by the customer, or any other costs. | [default to undefined]
**discount** | **number** | The amount of the discount applied to the shopping cart. | [default to undefined]
**total** | **number** | The total revenue or grand total associated with the transaction. It includes shipping, tax, and any other adjustment. | [default to undefined]
**coupon** | **string** | The coupon applied to the shopping cart. For example, \&quot;SUPER_DEALS\&quot;. | [default to undefined]
**lastUpdateTime** | **number** | The timestamp when the shopping cart was last updated, in milliseconds since epoch. | [default to undefined]

## Example

```typescript
import { Cart } from '@croct/export';

const instance: Cart = {
    currency,
    items,
    subtotal,
    shippingPrice,
    taxes,
    costs,
    discount,
    total,
    coupon,
    lastUpdateTime,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
