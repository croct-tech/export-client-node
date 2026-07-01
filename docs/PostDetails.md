# PostDetails

The detailed information of a post.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**postId** | **string** | The ID that uniquely identifies the post. | [default to undefined]
**url** | **string** | The URL of the post page. | [optional] [default to undefined]
**title** | **string** | The title of the post, non-empty. | [default to undefined]
**tags** | **Array&lt;string&gt;** | The set of post tags. | [optional] [default to undefined]
**categories** | **Array&lt;string&gt;** | The categories the post belongs to. | [optional] [default to undefined]
**authors** | **Array&lt;string | null&gt;** | The authors of the post. | [optional] [default to undefined]
**publishTime** | **number** | The timestamp of the post publication, in milliseconds since epoch. | [default to undefined]
**updateTime** | **number** | The timestamp of the post\&#39;s last update, in milliseconds since epoch. | [optional] [default to undefined]

## Example

```typescript
import { PostDetails } from '@croct/export';

const instance: PostDetails = {
    postId,
    url,
    title,
    tags,
    categories,
    authors,
    publishTime,
    updateTime,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
