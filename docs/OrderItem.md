# OrderItem

An item of an order.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**index** | **number** | The index, starting from zero, representing the order in which the item was added to the shopping cart. | [default to undefined]
**product** | [**ProductDetails**](ProductDetails.md) |  | [default to undefined]
**quantity** | **number** | The number of units of the item ordered. | [default to undefined]
**total** | **number** | The total for the item. It includes discounts and any other adjustment. | [default to undefined]
**discount** | **number** | The amount of the discount applied to the item. | [default to undefined]
**coupon** | **string** | The coupon applied to the item. For example, \&quot;SUPER_DEALS\&quot;. | [default to undefined]

## Example

```typescript
import { OrderItem } from '@croct/export';

const instance: OrderItem = {
    index,
    product,
    quantity,
    total,
    discount,
    coupon,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
