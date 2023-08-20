# Swagger\Client\TodolistApi

All URIs are relative to *https://{environment}.programmerzamannow.com/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**todolistGet**](TodolistApi.md#todolistget) | **GET** /todolist | Get all todolist
[**todolistPost**](TodolistApi.md#todolistpost) | **POST** /todolist | Create new todolist
[**todolistTodolistIdDelete**](TodolistApi.md#todolisttodolistiddelete) | **DELETE** /todolist/{todolistId} | Delete existing todolist
[**todolistTodolistIdPut**](TodolistApi.md#todolisttodolistidput) | **PUT** /todolist/{todolistId} | Update Existing todolist

# **todolistGet**
> \Swagger\Client\Model\InlineResponse200[] todolistGet($include_done, $name)

Get all todolist

get all active todolist by default

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: TodolistAuth
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');

$apiInstance = new Swagger\Client\Api\TodolistApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$include_done = false; // bool | Is include done todolist
$name = "name_example"; // string | Filter todolist by name

try {
    $result = $apiInstance->todolistGet($include_done, $name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TodolistApi->todolistGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **include_done** | **bool**| Is include done todolist | [optional] [default to false]
 **name** | **string**| Filter todolist by name | [optional]

### Return type

[**\Swagger\Client\Model\InlineResponse200[]**](../Model/InlineResponse200.md)

### Authorization

[TodolistAuth](../../README.md#TodolistAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **todolistPost**
> \Swagger\Client\Model\InlineResponse200 todolistPost($body)

Create new todolist

Create New todolist to database

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: TodolistAuth
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');

$apiInstance = new Swagger\Client\Api\TodolistApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\TodolistBody(); // \Swagger\Client\Model\TodolistBody | 

try {
    $result = $apiInstance->todolistPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TodolistApi->todolistPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\TodolistBody**](../Model/TodolistBody.md)|  |

### Return type

[**\Swagger\Client\Model\InlineResponse200**](../Model/InlineResponse200.md)

### Authorization

[TodolistAuth](../../README.md#TodolistAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **todolistTodolistIdDelete**
> object todolistTodolistIdDelete($todolist_id)

Delete existing todolist

Delete existing todolist in database

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: TodolistAuth
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');

$apiInstance = new Swagger\Client\Api\TodolistApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$todolist_id = "todolist_id_example"; // string | Todolist Id for deleted

try {
    $result = $apiInstance->todolistTodolistIdDelete($todolist_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TodolistApi->todolistTodolistIdDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **todolist_id** | **string**| Todolist Id for deleted |

### Return type

**object**

### Authorization

[TodolistAuth](../../README.md#TodolistAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **todolistTodolistIdPut**
> \Swagger\Client\Model\Todolist todolistTodolistIdPut($body, $todolist_id)

Update Existing todolist

Update existing todolist in database

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: TodolistAuth
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');

$apiInstance = new Swagger\Client\Api\TodolistApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\TodolistTodolistIdBody(); // \Swagger\Client\Model\TodolistTodolistIdBody | 
$todolist_id = "todolist_id_example"; // string | Todolist Id for updated

try {
    $result = $apiInstance->todolistTodolistIdPut($body, $todolist_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TodolistApi->todolistTodolistIdPut: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\TodolistTodolistIdBody**](../Model/TodolistTodolistIdBody.md)|  |
 **todolist_id** | **string**| Todolist Id for updated |

### Return type

[**\Swagger\Client\Model\Todolist**](../Model/Todolist.md)

### Authorization

[TodolistAuth](../../README.md#TodolistAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

