# ProductDetails

The detailed information of a product.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**productId** | **string** | The ID that uniquely identifies the product across the store, non-empty. For example, \&quot;3108\&quot; or \&quot;yO7q4r\&quot;. | [default to undefined]
**sku** | **string** | The code that uniquely identifies the product variant across the store, non-empty. For example, \&quot;IPH-GRE-64\&quot;. | [default to undefined]
**name** | **string** | The name of the product, non-empty. For example \&quot;iPhone\&quot;. | [default to undefined]
**category** | **string** | The category of the product, non-empty. For example, \&quot;Phone\&quot;. | [default to undefined]
**brand** | **string** | The brand associated with the product. For example, \&quot;Apple\&quot;. | [default to undefined]
**variant** | **string** | The variant of the product, such as size, color and style. For example, \&quot;64GB Green\&quot;. | [default to undefined]
**displayPrice** | **number** | The price of the product displayed in the store. For example, 59.90. | [default to undefined]
**originalPrice** | **number** | The original price of the product. For example, 99.90. | [default to undefined]
**url** | **string** | The URL of the product page. For example, \&quot;https://apple.com/iphone\&quot;. | [default to undefined]
**imageUrl** | **string** | The URL of the main product image. For example, \&quot;https://img.apple.com/iphone.png\&quot;. | [default to undefined]

## Example

```typescript
import { ProductDetails } from '@croct/export';

const instance: ProductDetails = {
    productId,
    sku,
    name,
    category,
    brand,
    variant,
    displayPrice,
    originalPrice,
    url,
    imageUrl,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
