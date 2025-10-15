# Session


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sessionId** | **string** | The ID that uniquely identifies the session across the application. | [optional] [default to undefined]
**userId** | **string** | The ID that uniquely identifies the user across the workspace. | [optional] [default to undefined]
**parentId** | **string** | The ID of the session that superseded this session. Usually, a session receives a parent ID when a user is identified, causing the current anonymous session to end and a new identified session to begin. In this case, the ID of the new session is assigned as the parent ID of the anonymous session. | [optional] [default to undefined]
**externalUserId** | **string** | The external user ID that is used to identify the user on the application side, unique across the workspace. It is always null for anonymous users. | [optional] [default to undefined]
**window** | [**SessionWindow**](SessionWindow.md) |  | [optional] [default to undefined]
**closeTime** | **number** | The time from which the session is closed for new events, but still may accept late-arriving events. The close time may be extended if new events arrive before the session is closed. | [optional] [default to undefined]
**referrer** | **string** | The URI of the content that linked to the page that started the session. | [optional] [default to undefined]
**landingPageUrl** | **string** | The page that started the session. | [optional] [default to undefined]
**campaign** | [**Campaign**](Campaign.md) |  | [optional] [default to undefined]
**location** | [**Location**](Location.md) |  | [optional] [default to undefined]
**client** | [**WebClient**](WebClient.md) |  | [optional] [default to undefined]
**attributes** | **{ [key: string]: any | undefined | null; }** | The custom attributes. | [optional] [default to undefined]
**statistics** | [**SessionStatistics**](SessionStatistics.md) |  | [optional] [default to undefined]

## Example

```typescript
import { Session } from '@croct/export';

const instance: Session = {
    sessionId,
    userId,
    parentId,
    externalUserId,
    window,
    closeTime,
    referrer,
    landingPageUrl,
    campaign,
    location,
    client,
    attributes,
    statistics,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
