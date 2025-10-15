# User


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**userId** | **string** | The internal ID assigned to the user, unique across the workspace. | [optional] [default to undefined]
**externalUserId** | **string** | The external user ID that is used to identify the user on the application side, unique across the workspace. It is always null for anonymous users. | [optional] [default to undefined]
**firstName** | **string** | The first name attribute. | [optional] [default to undefined]
**lastName** | **string** | The last name attribute. | [optional] [default to undefined]
**birthDate** | **number** | The birth date attribute. | [optional] [default to undefined]
**gender** | **string** | The gender attribute. | [optional] [default to undefined]
**email** | **string** | The email attribute. | [optional] [default to undefined]
**alternateEmail** | **string** | The alternate email attribute. | [optional] [default to undefined]
**phone** | **string** | The phone attribute. | [optional] [default to undefined]
**alternatePhone** | **string** | The alternate phone attribute. | [optional] [default to undefined]
**address** | [**UserAddress**](UserAddress.md) |  | [optional] [default to undefined]
**avatar** | **string** | The avatar attribute. | [optional] [default to undefined]
**company** | **string** | The company attribute. | [optional] [default to undefined]
**companyUrl** | **string** | The company URL attribute. | [optional] [default to undefined]
**jobTitle** | **string** | The job title attribute. | [optional] [default to undefined]
**activities** | **string** | The activities attribute. | [optional] [default to undefined]
**interests** | **string** | The interests attribute. | [optional] [default to undefined]
**customAttributes** | **{ [key: string]: any | undefined; }** | The custom attributes. | [optional] [default to undefined]
**lastModifiedTime** | **number** | The timestamp when the user was last modified, in milliseconds since epoch. It is not updated on sync. | [optional] [default to undefined]
**statistics** | [**UserStatistics**](UserStatistics.md) |  | [optional] [default to undefined]

## Example

```typescript
import { User } from '@croct/export';

const instance: User = {
    userId,
    externalUserId,
    firstName,
    lastName,
    birthDate,
    gender,
    email,
    alternateEmail,
    phone,
    alternatePhone,
    address,
    avatar,
    company,
    companyUrl,
    jobTitle,
    activities,
    interests,
    customAttributes,
    lastModifiedTime,
    statistics,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
