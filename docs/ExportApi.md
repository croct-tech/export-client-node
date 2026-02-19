# ExportApi

All URIs are relative to *https://api.croct.io/export*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**exportEventById**](#exporteventbyid) | **GET** /events/{id} | |
|[**exportEvents**](#exportevents) | **GET** /events | |
|[**exportSessionById**](#exportsessionbyid) | **GET** /session/{sessionId} | |
|[**exportSessions**](#exportsessions) | **GET** /session | |
|[**exportUserById**](#exportuserbyid) | **GET** /user/{userId} | |
|[**exportUsers**](#exportusers) | **GET** /user | |

# **exportEventById**
> SingleEventResponse exportEventById()


### Example

```typescript
import {
    ExportApi,
    Configuration
} from '@croct/export';

const configuration = new Configuration();
const apiInstance = new ExportApi(configuration);

let id: string; //The unique identifier of the event (default to undefined)

const { status, data } = await apiInstance.exportEventById(
    id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | The unique identifier of the event | defaults to undefined|


### Return type

**SingleEventResponse**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Event found |  -  |
|**404** | Request error |  -  |
|**0** | Request error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **exportEvents**
> EventResponse exportEvents()


### Example

```typescript
import {
    ExportApi,
    Configuration
} from '@croct/export';

const configuration = new Configuration();
const apiInstance = new ExportApi(configuration);

let start: number; // (optional) (default to undefined)
let end: number; // (optional) (default to undefined)
let pageSize: number; // (optional) (default to undefined)
let cursor: string; // (optional) (default to undefined)
let events: Array<EventType>; // (optional) (default to undefined)

const { status, data } = await apiInstance.exportEvents(
    start,
    end,
    pageSize,
    cursor,
    events
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**number**] |  | (optional) defaults to undefined|
| **end** | [**number**] |  | (optional) defaults to undefined|
| **pageSize** | [**number**] |  | (optional) defaults to undefined|
| **cursor** | [**string**] |  | (optional) defaults to undefined|
| **events** | **Array&lt;EventType&gt;** |  | (optional) defaults to undefined|


### Return type

**EventResponse**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**2XX** | Success response |  -  |
|**0** | Request error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **exportSessionById**
> Session exportSessionById()


### Example

```typescript
import {
    ExportApi,
    Configuration
} from '@croct/export';

const configuration = new Configuration();
const apiInstance = new ExportApi(configuration);

let sessionId: string; //The unique identifier of the session (default to undefined)

const { status, data } = await apiInstance.exportSessionById(
    sessionId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **sessionId** | [**string**] | The unique identifier of the session | defaults to undefined|


### Return type

**Session**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Session found |  -  |
|**404** | Request error |  -  |
|**0** | Request error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **exportSessions**
> SessionResponse exportSessions()


### Example

```typescript
import {
    ExportApi,
    Configuration
} from '@croct/export';

const configuration = new Configuration();
const apiInstance = new ExportApi(configuration);

let start: number; // (optional) (default to undefined)
let end: number; // (optional) (default to undefined)
let pageSize: number; // (optional) (default to undefined)
let cursor: string; // (optional) (default to undefined)

const { status, data } = await apiInstance.exportSessions(
    start,
    end,
    pageSize,
    cursor
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**number**] |  | (optional) defaults to undefined|
| **end** | [**number**] |  | (optional) defaults to undefined|
| **pageSize** | [**number**] |  | (optional) defaults to undefined|
| **cursor** | [**string**] |  | (optional) defaults to undefined|


### Return type

**SessionResponse**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**2XX** | Success response |  -  |
|**0** | Request error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **exportUserById**
> User exportUserById()


### Example

```typescript
import {
    ExportApi,
    Configuration
} from '@croct/export';

const configuration = new Configuration();
const apiInstance = new ExportApi(configuration);

let userId: string; //The unique identifier of the user (default to undefined)

const { status, data } = await apiInstance.exportUserById(
    userId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userId** | [**string**] | The unique identifier of the user | defaults to undefined|


### Return type

**User**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | User found |  -  |
|**404** | Request error |  -  |
|**0** | Request error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **exportUsers**
> UserResponse exportUsers()


### Example

```typescript
import {
    ExportApi,
    Configuration
} from '@croct/export';

const configuration = new Configuration();
const apiInstance = new ExportApi(configuration);

let start: number; // (optional) (default to undefined)
let end: number; // (optional) (default to undefined)
let pageSize: number; // (optional) (default to undefined)
let cursor: string; // (optional) (default to undefined)

const { status, data } = await apiInstance.exportUsers(
    start,
    end,
    pageSize,
    cursor
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**number**] |  | (optional) defaults to undefined|
| **end** | [**number**] |  | (optional) defaults to undefined|
| **pageSize** | [**number**] |  | (optional) defaults to undefined|
| **cursor** | [**string**] |  | (optional) defaults to undefined|


### Return type

**UserResponse**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**2XX** | Success response |  -  |
|**0** | Request error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

