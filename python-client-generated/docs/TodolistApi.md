# swagger_client.TodolistApi

All URIs are relative to *https://{environment}.programmerzamannow.com/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**todolist_get**](TodolistApi.md#todolist_get) | **GET** /todolist | Get all todolist
[**todolist_post**](TodolistApi.md#todolist_post) | **POST** /todolist | Create new todolist
[**todolist_todolist_id_delete**](TodolistApi.md#todolist_todolist_id_delete) | **DELETE** /todolist/{todolistId} | Delete existing todolist
[**todolist_todolist_id_put**](TodolistApi.md#todolist_todolist_id_put) | **PUT** /todolist/{todolistId} | Update Existing todolist

# **todolist_get**
> list[InlineResponse200] todolist_get(include_done=include_done, name=name)

Get all todolist

get all active todolist by default

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: TodolistAuth
configuration = swagger_client.Configuration()
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-API-KEY'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.TodolistApi(swagger_client.ApiClient(configuration))
include_done = false # bool | Is include done todolist (optional) (default to false)
name = 'name_example' # str | Filter todolist by name (optional)

try:
    # Get all todolist
    api_response = api_instance.todolist_get(include_done=include_done, name=name)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TodolistApi->todolist_get: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **include_done** | **bool**| Is include done todolist | [optional] [default to false]
 **name** | **str**| Filter todolist by name | [optional] 

### Return type

[**list[InlineResponse200]**](InlineResponse200.md)

### Authorization

[TodolistAuth](../README.md#TodolistAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **todolist_post**
> InlineResponse200 todolist_post(body)

Create new todolist

Create New todolist to database

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: TodolistAuth
configuration = swagger_client.Configuration()
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-API-KEY'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.TodolistApi(swagger_client.ApiClient(configuration))
body = swagger_client.TodolistBody() # TodolistBody | 

try:
    # Create new todolist
    api_response = api_instance.todolist_post(body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TodolistApi->todolist_post: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**TodolistBody**](TodolistBody.md)|  | 

### Return type

[**InlineResponse200**](InlineResponse200.md)

### Authorization

[TodolistAuth](../README.md#TodolistAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **todolist_todolist_id_delete**
> object todolist_todolist_id_delete(todolist_id)

Delete existing todolist

Delete existing todolist in database

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: TodolistAuth
configuration = swagger_client.Configuration()
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-API-KEY'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.TodolistApi(swagger_client.ApiClient(configuration))
todolist_id = 'todolist_id_example' # str | Todolist Id for deleted

try:
    # Delete existing todolist
    api_response = api_instance.todolist_todolist_id_delete(todolist_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TodolistApi->todolist_todolist_id_delete: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **todolist_id** | **str**| Todolist Id for deleted | 

### Return type

**object**

### Authorization

[TodolistAuth](../README.md#TodolistAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **todolist_todolist_id_put**
> Todolist todolist_todolist_id_put(body, todolist_id)

Update Existing todolist

Update existing todolist in database

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: TodolistAuth
configuration = swagger_client.Configuration()
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-API-KEY'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.TodolistApi(swagger_client.ApiClient(configuration))
body = swagger_client.TodolistTodolistIdBody() # TodolistTodolistIdBody | 
todolist_id = 'todolist_id_example' # str | Todolist Id for updated

try:
    # Update Existing todolist
    api_response = api_instance.todolist_todolist_id_put(body, todolist_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TodolistApi->todolist_todolist_id_put: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**TodolistTodolistIdBody**](TodolistTodolistIdBody.md)|  | 
 **todolist_id** | **str**| Todolist Id for updated | 

### Return type

[**Todolist**](Todolist.md)

### Authorization

[TodolistAuth](../README.md#TodolistAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

