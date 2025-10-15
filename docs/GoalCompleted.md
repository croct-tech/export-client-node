# GoalCompleted

An event recording a completed activity, such as a purchase.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**goalId** | **string** | The ID of the goal. | [default to undefined]
**value** | **string** | The monetary value associated to the completion of the goal. This can represent an estimated value or a symbolic value. For example, if the sales team can close 10% of people who sign up for a newsletter, and the average transaction is $500, then a possible value for newsletter sign-ups can be $50 (i.e., 10% of $500). | [default to undefined]
**currency** | **string** | The currency in which the monetary value is expressed. The currency should be specified using the 3-letter currency codes defined by the ISO 4217 standard. For currencies having no official recognition in ISO 4217, as is the case with cryptocurrencies, it is allowed the use of non-ISO codes adopted locally or commercially. For example, \&quot;BRL\&quot; for Brazilian real or \&quot;BTC\&quot; for Bitcoin. | [default to undefined]

## Example

```typescript
import { GoalCompleted } from '@croct/export';

const instance: GoalCompleted = {
    goalId,
    value,
    currency,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
