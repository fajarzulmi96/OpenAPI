# TodolistResTfulApi.TodolistApi

All URIs are relative to *https://{environment}.programmerzamannow.com/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**todolistGet**](TodolistApi.md#todolistGet) | **GET** /todolist | Get all todolist
[**todolistPost**](TodolistApi.md#todolistPost) | **POST** /todolist | Create new todolist
[**todolistTodolistIdDelete**](TodolistApi.md#todolistTodolistIdDelete) | **DELETE** /todolist/{todolistId} | Delete existing todolist
[**todolistTodolistIdPut**](TodolistApi.md#todolistTodolistIdPut) | **PUT** /todolist/{todolistId} | Update Existing todolist

<a name="todolistGet"></a>
# **todolistGet**
> [InlineResponse200] todolistGet(opts)

Get all todolist

get all active todolist by default

### Example
```javascript
import {TodolistResTfulApi} from 'todolist_res_tful_api';
let defaultClient = TodolistResTfulApi.ApiClient.instance;

// Configure API key authorization: TodolistAuth
let TodolistAuth = defaultClient.authentications['TodolistAuth'];
TodolistAuth.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//TodolistAuth.apiKeyPrefix = 'Token';

let apiInstance = new TodolistResTfulApi.TodolistApi();
let opts = { 
  'includeDone': false, // Boolean | Is include done todolist
  'name': "name_example" // String | Filter todolist by name
};
apiInstance.todolistGet(opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **includeDone** | **Boolean**| Is include done todolist | [optional] [default to false]
 **name** | **String**| Filter todolist by name | [optional] 

### Return type

[**[InlineResponse200]**](InlineResponse200.md)

### Authorization

[TodolistAuth](../README.md#TodolistAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="todolistPost"></a>
# **todolistPost**
> InlineResponse200 todolistPost(body)

Create new todolist

Create New todolist to database

### Example
```javascript
import {TodolistResTfulApi} from 'todolist_res_tful_api';
let defaultClient = TodolistResTfulApi.ApiClient.instance;

// Configure API key authorization: TodolistAuth
let TodolistAuth = defaultClient.authentications['TodolistAuth'];
TodolistAuth.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//TodolistAuth.apiKeyPrefix = 'Token';

let apiInstance = new TodolistResTfulApi.TodolistApi();
let body = new TodolistResTfulApi.TodolistBody(); // TodolistBody | 

apiInstance.todolistPost(body, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
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

<a name="todolistTodolistIdDelete"></a>
# **todolistTodolistIdDelete**
> Object todolistTodolistIdDelete(todolistId)

Delete existing todolist

Delete existing todolist in database

### Example
```javascript
import {TodolistResTfulApi} from 'todolist_res_tful_api';
let defaultClient = TodolistResTfulApi.ApiClient.instance;

// Configure API key authorization: TodolistAuth
let TodolistAuth = defaultClient.authentications['TodolistAuth'];
TodolistAuth.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//TodolistAuth.apiKeyPrefix = 'Token';

let apiInstance = new TodolistResTfulApi.TodolistApi();
let todolistId = "todolistId_example"; // String | Todolist Id for deleted

apiInstance.todolistTodolistIdDelete(todolistId, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **todolistId** | **String**| Todolist Id for deleted | 

### Return type

**Object**

### Authorization

[TodolistAuth](../README.md#TodolistAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="todolistTodolistIdPut"></a>
# **todolistTodolistIdPut**
> Todolist todolistTodolistIdPut(body, todolistId)

Update Existing todolist

Update existing todolist in database

### Example
```javascript
import {TodolistResTfulApi} from 'todolist_res_tful_api';
let defaultClient = TodolistResTfulApi.ApiClient.instance;

// Configure API key authorization: TodolistAuth
let TodolistAuth = defaultClient.authentications['TodolistAuth'];
TodolistAuth.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//TodolistAuth.apiKeyPrefix = 'Token';

let apiInstance = new TodolistResTfulApi.TodolistApi();
let body = new TodolistResTfulApi.TodolistTodolistIdBody(); // TodolistTodolistIdBody | 
let todolistId = "todolistId_example"; // String | Todolist Id for updated

apiInstance.todolistTodolistIdPut(body, todolistId, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**TodolistTodolistIdBody**](TodolistTodolistIdBody.md)|  | 
 **todolistId** | **String**| Todolist Id for updated | 

### Return type

[**Todolist**](Todolist.md)

### Authorization

[TodolistAuth](../README.md#TodolistAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

